# Smart-fit-website
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SmartFit Pro – Demo Product Website</title>
  <meta name="description" content="Demo product website for college project – works offline and on Android." />
  <style>
    :root{
      --bg:#0b1220;--card:#121a2b;--muted:#8892a6;--brand:#4f8cff;--brand2:#22d3ee;--text:#e6eefc;--ok:#22c55e;--warn:#f59e0b;--danger:#ef4444
    }
    *{box-sizing:border-box}
    html,body{margin:0;background:linear-gradient(180deg,var(--bg),#0d1426 40%,#0a1020);color:var(--text);font-family:system-ui,-apple-system,Segoe UI,Roboto,Inter,Arial,sans-serif}
    a{color:var(--brand);text-decoration:none}
    img{max-width:100%;display:block}
    .container{width:min(1100px,92%);margin-inline:auto}/* Header / Nav */
header{position:sticky;top:0;z-index:50;background:rgba(10,16,32,.75);backdrop-filter:saturate(160%) blur(8px);border-bottom:1px solid #1e293b}
.nav{display:flex;align-items:center;justify-content:space-between;padding:.8rem 0}
.brand{display:flex;gap:.6rem;align-items:center;font-weight:700;letter-spacing:.4px}
.badge{width:34px;height:34px;border-radius:10px;background:linear-gradient(135deg,var(--brand),var(--brand2));display:grid;place-items:center;font-weight:800}
.brand span{font-size:1.05rem}
.links{display:flex;gap:1rem;align-items:center}
.links a{padding:.4rem .7rem;border-radius:.7rem}
.links a:hover{background:#1b2439}
.cart{display:flex;gap:.5rem;align-items:center}
.cart-count{min-width:1.4rem;height:1.4rem;border-radius:999px;background:var(--brand);display:grid;place-items:center;font-size:.8rem;font-weight:700}
.menu-btn{display:none;border:1px solid #273349;border-radius:.7rem;padding:.45rem .6rem;background:#10182a}

/* Hero */
.hero{display:grid;grid-template-columns:1.15fr .85fr;gap:1.2rem;align-items:center;padding:2.2rem 0}
.title{font-size:clamp(1.8rem,3vw,3rem);line-height:1.1;margin:0 0 .6rem}
.subtitle{color:var(--muted);margin:.2rem 0 1.2rem}
.cta{display:flex;gap:.8rem;flex-wrap:wrap}
.btn{border:none;background:linear-gradient(135deg,var(--brand),var(--brand2));color:#061024;padding:.8rem 1rem;border-radius:1rem;font-weight:700}
.btn.sec{background:#10182a;color:var(--text);border:1px solid #2a3550}
.card{background:var(--card);border:1px solid #1f2a44;border-radius:1.2rem;padding:1rem}

/* Sections */
section{padding:2.2rem 0}
h2{margin:0 0 1rem;font-size:1.5rem}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem}
.grid-2{display:grid;grid-template-columns:repeat(2,1fr);gap:1rem}

/* Gallery placeholders */
.gallery{display:grid;grid-template-columns:repeat(4,1fr);gap:.8rem}
.ph{aspect-ratio:1/1;border-radius:1rem;background:linear-gradient(135deg,#1a2440,#0f162b);border:1px dashed #334155;display:grid;place-items:center;color:#93a4c7}

/* Product */
.price{font-size:1.4rem;font-weight:800}
.pill{display:inline-flex;gap:.5rem;align-items:center;background:#0e1628;border:1px solid #20304d;border-radius:999px;padding:.35rem .6rem;font-size:.85rem;color:#9fb2d5}

/* Footer */
footer{border-top:1px solid #1e293b;padding:1.6rem 0;color:#9fb2d5}

/* Mobile */
@media (max-width:860px){
  .hero{grid-template-columns:1fr}
  .grid-3{grid-template-columns:1fr}
  .grid-2{grid-template-columns:1fr}
  .gallery{grid-template-columns:repeat(2,1fr)}
  .links{display:none}
  .menu-btn{display:inline-flex}
  .mobile-menu{display:none;flex-direction:column;gap:.3rem;padding:.6rem 0}
  .mobile-menu a{padding:.6rem;border:1px solid #273349;border-radius:.7rem;background:#10182a}
}

  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="badge">SF</div>
        <span>SmartFit Pro</span>
      </div>
      <nav class="links" aria-label="Primary">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#product">Product</a>
        <a href="#gallery">Gallery</a>
        <a href="#contact">Contact</a>
      </nav>
      <div class="cart" role="button" aria-label="Cart" onclick="alert('Demo only: items stored locally.');">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6 6h15l-1.5 9h-12L6 3H3" stroke="#9fb2d5" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
        <span class="cart-count" id="cartCount">0</span>
      </div>
      <button class="menu-btn" id="menuBtn">☰</button>
    </div>
    <div class="container mobile-menu" id="mobileMenu">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#product">Product</a>
      <a href="#gallery">Gallery</a>
      <a href="#contact">Contact</a>
    </div>
  </header>  <!-- HERO / HOME -->  <main id="home" class="container hero">
    <div>
      <h1 class="title">Stay Connected, Stay Fit – Anytime, Anywhere!</h1>
      <p class="subtitle">Introducing <strong>SmartFit Pro</strong>, the ultimate smartwatch for fitness and lifestyle. Track your health, receive notifications, and look stylish – all in one.</p>
      <div class="cta">
        <button class="btn" onclick="addToCart('SmartFit Pro')">Buy Now</button>
        <a class="btn sec" href="#product">Learn More</a>
      </div>
      <div style="margin-top:1rem;display:flex;gap:.6rem;flex-wrap:wrap">
        <span class="pill">IP68 Water Resistant</span>
        <span class="pill">7‑Day Battery</span>
        <span class="pill">Bluetooth Calls</span>
      </div>
    </div>
    <div class="card">
      <!-- Inline SVG "product" render so it works offline -->
      <svg viewBox="0 0 520 520" width="100%" aria-label="Smartwatch illustration" role="img">
        <defs>
          <linearGradient id="g1" x1="0" y1="0" x2="1" y2="1">
            <stop offset="0" stop-color="#1f2c4d"/>
            <stop offset="1" stop-color="#0c1224"/>
          </linearGradient>
          <linearGradient id="g2" x1="0" y1="0" x2="1" y2="1">
            <stop offset="0" stop-color="#4f8cff"/>
            <stop offset="1" stop-color="#22d3ee"/>
          </linearGradient>
        </defs>
        <rect x="0" y="0" width="520" height="520" rx="26" fill="url(#g1)" />
        <g transform="translate(120 60)">
          <rect x="0" y="0" width="280" height="400" rx="46" fill="#0b1220" stroke="#2b3a62" stroke-width="10"/>
          <rect x="18" y="18" width="244" height="364" rx="30" fill="#0f1a34" stroke="#33446e"/>
          <circle cx="140" cy="200" r="90" fill="#081024" stroke="#3e538a"/>
          <path d="M140 120 a80 80 0 1 0 .1 0" fill="none" stroke="#4f8cff" stroke-width="10"/>
          <path d="M140 200 l55 -40" stroke="#22d3ee" stroke-width="10" stroke-linecap="round"/>
          <circle cx="140" cy="200" r="12" fill="#22d3ee"/>
        </g>
        <rect x="85" y="70" width="350" height="30" rx="14" fill="url(#g2)" opacity=".25"/>
        <rect x="85" y="420" width="350" height="30" rx="14" fill="url(#g2)" opacity=".25"/>
      </svg>
    </div>
  </main>  <!-- ABOUT -->  <section id="about">
    <div class="container">
      <h2>About SmartFit Pro</h2>
      <p class="subtitle">SmartFit Pro is designed to make your life easier and healthier. With advanced health monitoring, long battery life, and a sleek design, it’s your personal assistant on your wrist.</p>
      <div class="grid-3">
        <div class="card"><strong>Accurate Health Tracking</strong><br><span class="subtitle">Heart rate, steps, sleep insights.</span></div>
        <div class="card"><strong>Seamless Connectivity</strong><br><span class="subtitle">Calls, texts, app alerts.</span></div>
        <div class="card"><strong>Great Value</strong><br><span class="subtitle">Premium features at an affordable price.</span></div>
      </div>
    </div>
  </section>  <!-- PRODUCT -->  <section id="product">
    <div class="container">
      <h2>SmartFit Pro – Smartwatch</h2>
      <div class="grid-2">
        <div class="card">
          <p class="price">₹4,999 <span class="subtitle">(inclusive of taxes)</span></p>
          <ul class="subtitle">
            <li>Heart Rate & Sleep Monitor</li>
            <li>Step Counter & Calorie Tracker</li>
            <li>Bluetooth Calls & Notifications</li>
            <li>Water Resistant (IP68)</li>
            <li>7‑Day Battery Life</li>
          </ul>
          <div class="cta">
            <button class="btn" onclick="addToCart('SmartFit Pro')">Add to Cart</button>
            <button class="btn sec" onclick="fakeCheckout()">Buy Now</button>
          </div>
        </div>
        <div class="card">
          <h3 style="margin-top:0">What happens in this demo?</h3>
          <ol class="subtitle" style="margin:0;padding-left:1.1rem">
            <li><strong>Add to Cart</strong> saves an item count to your device (localStorage).</li>
            <li><strong>Buy Now</strong> shows a mock checkout message – no payments.</li>
            <li>Everything works fully <em>offline</em> and on Android/Chrome.</li>
          </ol>
          <p class="subtitle" style="margin-top:.8rem">Use this to <em>demonstrate</em> how a product website flows: browse → add to cart → checkout.</p>
        </div>
      </div>
    </div>
  </section>  <!-- GALLERY -->  <section id="gallery">
    <div class="container">
      <h2>Gallery</h2>
      <div class="gallery">
        <div class="ph">Product – Black</div>
        <div class="ph">Product – Silver</div>
        <div class="ph">Fitness Screen</div>
        <div class="ph">Calls & Alerts</div>
      </div>
      <p class="subtitle" style="margin-top:1rem">Tip: Replace these boxes with your own images if you want (insert <code>&lt;img src="yourimage.jpg" /&gt;</code>).</p>
    </div>
  </section>  <!-- CONTACT -->  <section id="contact">
    <div class="container">
      <h2>Contact</h2>
      <div class="grid-2">
        <form class="card" onsubmit="return fakeSubmit(this)">
          <label>Name<br><input required name="name" style="width:100%;padding:.7rem;border-radius:.7rem;border:1px solid #2a3550;background:#0c1426;color:var(--text)"></label><br><br>
          <label>Email<br><input required type="email" name="email" style="width:100%;padding:.7rem;border-radius:.7rem;border:1px solid #2a3550;background:#0c1426;color:var(--text)"></label><br><br>
          <label>Message<br><textarea required name="msg" rows="4" style="width:100%;padding:.7rem;border-radius:.7rem;border:1px solid #2a3550;background:#0c1426;color:var(--text)"></textarea></label><br><br>
          <button class="btn" type="submit">Send Message</button>
        </form>
        <div class="card">
          <p class="subtitle" style="margin-top:0">Email: support@smartfitpro.com<br>Phone: +91 98765 43210<br>Address: Pune, Maharashtra, India</p>
          <div style="display:flex;gap:.6rem;flex-wrap:wrap">
            <span class="pill">Facebook</span>
            <span class="pill">Instagram</span>
            <span class="pill">Twitter / X</span>
          </div>
          <p class="subtitle">(Social buttons are placeholders in this offline demo.)</p>
        </div>
      </div>
    </div>
  </section>  <footer>
    <div class="container">© 2025 SmartFit Pro • Demo site for academic use.</div>
  </footer>  <!-- Tiny Toast & Logic -->  <div id="toast" style="position:fixed;left:50%;bottom:20px;transform:translateX(-50%) scale(.98);background:#0e1628;border:1px solid #2a3654;color:#cfe1ff;padding:.7rem 1rem;border-radius:.8rem;box-shadow:0 10px 30px rgba(0,0,0,.35);opacity:0;pointer-events:none;transition:.18s ease;z-index:60"></div>  <script>
    const $ = s=>document.querySelector(s);
    const toast = msg=>{const t=$('#toast');t.textContent=msg;t.style.opacity='1';t.style.transform='translateX(-50%) scale(1)';setTimeout(()=>{t.style.opacity='0';t.style.transform='translateX(-50%) scale(.98)'},1700)}

    // Mobile menu toggle
    $('#menuBtn').addEventListener('click',()=>{
      const m = $('#mobileMenu');
      m.style.display = m.style.display==='flex' ? 'none' : 'flex';
    });

    // Cart count from localStorage
    const KEY='smartfit_cart_count';
    const getCount=()=>Number(localStorage.getItem(KEY)||0);
    const setCount=n=>{localStorage.setItem(KEY,n);$('#cartCount').textContent=n};
    setCount(getCount());

    window.addToCart=(name)=>{
      const n = getCount()+1; setCount(n);
      toast(`${name} added to cart • Total: ${n}`);
    }
    window.fakeCheckout=()=>{
      const n = getCount();
      if(!n){toast('Cart is empty. Add an item first.');return}
      toast('Demo checkout complete. (No real payment)');
      setTimeout(()=>{setCount(0)},900);
    }
    window.fakeSubmit=(form)=>{
      const data = Object.fromEntries(new FormData(form).entries());
      localStorage.setItem('smartfit_last_msg', JSON.stringify({ ...data, ts: Date.now() }));
      toast('Message saved locally (demo).');
      form.reset();
      return false; // prevent real submit
    }
  </script></body>
</html>
