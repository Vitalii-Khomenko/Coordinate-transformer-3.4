# Coordinate Transformer 3.4

Professional web-based tool for converting coordinates between different coordinate systems with map visualization and batch import/export capabilities.

## Supported Coordinate Systems

- **Gauß-Krüger (Bessel, Potsdam)** ↔ **WGS84** (Germany)
- **SWEREF99 18 00 (EPSG:3011)** ↔ **WGS84** (Sweden)
- Both systems support forward and inverse transformations

## Key Features

### ✅ Offline Functions (work without internet):
- **Coordinate mathematical calculations** - all transformations use built-in geodetic algorithms
- **TXT file import/export** - batch data processing
- **Basic results export** - save to text files
- **Data validation** - verification of input coordinate accuracy
- **KML export** - Google Earth compatible format

### 🌐 Internet-dependent Functions:
- **Map visualization** - OpenStreetMap tiles for display
- **PDF export** - external libraries jsPDF and html2canvas
- **Google Maps links** - quick navigation to coordinate points

### 📊 External Dependencies (CDN):
- **jsPDF** (~500KB) - PDF document generation
- **jsPDF AutoTable** (~150KB) - table formatting in PDFs
- **OpenLayers** (~1.5MB) - interactive map library
- **html2canvas** (~300KB) - map screenshot capture

## Mathematical Accuracy

- **GK (Bessel) ↔ WGS84**: Seven-parameter Helmert transformation with centimeter-level accuracy
- **SWEREF99 18 00 ↔ WGS84**: Standard Transverse Mercator projection algorithms (GRS80 ellipsoid)
- **Built-in polyfills** for legacy browser compatibility (Math.cosh, Math.sinh, Math.atanh, Math.asinh)

## Usage

1. Open `coordinate-transformer.html` in your web browser (no installation required)
2. Select the desired tab:
   - **Gauß-Krüger → WGS84:** Convert German coordinates
   - **WGS84 → GK:** Reverse transformation to GK
   - **SWEREF99 18 00 → WGS84:** Convert Swedish coordinates
   - **Map:** Visualize points and export map
3. Enter data or import TXT file
4. Click **Convert** and export results

## Input Data Format

```
PointID Easting Northing Height
1029 3568189.267 5657692.868 321.609
1030 674189.267 6557692.868 421.609
```

## System Requirements

- **Browser:** Chrome, Firefox, Edge, Safari (modern versions)
- **JavaScript:** Must be enabled
- **Internet:** Required only for maps and PDF export
- **File size:** Up to 5MB for TXT import

## Project Structure

- `coordinate-transformer.html` — main application (all functions in one file)
- `Function.txt` — mathematical algorithm documentation for coordinate transformations
- `README.md` — this documentation

## Performance

- **Core calculations:** ~80% functionality works offline
- **External dependencies:** ~2.5MB total size for optional features
- **File processing:** Handles up to 5MB TXT files efficiently
- **Browser compatibility:** Modern ES5+ JavaScript with polyfills

## Technical Implementation

- **Datum transformations:** Seven-parameter Helmert transformation
- **Projection algorithms:** Standard Transverse Mercator formulas
- **Error handling:** Comprehensive validation and user feedback
- **Self-contained:** No installation or server requirements

## License

MIT License

## Contributing

Feel free to submit issues and pull requests to improve the coordinate transformation accuracy or add new coordinate systems.

---

*For questions or suggestions, contact the project author.*
