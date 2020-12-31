# Wavma

A customizable framework for building design tools.

Wavma lets *designers that code* create lightweight tools to design-in-place. Inspired by wonderful tools like [Figma](https://www.figma.com/), [Linear](https://linear.app/), and [Slate](https://github.com/ianstormtaylor/slate), Wavma distills design tools into basic primitives that  can be combined to give you just the features you need, right when you need them.

Editing the color of a visual in Wordpress, tweaking the font of a published vector graphic, or adjusting the path of an SVG icon in VS Code, Wavma meets you where you are to let you make design changes on the fly.

## Why

1. **Design Tooling** - Relative to software engineering, design tooling is woefully underdeveloped. The typical workflow for visual creativity is to conceptualize an idea, open an Adobe product, iterate until you get management by-in, and then ship...oops the graphic looks off in production, red line the changes, now message the designer, etc.
2. **Standalone Features** - Full-feature design tools like Photoshop, Sketch, Figma let you add custom functionality with plugins, but still require the entire runtime of the main app.
3. **Resusable Vector Designs** - Javascript libraries depend on HTML canvas or their own unique data model—Paper.js, Fabric.js, and Konva.js—which means rasterized or proprietary data that is hard or impossible to wrangle.

## Principles

- **Micro (Design) Services** - Need to just edit an SVG path? Import the component. Building a font tool? Import the component. Need to edit colors? Import...you get the idea.
- **Betting on the DOM** - What's old is new: imperative programming. By ignoring an abstract syntax tree, Wavma utlizes the DOM as state and lets you drop-in any SVG and immediately start editing anything. It's slower for big files, but we're betting on the web and computers getting faster over time.
- **SVG most the things** - Like Javascript for code, SVG is the vector language of the web. While we're still living in SVG 1.2 land (which came out a decade ago), SVG is the core primitive of Wavma, but not only the output.
- **Normalize Events** - Drawing a rectangle on the web should work the same however you're doing it. For example you can draw a rectangle with SVG `<rect>`, HTML `<div>`, Canvas `rect()`, or WebGL `drawArrays(triangles)`.
- **Useful exports** - Need a transparent PNG, usable SVG, or just a simple JPG? Wavma focuses on output as a first-class feature.

## Primitives

- [**Zoom**](https://github.com/wavma/enhance) - Trackpad pinch-to-zoom, panning, keyboard shortcuts
- **Position** - Top, Left, Right, Center
- **Shapes (Native SVG Elements)** - Circle, Ellipse, Rectangle, Polygon, Polyline, Line
- **Layers and Groups**
- **Color**
- **Pen Tool** - Path
- **Export** - SVG, PNG, JPG
- **Text**
- *Mobile*
- *Transform*
- *Boolean Operations*
