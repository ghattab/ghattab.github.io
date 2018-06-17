---
layout: post
title: “Context Free”
description: “text”
comments: false
---

Context Free (CF) grammars rely on shape grammars. A shape grammar consists of a set of transformation and production rules. It applies a step-by-step way to generate and operate on a set, or language, of designs (1). The rules of a shape grammar defines how an existing (part of a) shape can be changed. Such rules operate on design elements to compute designs. Context Free Drawing or CFDG generates images from a written grammar (i.e. ```cfdg``` file) (2). The program follows the instructions or set of rules. 
Example usage: ```./cfdg instructions.cfdg img.png```


## Shapes
Shape grammars rely on shape elements or facts. They are often: points, lines, planes, etc. A shape rule can be written as follows to display either a triangle, or a square, or a circle. A shape rule starts with ```startshape```.

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule draw { 
TRIANGLE {} 
}</code></pre>  
The triangle command can be exchanged by a circle or square.
    </div>
    <div>
        <pre>![](https://ghattab.github.io/images/fig1.png)</pre>
    </div>
</div>


![](https://ghattab.github.io/images/fig1.png)

Shapes can be adjusted. There exists three types of shape adjustments: geometry, color, time.


## Geometry
Spatial rules employ shape operations of addition, subtraction, and many components of the procrustes analysis such as: translation, skew, rotation, uniform scaling, etc. For example, the translation of a shape along the x-axis is made using the adjustment x, as seen below.
 
<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule draw {
TRIANGLE {}    
CIRCLE {x 1}
}</code></pre>  
The extra line adds a circle 5 units away from the triangle on the x axis. The shapes scale within the bounds of the image space.
    </div>
    <div style="display: inline-block;">
        <pre>![](https://ghattab.github.io/images/fig2.png)</pre>
    </div>
</div>


<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
        rule draw {
	        TRIANGLE {}  
	        draw {x 1 s 0.7}
			  }</code></pre>
The extra line calls the ```draw``` instruction which draws an increasingly small triangle every 3 units from the previous triangle on the x axis (size is multiplied by 0.7). 
		</div>
    <div style="display: inline-block;">
        <pre>![](https://ghattab.github.io/images/fig3.png)</pre>
    </div>
</div>

This instruction is recursive and employs a new adjustment of size or s. The program stops once the triangle size can no longer be represented on the image space.


## Color
CF uses the HSBA color space. The HSBA coordinates are [0,360] for hue, [0,1] for saturation, [0,1] for brightness, and [0,1] for alpha (opacity). When brightness is set to 0 or 1, the result is white and black, respectively. 

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape cc
rule cc {
CIRCLE {sat 1 hue 0 b 1} //red
CIRCLE {sat 1 hue 120 b 1 x 1} //green  
CIRCLE {sat 1 hue 240 b 1 x 2} //blue
CIRCLE {sat 1 hue 180 b 1 y -1} //cyan
CIRCLE {sat 1 hue 300 b 1 x 1 y -1} //magenta
CIRCLE {sat 1 hue 60 b 1 x 2 y -1} //yellow
}</code></pre>
		</div>
    <div style="display: inline-block;">
        <pre>![](https://ghattab.github.io/images/fig4.png)</pre>
    </div>
</div>

## Time
CF is powerful enough to render an animation or a set of frames. Each shape has a start time, when it starts to be drawn, and an end time, when it’s drawn. This defines a 1D affine transform with a pair that share the same scale element. The adjustments are time and timescale.

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw[timescale 0.01]
CF::Time = [time 0 1] 
shape c{
CIRCLE[]
}
shape draw
{
c[x ftime()]
draw[x 0.1 r 4 time 1 0 x 0.1]
}</code></pre>  
CF::Time = [time 0 1] configurates the time variable. Notice in this example there are multiple rules and a new syntax style.
    </div>
    <div style="display: inline-block;">
        <pre>![](https://ghattab.github.io/images/fig5.gif)</pre>
    </div>
</div>


By default, CF accumulates the existence time for all of the primitive shapes and divides this time span evenly for each animation frame. In this case the timescale adjustment creates 11 steps given the time adjustment from 0 (inclusive) to 1. To generate the animation: 
```./cfdg -a 5 instructions.cfdg img.png

convert img_*.png animation.gif```

## Sierpinski triangle
To demonstrate the power of CF, let’s create the Sierpinski triangle. 

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule colortr{
TRIANGLE{}
}
rule draw {
colortr{sat 1 hue 240 b 0.5}
draw {s 0.5 y 0.288 b 0.1}
draw {s 0.5 x -0.25 y -0.144 b 0.1}
draw {s 0.5 x 0.25 y -0.144 b 0.1}
}</code></pre>
		</div>
    <div style="display: inline-block;">
        <pre>![](https://ghattab.github.io/images/fig6.png)</pre>
    </div>
</div>



1. Knight, T., 1999. Shape Grammars in Education and Practice: History and Prospects.
2. Coyne, C. and Horigan, J. and Lentczner, M. Context Free Art. ([website](https://www.contextfreeart.org/)).
3. 