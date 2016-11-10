# Useful Geospatial commands 

A list of useful commands to convert between geospatial file formats (\*.shp, \*.xml, topojson)


### Commands

**Displaying overview:**


Overview of file formats, data type of shapefile

```sh
ogr2info -al -so target.shp
```

Display all the data in shapefile

```sh
ogr2info -al target.shp
```

**Conversions:**  

Converts into `lat` and `lng` **GeoJSON** formats

```sh
 ogr2ogr -f "GeoJSON" output.json \ 
    -s_srs 'EPSG:4326' \ 
    -t_srs 'EPSG:3081' \
    input.shp 
```

Convert into **topojson**:

*recommended conversions if using D3 to visualize map data*

```sh
mkdir output && \
    ogr2ogr -f "GeoJSON" output.geo.json target.shp && \
    geo2topo --out output/output.topo.json output/ouput.geo.json

```



