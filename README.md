<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>rhode skin | by Jermaine Claire M. Rigonan</title>
    <style>
        /* Base Styling & Brand Colors */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Helvetica Neue', Arial, sans-serif;
            letter-spacing: 0.5px;
        }

        :root {
            --brand-gray: #f2f2f0;
            --brand-dark: #333333;
            --text-muted: #666666;
            --accent-soft: #e2dfd9;
            --ad-bg: #e9ecef;
        }

        body {
            background-color: #fafafa;
            color: var(--brand-dark);
            line-height: 1.5;
        }

        /* Top Ad Banner */
        .promo-ad-banner {
            background-color: var(--ad-bg);
            color: #000;
            text-align: center;
            padding: 10px 20px;
            font-size: 13px;
            font-weight: 500;
            border-bottom: 1px solid #ddd;
            position: relative;
        }

        .promo-ad-banner a {
            color: #d9534f;
            text-decoration: underline;
            font-weight: bold;
            margin-left: 5px;
        }

        .close-ad-btn {
            position: absolute;
            right: 15px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            font-size: 16px;
            cursor: pointer;
            color: var(--text-muted);
        }

        /* Navigation Bar Structure */
        header {
            background-color: #ffffff;
            border-bottom: 1px solid var(--brand-gray);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
        }

        /* Header Brand Section */
        .logo-area {
            display: flex;
            align-items: baseline;
            gap: 10px;
        }

        .logo {
            font-size: 26px;
            font-weight: 700;
            text-transform: lowercase;
            color: var(--brand-dark);
            text-decoration: none;
        }

        .creator-byline {
            font-size: 13px;
            color: #888888;
            font-weight: 400;
            font-style: italic;
            letter-spacing: 0.2px;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 25px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--brand-dark);
            font-size: 14px;
            text-transform: lowercase;
            font-weight: 500;
            transition: opacity 0.2s;
        }

        .nav-links a:hover {
            opacity: 0.6;
        }

        .cart-status {
            font-size: 14px;
            font-weight: 500;
            background: var(--brand-gray);
            padding: 6px 14px;
            border-radius: 20px;
        }

        /* Hero / About Brand Section */
        .hero {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .hero-text {
            padding-right: 20px;
        }

        .hero-text h1 {
            font-size: 42px;
            font-weight: 600;
            margin-bottom: 15px;
            text-transform: lowercase;
        }

        .hero-text p {
            color: var(--text-muted);
            margin-bottom: 20px;
            font-size: 16px;
        }

        .hero-img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }

        /* Sidebar Advertisement Grid */
        .layout-grid {
            display: grid;
            grid-template-columns: 3fr 1fr;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            gap: 30px;
        }

        /* Products Display CSS Grid */
        .section-title {
            font-size: 22px;
            margin-bottom: 20px;
            text-transform: lowercase;
            font-weight: 600;
            border-bottom: 1px solid var(--brand-gray);
            padding-bottom: 10px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: #ffffff;
            border: 1px solid var(--brand-gray);
            border-radius: 6px;
            padding: 15px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .product-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .product-image {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-radius: 4px;
            margin-bottom: 15px;
            background-color: var(--brand-gray);
        }

        .product-info h3 {
            font-size: 16px;
            font-weight: 600;
            text-transform: lowercase;
            margin-bottom: 5px;
        }

        .product-info .tag {
            display: inline-block;
            font-size: 10px;
            background: var(--brand-gray);
            padding: 2px 6px;
            border-radius: 3px;
            text-transform: uppercase;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .product-info p {
            font-size: 13px;
            color: var(--text-muted);
            margin-bottom: 15px;
            min-height: 40px;
        }

        .product-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
        }

        .price {
            font-weight: 600;
            font-size: 15px;
        }

        /* Action Buttons */
        .add-to-cart-btn {
            background-color: var(--brand-dark);
            color: white;
            border: none;
            padding: 8px 14px;
            font-size: 12px;
            font-weight: 600;
            border-radius: 4px;
            cursor: pointer;
            text-transform: uppercase;
            transition: background 0.2s;
        }

        .add-to-cart-btn:hover {
            background-color: #555555;
        }

        /* Sidebar Display Ads styling */
        .sidebar-ads {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .display-ad-box {
            background: linear-gradient(135deg, #e2dfd9, #efebd8);
            border: 1px solid #d3cfc4;
            padding: 20px;
            border-radius: 6px;
            text-align: center;
        }

        .display-ad-box h4 {
            font-size: 14px;
            text-transform: uppercase;
            margin-bottom: 10px;
            color: #555;
        }

        .display-ad-box p {
            font-size: 13px;
            margin-bottom: 15px;
        }

        .ad-image {
            width: 100%;
            height: 120px;
            object-fit: cover;
            border-radius: 4px;
            margin-bottom: 12px;
        }

        .ad-link-btn {
            display: inline-block;
            background: transparent;
            color: var(--brand-dark);
            border: 1px solid var(--brand-dark);
            padding: 6px 12px;
            font-size: 11px;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
            border-radius: 4px;
            cursor: pointer;
        }

        .ad-link-btn:hover {
            background: var(--brand-dark);
            color: white;
        }

        /* Footer styling */
        footer {
            background-color: #ffffff;
            border-top: 1px solid var(--brand-gray);
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            font-size: 13px;
            color: var(--text-muted);
        }

        /* Mobile responsive adjustments */
        @media (max-width: 768px) {
            .hero { grid-template-columns: 1fr; }
            .layout-grid { grid-template-columns: 1fr; }
            .logo-area { flex-direction: column; gap: 2px; }
        }
    </style>
</head>
<body>

    <!-- Advertisement Top Sticky Banner -->
    <div class="promo-ad-banner" id="topPromoBanner">
        ✨ <strong>Summer Collection Drop:</strong> Secure the new Highlight Milk & Pocket Bronze before they sell out! 
        <a href="#summer-drop">Shop Summer Lineup</a>
        <button class="close-ad-btn" onclick="closeAdBanner()">✕</button>
    </div>

    <!-- Navigation Header Layer -->
    <header>
        <div class="nav-container">
            <div class="logo-area">
                <a href="#" class="logo">rhode</a>
                <span class="creator-byline">by Jermaine Claire M. Rigonan</span>
            </div>
            <ul class="nav-links">
                <li><a href="#skin">shop skin</a></li>
                <li><a href="#summer-drop">summer essentials</a></li>
            </ul>
            <div class="cart-status">bag (<span id="cartCount">0</span>)</div>
        </div>
    </header>

    <!-- Brand Introduction Section -->
    <section class="hero">
        <div class="hero-text">
            <h1>one of everything.</h1>
            <p>Founded by Hailey Rhode Bieber, Rhode is an edited line of exceptional skincare and color essentials. Formulated for ultimate skin barrier health, our products provide immediate hydration, effortless texture, and an organic dewiness meant to mimic a healthy glaze.</p>
            <button class="add-to-cart-btn" style="padding: 12px 24px;" onclick="alert('Navigating to full collection sequence...')">explore routines</button>
        </div>
        <img class="hero-img" src="https://images.unsplash.com/photo-1601049541289-9b1b7bbbfe19?auto=format&fit=crop&q=80&w=800" alt="Dewy skin model aesthetic">
    </section>

    <!-- Main Content Layout Section (Products + Side Ads) -->
    <div class="layout-grid">
        
        <!-- Left Side: Interactive Product Catalog -->
        <main>
            <!-- Core Skincare Essentials Layer -->
            <h2 class="section-title" id="skin">skincare essentials</h2>
            <div class="products-grid" style="margin-bottom: 40px;">
                
                <!-- Product 1 -->
                <div class="product-card">
                    <div>
                        <img class="product-image" src="https://images.unsplash.com/photo-1556228720-195a672e8a03?auto=format&fit=crop&q=80&w=500" alt="Cleanser texture">
                        <div class="product-info">
                            <span class="tag">cleanse</span>
                            <h3>pineapple refresh cleanser</h3>
                            <p>A refreshing, balm-to-milk daily cleanser packed with pineapple enzymes to gently smooth skin texture.</p>
                        </div>
                    </div>
                    <div class="product-meta">
                        <span class="price">$30.00</span>
                        <button class="add-to-cart-btn" onclick="addToBag('pineapple refresh cleanser')">add to bag</button>
                    </div>
                </div>

                <!-- Product 2: Glazing Milk Essence -->
                <div class="product-card">
                    <div>
                        <img class="product-image" src="https://images.unsplash.com/photo-1601612628452-9e99ced43524?auto=format&fit=crop&q=80&w=500" alt="Glazing Milk Creamy Skin Essence">
                        <div class="product-info">
                            <span class="tag">prep</span>
                            <h3>glazing milk essence</h3>
                            <p>A nutrient-dense, creamy ceramide treatment essence that calms skin and boosts skin barrier function.</p>
                        </div>
                    </div>
                    <div class="product-meta">
                        <span class="price">$32.00</span>
                        <button class="add-to-cart-btn" onclick="addToBag('glazing milk essence')">add to bag</button>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="product-card">
                    <div>
                        <img class="product-image" src="https://images.unsplash.com/photo-1617897903246-719242758050?auto=format&fit=crop&q=80&w=500" alt="Serum fluid">
                        <div class="product-info">
                            <span class="tag">glaze</span>
                            <h3>peptide glazing fluid</h3>
                            <p>Hailey's signature gel-serum for a dewy look. Delivers intense hydration while plumping fine lines.</p>
                        </div>
                    </div>
                    <div class="product-meta">
                        <span class="price">$32.00</span>
                        <button class="add-to-cart-btn" onclick="addToBag('peptide glazing fluid')">add to bag</button>
                    </div>
                </div>

            </div>

            <!-- New Cosmetics Collection Layer -->
            <h2 class="section-title" id="summer-drop">summer collection essentials</h2>
            <div class="products-grid">
                
                <!-- Product 4 -->
                <div class="product-card">
                    <div>
                        <img class="product-image" src="https://images.unsplash.com/photo-1598440947619-2c35fc9aa908?auto=format&fit=crop&q=80&w=500" alt="Luminizer glow">
                        <div class="product-info">
                            <span class="tag">new launch</span>
                            <h3>highlight milk luminizer</h3>
                            <p>Part hydrating skin essence, part iridescent fluid. Leaves a head-to-toe pearlescent finish.</p>
                        </div>
                    </div>
                    <div class="product-meta">
                        <span class="price">$28.00</span>
                        <button class="add-to-cart-btn" onclick="addToBag('highlight milk luminizer')">add to bag</button>
                    </div>
                </div>

                <!-- Product 5 -->
                <div class="product-card">
                    <div>
                        <img class="product-image" src="https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?auto=format&fit=crop&q=80&w=500" alt="Cream makeup stick">
                        <div class="product-info">
                            <span class="tag">viral stick</span>
                            <h3>pocket bronze stick</h3>
                            <p>On-the-go cream bronzer built with skin-loving tamanu oil for an effortless, sun-kissed contour sculpt.</p>
                        </div>
                    </div>
                    <div class="product-meta">
                        <span class="price">$25.00</span>
                        <button class="add-to-cart-btn" onclick="addToBag('pocket bronze stick')">add to bag</button>
                    </div>
                </div>

                <!-- Product 6 -->
                <div class="product-card">
                    <div>
                        <img class="product-image" src="https://images.unsplash.com/photo-1512496015851-a90fb38ba796?auto=format&fit=crop&q=80&w=500" alt="Phone accessory case">
                        <div class="product-info">
                            <span class="tag">merch accessories</span>
                            <h3>signature phone lip case</h3>
                            <p>The viral silicone mobile phone case built perfectly to securely slot your favorite peptide lip treatment tint.</p>
                        </div>
                    </div>
                    <div class="product-meta">
                        <span class="price">$38.00</span>
                        <button class="add-to-cart-btn" onclick="addToBag('signature phone lip case')">add to bag</button>
                    </div>
                </div>

            </div>
        </main>

        <!-- Right Side: Sidebar Panel For Internal Advertisements -->
        <aside class="sidebar-ads">
            
            <!-- Side Ad 1 -->
            <div class="display-ad-box">
                <img class="ad-image" src="https://images.unsplash.com/photo-1620916566398-39f1143ab7be?auto=format&fit=crop&q=80&w=400" alt="Skincare set kit">
                <h4>exclusive set offer</h4>
                <p>Get the complete 4-step daily essentials routine bundled neatly for dynamic savings.</p>
                <button class="ad-link-btn" onclick="buyBundle()">shop the rhode kit</button>
            </div>

            <!-- Side Ad 2 -->
            <div class="display-ad-box" style="background: linear-gradient(135deg, #f0f4f8, #d9e2ec);">
                <img class="ad-image" src="https://images.unsplash.com/photo-1515688594390-b649af70d282?auto=format&fit=crop&q=80&w=400" alt="Fun skin patches">
                <h4>spotwear line</h4>
                <p>Discover the playful, limited pimple patch collab series designed to heal blemishes stylishly.</p>
                <button class="ad-link-btn" onclick="alert('Redirecting to Spotwear collection info...')">view collection</button>
            </div>

        </aside>

    </div>

    <!-- Page Footer -->
    <footer>
        <p>&copy; 2026 rhode skin. All formulas are vegan, cruelty-free, and dermatologist tested.</p>
    </footer>

    <!-- Interactive Working Script Interface -->
    <script>
        let currentCartCount = 0;

        function addToBag(productName) {
            currentCartCount += 1;
            document.getElementById('cartCount').innerText = currentCartCount;
            alert('Added ' + productName + ' to your Rhode Bag!');
        }

        function buyBundle() {
            currentCartCount += 4;
            document.getElementById('cartCount').innerText = currentCartCount;
            alert('The complete 4-item Rhode Kit has been loaded to your bag.');
        }

        function closeAdBanner() {
            const banner = document.getElementById('topPromoBanner');
            banner.style.display = 'none';
        }
    </script>

</body>
</html>


