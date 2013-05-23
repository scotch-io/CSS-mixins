SASS and LESS Mixins
===========

Preset mixins to help speed up web development. Provides **cross-browser compatibility** with things like:

- Rounded Corners
- Opacity
- Box Shadow
- Box Shadow (Inset)
- Gradient (Horizontal)
- Gradient (Vertical)
- CSS3 Transition
- CSS3 Transforms

These will automatically create browser-specific rules to accommodate multiple browsers. For example, the `.border-radius(4px)` mixin will create:

>
	border-radius			: 4px;
	-moz-border-radius		: 4px;
	-webkit-border-radius	: 4px;

* These instructions are for the LESS version. The SASS syntax is a little different, but will have the same results. Check out the [SASS Website](http://sass-lang.com/) for their syntax.

Requirements
------------

- [jQuery](http://jquery.com/)
- [LESS](http://lesscss.org/)

Installation
------------

- Include jQuery and LESS

>
	<script src="{path_to_jquery}"></script>
	<script src="{path_to_less}"></script>

- Include `mixins.less` in the head of your document.

>
	<link rel="stylesheet/less" href="{path_to_mixins}">

* Alternatively, you can import the mixins.less into the stylesheet you want. At the beginning of your LESS file, use:

`@import "mixins";`

Usage
------------

### Rounded Corners ###
Set the border radius. Accepts pixels or percentages.

Have a border radius all around: `.border-radius(5px);`

Create a circle: `.border-radius(50%);`

### Opacity ###
Set the opacity of any element. This will set the opacity of the element plus its children. For just setting the opacity of a background, look at Background Opacity

`.opacity(0.5);`

### Background Alpha ###
Creates a transparent background. The contents of the element will stay at normal capacity.

`.background-alpha(#000, 0.5);`

### Box Shadow ###
Create a box shadow. Accepts 4 options: `.box-shadow(@x-size, @y-size, @blur, @color, @spread);`

`.box-shadow(2px, 2px, 5px, #333, 0px);`

### Box Shadow (Inset) ###
Create an inner box shadow. Accepts 4 options: `.box-shadow(@x-size, @y-size, @blur, @color, @spread);`

`.box-shadow-inset(2px, 2px, 5px, #333, 0px);`

### Gradient (Horizontal) ###
Create a horizontal gradient. Accepts 2 colors: `.gradient-horizontal(#FFF, #E7E7E7);`

### Gradient (Vertical) ###
Create a vertical gradient. Accepts 2 colors: `.gradient-vertical(#FFF, #E7E7E7);`

### CSS3 Transition ###
Applies a CSS3 transition to an element. This will be used to transition CSS effects like :hover. 

`.transition(@type, @time, @ease);`
`.transition(all, 5s, ease-in-out);`

### CSS3 Transforms ###
This includes the simple CSS3 transforms. I'm currently working on a CSS3 animation library to help speed up CSS3 animations. Coming soon...

These transforms include:
- `.transform(@deg);`
- `.scale(@multiplier);`
- `.rotate(@deg);`
- `.skew(@deg, @deg2);`

These can be used on :hover actions to create cool effects.
