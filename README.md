# wavma.js

Wavma lets *designers that code* create lightweight tools to design-in-place. Inspired by wonderful tools like Figma, Linear, and Slate, Wavma distills design tools into basic primitives that  can be combined to give you just the features you need, right when you need them.

Editing an image in your Wordpress admin, tweaking the font of a published graphic, or adjusting the path of an SVG icon in VS Code, Wavma meets you where you are to let you make design changes on the fly.

## Why

1. **Design Tooling** - Relative to software engineering, design tooling is woefully underdeveloped. The typical workflow for visual creativity is to conceptualize an idea, open an Adobe product, iterate until you get management by-in, and then ship...oops the graphic looks off in production, red line the changes, now message the designer (who's probably on twitter), etc.

2. **Standalone Features** - Full-feature design tools like Photoshop, Sketch, Figma let you add custom functionality with plugins, but still require the entire runtime of the main app.

3. **Resusable Designs** - Javascript libraries depend on HTML canvas or their own unique data model—Paper.js, Fabric.js, and Konva.js—which means rasterized or proprietary data that is hard or impossible to wrangle.

## Principles

- **Micro (Design) Services** - Need to just edit an SVG path? Import the component. Building a font tool? Import the component. Need to edit colors? Import...you get the idea.
- **Betting on the DOM** - Im-Imper-Imperative programming (hacking cough). I thought the entire web mindshare moved to functional declarative code? While an amazing shift for code, no one wants to paint in JSON. By ignoring an abstract syntax tree, Wavma lets you drop-in an SVG or image and immediately start editing anything. It's slower for big files, but we're betting on the web and computers getting faster over time.
- **SVG all the things** - Like Javascript for code, SVG is the vector language of the web. While we're still living in SVG 1.2 land (which came out a decade ago), SVG is the core primitive of the Wavma.
- **Useful exports** - Need a transparent PNG, usable SVG, or just JSON data? Wavma focuses on output as a first-class feature.
