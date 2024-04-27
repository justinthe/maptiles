
**README.md**

**Interactive Orthophoto Viewer**

This repository provides a web page that allows you to visualize and compare orthophotos (aerial photographs) captured at different times for the same location. You can use radio buttons to switch between the various orthophotos, offering a convenient way to track changes or identify specific features across time.

**Prerequisites:**

* `maptiler` or `gdal2tiles` (installation instructions below)
* Basic HTML and JavaScript knowledge (optional, for customization)

**Installation:**

1. **Clone the repository:**

   ```bash
   git clone https://github.com/justinthe/maptiles.git
   ```

**Usage:**

1. **Prepare your orthophotos:**

   Ensure your orthophotos are in TIFF (TIF) format. Rename them descriptively (e.g., `orthophoto_2023-01-01.tif`, `orthophoto_2024-04-27.tif`) to indicate their capture times.

2. **Convert orthophotos to tiles (repeat for each orthophoto):**

	Use either [maptiler](https://www.maptiler.com/engine/) or [gdal2tiles.py](https://gdal.org/programs/gdal2tiles.html) to convert tif files to tiled maps. 

3. **Copy `googlemaps.html` (from any output directory) to the root of your repository.**

4. **(Optional) Customize the `googlemaps.html` file:**

   Open `googlemaps.html` in a text editor. You can modify the following:

   - Add **Radio button:** and change the value for each radio button to reflect the corresponding orthophoto's capture time.
   - **Map center coordinates:** Adjust the latitude and longitude values in the JavaScript code to center the map on your desired location.
   - **Appearance:** Use CSS to style the radio buttons, map container, and other elements.

**Running the viewer:**

1. Open `googlemaps.html` in a web browser to view your interactive orthophoto viewer.

**Additional Notes:**

* This example uses Leaflet for the interactive map. You can explore other JavaScript mapping libraries if desired.
