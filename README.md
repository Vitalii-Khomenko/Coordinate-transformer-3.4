# Coordinate Transformer

A web-based tool for converting coordinates between Gauss-Krüger (Bessel, Potsdam) and WGS84 systems, with map visualization and batch import/export features.

## Features

- Convert coordinates between GK (Bessel, Potsdam) and WGS84 (both directions)
- Uses precise manual formulas for all transformations (no external libraries required)
- Import/export TXT files for batch processing
- Export results and map to PDF (with adjustable JPEG quality)
- Google Maps integration for quick point visualization
- Responsive, modern interface

## Usage

1. Open `coordinate-transformer.html` in your web browser (no installation required).
2. Select the desired tab:
   - **GK → WGS84:** Convert Gauss-Krüger (Bessel) coordinates to WGS84.
   - **WGS84 → GK:** Convert WGS84 coordinates to Gauss-Krüger (Bessel).
   - **Map:** Visualize points and export the map as PDF.
3. Enter or import your data, click the **Convert** button, and export results as needed.

## Requirements

- Modern web browser (Chrome, Firefox, Edge, etc.)
- JavaScript enabled
- Internet connection for map tiles (OpenStreetMap)

## File Structure

- `coordinate-transformer.html` — main application file
- `Function.txt` — coordinate transformation logic (reference manual formulas)
- `правила.txt` — local project rules (not for publishing)

## License

MIT License (or specify your own).

---

*For questions or suggestions, contact the project author.*
