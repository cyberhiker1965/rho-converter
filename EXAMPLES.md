# Example Usage Guide

## Quick Start

1. Open `index.html` in your browser
2. Click "Upload Image"
3. Select a simple black and white image (or one that converts well to B&W)
4. Adjust the threshold slider until the binary image looks good
5. Click "Convert"
6. Download your .rho file

## Example Workflow

### Converting a Logo

**Input**: Company logo (PNG, 800x600px)

1. Upload the logo
2. Set threshold to 128 (adjust if logo disappears or has too much noise)
3. Set points to 500 for smooth curves
4. Choose "Separate (no lines)" for clean shapes
5. Convert and download

**Result**: Clean RHO file ready for Sandify

### Converting a Silhouette

**Input**: Portrait silhouette (JPG, 1000x1000px)

1. Upload the image
2. Check "Invert Colors" if the subject is light on dark
3. Increase threshold to 180 for sharper edges
4. Set points to 1000 for detailed curves
5. Choose connection type based on preference
6. Convert and verify in visualization

### Converting Text

**Input**: Text image (PNG, 600x200px)

1. Upload the text image
2. Adjust threshold to capture letters clearly (usually 100-150)
3. Set points to 300-500 depending on text complexity
4. Use "Separate" mode to keep letters distinct
5. Convert and check that letters are complete

## Parameter Guide

### Threshold (0-255)
- **Low (0-100)**: Captures more details, may include noise
- **Medium (100-180)**: Good for most images
- **High (180-255)**: Only darkest areas, very clean output

### Points (100-2000)
- **Low (100-300)**: Faster, angular output
- **Medium (300-800)**: Good balance for most uses
- **High (800-2000)**: Smooth curves, larger file size

### Connection Types

**Separate (No Lines)**
- Best for: Multiple distinct shapes, text, logos
- Creates: Clean breaks between contours
- Sandify behavior: Lifts between shapes

**Straight Lines**
- Best for: Continuous patterns, geometric designs
- Creates: Direct connections between endpoints
- Sandify behavior: Straight transition lines

**Along Perimeter**
- Best for: Artistic effects, flowing designs
- Creates: Curved arcs along circular paths
- Sandify behavior: Smooth circular transitions

## Tips for Different Image Types

### Photographs
1. Pre-process in image editor to increase contrast
2. Convert to black and white before uploading
3. Use high threshold (160-200)
4. Expect longer processing time

### Line Art
1. Works best with clean, vector-style images
2. Medium threshold (120-140)
3. Lower point count is often sufficient (300-500)

### Detailed Drawings
1. May need manual cleanup in image editor first
2. Adjust threshold carefully to preserve detail
3. Higher point count (800-1500)
4. Check visualization carefully before downloading

### Geometric Shapes
1. Usually very clean conversion
2. Medium-low point count (200-400)
3. Any connection type works well
4. Fast processing

## Common Issues and Solutions

### "Too Many Contours"
- Increase threshold to eliminate noise
- Pre-clean image in editor
- Use simpler source image

### "Missing Details"
- Lower threshold
- Increase point count
- Check if image has sufficient contrast

### "Jagged Edges"
- Increase point count
- Use higher resolution source image
- Apply slight blur in image editor before conversion

### "File Too Large"
- Reduce point count
- Simplify source image
- Remove unnecessary details in editor

## Advanced Techniques

### Creating Patterns
1. Start with symmetrical source image
2. Use medium point count
3. Try different connection types for various effects
4. Combine multiple conversions in Sandify

### Layered Effects
1. Convert same image with different thresholds
2. Create multiple RHO files
3. Layer them in Sandify with different offsets
4. Experiment with scale and rotation

### Text Effects
1. Use bold, high-contrast fonts
2. Increase letter spacing in source image
3. Convert with "Separate" mode
4. Adjust point count based on font complexity
