# The-Triple-Bite
The Triple Bite is an artisanal dessert brand specializing in blondies, brownies, and brookies made with premium ingredients and baked fresh daily. Our website offers a modern, aesthetic, and mobile-friendly experience where customers can explore flavors, place orders, and connect with the brand online.
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Triple Bite</title>

  <style>
    body{
      margin:0;
      font-family: Arial, sans-serif;
      background:#fff8f2;
      color:#2d1b12;
    }

    /* HERO */
    .hero{
      height:100vh;
      background:linear-gradient(rgba(0,0,0,.4),rgba(0,0,0,.4)),
      url('https://images.unsplash.com/photo-1559622214-f8a9850965bb?q=80&w=1400&auto=format&fit=crop');
      background-size:cover;
      background-position:center;
      color:white;
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      text-align:center;
      padding:20px;
    }

    .hero h1{
      font-size:4rem;
      margin:0;
    }

    .hero p{
      font-size:1.3rem;
      margin:15px 0 25px;
    }

    /* BUTTON */
    .btn{
      background:#d9a066;
      color:white;
      padding:12px 25px;
      border-radius:10px;
      text-decoration:none;
      font-weight:bold;
      display:inline-block;
    }

    .btn.big{
      font-size:1.2rem;
      padding:15px 30px;
    }

    /* SECTIONS */
    .section{
      padding:60px 20px;
      text-align:center;
    }

    .section.dark{
      background:#4a2c2a;
      color:white;
    }

    /* GRID */
    .grid{
      display:flex;
      gap:20px;
      justify-content:center;
      flex-wrap:wrap;
      margin-top:30px;
    }

    /* CARDS */
    .card{
      background:white;
      padding:20px;
      border-radius:15px;
      width:250px;
      box-shadow:0 6px 15px rgba(0,0,0,.1);
    }

    .card.small{
      width:180px;
    }

    .card h3{
      margin-bottom:10px;
    }

    .card span{
      display:block;
      margin:10px 0;
      font-weight:bold;
    }

    .card button{
      background:#4a2c2a;
      color:white;
      border:none;
      padding:10px;
      border-radius:8px;
      cursor:pointer;
    }

    /* DELIVERY */
    .delivery{
      font-size:1.1rem;
      line-height:1.8;
    }

    /* CENTER */
    .center{
      display:flex;
      flex-direction:column;
      align-items:center;
    }
  </style>
</head>

<body>

  <!-- HERO -->
  <header class="hero">
    <h1>The Triple Bite</h1>
    <p>Freshly baked blondies, brownies & brookies 🍫</p>
    <a href="#menu" class="btn">View Menu</a>
  </header>

  <!-- MENU -->
  <section id="menu" class="section">

    <h2>Our Desserts</h2>

    <div class="grid">

      <div class="card">
        <h3>Brownies</h3>
        <p>Rich fudgy chocolate brownie.</p>
        <span>$5</span>
        <button onclick="order('Brownie')">Order</button>
      </div>

      <div class="card">
        <h3>Blondies</h3>
        <p>Soft vanilla caramel bar.</p>
        <span>$5</span>
        <button onclick="order('Blondie')">Order</button>
      </div>

      <div class="card">
        <h3>Brookies</h3>
        <p>Cookie + brownie fusion.</p>
        <span>$6</span>
        <button onclick="order('Brookie')">Order</button>
      </div>

    </div>

  </section>

  <!-- TOPPINGS -->
  <section class="section dark">

    <h2>Premium Toppings</h2>

    <div class="grid">

      <div class="card small">
        <h3>Nutella</h3>
        <p>+ $1.50</p>
      </div>

      <div class="card small">
        <h3>Nido</h3>
        <p>+ $1.00</p>
      </div>

    </div>

  </section>

  <!-- DELIVERY -->
  <section class="section">

    <h2>Delivery</h2>

    <p class="delivery">
      🚚 Fast delivery available in Santa Cruz<br>
      ⏱ 30–45 minutes<br>
      📍 Pickup available
    </p>

  </section>

  <!-- ORDER -->
  <section class="section center">

    <h2>Place your order</h2>

    <a id="whatsappBtn" class="btn big" target="_blank">
      Order via WhatsApp
    </a>

  </section>

  <script>
    const phone = "TUNUMERO"; // cambia esto por tu número

    let orderItem = "";

    function order(product){
      orderItem = product;

      const btn = document.getElementById("whatsappBtn");

      const message = `Hello! I want to order a ${product} from The Triple Bite 🍫`;

      btn.href = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
    }
  </script>

</body>
</html>
