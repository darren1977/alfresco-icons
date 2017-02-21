# Alfresco icons

- [Implementing Alfresco icons imagery in a project](#implementing-alfresco-icons-imagery-in-a-project)
    - [Installation](#installation)
    - [Usage](#usage)
- [Adding to the image library](#adding-to-the-image-library)
    - [Installation](#installation-1)
    - [Adding new images to the generated sprite](#adding-new-images-to-the-generated-sprite)
    - [Sprite generation](#sprite-generation)
    - [Pull requests](#pull-requests)
- [License](#license)

Alfresco icons is a library of Alfresco SVG imagery for use within Alfresco client applications.

**Note:** This project is a work in progress and is not yet intended for production use.

## Implementing Alfresco icons imagery in a project

### Installation

Add alfresco-icons as a package dependency.

```
npm install alfresco-icons --save
```

You may need to make suitable build configurations for packaging tools such as systemjs and webpack.

### Usage

```
<svg role="img" class="my-logo-class">
  <description>Alfresco Logo</description>
  <use xlink:href="path/to/alfresco.sprite.css.svg#svg-alfresco-flower"></use>
</svg>
```

## Adding to the image library

This package uses the **svg-sprite** cli tool to convert a folder of svg icons into the sprite that is then 
exported.

### Installation

Clone the project to a directory of your choice and perform the usual npm command to install dev dependencies:

```
npm install
```

### Adding new images to the generated sprite

The directory *raw_svgs* contains all of the individual svg images that are included in the sprite. Their file 
names will become the **id** of the svg after generation. To add a new image to the generated sprite simply 
drop the new image into the *raw_svgs* directory, making sure that the file name is suitable, and follow the 
generation commands below.

### Sprite generation

The following command, run in the project root, will convert all svg images in the *raw_svgs* directory into 
combined svg sprites with accompanying css, scss and sass files and a demo page, all in the assets directory of 
the project.

```
svg-sprite raw_svgs/*.svg --config svg-sprite.config.json
```

Further information about the configuration of svg-sprite can be found here:

[https://github.com/jkphl/svg-sprite/blob/master/docs/command-line.md](https://github.com/jkphl/svg-sprite/blob/master/docs/command-line.md)

### Pull requests

Assuming the images are appropriate for inclusion in the library, we would be delighted to receive pull requests 
with new images. Please add images to the library and generate the new svg sprite yourself using the 
instructions shown. Please rebase onto an updated develop branch before pushing to avoid PRs containing out-of-
date content.

## License

These icons are made available under the Apache License Version 2.0. Feel free to remix and re-share these icons 
and documentation in your products. We'd love attribution in your app's about screen, but it's not required. The 
only thing we ask is that you not re-sell these icons.