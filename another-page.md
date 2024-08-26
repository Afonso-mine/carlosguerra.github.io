---
layout: default
---

## Welcome to my research page

[back](./)

**My articles**

{% include publications %}

**Main collaborations**

# My Interactive Map

<div id="map" style="height: 500px;"></div>

<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />

<script>
  var map = L.map('map').setView([37.7749, -122.4194], 10); // Example: San Francisco coordinates

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
  }).addTo(map);

  fetch('assets/your-geojson-file.geojson')
    .then(response => response.json())
    .then(data => {
      L.geoJSON(data).addTo(map);
    });
</script>


[back](./)
