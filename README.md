- 👋 Hi, I’m @Thisisit1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Thisisit1/Thisisit1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html>
<head>
  <title>ScanPaylaundry</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
      background-color: #f2f2f2;
    }

    h1 {
      margin: 20px;
      color: #333;
    }

    #main-image {
      max-width: 600px;
      margin: 20px auto;
      border-radius: 10px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    #qr-code {
      margin: 20px auto;
      max-width: 300px;
    }

    #result {
      font-weight: bold;
      margin: 20px;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>Welcome to ScanPaylaundry</h1>
  <img id="main-image" src="laundry.jpg" alt="Laundry Machines and Building" />
  <p>Scan the QR code to make a payment:</p>
  <div id="qr-code">
    <img id="qr-image" src="placeholder.png" alt="QR Code" />
  </div>
  <div id="result"></div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script src="https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js"></script>
  <script>
    // Generate QR code using qrcode.js library
    var qrCode = new QRCode(document.getElementById("qr-code"), {
      width: 300,
      height: 300
    });

    // Replace "placeholder.png" with the actual QR code image path
    qrCode.makeCode("https://www.example.com");

    // Function to handle scanning results
    function handleScanResult(result) {
      $("#result").text("Scanned: " + result);
    }

    // Function to simulate scanning a QR code
    function simulateScan() {
      var scannedResult = "https://www.example.com"; // Replace with the actual scanned result
      handleScanResult(scannedResult);
    }

    // Simulate scanning a QR code when the page loads
    $(document).ready(function() {
      simulateScan();
    });
  </script>
</body>
</html>
