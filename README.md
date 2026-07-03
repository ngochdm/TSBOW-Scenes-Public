# Filter-Scenes-in-TSBOW

Web-based interface for filtering all scenes in the TSBOW dataset according to individual attributes.



## How to RUN

```bash
cd Filter-Scenes-TSBOW/

python -m http.server 8000  # Start a local HTTP server
```

Open your browser and navigate to:

http://localhost:8000/index.html



## Scenes Filtering

1. Weather: All, Normal, Haze, Rain, Snow

2. Scenario: All, Road, Intersection, Special Cases, Disaster

3. Road Type: All, Urban, Standard, Boulevard

4. Scale: All, Fine, Medium, Coarse

Click on `FILTER` button after chosing the filtering values.



## TSBOW_info.csv

The `TSBOW_info.csv` file includes column name: `videoID`, `scenario`, `daytime`, `weather`, `scale`, `roadtype`, `duration`.

Please check the order of column name in csv file with the filter data in `main.js`

```js
const filteredData = data.filter(row => {
            const [videoID, scenario, daytime, weather, scale, roadtype, duration] = row;
})
```
