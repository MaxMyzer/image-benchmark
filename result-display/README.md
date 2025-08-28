This folder holds tooling to display results. 
* This will most likely use a static site generator, such as Hugo.
* Data will be output to a file, likely YAML
* Image results will be dumped into the assets


Possible YAML scheme, where files are named based off attributes, such as `{image-name}_{quality-setting}_{speed}_{lib]}_{other-params}.{ext}`
Make everything a property under the file, rather than a tree of data (like `image.format.speed.quality`)

```yaml
- format: {format}
  properties: # format specific properties, like support for monochrome, alpha, max size, HDR, animated, etc.
  libraries:
    - {libraryA}:
      {library-property-A-label}: {library-property-A-value}
      files:
        - file_name: {file-name}
          speed: {speed}
          quality: {quality}
          image: {image-name}
          file-size: {file-size}
          compression-time: {compression-time}
          decompression-time: {decompression-time}
          compression-ratio: {compression-ratio}
          quality-observe: {quality-measurement}
```
