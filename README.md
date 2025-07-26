# Universal Coordinate Converter

Professional web-based tool for converting coordinates between different coordinate systems with map visualization and batch import/export capabilities.

## Supported Coordinate Systems

- **Gauß-Krüger (Bessel, Potsdam)** ↔ **WGS84** (Germany)
- **SWEREF99 18 00 (EPSG:3011)** ↔ **WGS84** (Sweden)
- **WGS84** → **Multiple Target Systems** (dropdown selection)
- All systems support bidirectional transformations with high precision

## Key Features

### ✅ Offline Functions (work without internet):
- **Coordinate mathematical calculations** - all transformations use built-in geodetic algorithms
- **Multi-target WGS84 conversion** - dropdown selection between GK and SWEREF99 systems
- **TXT file import/export** - batch data processing with system-specific file naming
- **Dynamic table headers** - automatically adjust based on selected coordinate system
- **Data validation** - comprehensive verification of input coordinate accuracy
- **KML export** - Google Earth compatible format with clean point naming

### 🌐 Internet-dependent Functions:
- **Map visualization** - OpenStreetMap tiles with multi-source point display
- **PDF export** - system-aware headers and file naming (jsPDF and html2canvas)
- **Google Maps links** - quick navigation to coordinate points
- **Map screenshots** - export interactive maps as PDF with quality control

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

1. Open `universal-coordinate-converter.html` in your web browser (no installation required)
2. Select the desired tab:
   - **Gauß-Krüger → WGS84:** Convert German coordinates to latitude/longitude
   - **WGS84 → Target System:** Convert WGS84 coordinates with dropdown selection:
     - Target: **Gauß-Krüger (GK)** - German coordinate system
     - Target: **SWEREF99 18 00** - Swedish coordinate system
   - **SWEREF99 18 00 → WGS84:** Convert Swedish coordinates to latitude/longitude
   - **Map:** Visualize all converted points and export map as PDF/KML
3. Enter data manually or import TXT file
4. Select target coordinate system (when applicable)
5. Click **Convert** and export results in multiple formats

## Input Data Format

**Gauß-Krüger and SWEREF99 to WGS84:**
```
PointID Easting Northing Height
1029 3568189.267 5657692.868 321.609
1030 674189.267 6557692.868 421.609
```

**WGS84 to Target System:**
```
PointID Latitude Longitude
1029 51.05031687 9.971396507
1030 55.12345678 18.98765432
```

*Note: Target coordinate system (GK or SWEREF99) is selected via dropdown menu.*

## System Requirements

- **Browser:** Chrome, Firefox, Edge, Safari (modern versions)
- **JavaScript:** Must be enabled
- **Internet:** Required only for maps and PDF export
- **File size:** Up to 5MB for TXT import

## Project Structure

- `universal-coordinate-converter.html` — main application (all functions in one file)
- `Function.txt` — mathematical algorithm documentation for coordinate transformations
- `README.md` — this documentation

## Performance

- **Core calculations:** ~80% functionality works offline
- **External dependencies:** ~2.5MB total size for optional features
- **File processing:** Handles up to 5MB TXT files efficiently
- **Browser compatibility:** Modern ES5+ JavaScript with polyfills

## Technical Implementation

- **Enhanced UI:** Dropdown selection for target coordinate systems in WGS84 conversion tab
- **Dynamic functionality:** Table headers and export filenames adjust based on selected system
- **Datum transformations:** Seven-parameter Helmert transformation for GK ↔ WGS84
- **Projection algorithms:** Standard Transverse Mercator formulas for SWEREF99
- **Error handling:** Comprehensive validation with detailed user feedback
- **Self-contained:** No installation or server requirements - runs entirely in browser

## License

MIT License

## Contributing

Feel free to submit issues and pull requests to improve the coordinate transformation accuracy or add new coordinate systems.

---

*For questions or suggestions, contact the project author.*
