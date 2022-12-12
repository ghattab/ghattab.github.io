---
layout: page
title: Context Free grammar
description: “Context Free Drawing relies on a set of rules (grammar) that the program uses to generates images.”
tags: [design, shape, context, free, grammar]
modified: 12-09-2019
comments: false
---

Context Free (CF) grammars rely on shape grammars. A shape grammar consists of a set of transformation and production rules. It applies a step-by-step way to generate and operate on a set, or language, of designs (1). The rules of a shape grammar defines how an existing (part of a) shape can be changed. Such rules operate on design elements to compute designs. Context Free Drawing or CFDG generates images from a written grammar (i.e. `cfdg` file) (2). The program follows the instructions or set of rules.
An example usage is as follows: `$ ./cfdg instructions.cfdg img.png`


## Shapes
Shape grammars rely on shape elements or facts. They are often: points, lines, planes, etc. A shape rule can be written as follows to display either a triangle, or a square, or a circle. A shape rule starts with `startshape`.

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule draw {
TRIANGLE {}
}</code></pre>
		</div>
		<div>The triangle command can be exchanged by a circle or square.</div>
</div>

![](/images/fig1.png){: .center-image }

<div style="display: inline-block;">
Shapes can be adjusted. There exists three types of shape adjustments: geometry, color, time.
</div>


## Geometry
Spatial rules employ shape operations of addition, subtraction, and many components of the procrustes analysis such as: translation, skew, rotation, uniform scaling, etc. For example, the translation of a shape along the x-axis is made using the adjustment x, as seen below.

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule draw {
	TRIANGLE {}    
	CIRCLE {x 1}
}</code></pre>
The extra line adds a circle 1 unit away from the triangle on the x axis. The shapes scale within the bounds of the image space.
    </div>
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule draw {
	TRIANGLE {}  
	draw {x 1 s 0.7}
}</code></pre>
Here the program draws an increasingly small triangle (size is multiplied by 0.7) every unit on the x axis.
    </div>
</div>

![](/images/fig2.png){: .center-image } ![](/images/fig3.png){: .center-image }

The second grammar is recursive and employs a new adjustment of size or s. The program stops once the triangle size can no longer be represented on the image space.

## Color
CF uses the HSBA color space. The HSBA coordinates are [0,360] for hue, [0,1] for saturation, [0,1] for brightness, and [0,1] for alpha (opacity). When brightness is set to 0 or 1, the result is white and black, respectively.

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape cc
rule cc {
 CIRCLE {sat 1 hue 0 b 1}  
 CIRCLE {sat 1 hue 120 b 1 x 1}  
 CIRCLE {sat 1 hue 240 b 1 x 2}
 CIRCLE {sat 1 hue 180 b 1 y -1}
 CIRCLE {sat 1 hue 300 b 1 x 1 y -1}
 CIRCLE {sat 1 hue 60 b 1 x 2 y -1}
}</code></pre>
		</div>
    <div style="display: inline-block;">
		Each circle instruction displays a color: red, green, blue, cyan, magenta, yellow.
    </div>
</div>

![](/images/fig4.png){: .center-image }

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
    </div>
    <div style="display: inline-block;">
        CF::Time = [time 0 1] configurates the time variable. Notice in this example there are multiple rules and a new syntax style.
    </div>
</div>

![](/images/fig5.gif){: .center-image }

By default, CF accumulates the existing time for all of the primitive shapes and divides this time span evenly for each animation frame. In this case the timescale adjustment creates 11 steps given the time adjustment from 0 (inclusive) to 1. To generate the animation:
```
$ ./cfdg -a 5 instructions.cfdg img.png
$ convert img_*.png animation.gif
```

## Sierpinski triangle
To demonstrate the power of CF, let’s create the Sierpinski triangle (3).

<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; -webkit-column-rule: 1px dotted #e0e0e0; -moz-column-rule: 1px dotted #e0e0e0; column-rule: 1px dotted #e0e0e0;">
    <div style="display: inline-block;">
        <pre><code class="language-c">startshape draw
rule tr{
 TRIANGLE{}
}
rule draw {
 tr{b 0.01} // for better contrast
 draw {s 0.5 y 0.288 b 0.1}
 draw {s 0.5 x -0.25 y -0.144 b 0.1}
 draw {s 0.5 x 0.25 y -0.144 b 0.1}
}</code></pre>
		</div>
    <div style="display: inline-block;">
For each triangle, 3 triangles — that are half the size — are created at each corner of the triangle. E.g. for the top triangle: The distance between the center of the triangle to its top is given by x/sqrt(3). The smaller triangle moves up by x/2*sqrt(3). At the start, its length is 1 so 1/2*sqrt(3) is 0.288. Etc.
    </div>
</div>

![](/images/fig6.png){: .center-image }


For complete documentation, the official wiki details shape adjustements, shape replacements, shape rules, expressions, and control structures (4).

1. Knight, T., 1999. Shape Grammars in Education and Practice: History and Prospects.
2. Coyne, C. and Horigan, J. and Lentczner, M. [Context Free Art](https://www.contextfreeart.org/).
3. Conversano, E. and Tedeschini-Lalli, L., 2011. Sierpinski Triangles in Stone on Medieval Floors in Rome, APLIMAT Journal of Applied Mathematics, 4: 114, 122.
4. Context-free by John Horigan. [Wiki](https://github.com/MtnViewJohn/context-free/wiki).
