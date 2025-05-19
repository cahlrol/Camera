# Camera<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Camera Access</title>
  <style>
    body { font-family: Arial; text-align: center; margin-top: 50px; }
    video { width: 80%; max-width: 600px; border: 2px solid #ccc; border-radius: 10px; }
  </style>
</head>
<body>
  <h1>📷 Camera Access Demo</h1>
  <video id="video" autoplay playsinline></video>
  <script>
    const video = document.getElementById("video");
    navigator.mediaDevices.getUserMedia({ video: true })
      .then(stream => { video.srcObject = stream; })
      .catch(err => { alert("Camera access denied or not available."); });
  </script>
</body>
</html>
