# muse

[View the live site on GitHub Pages](https://artemis-rage.github.io/muse/)

A modern, interactive 3D asset gallery for the web. Built with [Three.js](https://threejs.org/) and [Tailwind CSS](https://tailwindcss.com/), muse allows you to showcase, annotate, and explore 3D models in a beautiful, responsive interface.

## Features

- **3D Model Viewer:** View OBJ+MTL models with lighting and orbit controls.
- **Asset Metadata:** Each asset can have a title and description (Markdown files).
- **Annotations:**
  - Add interactive markers to models in fullscreen mode.
  - Annotations can be preloaded from an `annotations.json` file or added by users.
  - User-added annotations display the full JSON record for easy copy-paste.
  - Preloaded annotations display only the annotation text.
- **Context Menu:** Right-click on a model in fullscreen to add an annotation at a specific point.
- **Responsive UI:** Clean, mobile-friendly layout using Tailwind CSS.
- **Fullscreen Mode:** Expand any asset for immersive viewing and annotation.

## Directory Structure

```
assets/
  <asset_name>/
    3DModel.obj
    3DModel.mtl
    3DModel.jpg         # (optional preview image)
    title.md            # Title (Markdown)
    description.md      # Description (Markdown)
    annotations.json    # (optional) Array of annotation objects
```

Example `annotations.json`:
```json
[
  {
    "x": 0.0,
    "y": 1.0,
    "z": 0.0,
    "annotation": "This is the top of the object."
  }
]
```

## Usage

1. **Add your assets:**
   - Place each asset in its own folder under `assets/`.
   - Include the required files (`3DModel.obj`, `3DModel.mtl`, `title.md`, `description.md`).
   - Optionally add `annotations.json` and a preview image.
2. **Configure the gallery:**
   - Edit the `assetDirectoryNames` array in `gallery.html` to list your asset folders.
3. **Run locally:**
   - Use the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) VS Code extension or any static server.
   - Open `index.html` (which redirects to `gallery.html`).
4. **Deploy:**
   - For GitHub Pages, ensure `index.html` is present (it redirects to `gallery.html`).
   - Push your repository to GitHub and enable Pages.

## Development

- Main code is in `gallery.html`.
- Styling is via Tailwind CSS (CDN).
- 3D logic uses Three.js modules from CDN.

## License

MIT License
