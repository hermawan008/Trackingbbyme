# Trackingbbyme
Track
<!DOCTYPE html>
<html>
<head>
  <title>Lokasi Tracker</title>
  <script>
    function getLocation() {
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition, showError);
      } else {
        alert("Browser tidak mendukung geolocation.");
      }
    }

    function showPosition(position) {
      const lat = position.coords.latitude;
      const lon = position.coords.longitude;
      alert("Lokasi kamu:\nLatitude: " + lat + "\nLongitude: " + lon);
    }

    function showError(error) {
      alert("Gagal mengakses lokasi: " + error.message);
    }
  </script>
</head>
<body>
  <h2>Tracking Lokasi</h2>
  <button onclick="getLocation()">Klik untuk cek lokasi kamu</button>
</body>
</html>
