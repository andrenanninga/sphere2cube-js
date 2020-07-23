# @zebrajaeger/createpano

[![NPM Version](https://img.shields.io/npm/v/@zebrajaeger/createpano.svg?style=flat)](https://www.npmjs.org/package/@zebrajaeger/createpano)
[![Install Size](https://packagephobia.now.sh/badge?p=@zebrajaeger/createpano)](https://packagephobia.now.sh/result?p=@zebrajaeger/createpano)
![npm bundle size (scoped)](https://img.shields.io/bundlephobia/min/@zebrajaeger/createpano)
[![License](https://img.shields.io/github/license/zebrajaeger/sphere2cube-js)](https://img.shields.io/github/license/zebrajaeger/sphere2cube-js)

Convert
- full spheric panorama image to viewer (equirectangular)
- 360° panorama image to viewer (y to small for equirectangular)
- partial panorama image to viewer

Reads 
- PSD and PSB with RAW or RLE Encoding
- jpg
- png (TODO)

Writes
- preview (cubic)
- preview (downscaled)
- tiles (pyramide levels)
- html (pannellum implementation)
- all above as zip file 

## Installation

```bash
$ npm install -g  @zebrajaeger/createpano
```

## Usage

### Minimum

```bash
$ createpano -i sourceimage.psd
```

## Options
```bash
Usage: cli [options]

Options:
  -V, --version                    output the version number
  -i, --input <path>               Input image (mandatory)
  -pa, --panoAngle <degree>        Angle of pano (default: "360")
  -py, --panoYOffset <degree>      Y-Offset in degree [-90.0...90.0] (default: "0")
  -o, --output <path>              Output folder (default: ".")
  -te, --targetSize <pixel>        Image edge length of a face @ max resolution (default: inputImage.x / 4)
  -ti, --tilesIgnore               Dont render tiles
  -ts, --tileSize <pixel>          Tile size (default: "512")
  -tq, --tileQuality <percent>     Jpg Image quality of tiles in percent (default: "85")
  -pi, --previewIgnore             Dont render preview
  -pp, --previewPath <path>        path and name of preiew image (default: "./preview.png")
  -pw, --previewWidth <pixel>      Preview width (default: "1000")
  -pw, --previewQuality <percent>  Preview quality in percent (default: "85")
  -hi, --htmlIgnore                Don't render html
  -ht, --htmlTitle <name>          Head-Title-Tag (default: inputImage)
  -zi, --zipIgnore                 Don't zip
  -zp, --zipPath <path>            Path for Zip File (default: "pano.zip")
  -v, --verbose                    verbose
  -h, --help                       display help for command


```

## Preview

### Downscaled

![dsf](./doc/preview.eq.png)

### Cubic

![dsf](./doc/preview.png)

## Many Thanks to

- https://stackoverflow.com/questions/29678510/convert-21-equirectangular-panorama-to-cube-map
- https://stackoverflow.com/questions/1726630/formatting-a-number-with-exactly-two-decimals-in-javascript
