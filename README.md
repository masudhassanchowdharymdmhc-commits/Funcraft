o# Funcraft
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Green Dharmanagar - Plant Shop</title>
  <style>
    * {margin:0; padding:0; box-sizing:border-box; font-family:'Segoe UI',sans-serif}
    body {background:#f6fbf6; color:#1a1a1a}
    header {background:#2d6a4f; color:white; padding:1rem 5%; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap}
    header h1 {font-size:1.5rem}
    nav a {color:white; margin-left:1.5rem; text-decoration:none; font-weight:500}
    .hero {padding:4rem 5%; text-align:center; background:url('https://images.unsplash.com/photo-1463320726281-696a485928c7?w=1200') center/cover; color:white}
    .hero h2 {font-size:2.5rem; margin-bottom:1rem; text-shadow:2px 2px 4px rgba(0,0,0,0.5)}
    .btn {background:#52b788; color:white; padding:0.8rem 1.5rem; border:none; border-radius:8px; cursor:pointer; font-size:1rem; text-decoration:none; display:inline-block}
    .btn:hover {background:#40916c}
    .section {padding:3rem 5%}
    .section h3 {text-align:center; font-size:2rem; margin-bottom:2rem; color:#2d6a4f}
    .products {display:grid; grid-template-columns:repeat(auto-fit, minmax(250px, 1fr)); gap:2rem}
    .card {background:white; border-radius:12px; overflow:hidden; box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    .card img {width:100%; height:200px; object-fit:cover}
    .card-body {padding:1rem}
    .card-body h4 {margin-bottom:0.5rem}
    .price {color:#2d6a4f; font-weight:bold; font-size:1.2rem; margin:0.5rem 0}
    .category {display:flex; gap:1rem; justify-content:center; flex-wrap:wrap; margin-bottom:2rem}
    .tag {background:#d8f3dc; color:#2d6a4f; padding:0.5rem 1rem; border-radius:20px; cursor:pointer}
    .tag:hover {background:#b7e4c7}
    footer {background:#1b4332; color:white; text-align:center; padding:2rem 5%; margin-top:3rem}
    #cart {position:fixed; bottom:20px; right:20px; background:#2d6a4f; color:white; padding:1rem; border-radius:50px; cursor:pointer}
  </style>
</head>
<body>

  <header>
    <h1>Green Dharmanagar 🌿</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#shop">Shop</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <h2>Bring Nature Home</h2>
    <p>Fresh Indoor & Outdoor Plants directly from our nursery</p>
    <br>
    <a href="#shop" class="btn">Shop Now</a>
  </section>

  <section class="section" id="shop">
    <h3>Best Selling Plants</h3>
    <div class="category">
      <span class="tag">Indoor</span>
      <span class="tag">Outdoor</span>
      <span class="tag">Low Light</span>
      <span class="tag">Air Purifying</span>
    </div>
    <div class="products">
      <div class="card">
        <img src="https://images.unsplash.com/photo-1614594975525-e45190c55d0b?w=500" alt="Snake Plant">
        <div class="card-body">
          <h4>Snake Plant</h4>
          <p>Perfect for bedrooms. Thrives with minimal care.</p>
          <div class="price">₹299</div>
          <button class="btn" onclick="addToCart('Snake Plant')">Add to Cart</button>
        </div>
      </div>
      <div class="card">
        <img src="https://images.unsplash.com/photo-1593691509543-c55fb32d8de5?w=500" alt="Money Plant">
        <div class="card-body">
          <h4>Money Plant</h4>
          <p>Brings positivity. Grows in water or soil.</p>
          <div class="price">₹149</div>
          <button class="btn" onclick="addToCart('Money Plant')">Add to Cart</button>
        </div>
      <div class="card">
        <img src="https://images.unsplash.com/photo-1509423350716-97f2360af8e4?w=500" alt="Areca Palm">
        <div class="card-body">
          <h4>Areca Palm</h4>
          <p>Elevates your living room. Natural air purifier.</p>
          <div class="price">₹399</div>
          <button class="btn" onclick="addToCart('Areca Palm')">Add to Cart</button>
        </div>
      </div>
    </div>
  </section>

  <section class="section" id="about">
    <h3>Our Story</h3>
    <p style="text-align:center; max-width:700px; margin:auto">From Dharmanagar, we've been delivering fresh and healthy plants to your doorstep since 2020. Every plant is grown with care in our own nursery. We offer COD and free plant care guides with delivery.</p>
  </section>

  <section class="section" id="contact">
    <h3>Contact Us</h3>
    <p style="text-align:center">
      📍 Dharmanagar, Tripura <br>
      📞 WhatsApp: +91 98765 43210 <br>
      🕒 9 AM - 7 PM, Monday to Sunday
    </p>
  </section>

  <footer>
    © 2026 Green Dharmanagar. All rights reserved.
  </footer>

  <div id="cart" onclick="showCart()">🛒 <span id="count">0</span></div>

  <script>
    let cart = 0;
    function addToCart(name) {
      cart++;
      document.getElementById('count').innerText = cart;
      alert(name + ' added to cart!');
    }
    function showCart() {
      alert('You have ' + cart + ' plants in cart. Checkout feature coming soon!');
    }
  </script>

</body>
</html>
