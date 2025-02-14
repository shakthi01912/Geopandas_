# NYC Neighborhood Accessibility Analysis

## Overview
This project analyzes accessibility in New York City neighborhoods by integrating various datasets, including schools, subway entrances, bike paths, parks, and neighborhood boundaries. The analysis involves spatial data processing using GeoPandas and H3 grid indexing.

## Data Sources
- **Schools**: `data/nyc/SchoolPoints_APS_2024_08_28.shp`
- **Subway Entrances**: `data/nyc/nyc_subway_entrances.shp`
- **Bike Paths**: `data/nyc/New York City Bike Routes_20241223.geojson`
- **Neighborhood Boundaries**: `https://raw.githubusercontent.com/HodgesWardElliott/custom-nyc-neighborhoods/main/nyc_neighborhoods.geojson`
- **Parks**: `data/nyc/Parks Properties_20241223.geojson`

## Steps in the Analysis
1. **Load Data**
   - Read GeoJSON, shapefiles, and other spatial data into GeoPandas.
2. **Convert to Consistent CRS**
   - Convert all datasets to EPSG:3857 for accurate spatial calculations.
3. **Set Up H3 Grid**
   - Overlay H3 hexagonal grid to standardize spatial analysis.
4. **Run Normalization Analysis**
   - Normalize accessibility scores for different datasets.
5. **Compute Total Score**
   - Aggregate and calculate accessibility scores per neighborhood.

## Requirements
- Python 3.x
- GeoPandas
- H3-Py
- Pandas
- Fiona
- Shapely
- Pyogrio

## Usage
Run the script in a Python environment:
```bash
python analysis.py
```

## Output
- A processed GeoDataFrame with accessibility scores.
- GeoJSON and Parquet file outputs for further analysis.
<img width="1317" alt="image" src="https://github.com/user-attachments/assets/76393ff2-c4c5-4a7d-b2e2-d909726b0e27" />


## License
This project is licensed under the MIT License.

