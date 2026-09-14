<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Voltech Industrial Solution | Preview</title>
    <link href="https://googleapis.com" rel="stylesheet">
    <link rel="stylesheet" href="https://cloudflare.com">
    <style>
        :root {
            --navy-blue: #0b2545;
            --dark-slate: #134074;
            --accent-green: #2e7d32;
            --light-accent-green: #4caf50;
            --white: #ffffff;
            --light-gray: #f8fafc;
            --text-color: #334155;
            --border-color: #e2e8f0;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light-gray);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header Navigation */
        header {
            background-color: var(--navy-blue);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-icon {
            font-size: 28px;
            color: var(--light-accent-green);
        }

        .logo-text h1 {
            font-size: 20px;
            color: var(--white);
            letter-spacing: 1px;
        }

        .logo-text span {
            font-size: 11px;
            color: #94a3b8;
            display: block;
        }

        nav {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        nav a {
            color: #cbd5e1;
            text-decoration: none;
            font-weight: 600;
            font-size: 14px;
            transition: color 0.2s;
        }

        nav a:hover {
            color: var(--white);
        }

        .nav-quote-btn {
            background-color: var(--accent-green);
            color: var(--white);
            padding: 8px 16px;
            border-radius: 4px;
            transition: background-color 0.2s;
        }

        /* Hero Banner */
        .hero-banner {
            position: relative;
            background: linear-gradient(to bottom, rgba(11,37,69,0.95), rgba(19,64,116,0.9)), url('https://unsplash.com') no-repeat center center/cover;
            padding: 80px 0;
            text-align: center;
            color: var(--white);
        }

        .hero-content h2 {
            font-size: 32px;
            margin-bottom: 20px;
        }

        .hero-content p {
            font-size: 16px;
            color: #e2e8f0;
            max-width: 700px;
            margin: 0 auto 30px auto;
        }

        .hero-badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .hero-badges span {
            background-color: rgba(255,255,255,0.1);
            padding: 6px 14px;
            border-radius: 30px;
            font-size: 13px;
        }

        /* Product Panels */
        .product-section {
            padding: 50px 0 20px 0;
        }

        .section-title {
            font-size: 24px;
            color: var(--navy-blue);
            text-transform: uppercase;
            text-align: center;
            margin-bottom: 30px;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background-color: var(--accent-green);
            margin: 8px auto 0 auto;
        }

        .product-grid {
            display: flex;
            align-items: center;
            gap: 30px;
            background-color: var(--white);
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.03);
            border: 1px solid var(--border-color);
            margin-bottom: 30px;
        }

        .product-grid.inverse {
            flex-direction: row-reverse;
        }

        .product-info-card {
            flex: 1.2;
        }

        .product-tag {
            background-color: #e2e8f0;
            color: var(--navy-blue);
            font-size: 11px;
            font-weight: 700;
            padding: 4px 8px;
            border-radius: 4px;
        }

        .product-info-card h4 {
            font-size: 20px;
            color: var(--navy-blue);
            margin: 12px 0;
        }

        .spec-list {
            list-style: none;
            margin: 15px 0 25px 0;
        }

        .spec-list li {
            margin-bottom: 10px;
            font-size: 14px;
        }

        .spec-list i {
            color: var(--accent-green);
            margin-right: 8px;
        }

        .product-image-card {
            flex: 0.8;
            text-align: center;
        }

        .product-image-card img {
            width: 100%;
            max-height: 260px;
            object-fit: cover;
            border-radius: 6px;
            border: 1px solid var(--border-color);
        }

        /* Buttons Setup */
        .action-row {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 10px 20px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            font-size: 13px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-whatsapp {
            background-color: #25D366;
            color: var(--white);
        }

        .btn-secondary {
            background-color: var(--navy-blue);
            color: var(--white);
        }

        /* 6-Core Matrix */
        .matrix-bg {
            background-color: #f1f5f9;
            padding: 50px 0;
        }

        .matrix-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .matrix-card {
            background-color: var(--white);
            border-radius: 6px;
            padding: 20px;
            border-top: 4px solid var(--navy-blue);
        }

        .card-num-header {
            font-weight: 700;
            font-size: 15px;
            color: var(--navy-blue);
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 12px;
        }

        .card-num-header span {
            background-color: var(--accent-green);
            color: var(--white);
            font-size: 12px;
            width: 26px;
            height: 26px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }

        .matrix-card ul {
            list-style: none;
            margin-bottom: 15px;
        }

        .matrix-card li {
            font-size: 13px;
            padding: 5px 0;
            border-bottom: 1px dotted #e2e8f0;
        }

        .card-brands {
            font-size: 11px;
            color: #64748b;
            background-color: var(--light-gray);
            padding: 6px;
            border-left: 3px solid var(--accent-green);
        }

        /* Contact Section */
        .contact-section {
            background-color: var(--navy-blue);
            color: var(--white);
            padding: 50px 0;
        }

        .contact-flex {
            display: flex;
            gap: 40px;
            flex-wrap: wrap;
        }

        .contact-info {
            flex: 1;
            min-width: 280px;
        }

        .contact-info h3 {
            font-size: 22px;
            margin-bottom: 12px;
        }

        .contact-detail-row {
            display: flex;
            gap: 12px;
            margin-bottom: 20px;
        }

        .contact-detail-row i {
            color: var(--light-accent-green);
            font-size: 18px;
            margin-top: 3px;
        }

        .form-container {
            flex: 1;
            min-width: 300px;
            background-color: var(--white);
            padding: 25px;
            border-radius: 6px;
            color: var(--text-color);
        }

        .form-group {
            margin-bottom: 12px;
        }

        .form-group label {
            display: block;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid var(--border-color);
            border-radius: 4px;
            font-size: 13px;
        }

        .submit-btn {
            width: 100%;
            background-color: var(--accent-green);
            color: var(--white);
            border: none;
            padding: 10px;
            font-weight: 600;
            cursor: pointer;
            border-radius: 4px;
        }

        footer {
            background-color: #061529;
            color: #64748b;
            text-align: center;
            padding: 15px;
            font-size: 12px;
        }
    </style>
</head>
<body>

    <!-- Navigation Header -->
    <header>
        <div class="nav-container container">
            <div class="logo-area">
