<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VONDO - Premium Online Shopping</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #4a6572;
            --accent: #ff6b6b;
            --light: #f8f9fa;
            --dark: #343a40;
            --success: #28a745;
            --warning: #ffc107;
            --gray: #6c757d;
            --light-gray: #e9ecef;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            color: white;
        }

        .logo-img {
            width: 45px;
            height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 20px;
            color: white;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            border-radius: 10px;
        }

        .logo-text {
            font-size: 26px;
            font-weight: 700;
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .header-action-item {
            display: flex;
            align-items: center;
            gap: 8px;
            color: white;
            text-decoration: none;
            font-size: 14px;
        }

        .header-bottom {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 10px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            font-size: 15px;
            position: relative;
        }

        nav ul li a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: white;
            transition: var(--transition);
        }

        nav ul li a:hover:after {
            width: 100%;
        }

        .search-bar {
            display: flex;
            align-items: center;
            background: white;
            border-radius: 30px;
            padding: 8px 18px;
            width: 350px;
        }

        .search-bar input {
            border: none;
            outline: none;
            padding: 6px;
            width: 100%;
            background: transparent;
            font-size: 14px;
        }

        .search-bar button {
            background: none;
            border: none;
            cursor: pointer;
            color: var(--primary);
        }

        .cart-icon {
            position: relative;
            font-size: 22px;
        }

        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: var(--accent);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 12px;
            font-weight: bold;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1607082350899-7e105aa886ae?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 80px 20px;
            margin-bottom: 40px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 42px;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 14px 32px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 16px;
        }

        .btn:hover {
            background: #ff4757;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }

        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }

        /* Categories Section */
        .categories {
            padding: 50px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            font-size: 32px;
            color: var(--dark);
            position: relative;
            font-weight: 600;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--accent);
            margin: 15px auto;
            border-radius: 2px;
        }

        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .category-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
            padding: 20px 15px;
            cursor: pointer;
        }

        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .category-icon {
            font-size: 30px;
            margin-bottom: 15px;
            color: var(--secondary);
        }

        .category-name {
            font-weight: 500;
            font-size: 16px;
        }

        /* Products Section with Filter */
        .products-section {
            padding: 30px 0 50px;
        }

        .products-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            flex-wrap: wrap;
            gap: 15px;
        }

        .filter-options {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 8px 18px;
            background: white;
            border: 1px solid var(--light-gray);
            border-radius: 30px;
            cursor: pointer;
            transition: var(--transition);
            font-size: 14px;
        }

        .filter-btn.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .view-options {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .view-btn {
            width: 38px;
            height: 38px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: white;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            cursor: pointer;
            transition: var(--transition);
        }

        .view-btn.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .product-badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--accent);
            color: white;
            padding: 5px 12px;
            border-radius: 30px;
            font-size: 12px;
            font-weight: 500;
            z-index: 2;
        }

        .product-image {
            height: 220px;
            width: 100%;
            object-fit: cover;
            border-bottom: 1px solid var(--light-gray);
        }

        .product-content {
            padding: 20px;
        }

        .product-title {
            font-size: 16px;
            margin-bottom: 10px;
            font-weight: 500;
            line-height: 1.4;
        }

        .product-price {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 12px;
        }

        .current-price {
            font-size: 18px;
            font-weight: 600;
            color: var(--secondary);
        }

        .original-price {
            font-size: 15px;
            text-decoration: line-through;
            color: var(--gray);
        }

        .discount {
            color: var(--success);
            font-size: 14px;
            font-weight: 500;
        }

        .product-rating {
            display: flex;
            align-items: center;
            gap: 5px;
            margin-bottom: 15px;
        }

        .stars {
            color: var(--warning);
        }

        .rating-count {
            font-size: 13px;
            color: var(--gray);
        }

        .product-actions {
            display: flex;
            gap: 10px;
        }

        .add-to-cart {
            flex: 1;
            padding: 10px;
            background: var(--secondary);
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .add-to-cart:hover {
            background: var(--primary);
        }

        .buy-now {
            flex: 1;
            padding: 10px;
            background: var(--accent);
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .buy-now:hover {
            background: #ff4757;
        }

        .wishlist-btn {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--light);
            border: 1px solid var(--light-gray);
            border-radius: 6px;
            cursor: pointer;
            transition: var(--transition);
        }

        .wishlist-btn:hover {
            color: var(--accent);
            border-color: var(--accent);
        }

        /* Checkout Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 2000;
            overflow-y: auto;
        }

        .modal-content {
            background: white;
            margin: 50px auto;
            border-radius: 12px;
            width: 90%;
            max-width: 600px;
            box-shadow: var(--shadow);
            animation: modalFade 0.3s;
        }

        @keyframes modalFade {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .modal-header {
            padding: 20px;
            border-bottom: 1px solid var(--light-gray);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-title {
            font-size: 22px;
            font-weight: 600;
            color: var(--primary);
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--gray);
        }

        .modal-body {
            padding: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--dark);
        }

        .form-input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--light-gray);
            border-radius: 6px;
            font-size: 15px;
            transition: var(--transition);
        }

        .form-input:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(74, 101, 114, 0.2);
        }

        .form-row {
            display: flex;
            gap: 15px;
        }

        .form-row .form-group {
            flex: 1;
        }

        .payment-methods {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
        }

        .payment-method {
            flex: 1;
            text-align: center;
            padding: 15px;
            border: 2px solid var(--light-gray);
            border-radius: 8px;
            cursor: pointer;
            transition: var(--transition);
        }

        .payment-method.active {
            border-color: var(--secondary);
            background: rgba(74, 101, 114, 0.05);
        }

        .payment-icon {
            font-size: 32px;
            margin-bottom: 10px;
            color: var(--secondary);
        }

        .payment-name {
            font-weight: 500;
        }

        .card-form {
            display: none;
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            margin-top: 15px;
        }

        .card-form.active {
            display: block;
        }

        .modal-footer {
            padding: 20px;
            border-top: 1px solid var(--light-gray);
            display: flex;
            justify-content: flex-end;
            gap: 15px;
        }

        .btn-cancel {
            background: var(--light-gray);
            color: var(--dark);
        }

        .btn-cancel:hover {
            background: #dcdcdc;
        }

        .btn-confirm {
            background: var(--success);
        }

        .btn-confirm:hover {
            background: #218838;
        }

        /* Order Summary */
        .order-summary {
            background: var(--light);
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .summary-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .summary-total {
            display: flex;
            justify-content: space-between;
            font-weight: 600;
            font-size: 18px;
            padding-top: 15px;
            border-top: 1px solid var(--light-gray);
            margin-top: 15px;
        }

        /* Pagination */
        .pagination {
            display: flex;
            justify-content: center;
            margin-top: 50px;
            gap: 8px;
        }

        .pagination-item {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            font-size: 15px;
            cursor: pointer;
            transition: var(--transition);
        }

        .pagination-item.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .pagination-item:hover:not(.active) {
            background: var(--light);
        }

        /* Newsletter Section */
        .newsletter {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 60px 0;
            text-align: center;
        }

        .newsletter-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .newsletter h2 {
            font-size: 28px;
            margin-bottom: 15px;
        }

        .newsletter p {
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .newsletter-form {
            display: flex;
            gap: 10px;
            max-width: 500px;
            margin: 0 auto;
        }

        .newsletter-input {
            flex: 1;
            padding: 14px 20px;
            border: none;
            border-radius: 30px;
            font-size: 15px;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--accent);
        }

        .footer-column p {
            margin-bottom: 15px;
            opacity: 0.8;
            line-height: 1.8;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-links a:hover {
            color: white;
            transform: translateX(5px);
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }

        .social-icons a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        .payment-methods-footer {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .payment-method-footer {
            width: 60px;
            height: 38px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: white;
            border-radius: 6px;
            font-size: 20px;
            color: var(--dark);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.7);
            font-size: 14px;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .search-bar {
                width: 250px;
            }
            
            nav ul {
                gap: 15px;
            }
        }

        @media (max-width: 768px) {
            .header-top, .header-bottom {
                flex-direction: column;
                gap: 15px;
            }
            
            .search-bar {
                width: 100%;
                max-width: 400px;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .products-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .form-row {
                flex-direction: column;
                gap: 0;
            }
            
            .payment-methods {
                flex-direction: column;
            }
        }

        @media (max-width: 576px) {
            .products-grid {
                grid-template-columns: 1fr;
            }
            
            .categories-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .hero {
                padding: 50px 20px;
            }
            
            .hero h1 {
                font-size: 28px;
            }
            
            .btn {
                padding: 12px 25px;
            }
            
            .modal-content {
                width: 95%;
                margin: 20px auto;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <a href="https://i.ibb.co.com/0yVPc2kX/1756539704581.jpg" class="logo">
                    <div class="logo-img">V</div>
                    <div class="logo-text">VONDO</div>
               </a>
                
                <div class="header-actions">
                    <a href="#" class="header-action-item">
                        <i class="fas fa-user"></i>
                        <span>My Account</span>
                    </a>
                    <a href="#" class="header-action-item">
                        <i class="fas fa-gift"></i>
                        <span>Daily Deals</span>
                    </a>
                    <a href="#" class="header-action-item">
                        <i class="fas fa-headset"></i>
                        <span>Support</span>
                    </a>
                </div>
            </div>
            
            <div class="header-bottom">
                <nav>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Products</a></li>
                        <li><a href="#">Categories</a></li>
                        <li><a href="#">Electronics</a></li>
                        <li><a href="#">Fashion</a></li>
                        <li><a href="#">Home & Garden</a></li>
                        <li><a href="#">Sports</a></li>
                    </ul>
                </nav>
                
                <div class="header-actions">
                    <div class="search-bar">
                        <input type="text" placeholder="Search for products...">
                        <button><i class="fas fa-search"></i></button>
                    </div>
                    <a href="#" class="cart-icon">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="cart-count">1</span>
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>VONDO Sale: Up To 50% Off</h1>
                <p>Discover the latest trends in fashion, electronics, and home goods with our exclusive summer collection. Limited time offer!</p>
                <div class="hero-buttons">
                    <a href="#" class="btn">Shop Now</a>
                    <a href="#" class="btn btn-outline">View Deals</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="categories">
        <div class="container">
            <h2 class="section-title">Shop By Category</h2>
            <div class="categories-grid">
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <div class="category-name">Electronics</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-tshirt"></i>
                    </div>
                    <div class="category-name">Fashion</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <div class="category-name">Home & Garden</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <div class="category-name">Health & Beauty</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-futbol"></i>
                    </div>
                    <div class="category-name">Sports</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-baby"></i>
                    </div>
                    <div class="category-name">Baby & Kids</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-utensils"></i>
                    </div>
                    <div class="category-name">Food & Grocery</div>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-car"></i>
                    </div>
                    <div class="category-name">Automotive</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products-section">
        <div class="container">
            <div class="products-header">
                <h2 class="section-title">Featured Products</h2>
                <div class="filter-options">
                    <button class="filter-btn active">All Products</button>
                    <button class="filter-btn">New Arrivals</button>
                    <button class="filter-btn">Best Sellers</button>
                    <button class="filter-btn">Discounted</button>
                </div>
                <div class="view-options">
                    <span>View:</span>
                    <button class="view-btn active"><i class="fas fa-th"></i></button>
                    <button class="view-btn"><i class="fas fa-list"></i></button>
                </div>
            </div>
            
            <div class="products-grid">
                <!-- Product 1 -->
                <div class="product-card">
                    <span class="product-badge">Sale</span>
                    <img src="https://i.ibb.co.com/KxkMrhkJ/IMG-20250720-WA0067.jpg" alt="Sneakers" class="product-image">
                    <div class="product-content">
                        <h3 class="product-title">Bangladesh Flag</h3>
                        <div class="product-price">
                            <span class="current-price">$89.99</span>
                            <span class="original-price">$129.99</span>
                            <span class="discount">30% off</span>
                        </div>
                        <div class="product-rating">
                            <div class="stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                            <span class="rating-count">(128)</span>
                        </div>
                        <div class="product-actions">
                            <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> Add to Cart</button>
                            <button class="buy-now" data-product="Premium Running Sneakers" data-price="89.99"><i class="fas fa-bolt"></i> Buy Now</button>
                        </div>
                    </div>
                </div>

                <!-- Product 2 -->
                <div class="product-card">
                    <span class="product-badge">New</span>
                    <img src="https://i.ibb.co.com/BKBKMmmy/20240917-121925.jpg" alt="Watch" class="product-image">
                    <div class="product-content">
                        <h3 class="product-title">Luxury T-Shirt</h3>
                        <div class="product-price">
                            <span class="current-price">$160.99</span>
                            <span class="original-price">$229.99</span>
                            <span class="discount">30% off</span>
                        </div>
                        <div class="product-rating">
                            <div class="stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="far fa-star"></i>
                            </div>
                            <span class="rating-count">(64)</span>
                        </div>
                        <div class="product-actions">
                            <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> Add to Cart</button>
                            <button class="buy-now" data-product="Luxury Chronograph Watch" data-price="160.99"><i class="fas fa-bolt"></i> Buy Now</button>
                        </div>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="product-card">
                    <img src="https://i.ibb.co.com/chDr90hW/PXL-20250630-162949271-PORTRAIT.jpg" alt="Headphones" class="product-image">
                    <div class="product-content">
                        <h3 class="product-title">NSTU Logo T-Shirt</h3>
                        <div class="product-price">
                            <span class="current-price">$129.99</span>
                        </div>
                        <div class="product-rating">
                            <div class="stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                            <span class="rating-count">(245)</span>
                        </div>
                        <div class="product-actions">
                            <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> Add to Cart</button>
                            <button class="buy-now" data-product="Wireless Bluetooth Headphones" data-price="129.99"><i class="fas fa-bolt"></i> Buy Now</button>
                        </div>
                    </div>
                </div>

                <!-- Product 4 -->
                <div class="product-card">
                    <span class="product-badge">Sale</span>
                    <img src="https://images.unsplash.com/photo-1491553895911-0055eca6402d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1480&q=80" alt="Sports Shoes" class="product-image">
                    <div class="product-content">
                        <h3 class="product-title">Athletic Running Shoes</h3>
                        <div class="product-price">
                            <span class="current-price">$79.99</span>
                            <span class="original-price">$99.99</span>
                            <span class="discount">20% off</span>
                        </div>
                        <div class="product-rating">
                            <div class="stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                                <i class="far fa-star"></i>
                            </div>
                            <span class="rating-count">(89)</span>
                        </div>
                        <div class="product-actions">
                            <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> Add to Cart</button>
                            <button class="buy-now" data-product="Athletic Running Shoes" data-price="79.99"><i class="fas fa-bolt"></i> Buy Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="pagination">
                <div class="pagination-item active">1</div>
                <div class="pagination-item">2</div>
                <div class="pagination-item">3</div>
                <div class="pagination-item">4</div>
                <div class="pagination-item">5</div>
                <div class="pagination-item"><i class="fas fa-chevron-right"></i></div>
            </div>
        </div>
    </section>

    <!-- Checkout Modal -->
    <div class="modal" id="checkoutModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2 class="modal-title">Complete Your Purchase</h2>
                <button class="close-modal">&times;</button>
            </div>
            <div class="modal-body">
                <div class="order-summary">
                    <h3>Order Summary</h3>
                    <div class="summary-item">
                        <span id="summary-product">Product: Premium Running Sneakers</span>
                        <span id="summary-price">$89.99</span>
                    </div>
                    <div class="summary-item">
                        <span>Shipping</span>
                        <span>$5.99</span>
                    </div>
                    <div class="summary-item">
                        <span>Tax</span>
                        <span>$7.20</span>
                    </div>
                    <div class="summary-total">
                        <span>Total</span>
                        <span id="summary-total">$103.18</span>
                    </div>
                </div>

                <h3>Customer Information</h3>
                <div class="form-group">
                    <label class="form-label" for="customer-name">Full Name</label>
                    <input type="text" class="form-input" id="customer-name" placeholder="Enter your full name">
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label class="form-label" for="customer-email">Email Address</label>
                        <input type="email" class="form-input" id="customer-email" placeholder="Enter your email">
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="customer-phone">Phone Number</label>
                        <input type="tel" class="form-input" id="customer-phone" placeholder="Enter your phone number">
                    </div>
                </div>

                <div class="form-group">
                    <label class="form-label" for="delivery-address">Delivery Address</label>
                    <textarea class="form-input" id="delivery-address" rows="3" placeholder="Enter your complete delivery address"></textarea>
                </div>

                <h3>Payment Method</h3>
                <div class="payment-methods">
                    <div class="payment-method" data-method="card">
                        <div class="payment-icon"><i class="far fa-credit-card"></i></div>
                        <div class="payment-name">Credit/Debit Card</div>
                    </div>
                    <div class="payment-method" data-method="paypal">
                        <div class="payment-icon"><i class="fab fa-paypal"></i></div>
                        <div class="payment-name">PayPal</div>
                    </div>
                    <div class="payment-method" data-method="cod">
                        <div class="payment-icon"><i class="fas fa-money-bill-wave"></i></div>
                        <div class="payment-name">Cash on Delivery</div>
                    </div>
                </div>

                <div class="card-form" id="cardForm">
                    <h4>Card Details</h4>
                    <div class="form-group">
                        <label class="form-label" for="card-number">Card Number</label>
                        <input type="text" class="form-input" id="card-number" placeholder="Enter card number">
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label" for="card-expiry">Expiry Date</label>
                            <input type="text" class="form-input" id="card-expiry" placeholder="MM/YY">
                        </div>
                        <div class="form-group">
                            <label class="form-label" for="card-cvv">CVV</label>
                            <input type="text" class="form-input" id="card-cvv" placeholder="CVV">
                        </div>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="card-name">Name on Card</label>
                        <input type="text" class="form-input" id="card-name" placeholder="Enter name on card">
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <button class="btn btn-cancel">Cancel</button>
                <button class="btn btn-confirm">Confirm Order</button>
            </div>
        </div>
    </div>

    <!-- Newsletter Section -->
    <section class="newsletter">
        <div class="container">
            <div class="newsletter-content">
                <h2>Subscribe to Our Newsletter</h2>
                <p>Get the latest updates on new products, special offers, and exclusive discounts.</p>
                <form class="newsletter-form">
                    <input type="email" class="newsletter-input" placeholder="Enter your email address">
                    <button type="submit" class="btn">Subscribe</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>About VONDO</h3>
                    <p>VONDO is a leading e-commerce platform offering a wide range of products at competitive prices. We are committed to providing the best shopping experience for our customers.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-pinterest"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Home</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Products</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Featured</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> New Arrivals</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Sale</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Customer Service</h3>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Contact Us</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> FAQs</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Returns & Refunds</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Shipping Policy</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Privacy Policy</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <p><i class="fas fa-map-marker-alt"></i> 123 Fashion Avenue, Downtown District, New York, NY 10001</p>
                    <p><i class="fas fa-phone"></i> +1 (555) 123-4567</p>
                    <p><i class="fas fa-envelope"></i> info@vondo.com</p>
                    <div class="payment-methods-footer">
                        <div class="payment-method-footer"><i class="fab fa-cc-visa"></i></div>
                        <div class="payment-method-footer"><i class="fab fa-cc-mastercard"></i></div>
                        <div class="payment-method-footer"><i class="fab fa-cc-amex"></i></div>
                        <div class="payment-method-footer"><i class="fab fa-cc-paypal"></i></div>
                        <div class="payment-method-footer"><i class="fab fa-cc-apple-pay"></i></div>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 VONDO. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Interactive Elements
        document.addEventListener('DOMContentLoaded', function() {
            // Filter buttons
            const filterButtons = document.querySelectorAll('.filter-btn');
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // View options
            const viewButtons = document.querySelectorAll('.view-btn');
            viewButtons.forEach(button => {
                button.addEventListener('click', function() {
                    viewButtons.forEach(btn => btn.classList.remove('active'));
                    this.classList.add('active');
                    
                    const productsGrid = document.querySelector('.products-grid');
                    if (this.querySelector('i').classList.contains('fa-list')) {
                        productsGrid.style.gridTemplateColumns = '1fr';
                    } else {
                        productsGrid.style.gridTemplateColumns = 'repeat(auto-fill, minmax(250px, 1fr))';
                    }
                });
            });
            
            // Add to cart functionality
            const addToCartButtons = document.querySelectorAll('.add-to-cart');
            const cartCount = document.querySelector('.cart-count');
            let count = parseInt(cartCount.textContent);
            
            addToCartButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const product = this.closest('.product-card');
                    const title = product.querySelector('.product-title').textContent;
                    
                    count++;
                    cartCount.textContent = count;
                    
                    // Show confirmation
                    showNotification(`Added ${title} to your cart!`, 'success');
                });
            });
            
            // Buy Now functionality
            const buyNowButtons = document.querySelectorAll('.buy-now');
            const checkoutModal = document.getElementById('checkoutModal');
            const closeModalBtn = document.querySelector('.close-modal');
            const cancelBtn = document.querySelector('.btn-cancel');
            const confirmBtn = document.querySelector('.btn-confirm');
            const paymentMethods = document.querySelectorAll('.payment-method');
            const cardForm = document.getElementById('cardForm');
            
            buyNowButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const productName = this.getAttribute('data-product');
                    const productPrice = this.getAttribute('data-price');
                    
                    // Update order summary
                    document.getElementById('summary-product').textContent = `Product: ${productName}`;
                    document.getElementById('summary-price').textContent = `$${productPrice}`;
                    
                    // Calculate total
                    const price = parseFloat(productPrice);
                    const shipping = 5.99;
                    const tax = price * 0.08; // 8% tax
                    const total = price + shipping + tax;
                    
                    document.getElementById('summary-total').textContent = `$${total.toFixed(2)}`;
                    
                    // Show modal
                    checkoutModal.style.display = 'block';
                    document.body.style.overflow = 'hidden';
                });
            });
            
            // Close modal
            function closeModal() {
                checkoutModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
            
            closeModalBtn.addEventListener('click', closeModal);
            cancelBtn.addEventListener('click', closeModal);
            
            // Click outside modal to close
            window.addEventListener('click', function(event) {
                if (event.target === checkoutModal) {
                    closeModal();
                }
            });
            
            // Payment method selection
            paymentMethods.forEach(method => {
                method.addEventListener('click', function() {
                    paymentMethods.forEach(m => m.classList.remove('active'));
                    this.classList.add('active');
                    
                    const paymentType = this.getAttribute('data-method');
                    
                    if (paymentType === 'card') {
                        cardForm.classList.add('active');
                    } else {
                        cardForm.classList.remove('active');
                    }
                });
            });
            
            // Confirm order
            confirmBtn.addEventListener('click', function() {
                // Basic validation
                const name = document.getElementById('customer-name').value;
                const email = document.getElementById('customer-email').value;
                const address = document.getElementById('delivery-address').value;
                
                if (!name || !email || !address) {
                    showNotification('Please fill in all required fields', 'error');
                    return;
                }
                
                const selectedPayment = document.querySelector('.payment-method.active');
                if (!selectedPayment) {
                    showNotification('Please select a payment method', 'error');
                    return;
                }
                
                const paymentType = selectedPayment.getAttribute('data-method');
                
                if (paymentType === 'card') {
                    const cardNumber = document.getElementById('card-number').value;
                    const cardExpiry = document.getElementById('card-expiry').value;
                    const cardCVV = document.getElementById('card-cvv').value;
                    
                    if (!cardNumber || !cardExpiry || !cardCVV) {
                        showNotification('Please fill in all card details', 'error');
                        return;
                    }
                }
                
                // If all validation passes
                closeModal();
                showNotification('Your order has been placed successfully!', 'success');
                
                // Reset form
                document.getElementById('customer-name').value = '';
                document.getElementById('customer-email').value = '';
                document.getElementById('customer-phone').value = '';
                document.getElementById('delivery-address').value = '';
                document.getElementById('card-number').value = '';
                document.getElementById('card-expiry').value = '';
                document.getElementById('card-cvv').value = '';
                document.getElementById('card-name').value = '';
                
                paymentMethods.forEach(m => m.classList.remove('active'));
                cardForm.classList.remove('active');
            });
            
            // Pagination
            const paginationItems = document.querySelectorAll('.pagination-item');
            paginationItems.forEach(item => {
                item.addEventListener('click', function() {
                    paginationItems.forEach(i => i.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Notification function
            function showNotification(message, type) {
                const notification = document.createElement('div');
                notification.style.position = 'fixed';
                notification.style.bottom = '20px';
                notification.style.right = '20px';
                notification.style.backgroundColor = type === 'success' ? 'var(--success)' : 'var(--accent)';
                notification.style.color = 'white';
                notification.style.padding = '12px 20px';
                notification.style.borderRadius = '6px';
                notification.style.boxShadow = 'var(--shadow)';
                notification.style.zIndex = '1000';
                notification.textContent = message;
                
                document.body.appendChild(notification);
                
                setTimeout(() => {
                    notification.style.opacity = '0';
                    notification.style.transition = 'opacity 0.5s ease';
                    setTimeout(() => {
                        document.body.removeChild(notification);
                    }, 500);
                }, 3000);
            }
        });
    </script>
</body>
</html>
