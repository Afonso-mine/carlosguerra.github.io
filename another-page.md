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
  // Initialize the map centered on a specific location
  var map = L.map('map').setView([37.7749, -122.4194], 10); // Example: San Francisco coordinates

  // Add OpenStreetMap tiles to the map
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
  }).addTo(map);

  // Load GeoJSON data from an external file
  fetch('assets/your-geojson-file.geojson')
    .then(response => response.json())
    .then(data => {
      L.geoJSON(data).addTo(map);
    });

  // Add a marker to the map at a specific location
  var marker = L.marker([37.7749, -122.4194]).addTo(map); // Example: San Francisco coordinates

  // Optional: Add a popup to the marker
  marker.bindPopup("<b>Carlos!</b><br>https://en.wikipedia.org/wiki/San_Francisco").openPopup();

  var marker = L.marker([39.557191, -7.8536599]).addTo(map); // Example: Portugal coordinates

  // Optional: Add a popup to the marker
  marker.bindPopup("<b>Portugal!</b><br>https://en.wikipedia.org/wiki/Portugal").openPopup();
</script>



[back](./)
