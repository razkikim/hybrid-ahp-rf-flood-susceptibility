# Data Directory

## samples/
- `dataset_training.csv` — Training dataset with columns: [lat, lon, label, elevasi, slope, jarak_sungai, jarak_pantai, tutupan_lahan, jenis_tanah, ndvi, curah_hujan]

## raw/
Place your raw geospatial data here:
- `elevasi.tif` — DEMNAS digital elevation model
- `slope.tif` — Slope derived from DEM
- `jarak_sungai.tif` — Distance to river
- `jarak_pantai.tif` — Distance to coast
- `tutupan_lahan.tif` — Land cover classification
- `jenis_tanah.tif` — Soil type classification
- `ndvi.tif` — NDVI from Sentinel-2
- `curah_hujan.tif` — Rainfall from CHIRPS
- `admin_tapteng_UTM47N.shp` — Administrative boundary shapefile
- `rekap_kecamatan.xlsx` — Flood event summary by sub-district

## raster/
Place classified susceptibility rasters here:
- `ahp_classified.tif` — AHP susceptibility classes (1-5)
- `rf_classified.tif` — RF susceptibility classes (1-5)
