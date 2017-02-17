# Alfresco icons

Alfresco icons is a library of Alfresco SVG imagery.

## Preproduction

**Note:** This is a work in progress and not intended for production use.

## Installation

This package uses the **svg-sprite** cli tool to convert a folder of svg icons into the sprite that is then exported. 
Perform the usual npm command to install:

```
npm install
```

## Sprite generation

The following command, run in the project root, will convert all svg images in the raw_svgs directory into combined 
svg sprites with accompanying css, scss and sass files and a demo page, all in the assets directory of the project.

```
svg-sprite raw_svgs/*.svg --config svg-sprite.config.json
```

Further information about the configuration of svg-sprite can be found here:

(https://github.com/jkphl/svg-sprite/blob/master/docs/command-line.md)

## License

These icons are made available under the Apache License Version 2.0. Feel free to remix and re-share these icons 
and documentation in your products. We'd love attribution in your app's about screen, but it's not required. The 
only thing we ask is that you not re-sell these icons.