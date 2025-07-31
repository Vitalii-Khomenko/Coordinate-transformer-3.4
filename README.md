# Universal Coordinate Converter

Web-based tool for converting coordinates between supported systems, with map visualization and TXT/PDF/KML import/export.

## Supported Coordinate Systems

- **Gauß-Krüger (Bessel, Potsdam)** ↔ **WGS84** (Germany)
- **SWEREF99 18 00 (EPSG:3011)** ↔ **WGS84** (Sweden)
- **WGS84** → **Gauß-Krüger (GK)** or **SWEREF99 18 00** (dropdown)
*Each direction is available as a separate function/tab.*

## Features

- All coordinate transformations are performed in-browser using built-in geodetic algorithms.
- WGS84 can be converted to GK or SWEREF99 (dropdown selection).
- TXT file import/export for batch processing.
- KML export for Google Earth.
- PDF export (tables and map).
- Map visualization (OpenLayers, OpenStreetMap tiles; requires internet).
- Google Maps links for each point.
- Dynamic table headers and export filenames.
- Input validation with user feedback.
- Polyfills for legacy browser math functions.

*Map and PDF export require internet for external libraries and map tiles.*

## Mathematical Details

- **GK (Bessel) ↔ WGS84**: Seven-parameter Helmert transformation
- **SWEREF99 18 00 ↔ WGS84**: Standard Transverse Mercator projection (GRS80 ellipsoid)
- Polyfills for legacy browser compatibility (Math.cosh, Math.sinh, Math.atanh, Math.asinh)

## Usage

1. Open `universal-coordinate-converter.html` in your browser (no installation needed).
2. Select the desired tab:
   - **Gauß-Krüger → WGS84**
   - **WGS84 → GK or SWEREF99** (dropdown)
   - **SWEREF99 18 00 → WGS84**
   - **Map** (visualize/export points)
3. Enter data manually or import TXT file.
4. Select target system if needed.
5. Click **Convert** and export results as TXT, PDF, or KML.

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

*Target system (GK or SWEREF99) is selected via dropdown.*

## System Requirements

- Modern browser (Chrome, Firefox, Edge, Safari)
- JavaScript enabled
- Internet required for map and PDF export
- TXT import up to 5MB

## Project Structure

- `universal-coordinate-converter.html` — main application (all functions in one file)
- `Function.txt` — mathematical algorithm documentation for coordinate transformations
- `README.md` — this documentation

## Performance

- Most functions work offline (except map and PDF export)
- Handles TXT files up to 5MB
- Uses CDN libraries for map and PDF features

## Technical Notes

- UI: Tabs for each conversion direction, dropdown for WGS84 target
- Table headers and export filenames adjust to selected system
- Standard geodetic formulas for all conversions
- Input validation with user feedback
- No installation or server required; runs in browser

## License

MIT License

## Contributing

Feel free to submit issues or pull requests to improve accuracy or add new systems.

---

*For questions or suggestions, contact the project author.*
