## Interactive Orthophoto Viewer

This repository provides a web page that allows you to visualize and compare orthophotos (aerial photographs) captured at different times for the same location. You can use radio buttons to switch between the various orthophotos, offering a convenient way to track changes or identify specific features across time.

**Prerequisites:**

* **Choose one of the following tools for converting orthophotos to tiles:**
    * `maptiler` ([https://www.maptiler.com/](https://www.maptiler.com/))
    * `gdal2tiles` ([https://gdal.org/download.html](https://gdal.org/download.html))


**Usage:**

1. **Prepare your orthophotos:**

   Ensure your orthophotos are in TIFF (TIF) format. Rename them descriptively (e.g., `orthophoto_2023-01-01.tif`, `orthophoto_2024-04-27.tif`) to indicate their capture times.

2. **Convert orthophotos to tiles (repeat for each orthophoto):**

   Use either [maptiler](https://www.maptiler.com/engine/) or [gdal2tiles.py](https://gdal.org/programs/gdal2tiles.html) to convert tif files to tiled maps. 

3. **Organize your tile folders:**

   - Move each generated tile folder (e.g., `orthophoto_2023-01-01`, `orthophoto_2024-04-27`) from the output directory to the root directory of your repository.

4. **Modify `googlemaps.html`:**

   - Open `googlemaps.html` in a text editor.

   - **Add radio buttons:**

     In the HTML section, locate the area where radio buttons or other selection elements are defined (it might vary depending on the existing code). Add new radio buttons like this (adjust the names and IDs as needed):

     ```html
     <input type="radio" name="date" value="WP4-072021" onclick="toggleOverlay(this)" /> WP4-072021<br />
     ```

   - **Update the initialization script (optional):**

     ```html
     ret = ret + "/WP4-072021/" + zoom + "/" + coord.x + "/" + coord.y + ".png";
     ```

   - **Map center coordinates:** In the init function, adjust the latitude and longitude values in the JavaScript code to center the map on your desired location.  

**Running the viewer:**

1. Open `googlemaps.html` in a web browser to view your interactive orthophoto viewer.

**Additional Notes:**

* This example uses Leaflet for the interactive map. You can explore other JavaScript mapping libraries if desired.
