<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kannan Farms - Natural Health Products</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f8f8f8;
      color: #333;
    }
    header {
      background-color: #4CAF50;
      color: white;
      padding: 20px;
      text-align: center;
      position: relative;
    }
    header img {
      position: absolute;
      top: 10px;
      left: 10px;
      height: 50px;
    }
    .container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 20px;
    }
    .product {
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin: 15px;
      padding: 20px;
      width: 300px;
      text-align: center;
    }
    .carousel {
      position: relative;
      width: 100%;
      overflow: hidden;
      border-radius: 10px;
    }
    .carousel img {
      width: 100%;
      display: none;
      transition: opacity 0.5s ease-in-out;
    }
    .carousel img.active {
      display: block;
    }
    .product h2 {
      margin: 15px 0 10px;
    }
    .product p {
      font-size: 14px;
    }
    .whatsapp-button {
      background-color: #25D366;
      color: white;
      border: none;
      padding: 10px 20px;
      margin-top: 10px;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
    }
    footer {
      text-align: center;
      padding: 20px;
      background-color: #4CAF50;
      color: white;
    }
  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="Kannan Farms Logo">
    <h1>Kannan Farms</h1>
    <p>Natural Products for a Healthier You</p>
  </header>

  <div class="container">
    <div class="product">
      <div class="carousel" id="banana-carousel">
        <img src="banana1.jpg" class="active" alt="Banana Powder 1">
        <img src="banana2.jpg" alt="Banana Powder 2">
        <img src="banana3.jpg" alt="Banana Powder 3">
      </div>
      <h2>Banana Powder</h2>
      <p>Ideal for children and gym-goers. Natural weight gain and energy booster.</p>
      <a class="whatsapp-button" href="https://wa.me/919000000000?text=I%20want%20to%20order%20Banana%20Powder">Order on WhatsApp</a>
    </div>

    <div class="product">
      <div class="carousel" id="moringa-carousel">
        <img src="moringa1.jpg" class="active" alt="Moringa Powder 1">
        <img src="moringa2.jpg" alt="Moringa Powder 2">
        <img src="moringa3.jpg" alt="Moringa Powder 3">
      </div>
      <h2>Moringa Powder</h2>
      <p>Rich in vitamins and antioxidants. A daily dose of health in every spoon.</p>
      <a class="whatsapp-button" href="https://wa.me/919000000000?text=I%20want%20to%20order%20Moringa%20Powder">Order on WhatsApp</a>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Kannan Farms. All rights reserved.</p>
  </footer>

  <script>
    function setupCarousel(carouselId) {
      const carousel = document.getElementById(carouselId);
      const images = carousel.getElementsByTagName('img');
      let index = 0;
      setInterval(() => {
        images[index].classList.remove('active');
        index = (index + 1) % images.length;
        images[index].classList.add('active');
      }, 3000);
    }

    setupCarousel('banana-carousel');
    setupCarousel('moringa-carousel');
  </script>
</body>
</html>
