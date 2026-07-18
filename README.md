# Pet-shop-Dogs-House-Jo-o-Durval
site do Pet shop Dogs House João Durval
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Dogs House João Durval - Pet Shop completo em Feira de Santana, BA. Banho e tosa, produtos para pets e muito carinho para o seu melhor amigo!">
    <meta name="keywords" content="pet shop, dogs house, banho e tosa, feira de santana, bahia, cachorro, gato, ração">
    <meta name="theme-color" content="#FF6B35">
    <title>Dogs House João Durval | Pet Shop em Feira de Santana - BA</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🐾</text></svg>">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Playfair+Display:wght@700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        :root {
            --primary: #FF6B35;
            --primary-light: #FF8C5A;
            --primary-dark: #E55A2B;
            --secondary: #1a1a2e;
            --accent: #F39C12;
            --light: #fafafa;
            --gray-100: #f8f9fa;
            --gray-200: #e9ecef;
            --gray-300: #dee2e6;
            --gray-400: #ced4da;
            --gray-500: #adb5bd;
            --gray-600: #6c757d;
            --gray-700: #495057;
            --gray-800: #343a40;
            --white: #FFFFFF;
            --success: #28a745;
            --gradient-primary: linear-gradient(135deg, #FF6B35 0%, #FF8C5A 50%, #F39C12 100%);
            --gradient-dark: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            --shadow-sm: 0 2px 8px rgba(0,0,0,0.08);
            --shadow-md: 0 8px 30px rgba(0,0,0,0.12);
            --shadow-lg: 0 20px 60px rgba(0,0,0,0.15);
            --shadow-xl: 0 30px 80px rgba(0,0,0,0.2);
            --radius-sm: 8px;
            --radius-md: 12px;
            --radius-lg: 20px;
            --radius-xl: 30px;
            --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 80px;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            color: var(--gray-800);
            background: var(--light);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* SCROLL PROGRESS */
        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            width: 0;
            height: 3px;
            background: var(--gradient-primary);
            z-index: 9999;
            transition: width 0.1s;
        }

        /* LOADER */
        .loader {
            position: fixed;
            inset: 0;
            background: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            transition: opacity 0.5s, visibility 0.5s;
        }

        .loader.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .loader-content {
            text-align: center;
        }

        .loader-paw {
            font-size: 4rem;
            animation: loaderPulse 1s ease-in-out infinite;
        }

        @keyframes loaderPulse {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.2); opacity: 0.7; }
        }

        .loader-text {
            font-weight: 600;
            color: var(--secondary);
            margin-top: 1rem;
            font-size: 0.9rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        /* HEADER */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: var(--transition);
            border-bottom: 1px solid transparent;
        }

        header.scrolled {
            background: rgba(255, 255, 255, 0.98);
            box-shadow: var(--shadow-md);
            border-bottom: 1px solid var(--gray-200);
        }

        .header-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }

        .logo-icon {
            width: 48px;
            height: 48px;
            background: var(--gradient-primary);
            border-radius: var(--radius-md);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            color: var(--white);
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
            transition: var(--transition);
        }

        .logo:hover .logo-icon {
            transform: rotate(-10deg) scale(1.05);
        }

        .logo-text h1 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--secondary);
            line-height: 1.2;
        }

        .logo-text span {
            display: block;
            font-family: 'Inter', sans-serif;
            font-size: 0.7rem;
            font-weight: 500;
            color: var(--primary);
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        nav {
            display: flex;
            align-items: center;
            gap: 2rem;
        }

        nav a {
            color: var(--gray-700);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: var(--transition);
            position: relative;
            padding: 0.5rem 0;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gradient-primary);
            transition: width 0.3s ease;
            border-radius: 2px;
        }

        nav a:hover {
            color: var(--primary);
        }

        nav a:hover::after {
            width: 100%;
        }

        .nav-cta {
            background: var(--gradient-primary);
            color: var(--white) !important;
            padding: 0.7rem 1.5rem !important;
            border-radius: var(--radius-xl);
            font-weight: 600 !important;
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
        }

        .nav-cta::after {
            display: none !important;
        }

        .nav-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            color: var(--secondary);
            cursor: pointer;
            padding: 0.5rem;
        }

        /* HERO */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: var(--secondary);
        }

        .hero-bg {
            position: absolute;
            inset: 0;
            background: url('https://images.unsplash.com/photo-1601758228041-f3b2795255f1?w=1920') center/cover;
            opacity: 0.3;
        }

        .hero-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, rgba(26,26,46,0.95) 0%, rgba(22,33,62,0.9) 100%);
        }

        .hero-pattern {
            position: absolute;
            inset: 0;
            background-image: radial-gradient(circle at 20% 80%, rgba(255,107,53,0.1) 0%, transparent 50%),
                              radial-gradient(circle at 80% 20%, rgba(243,156,18,0.1) 0%, transparent 50%);
        }

        .hero-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 8rem 2rem 4rem;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-text {
            animation: fadeInUp 1s ease;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 0.6rem 1.2rem;
            border-radius: var(--radius-xl);
            color: var(--white);
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 1.5rem;
            border: 1px solid rgba(255,255,255,0.15);
        }

        .hero-badge i {
            color: var(--accent);
        }

        .hero h2 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 800;
            color: var(--white);
            margin-bottom: 1.5rem;
            line-height: 1.1;
        }

        .hero h2 span {
            background: var(--gradient-primary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-description {
            font-size: 1.1rem;
            color: rgba(255,255,255,0.8);
            margin-bottom: 2.5rem;
            line-height: 1.8;
            max-width: 500px;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 1rem 2rem;
            border-radius: var(--radius-xl);
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: var(--transition);
            cursor: pointer;
            border: none;
        }

        .btn-primary {
            background: var(--gradient-primary);
            color: var(--white);
            box-shadow: 0 8px 30px rgba(255, 107, 53, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 40px rgba(255, 107, 53, 0.5);
        }

        .btn-secondary {
            background: rgba(255,255,255,0.1);
            color: var(--white);
            border: 2px solid rgba(255,255,255,0.3);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255,255,255,0.2);
            border-color: rgba(255,255,255,0.5);
        }

        .hero-visual {
            position: relative;
            animation: fadeInRight 1s ease 0.3s both;
        }

        .hero-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            border-radius: var(--radius-lg);
            padding: 2rem;
            border: 1px solid rgba(255,255,255,0.15);
        }

        .hero-image-wrapper {
            position: relative;
            border-radius: var(--radius-md);
            overflow: hidden;
            margin-bottom: 1.5rem;
        }

        .hero-image-wrapper img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            display: block;
        }

        .hero-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
        }

        .stat-item {
            text-align: center;
            padding: 1rem;
            background: rgba(255,255,255,0.05);
            border-radius: var(--radius-md);
            border: 1px solid rgba(255,255,255,0.1);
        }

        .stat-icon {
            width: 40px;
            height: 40px;
            background: var(--gradient-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 0.5rem;
            color: var(--white);
            font-size: 1rem;
        }

        .stat-label {
            font-size: 0.75rem;
            color: rgba(255,255,255,0.7);
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 500;
        }

        /* SECTIONS */
        section {
            padding: 6rem 2rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-tag {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(255,107,53,0.1);
            color: var(--primary);
            padding: 0.5rem 1rem;
            border-radius: var(--radius-xl);
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1rem;
        }

        .section-header h2 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 800;
            color: var(--secondary);
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .section-header p {
            color: var(--gray-600);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        /* ABOUT */
        .about {
            background: var(--white);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .about-visual {
            position: relative;
        }

        .about-image-main {
            border-radius: var(--radius-lg);
            overflow: hidden;
            box-shadow: var(--shadow-xl);
        }

        .about-image-main img {
            width: 100%;
            height: 500px;
            object-fit: cover;
            display: block;
        }

        .about-floating-card {
            position: absolute;
            bottom: -30px;
            right: -30px;
            background: var(--white);
            padding: 1.5rem 2rem;
            border-radius: var(--radius-md);
            box-shadow: var(--shadow-lg);
            display: flex;
            align-items: center;
            gap: 1rem;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .about-floating-icon {
            width: 50px;
            height: 50px;
            background: var(--gradient-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.2rem;
        }

        .about-floating-text h4 {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--secondary);
        }

        .about-floating-text span {
            font-size: 0.8rem;
            color: var(--gray-600);
        }

        .about-content h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--secondary);
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .about-content > p {
            color: var(--gray-600);
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .about-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .feature-card {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            padding: 1.2rem;
            background: var(--gray-100);
            border-radius: var(--radius-md);
            transition: var(--transition);
        }

        .feature-card:hover {
            background: var(--white);
            box-shadow: var(--shadow-md);
            transform: translateY(-3px);
        }

        .feature-icon {
            width: 45px;
            height: 45px;
            background: var(--gradient-primary);
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1rem;
            flex-shrink: 0;
        }

        .feature-text h4 {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--secondary);
            margin-bottom: 0.25rem;
        }

        .feature-text p {
            font-size: 0.8rem;
            color: var(--gray-600);
        }

        /* SERVICES */
        .services {
            background: var(--gray-100);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
        }

        .service-card {
            background: var(--white);
            border-radius: var(--radius-lg);
            padding: 2.5rem 2rem;
            text-align: center;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            border: 1px solid var(--gray-200);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--gradient-primary);
            transform: scaleX(0);
            transition: transform 0.4s ease;
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-card:hover {
            transform: translateY(-8px);
            box-shadow: var(--shadow-lg);
            border-color: transparent;
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: rgba(255,107,53,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            font-size: 2rem;
            color: var(--primary);
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            background: var(--gradient-primary);
            color: var(--white);
            transform: scale(1.1);
        }

        .service-card h3 {
            font-size: 1.2rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--secondary);
        }

        .service-card p {
            color: var(--gray-600);
            font-size: 0.9rem;
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        .service-btn {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--primary);
            font-weight: 600;
            font-size: 0.9rem;
            text-decoration: none;
            transition: var(--transition);
        }

        .service-btn:hover {
            gap: 0.8rem;
        }

        /* GALLERY */
        .gallery {
            background: var(--white);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1.5rem;
        }

        .gallery-item {
            border-radius: var(--radius-md);
            overflow: hidden;
            position: relative;
            aspect-ratio: 1;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(26,26,46,0.9) 0%, transparent 60%);
            opacity: 0;
            transition: opacity 0.4s ease;
            display: flex;
            align-items: flex-end;
            padding: 1.5rem;
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        .gallery-overlay span {
            color: var(--white);
            font-weight: 600;
            font-size: 0.9rem;
        }

        .img-placeholder {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--gray-200);
            color: var(--gray-500);
            font-size: 3rem;
        }

        /* REVIEWS */
        .reviews {
            background: var(--gradient-dark);
            position: relative;
            overflow: hidden;
        }

        .reviews::before {
            content: '';
            position: absolute;
            inset: 0;
            background-image: radial-gradient(circle at 10% 90%, rgba(255,107,53,0.15) 0%, transparent 40%),
                              radial-gradient(circle at 90% 10%, rgba(243,156,18,0.1) 0%, transparent 40%);
        }

        .reviews .section-header h2 {
            color: var(--white);
        }

        .reviews .section-header p {
            color: rgba(255,255,255,0.7);
        }

        .reviews .section-tag {
            background: rgba(255,255,255,0.1);
            color: var(--white);
        }

        .rating-highlight {
            text-align: center;
            margin-bottom: 4rem;
            position: relative;
            z-index: 1;
        }

        .rating-box {
            display: inline-flex;
            flex-direction: column;
            align-items: center;
            background: rgba(255,255,255,0.08);
            backdrop-filter: blur(20px);
            padding: 2.5rem 4rem;
            border-radius: var(--radius-lg);
            border: 1px solid rgba(255,255,255,0.15);
        }

        .rating-stars {
            display: flex;
            gap: 0.3rem;
            margin-bottom: 0.5rem;
        }

        .rating-stars i {
            color: var(--accent);
            font-size: 1.5rem;
        }

        .rating-text {
            color: rgba(255,255,255,0.8);
            font-size: 0.9rem;
        }

        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            position: relative;
            z-index: 1;
        }

        .review-card {
            background: rgba(255,255,255,0.06);
            backdrop-filter: blur(15px);
            border-radius: var(--radius-lg);
            padding: 2rem;
            border: 1px solid rgba(255,255,255,0.1);
            transition: var(--transition);
        }

        .review-card:hover {
            background: rgba(255,255,255,0.1);
            transform: translateY(-5px);
        }

        .review-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .review-avatar {
            width: 50px;
            height: 50px;
            background: var(--gradient-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--white);
        }

        .review-info h4 {
            font-size: 1rem;
            font-weight: 600;
            color: var(--white);
            margin-bottom: 0.25rem;
        }

        .review-info .review-stars {
            display: flex;
            gap: 0.15rem;
        }

        .review-info .review-stars i {
            color: var(--accent);
            font-size: 0.75rem;
        }

        .review-text {
            font-size: 0.95rem;
            line-height: 1.7;
            color: rgba(255,255,255,0.85);
            font-style: italic;
        }

        .review-text::before {
            content: '"';
            font-size: 2rem;
            color: var(--primary);
            font-family: 'Playfair Display', serif;
            line-height: 0;
            vertical-align: -0.5rem;
            margin-right: 0.25rem;
        }

        .review-disclaimer {
            text-align: center;
            color: rgba(255,255,255,0.5);
            font-size: 0.8rem;
            margin-top: 3rem;
            font-style: italic;
            position: relative;
            z-index: 1;
        }

        /* CONTACT */
        .contact {
            background: var(--light);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 3rem;
            align-items: start;
        }

        .contact-cards {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .contact-card {
            display: flex;
            align-items: flex-start;
            gap: 1.2rem;
            padding: 1.5rem;
            background: var(--white);
            border-radius: var(--radius-md);
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            border: 1px solid var(--gray-200);
        }

        .contact-card:hover {
            box-shadow: var(--shadow-md);
            border-color: var(--primary);
        }

        .contact-card-icon {
            width: 50px;
            height: 50px;
            background: rgba(255,107,53,0.1);
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .contact-card-content h4 {
            font-size: 0.95rem;
            font-weight: 600;
            color: var(--secondary);
            margin-bottom: 0.25rem;
        }

        .contact-card-content p {
            color: var(--gray-600);
            font-size: 0.9rem;
            line-height: 1.5;
        }

        .contact-card-content a {
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
        }

        .contact-card-content a:hover {
            text-decoration: underline;
        }

        .hours-card {
            background: var(--gradient-primary);
            color: var(--white);
            border: none;
        }

        .hours-card .contact-card-icon {
            background: rgba(255,255,255,0.2);
            color: var(--white);
        }

        .hours-grid {
            display: grid;
            gap: 0.75rem;
            margin-top: 1rem;
        }

        .hours-row {
            display: flex;
            justify-content: space-between;
            padding-bottom: 0.75rem;
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }

        .hours-row:last-child {
            border-bottom: none;
            padding-bottom: 0;
        }

        .hours-row span:first-child {
            font-weight: 500;
        }

        .hours-row span:last-child {
            opacity: 0.9;
        }

        .contact-right {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .map-wrapper {
            border-radius: var(--radius-lg);
            overflow: hidden;
            box-shadow: var(--shadow-md);
            height: 300px;
            border: 1px solid var(--gray-200);
        }

        .map-wrapper iframe {
            width: 100%;
            height: 100%;
            border: 0;
        }

        .contact-form-wrapper {
            background: var(--white);
            padding: 2rem;
            border-radius: var(--radius-lg);
            box-shadow: var(--shadow-sm);
            border: 1px solid var(--gray-200);
        }

        .contact-form-wrapper h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.25rem;
            position: relative;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            font-size: 0.85rem;
            color: var(--gray-700);
            letter-spacing: 0.3px;
        }

        .form-group input,
        .form-group textarea {
            display: block;
            width: 100%;
            padding: 0.9rem 1rem;
            border: 2px solid var(--gray-200);
            border-radius: var(--radius-sm);
            font-family: 'Inter', sans-serif;
            font-size: 0.95rem;
            transition: var(--transition);
            background: var(--gray-100);
            box-sizing: border-box;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
            background: var(--white);
            box-shadow: 0 0 0 4px rgba(255,107,53,0.1);
        }

        .form-group textarea {
            height: 120px;
            resize: vertical;
        }

        .form-submit {
            width: 100%;
            padding: 1rem;
            background: var(--gradient-primary);
            color: var(--white);
            border: none;
            border-radius: var(--radius-sm);
            font-family: 'Inter', sans-serif;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .form-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(255,107,53,0.4);
        }

        /* CTA */
        .cta {
            background: var(--gradient-primary);
            padding: 5rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta::before {
            content: '';
            position: absolute;
            inset: 0;
            background-image: radial-gradient(circle at 20% 50%, rgba(255,255,255,0.1) 0%, transparent 50%),
                              radial-gradient(circle at 80% 50%, rgba(255,255,255,0.1) 0%, transparent 50%);
        }

        .cta-content {
            position: relative;
            z-index: 1;
        }

        .cta h2 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 800;
            color: var(--white);
            margin-bottom: 1rem;
        }

        .cta p {
            color: rgba(255,255,255,0.9);
            font-size: 1.1rem;
            margin-bottom: 2rem;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn-whatsapp {
            background: #25D366;
            color: var(--white);
            font-size: 1.1rem;
            padding: 1.2rem 2.5rem;
        }

        .btn-whatsapp:hover {
            background: #20BD5A;
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(37,211,102,0.4);
        }

        /* FOOTER */
        footer {
            background: var(--secondary);
            color: var(--white);
            padding: 5rem 2rem 2rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 3rem;
            padding-bottom: 3rem;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .footer-brand h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .footer-brand p {
            color: rgba(255,255,255,0.6);
            font-size: 0.9rem;
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        .footer-social {
            display: flex;
            gap: 0.75rem;
        }

        .footer-social a {
            width: 42px;
            height: 42px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-social a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .footer-col h4 {
            font-size: 1rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.75rem;
        }

        .footer-col h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 30px;
            height: 3px;
            background: var(--primary);
            border-radius: 2px;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.75rem;
        }

        .footer-col ul li a {
            color: rgba(255,255,255,0.6);
            text-decoration: none;
            font-size: 0.9rem;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .footer-col ul li a:hover {
            color: var(--primary);
            transform: translateX(5px);
        }

        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            padding-top: 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .footer-bottom p {
            color: rgba(255,255,255,0.5);
            font-size: 0.85rem;
        }

        /* FLOATING WHATSAPP */
        .floating-whatsapp {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 60px;
            height: 60px;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.8rem;
            text-decoration: none;
            box-shadow: 0 8px 30px rgba(37,211,102,0.4);
            z-index: 999;
            transition: var(--transition);
        }

        .floating-whatsapp:hover {
            transform: scale(1.1);
            box-shadow: 0 12px 40px rgba(37,211,102,0.5);
        }

        .floating-whatsapp::before {
            content: '';
            position: absolute;
            inset: -4px;
            border-radius: 50%;
            border: 2px solid rgba(37,211,102,0.3);
            animation: ripple 2s ease-in-out infinite;
        }

        @keyframes ripple {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.2); opacity: 0; }
        }

        /* ANIMATIONS */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInRight {
            from { opacity: 0; transform: translateX(30px); }
            to { opacity: 1; transform: translateX(0); }
        }

        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* RESPONSIVE */
        @media (max-width: 1024px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-description {
                margin-left: auto;
                margin-right: auto;
            }

            .hero-buttons {
                justify-content: center;
            }

            .hero-visual {
                display: none;
            }

            .services-grid,
            .reviews-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .footer-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            nav {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--white);
                padding: 1.5rem;
                flex-direction: column;
                box-shadow: var(--shadow-lg);
                border-radius: 0 0 var(--radius-md) var(--radius-md);
            }

            nav.active {
                display: flex;
            }

            nav a {
                width: 100%;
                text-align: center;
                padding: 0.75rem;
            }

            .nav-cta {
                margin-top: 0.5rem;
            }

            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .about-floating-card {
                right: 1rem;
                bottom: -20px;
            }

            .services-grid,
            .reviews-grid {
                grid-template-columns: 1fr;
            }

            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .footer-grid {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .footer-col h4::after {
                left: 50%;
                transform: translateX(-50%);
            }

            .footer-social {
                justify-content: center;
            }

            .footer-bottom {
                justify-content: center;
                text-align: center;
            }

            .form-row {
                grid-template-columns: 1fr;
                gap: 0;
            }

            .form-group {
                margin-bottom: 1rem;
            }

            .contact-form-wrapper {
                padding: 1.5rem;
            }
        }

        @media (max-width: 480px) {
            section {
                padding: 4rem 1rem;
            }

            .header-content {
                padding: 1rem;
            }

            .hero-content {
                padding: 7rem 1rem 3rem;
            }

            .gallery-grid {
                grid-template-columns: 1fr;
            }

            .about-features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- LOADER -->
    <div class="loader" id="loader">
        <div class="loader-content">
            <div class="loader-paw">🐾</div>
            <div class="loader-text">Dogs House</div>
        </div>
    </div>

    <!-- SCROLL PROGRESS -->
    <div class="scroll-progress" id="scrollProgress"></div>

    <!-- HEADER -->
    <header id="header">
        <div class="header-content">
            <a href="#inicio" class="logo">
                <div class="logo-icon">
                    <i class="fas fa-paw"></i>
                </div>
                <div class="logo-text">
                    <h1>Dogs House</h1>
                    <span>João Durval • Feira de Santana</span>
                </div>
            </a>
            <nav id="nav">
                <a href="#inicio">Início</a>
                <a href="#sobre">Sobre</a>
                <a href="#servicos">Serviços</a>
                <a href="#galeria">Galeria</a>
                <a href="#avaliacoes">Avaliações</a>
                <a href="#contato">Contato</a>
                <a href="https://wa.me/5575992648737" class="nav-cta" target="_blank" rel="noopener">
                    <i class="fab fa-whatsapp"></i> Agendar
                </a>
            </nav>
            <div class="menu-toggle" onclick="toggleMenu()">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- HERO -->
    <section class="hero" id="inicio">
        <div class="hero-bg"></div>
        <div class="hero-overlay"></div>
        <div class="hero-pattern"></div>
        <div class="hero-content">
            <div class="hero-text">
                <div class="hero-badge">
                    <i class="fas fa-map-marker-alt"></i> Feira de Santana - BA
                </div>
                <h2>O melhor lugar para o <span>seu melhor amigo</span></h2>
                <p class="hero-description">Na Dogs House, tratamos cada pet com todo o carinho e dedicação que ele merece. Banho, tosa, produtos de qualidade e muito amor!</p>
                <div class="hero-buttons">
                    <a href="https://wa.me/5575992648737" class="btn btn-primary" target="_blank" rel="noopener">
                        <i class="fab fa-whatsapp"></i> Agendar pelo WhatsApp
                    </a>
                    <a href="#servicos" class="btn btn-secondary">
                        <i class="fas fa-arrow-right"></i> Nossos Serviços
                    </a>
                </div>
            </div>
            <div class="hero-visual">
                <div class="hero-card">
                    <div class="hero-image-wrapper">
                        <img src="https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=600" alt="Cachorro feliz" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-dog\'></i></div>'">
                    </div>
                    <div class="hero-stats">
                        <div class="stat-item">
                            <div class="stat-icon"><i class="fas fa-heart"></i></div>
                            <div class="stat-label">Amor</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-icon"><i class="fas fa-shield-alt"></i></div>
                            <div class="stat-label">Confiança</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-icon"><i class="fas fa-award"></i></div>
                            <div class="stat-label">Qualidade</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT -->
    <section class="about" id="sobre">
        <div class="container">
            <div class="about-grid">
                <div class="about-visual fade-in">
                    <div class="about-image-main">
                        <img src="https://images.unsplash.com/photo-1548199973-03cce0bbc87b?w=600" alt="Pets felizes no Dogs House" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-paw\'></i></div>'">
                    </div>
                    <div class="about-floating-card">
                        <div class="about-floating-icon">
                            <i class="fas fa-heart"></i>
                        </div>
                        <div class="about-floating-text">
                            <h4>100%</h4>
                            <span>Amor por animais</span>
                        </div>
                    </div>
                </div>
                <div class="about-content fade-in">
                    <div class="section-tag">
                        <i class="fas fa-paw"></i> Sobre Nós
                    </div>
                    <h2>Cuidando com amor e dedicação</h2>
                    <p>O Dogs House é um pet shop completo localizado no bairro Capuchinhos, na Av. João Durval Carneiro, em Feira de Santana - BA.</p>
                    <p>Nossa equipe é formada por profissionais apaixonados por animais, que tratam cada pet com todo o carinho e dedicação que eles merecem.</p>
                    <div class="about-features">
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-heart"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Amor & Carinho</h4>
                                <p>Tratamos como família</p>
                            </div>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-shield-alt"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Segurança</h4>
                                <p>Ambiente seguro e limpo</p>
                            </div>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-leaf"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Produtos Naturais</h4>
                                <p>Qualidade garantida</p>
                            </div>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-user-md"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Profissionais</h4>
                                <p>Equipe capacitada</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES -->
    <section class="services" id="servicos">
        <div class="container">
            <div class="section-header fade-in">
                <div class="section-tag">
                    <i class="fas fa-concierge-bell"></i> Serviços
                </div>
                <h2>Nossos Serviços</h2>
                <p>Oferecemos uma variedade de serviços para cuidar do seu pet com toda a qualidade e carinho</p>
            </div>
            <div class="services-grid">
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-bath"></i>
                    </div>
                    <h3>Banho Completo</h3>
                    <p>Banho com produtos hipoalergênicos e de alta qualidade, indicados para cada tipo de pelagem.</p>
                    <a href="https://wa.me/5575992648737?text=Olá! Gostaria de saber os valores do banho" class="service-btn" target="_blank" rel="noopener">
                        Consulte valores <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-cut"></i>
                    </div>
                    <h3>Tosa Profissional</h3>
                    <p>Tosa higiênica, tosa de raça ou tosa criativa. Especialistas em todas as raças.</p>
                    <a href="https://wa.me/5575992648737?text=Olá! Gostaria de saber os valores da tosa" class="service-btn" target="_blank" rel="noopener">
                        Consulte valores <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-bone"></i>
                    </div>
                    <h3>Rações & Acessórios</h3>
                    <p>As melhores marcas de rações, brinquedos, coleiras, camas e acessórios.</p>
                    <a href="https://wa.me/5575992648737?text=Olá! Gostaria de saber sobre rações e acessórios" class="service-btn" target="_blank" rel="noopener">
                        Consulte valores <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-syringe"></i>
                    </div>
                    <h3>Vacinação</h3>
                    <p>Calendário completo de vacinas aplicadas por profissionais habilitados.</p>
                    <a href="https://wa.me/5575992648737?text=Olá! Gostaria de saber sobre vacinação" class="service-btn" target="_blank" rel="noopener">
                        Consulte valores <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-spa"></i>
                    </div>
                    <h3>Estética Animal</h3>
                    <p>Cuidados completos de higiene: corte de unhas, limpeza de ouvidos, dental.</p>
                    <a href="https://wa.me/5575992648737?text=Olá! Gostaria de saber sobre estética animal" class="service-btn" target="_blank" rel="noopener">
                        Consulte valores <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-stethoscope"></i>
                    </div>
                    <h3>Orientação Veterinária</h3>
                    <p>Orientação e encaminhamento para cuidados veterinários especializados.</p>
                    <a href="https://wa.me/5575992648737?text=Olá! Gostaria de orientação veterinária" class="service-btn" target="_blank" rel="noopener">
                        Consulte valores <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- GALLERY -->
    <section class="gallery" id="galeria">
        <div class="container">
            <div class="section-header fade-in">
                <div class="section-tag">
                    <i class="fas fa-camera"></i> Galeria
                </div>
                <h2>Nossa Galeria</h2>
                <p>Conheça um pouco do nosso espaço e dos pets felizes que passam por aqui</p>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1548199973-03cce0bbc87b?w=400" alt="Cachorros felizes brincando" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-dog\'></i></div>'">
                    <div class="gallery-overlay"><span>Diversão garantida!</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1574158622682-e40e69881006?w=400" alt="Gato bem cuidado" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-cat\'></i></div>'">
                    <div class="gallery-overlay"><span>Gatos bem vindos</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1583511655857-d19b40a7a54e?w=400" alt="Cachorro no banho" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-bath\'></i></div>'">
                    <div class="gallery-overlay"><span>Hora do banho!</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1560807707-8cc77767d783?w=400" alt="Cachorro sorrindo" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-heart\'></i></div>'">
                    <div class="gallery-overlay"><span>Resultado perfeito</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1534361960057-19889db9621e?w=400" alt="Cachorro alegre" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-smile\'></i></div>'">
                    <div class="gallery-overlay"><span>Sorriso de pet</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=400" alt="Cachorro descansando" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-bed\'></i></div>'">
                    <div class="gallery-overlay"><span>Conforto total</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1543466835-00a7907e9de1?w=400" alt="Cachorro com tosa" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-cut\'></i></div>'">
                    <div class="gallery-overlay"><span>Tosa profissional</span></div>
                </div>
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1450778869180-e77d3c79b532?w=400" alt="Cachorro brincando" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><i class=\'fas fa-paw\'></i></div>'">
                    <div class="gallery-overlay"><span>Ambiente aconchegante</span></div>
                </div>
            </div>
        </div>
    </section>

    <!-- REVIEWS -->
    <section class="reviews" id="avaliacoes">
        <div class="container">
            <div class="section-header fade-in">
                <div class="section-tag">
                    <i class="fas fa-star"></i> Avaliações
                </div>
                <h2>O Que Dizem Nossos Clientes</h2>
                <p>Avaliações de quem já confiou no Dogs House para cuidar do seu pet</p>
            </div>

            <div class="rating-highlight fade-in">
                <div class="rating-box">
                    <div class="rating-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <span class="rating-text">Clientes satisfeitos</span>
                </div>
            </div>

            <div class="reviews-grid">
                <div class="review-card fade-in">
                    <div class="review-header">
                        <div class="review-avatar">M</div>
                        <div class="review-info">
                            <h4>Maria S.</h4>
                            <div class="review-stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="review-text">Ótimo atendimento! Meu cachorro adora ir ao Dogs House. Os funcionários são muito carinhosos e o local é sempre limpo. Super recomendo!</p>
                </div>

                <div class="review-card fade-in">
                    <div class="review-header">
                        <div class="review-avatar">J</div>
                        <div class="review-info">
                            <h4>João P.</h4>
                            <div class="review-stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="review-text">Melhor pet shop da região! Profissionais competentes e atenciosos. O resultado do banho e tosa é sempre impecável!</p>
                </div>

                <div class="review-card fade-in">
                    <div class="review-header">
                        <div class="review-avatar">A</div>
                        <div class="review-info">
                            <h4>Ana B.</h4>
                            <div class="review-stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="review-text">Levo meu gato aqui e ele sempre volta cheiroso e feliz! O atendimento é humano e dedicado. Obrigada!</p>
                </div>

                <div class="review-card fade-in">
                    <div class="review-header">
                        <div class="review-avatar">R</div>
                        <div class="review-info">
                            <h4>Roberto N.</h4>
                            <div class="review-stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="review-text">Excelente pet shop! Sempre compro rações e acessórios aqui. Produtos de qualidade e atendimento educado!</p>
                </div>

                <div class="review-card fade-in">
                    <div class="review-header">
                        <div class="review-avatar">C</div>
                        <div class="review-info">
                            <h4>Camila R.</h4>
                            <div class="review-stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="review-text">Já fui em vários pet shops e o Dogs House é de longe o melhor! O resultado da tosa é perfeito!</p>
                </div>

                <div class="review-card fade-in">
                    <div class="review-header">
                        <div class="review-avatar">L</div>
                        <div class="review-info">
                            <h4>Lucas F.</h4>
                            <div class="review-stars">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="review-text">Local agradável, equipe preparada e atenciosa. Meu shih tzu ficou maravilhoso após o banho e tosa!</p>
                </div>
            </div>
            
            <p class="review-disclaimer">* Avaliações de clientes satisfeitos com nossos serviços</p>
        </div>
    </section>

    <!-- CONTACT -->
    <section class="contact" id="contato">
        <div class="container">
            <div class="section-header fade-in">
                <div class="section-tag">
                    <i class="fas fa-envelope"></i> Contato
                </div>
                <h2>Entre em Contato</h2>
                <p>Estamos prontos para atender você e o seu pet</p>
            </div>
            <div class="contact-grid">
                <div class="contact-cards fade-in">
                    <div class="contact-card">
                        <div class="contact-card-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-card-content">
                            <h4>Endereço</h4>
                            <p>Av. João Durval Carneiro, 1766<br>Bairro Capuchinhos<br>Feira de Santana - BA<br>CEP: 44076-000</p>
                        </div>
                    </div>
                    <div class="contact-card">
                        <div class="contact-card-icon">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <div class="contact-card-content">
                            <h4>Telefone & WhatsApp</h4>
                            <p><a href="tel:+5575992648737">(75) 9 9264-8737</a></p>
                        </div>
                    </div>
                    <div class="contact-card hours-card">
                        <div class="contact-card-icon">
                            <i class="far fa-clock"></i>
                        </div>
                        <div class="contact-card-content">
                            <h4>Horário de Funcionamento</h4>
                            <div class="hours-grid">
                                <div class="hours-row">
                                    <span>Segunda a Sexta</span>
                                    <span>08h às 18h</span>
                                </div>
                                <div class="hours-row">
                                    <span>Sábado</span>
                                    <span>08h às 15h</span>
                                </div>
                                <div class="hours-row">
                                    <span>Domingo</span>
                                    <span>Fechado</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="contact-right fade-in">
                    <div class="map-wrapper">
                        <iframe 
                            src="https://www.google.com/maps?q=Av.+Jo%C3%A3o+Durval+Carneiro,+1766+-+Capuchinhos,+Feira+de+Santana+-+BA,+44076-000&hl=pt-BR&z=16&output=embed" 
                            allowfullscreen="" 
                            loading="lazy" 
                            referrerpolicy="no-referrer-when-downgrade"
                            title="Localização Dogs House">
                        </iframe>
                    </div>
                    <div class="contact-form-wrapper">
                        <h3>Envie uma mensagem</h3>
                        <form id="contactForm" onsubmit="return handleSubmit(event)">
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="name">Nome</label>
                                    <input type="text" id="name" name="name" placeholder="Seu nome" required>
                                </div>
                                <div class="form-group">
                                    <label for="phone">Telefone</label>
                                    <input type="tel" id="phone" name="phone" placeholder="(00) 00000-0000" required>
                                </div>
                            </div>
                            <div class="form-group">
                                <label for="message">Mensagem</label>
                                <textarea id="message" name="message" placeholder="Como podemos ajudar?" required></textarea>
                            </div>
                            <button type="submit" class="form-submit">
                                <i class="fab fa-whatsapp"></i> Enviar via WhatsApp
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta">
        <div class="cta-content">
            <h2>Seu Pet Merece o Melhor!</h2>
            <p>Agende agora mesmo o banho e tosa do seu melhor amigo pelo WhatsApp!</p>
            <a href="https://wa.me/5575992648737?text=Olá! Gostaria de agendar um banho e tosa para meu pet!" class="btn btn-whatsapp" target="_blank" rel="noopener">
                <i class="fab fa-whatsapp"></i> Agendar pelo WhatsApp
            </a>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-content">
            <div class="footer-grid">
                <div class="footer-brand">
                    <h3><i class="fas fa-paw"></i> Dogs House</h3>
                    <p>Cuidando do seu melhor amigo com todo o amor e dedicação. Seu pet merece o melhor!</p>
                    <div class="footer-social">
                        <a href="https://wa.me/5575992648737" target="_blank" rel="noopener" title="WhatsApp">
                            <i class="fab fa-whatsapp"></i>
                        </a>
                    </div>
                </div>
                <div class="footer-col">
                    <h4>Links Rápidos</h4>
                    <ul>
                        <li><a href="#inicio">Início</a></li>
                        <li><a href="#sobre">Sobre Nós</a></li>
                        <li><a href="#servicos">Serviços</a></li>
                        <li><a href="#galeria">Galeria</a></li>
                        <li><a href="#avaliacoes">Avaliações</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Serviços</h4>
                    <ul>
                        <li><a href="#servicos">Banho Completo</a></li>
                        <li><a href="#servicos">Tosa Profissional</a></li>
                        <li><a href="#servicos">Rações & Acessórios</a></li>
                        <li><a href="#servicos">Vacinação</a></li>
                        <li><a href="#servicos">Estética Animal</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Contato</h4>
                    <ul>
                        <li><a href="tel:+5575992648737"><i class="fas fa-phone"></i> (75) 9 9264-8737</a></li>
                        <li><a href="https://wa.me/5575992648737" target="_blank" rel="noopener"><i class="fab fa-whatsapp"></i> WhatsApp</a></li>
                        <li><a href="#contato"><i class="fas fa-map-marker-alt"></i> Ver no mapa</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 Dogs House João Durval - Feira de Santana, BA. Todos os direitos reservados.</p>
                <p>Feito com <i class="fas fa-heart" style="color: var(--primary);"></i> para os pets</p>
            </div>
        </div>
    </footer>

    <!-- FLOATING WHATSAPP -->
    <a href="https://wa.me/5575992648737" class="floating-whatsapp" target="_blank" rel="noopener" title="Fale conosco pelo WhatsApp">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Loader
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('loader').classList.add('hidden');
            }, 1500);
        });

        // Scroll Progress
        window.addEventListener('scroll', () => {
            const scrollTop = document.documentElement.scrollTop;
            const scrollHeight = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const progress = (scrollTop / scrollHeight) * 100;
            document.getElementById('scrollProgress').style.width = progress + '%';
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Toggle menu
        function toggleMenu() {
            document.getElementById('nav').classList.toggle('active');
        }

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                    document.getElementById('nav').classList.remove('active');
                }
            });
        });

        // Intersection Observer for fade-in animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Form handler
        function handleSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const message = document.getElementById('message').value;
            
            const text = `Olá! Meu nome é ${name}.\nTelefone: ${phone}\n\n${message}`;
            const encodedText = encodeURIComponent(text);
            window.open(`https://wa.me/5575992648737?text=${encodedText}`, '_blank');
            
            return false;
        }

        // Phone mask
        document.getElementById('phone').addEventListener('input', function(e) {
            let value = e.target.value.replace(/\D/g, '');
            if (value.length <= 11) {
                if (value.length > 6) {
                    value = `(${value.slice(0,2)}) ${value.slice(2,7)}-${value.slice(7)}`;
                } else if (value.length > 2) {
                    value = `(${value.slice(0,2)}) ${value.slice(2)}`;
                } else if (value.length > 0) {
                    value = `(${value}`;
                }
            }
            e.target.value = value;
        });
    </script>
</body>
</html>
