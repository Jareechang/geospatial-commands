# Useful Geospatial commands 

A list of useful commands to convert between geospatial file formats (\*.shp, \*.xml, topojson)


### Commands

**Displaying overview:**


Overview of file formats, data type of shapefile

```sh
ogr2info -al -so target.shp
```

**Conversions:**  

```sh
 ogr2ogr -f "GeoJSON" output.json \ 
    -s_srs 'EPSG:4326' \ 
    -t_srs 'EPSG:3081' \
    input.shp 
```



