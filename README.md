```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SkyNett Telecom - Internet Rápida e Confiável</title>
    <meta name="description" content="SkyNett Telecom - Provedor de internet fibra óptica de alta velocidade em sua região. Cobertura local com suporte 24/7.">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --secondary-gradient: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            --dark-bg: #0a0a0a;
            --card-bg: rgba(255, 255, 255, 0.05);
            --glass-bg: rgba(255, 255, 255, 0.1);
            --text-primary: #ffffff;
            --text-secondary: #b0b0b0;
            --accent: #00d4ff;
            --gold: #ffd700;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--dark-bg);
            color: var(--text-primary);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(20px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
        }

        .logo {
            font-size: 2rem;
            font-weight: 700;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--text-primary);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
            cursor: pointer;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-menu-toggle {
            display: none;
            font-size: 1.5rem;
            color: var(--text-primary);
            cursor: pointer;
        }

        .cta-button {
            background: var(--primary-gradient);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.6);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: 
                radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(120, 219, 255, 0.3) 0%, transparent 50%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="white" opacity="0.1"/><circle cx="75" cy="75" r="1" fill="white" opacity="0.05"/><circle cx="50" cy="10" r="0.5" fill="white" opacity="0.08"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            animation: grain 20s linear infinite;
        }

        @keyframes grain {
            0%, 100% { transform: translate(0, 0); }
            10% { transform: translate(-5%, -5%); }
            20% { transform: translate(-10%, 5%); }
            30% { transform: translate(5%, -10%); }
            40% { transform: translate(-5%, 15%); }
            50% { transform: translate(-10%, 5%); }
            60% { transform: translate(15%, 0%); }
            70% { transform: translate(0%, 10%); }
            80% { transform: translate(-15%, 0%); }
            90% { transform: translate(10%, 5%); }
        }

        .hero-content {
            max-width: 900px;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 700;
            margin-bottom: 1.5rem;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            color: var(--text-secondary);
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: var(--primary-gradient);
            color: white;
            padding: 18px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-primary);
            padding: 18px 40px;
            border: 2px solid var(--accent);
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }

        .btn-primary:hover, .btn-secondary:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px rgba(102, 126, 234, 0.6);
        }

        .btn-secondary:hover {
            background: var(--accent);
            color: var(--dark-bg);
        }

        /* Main Tabs Container */
        .main-tabs {
            padding: 100px 0;
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 5%;
        }

        /* Tabs Navigation */
        .tabs-nav {
            display: flex;
            justify-content: center;
            margin-bottom: 4rem;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .tab-btn {
            padding: 15px 35px;
            background: var(--card-bg);
            color: var(--text-secondary);
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.4s ease;
            backdrop-filter: blur(20px);
            border: 2px solid transparent;
            position: relative;
            overflow: hidden;
        }

        .tab-btn:hover {
            color: var(--text-primary);
            border-color: var(--accent);
            transform: translateY(-3px);
        }

        .tab-btn.active {
            background: var(--primary-gradient);
            color: white;
            border-color: var(--accent);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.4);
            transform: translateY(-5px);
        }

        /* Tab Content */
        .tab-content {
            display: none;
            animation: fadeInUp 0.8s ease;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Location Tab */
        .location-section {
            background: var(--glass-bg);
            padding: 4rem 0;
            border-radius: 25px;
            backdrop-filter: blur(10px);
        }

        .location-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .location-info h2 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .location-info h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }

        .location-details {
            display: grid;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .location-detail {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1.5rem;
            background: var(--card-bg);
            border-radius: 15px;
            transition: transform 0.3s ease;
        }

        .location-detail:hover {
            transform: translateX(10px);
        }

        .location-detail i {
            font-size: 1.5rem;
            color: var(--accent);
            width: 40px;
        }

        .map-container {
            position: relative;
            height: 450px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.5);
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            border: none;
            filter: grayscale(0.2) contrast(1.1);
            transition: filter 0.3s ease;
        }

        .map-container:hover iframe {
            filter: grayscale(0) contrast(1.2);
        }

        /* Services Tab */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2.5rem;
        }

        .service-card {
            background: var(--card-bg);
            padding: 3rem 2.5rem;
            border-radius: 25px;
            text-align: center;
            transition: all 0.4s ease;
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
            transition: left 0.5s;
        }

        .service-card:hover::before {
            left: 100%;
        }

        .service-card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.6);
        }

        .service-icon {
            width: 100px;
            height: 100px;
            background: var(--primary-gradient);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 2rem;
            font-size: 2.5rem;
            color: white;
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.4);
            transition: all 0.3s ease;
        }

        .service-card:hover .service-icon {
            transform: rotate(360deg) scale(1.1);
        }

        /* Plans Tab */
        .plans-section {
            background: var(--glass-bg);
            padding: 4rem 0;
            border-radius: 25px;
        }

        .plans-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .plan-card {
            background: var(--card-bg);
            padding: 3.5rem 2.5rem;
            border-radius: 25px;
            text-align: center;
            transition: all 0.4s ease;
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
        }

        .plan-card.featured {
            background: linear-gradient(145deg, rgba(102, 126, 234, 0.2), rgba(118, 75, 162, 0.2));
            border: 2px solid var(--accent);
            transform: scale(1.05);
        }

        .plan-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.6);
        }

        .plan-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background: var(--accent);
            color: var(--dark-bg);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
        }

        .plan-price {
            font-size: 4rem;
            font-weight: 700;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin: 1rem 0;
        }

        .plan-speed {
            font-size: 1.6rem;
            color: var(--accent);
            margin-bottom: 2rem;
            font-weight: 600;
        }

        .plan-features {
            list-style: none;
            margin-bottom: 2rem;
        }

        .plan-features li {
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--text-secondary);
        }

        .plan-features li:last-child {
            border-bottom: none;
        }

        /* Contact Tab */
        .contact-section {
            background: var(--card-bg);
            padding: 4rem 0;
            border-radius: 25px;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: start;
        }

        .contact-info h2 {
            font-size: 3rem;
            margin-bottom: 2rem;
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 2rem;
            padding: 1.5rem;
            background: var(--glass-bg);
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            transform: translateX(10px);
            background: var(--glass-bg);
        }

        .contact-item i {
            font-size: 1.8rem;
            color: var(--accent);
            width: 50px;
            text-align: center;
        }

        .contact-form {
            background: var(--glass-bg);
            padding: 3rem;
            border-radius: 25px;
            backdrop-filter: blur(20px);
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1.2rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 12px;
            color: var(--text-primary);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline
