<h3>Resource</h3>
go to geodata.gov.gr/el/dataset/poleis, then under "Sinolo Dedomenon" click on "Metamorfosi". Then choose "GeoJSON" as a format and "WGS84 (EPSG:4326)" as the coordinate system. Then click on "Metamorfosi" to see the JSON with the corresponding geospatial data of each greek city.

After testing the coordinates array, using an online service such as https://www.gps-coordinates.net/gps-coordinates-converter I found out that

<ul>
<li>coordinates[0] -> lon</li>
<li>coordinates [1] -> lat</li>
</ul>

---

<h3>Goal</h3>
associate each city with each corresponding lat long coordinates

---

<h3>Strategy</h3>
First verify that the cities you find from the api are already existing to the elUtils package. Then translate the array coordinates to lat lon and then after looping for each city add the corresponding properties.

---

<h3>TS project setup</h3>

<code>sudo npm install -g typescript ts-node</code>

<code>npm init -y</code>

<code>ts-node index.ts</code>

---

<h3>Conventions</h3>

WGS84 aka World Geodetic System 84

GeoJSON aka format for encoding a variety of geographic data structures

```javascript
{
    "type": "Feature",
    "geometry": {
        "type": "Point",
        "coordinates": [longitude, latitude]
    },
    "properties": {
    "name": "Example Point"
    }
}
```

GIS aka geographic information systems

Geospatial or geodata aka data that includes information related to locations on the Earth's surface.
