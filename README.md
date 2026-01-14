# RHO File Converter

A web-based tool for converting images to theta-rho polar coordinate format (.rho files) for use with [Sandify](https://sandify.org/).

## Features

- 🖼️ **Image Upload**: Support for PNG, JPG, and JPEG formats
- 🎛️ **Adjustable Parameters**: 
  - Binary threshold control
  - Point density adjustment (100-2000 points)
  - Color inversion option
- 🔗 **Connection Modes**:
  - Separate (no lines between contours)
  - Straight lines
  - Along perimeter (circular arcs)
- 📊 **Real-time Visualization**: View original, binary, and polar coordinate representations
- 💾 **Export Options**: Download or copy to clipboard
- 🔍 **Debug Information**: Contour and figure statistics

## Usage

1. **Open the Application**
   - Simply open `index.html` in a modern web browser
   - No installation or build process required!

2. **Upload an Image**
   - Click "Upload Image" and select a PNG or JPG file
   - The original image will be displayed

3. **Adjust Settings**
   - **Threshold**: Controls the binary conversion (0-255)
   - **Points**: Number of points to generate (100-2000)
   - **Connection Type**: How contours are connected
   - **Invert Colors**: Swap black and white

4. **Convert**
   - Click "Convert" to process the image
   - View the binary conversion and polar visualization

5. **Download**
   - Click "Download RHO" to save the file
   - Or "Copy to Clipboard" to paste elsewhere

## How It Works

### Image Processing Pipeline

1. **Binary Conversion**: The image is converted to black and white using a threshold value
2. **Contour Detection**: Edge-following algorithm detects object boundaries
3. **Figure Grouping**: Outer boundaries and inner holes are grouped together
4. **Resampling**: Contour points are evenly distributed
5. **Polar Conversion**: Cartesian coordinates are converted to theta-rho format
6. **Export**: Data is formatted for Sandify compatibility

### File Format

The output `.rho` file contains lines of space-separated values:
```
theta1 rho1
theta2 rho2
theta3 rho3

theta4 rho4
...
```

- **theta**: Angle in radians (0 to 2π)
- **rho**: Normalized radius (0 to 1)
- **Blank lines**: Indicate breaks between separate contours

## Technical Details

- **Pure Client-Side**: All processing happens in the browser (no server required)
- **React 18**: Built with React hooks
- **HTML5 Canvas**: Used for image processing and visualization
- **Contour Tracing**: Moore-Neighbor boundary following algorithm
- **Polar Coordinates**: Centered at image center with normalized radius

## Browser Compatibility

Works in all modern browsers that support:
- HTML5 Canvas
- ES6+ JavaScript
- React 18

Tested on:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Use Cases

- **Sand Tables**: Create patterns for sand plotting machines
- **CNC/Plotters**: Generate polar coordinate toolpaths
- **Art Projects**: Convert artwork to mathematical representations
- **Educational**: Demonstrate coordinate system transformations

## Tips for Best Results

1. **High Contrast Images**: Work best for clear edge detection
2. **Simple Shapes**: Produce cleaner output than complex textures
3. **Adjust Threshold**: Fine-tune to capture desired details
4. **More Points**: Smoother curves but larger file size
5. **Preview First**: Always check the binary conversion before converting

## Troubleshooting

**Problem**: Output has too many small contours
- **Solution**: Adjust threshold or use image editing software to clean up the source

**Problem**: Missing details in the output
- **Solution**: Increase point count or adjust threshold

**Problem**: Connection lines look wrong
- **Solution**: Try different connection modes (separate/straight/perimeter)

## License

MIT License - Feel free to use, modify, and distribute

## Contributing

Contributions are welcome! This is a single-file application for simplicity.

## Related Projects

- [Sandify](https://sandify.org/) - The sand table pattern generator this tool was designed for
- [svg2thr](https://github.com/user/svg2thr) - SVG to THR converter (Python version)

## Author

Created for the Sandify community

## Changelog

### Version 1.0
- Initial release
- Basic image to RHO conversion
- Three connection modes
- Real-time visualization
- Debug information display
