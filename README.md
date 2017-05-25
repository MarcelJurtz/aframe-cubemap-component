## aframe-cubemap-component

An [A-Frame](https://aframe.io) component for creating a skybox from a cubemap.  
Originally created by [Ben Pyrik](https://github.com/bryik/aframe-cubemap-component).

### Properties

|  Property  |               Description               | Default Value |
|:----------:|:---------------------------------------:|:-------------:|
|   folder   | Path to the folder holding your cubemap |      none     |
| edgeLength |  Controls the dimensions of the skybox  |      5000     |

By default, the height, width, and depth of the skybox are set to 5000. In other words, the dimensions of the skybox are 5000x5000x5000.

### Usage

Attach the component to an entity using the path to the folder holding your cubemap as the attribute.

```html
  <!-- index.html -->
  <a-entity cubemap="folder: /assets/skybox/"></a-entity>
```

The folder structure (including filenames) should be similar to this:

```
project/
├── assets/
│   └── skybox.css
│       ├── up.jpg
│       ├── down.jpg
│       ├── left.jpg
│       ├── right.jpg
│       ├── front.jpg
│       └── back.jpg
└── index.html
```

The original repo uses Three.js's scheme. The following table shows the namings to convert these:

| Original | Fork  |
|----------|-------|
| posx     | left  |
| negx     | right |
| posy     | up    |
| negy     | down  |
| posz     | front |
| negz     | back  |


To modify the size of the resulting skybox, use the edgeLength property.

```html
  <a-entity cubemap="folder: /assets/Yokohama3/; edgeLength: 1000"></a-entity>
```

To use this script, paste the index.js file into your projects folder and link it:

```html
<script src="aframe-cubemap.js"></script>
```
