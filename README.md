<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Belize Districts Game</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

  <!-- Animate.css for easy animations -->
  <link href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" rel="stylesheet">

  <style>
    body {
      background: linear-gradient(to bottom right, #dff3ff, #f9fcff);
      min-height: 100vh;
    }
    h2 {
      font-weight: 700;
    }
    .card {
      border-radius: 20px;
      overflow: hidden;
    }
    .btn-group-vertical .btn {
      width: 200px;
      font-weight: 500;
      transition: transform 0.2s ease;
    }
    .btn-group-vertical .btn:hover {
      transform: scale(1.05);
    }
  </style>
</head>
<body class="text-center p-4">

  <div class="container">
    <h2 class="mb-3 text-primary animate__animated animate__fadeInDown">Belize Districts Game</h2>
    <p class="text-muted animate__animated animate__fadeInUp">Made by Michael Lammey</p>
    <p class="animate__animated animate__fadeInUp">Click a district name to see its map.</p>

    <!-- Image Display -->
    <div class="card shadow mx-auto animate__animated animate__zoomIn" style="max-width: 400px;">
      <img id="myImage" src="BelizeBlank.png" class="card-img-top img-fluid animate__animated animate__fadeIn" alt="Belize Map">
      <div class="card-body">
        <p class="card-text text-secondary">Select a district below:</p>
      </div>
    </div>

    <!-- Buttons -->
    <div class="mt-4 animate__animated animate__fadeInUp">
      <div class="btn-group-vertical mx-auto">
        <button class="btn btn-outline-primary mb-2" onclick="changeImage('Belize.png')">Belize</button>
        <button class="btn btn-outline-success mb-2" onclick="changeImage('Cayo.png')">Cayo</button>
        <button class="btn btn-outline-warning mb-2" onclick="changeImage('Corozal.png')">Corozal</button>
        <button class="btn btn-outline-danger mb-2" onclick="changeImage('OrangeWalk.png')">Orange Walk</button>
        <button class="btn btn-outline-info mb-2" onclick="changeImage('StannCreek.png')">Stann Creek</button>
        <button class="btn btn-outline-dark" onclick="changeImage('Toledo.png')">Toledo</button>
      </div>
    </div>
  </div>

  <!-- JavaScript -->
  <script>
    function changeImage(imageName) {
      const img = document.getElementById('myImage');
      // Add fade-out animation
      img.classList.remove('animate__fadeIn');
      img.classList.add('animate__fadeOut');

      // Wait for fade-out, then switch image and fade back in
      setTimeout(() => {
        img.src = imageName;
        img.classList.remove('animate__fadeOut');
        img.classList.add('animate__fadeIn');
      }, 400);
    }
  </script>

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
