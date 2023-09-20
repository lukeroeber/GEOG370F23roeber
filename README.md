# GEOG370F23roeber
Github Repo for GEOG 370 class @ UNC-CH
<!DOCTYPE html>
<html>
<head>
  <title>Leaflet Preview</title>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css"
   integrity="sha384-o/2yZuJZWGJ4s/adjxVW71R+EO/LyCwdQfP5UWSgX/w87iiTXuvDZaejd3TsN7mf"
   crossorigin=""/>
  <script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js"
   integrity="sha384-okbbMvvx/qfQkmiQKfd5VifbKZ/W8p1qIsWvE1ROPUfHWsDcC8/BnHohF7vPg2T6"
   crossorigin=""></script>
  <style type="text/css">
    body {
       margin: 0;
       padding: 0;
    }
    html, body, #map{
       width: 100%;
       height: 100%;
    }
  </style>
</head>
<body>
  <div id="map"></div>
  <script>
      var map = L.map('map', { attributionControl: false } ).setView([35.904400529, -79.04991829849999], 14.0);
      L.control.attribution( { prefix: false } ).addTo( map );
      
      var tilesource_layer = L.tileLayer('./mytiles/{z}/{x}/{y}.png', {
        minZoom: 12,
        maxZoom: 16,
        tms: false,
        attribution: 'Created by QGIS algorithm: Generate XYZ tiles (Directory)'
      }).addTo(map);
  </script>
</body>
</html>
