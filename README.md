<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jayasimbu Jayamani | Developer & UI Designer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700&family=Source+Sans+Pro:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* CSS Variables for Medium Contrast Color Palette */
        :root {
            /* Medium Contrast Blue-based Color Palette */
            --primary-dark: #2A4365;
            --primary: #4A6FA5;
            --primary-light: #6B93CC;
            --accent-blue: #4C7ED0;
            --accent-green: #38A169;
            --accent-purple: #805AD5;
            --accent-orange: #ED8936;
            --accent-red: #E53E3E;
            --light-bg: #F0F4F8;
            --light-gray: #D9E2EC;
            --medium-gray: #9FB3C8;
            --dark-text: #334155;
            --medium-text: #486581;
            --light-text: #627D98;
            --white: #FFFFFF;
            --border-radius: 12px;
            --transition: all 0.3s ease;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            --shadow-hover: 0 10px 25px rgba(0, 0, 0, 0.12);
            --shadow-strong: 0 8px 25px rgba(0, 0, 0, 0.15);
        }

        /* Letter-specific colors for medium contrast */
        .letter-a { color: var(--accent-blue); }
        .letter-b { color: var(--primary); }
        .letter-c { color: var(--accent-green); }
        .letter-d { color: var(--accent-purple); }
        .letter-e { color: var(--primary-dark); }
        .letter-f { color: var(--accent-orange); }
        .letter-g { color: var(--accent-red); }
        .letter-h { color: #4299E1; }
        .letter-i { color: #38B2AC; }
        .letter-j { color: #805AD5; }
        .letter-k { color: var(--primary-dark); }
        .letter-l { color: var(--accent-blue); }
        .letter-m { color: var(--accent-green); }
        .letter-n { color: var(--accent-orange); }
        .letter-o { color: #C53030; }
        .letter-p { color: #4A6FA5; }
        .letter-q { color: #805AD5; }
        .letter-r { color: var(--accent-blue); }
        .letter-s { color: var(--accent-green); }
        .letter-t { color: #D69E2E; }
        .letter-u { color: #38B2AC; }
        .letter-v { color: #9F7AEA; }
        .letter-w { color: var(--primary-dark); }
        .letter-x { color: var(--accent-red); }
        .letter-y { color: #D69E2E; }
        .letter-z { color: #319795; }

        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Source Sans Pro', sans-serif;
            line-height: 1.6;
            color: var(--dark-text);
            background-color: var(--white);
            transition: var(--transition);
        }
       
        /* Header and Titles use Dark Colors */
        h1, h2, h3, h4 {
            font-family: 'Outfit', sans-serif;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        h1 {
            font-size: 3.5rem;
        }

        h2 {
            font-size: 2.5rem;
            position: relative;
            display: inline-block;
            margin-bottom: 3rem;
        }
       
        h2:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-blue), var(--accent-green));
            border-radius: 2px;
        }

        h3 {
            font-size: 1.8rem;
        }

        p {
            margin-bottom: 1.5rem;
            color: var(--medium-text);
        }
       
        a {
            text-decoration: none;
            color: var(--accent-blue);
            transition: var(--transition);
        }
       
        a:hover {
            color: var(--primary-light);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 10px;
        }

        section {
            padding: 80px 0;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            background: linear-gradient(135deg, var(--accent-blue), var(--primary));
            color: var(--white);
            border-radius: var(--border-radius);
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            font-family: 'Outfit', sans-serif;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow-hover);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid var(--accent-blue);
            color: var(--accent-blue);
        }

        .btn-secondary:hover {
            background: var(--accent-blue);
            color: var(--white);
        }

        .btn-resume {
            background: linear-gradient(135deg, var(--accent-green), #48BB78);
            margin-left: 15px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2:after {
            left: 50%;
            transform: translateX(-50%);
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: var(--primary-dark);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 20px 0;
            transition: var(--transition);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Outfit', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--white);
        }

        .logo .letter-j {
            color: var(--white);
        }

        .logo span {
            color: var(--accent-blue);
        }

        nav ul {
            display: flex;
            list-style: none;
            align-items: center;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: var(--white);
            font-weight: 500;
            position: relative;
            padding: 5px 0;
            transition: var(--transition);
        }

        nav ul li a:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent-blue);
            transition: var(--transition);
        }

        nav ul li a:hover:after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 100%);
            color: var(--white);
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1.5rem;
            color: var(--white);
        }

        .hero h1 span {
            color: var(--accent-blue);
        }

        .hero-role {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            color: var(--light-gray);
        }

        /* Specific styling for the hero paragraph text */
        .hero-content p {
            color: #000000 !important; /* Black color */
            font-weight: 700 !important; /* Bold weight */
            font-size: 1.2rem;
            line-height: 1.8;
        }

        .hero-btns {
            display: flex;
            gap: 20px;
            margin-top: 3rem;
        }

        /* NEW: Professional Summary Section - Redesigned */
        .professional-summary {
            background: linear-gradient(135deg, var(--light-bg) 0%, #E3F2FD 100%);
            border-radius: var(--border-radius);
            padding: 50px;
            margin: 40px 0;
            box-shadow: var(--shadow-strong);
            border-left: 6px solid var(--accent-blue);
            position: relative;
            overflow: hidden;
        }

        .professional-summary:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, rgba(76, 126, 208, 0.1) 0%, rgba(56, 161, 105, 0.1) 100%);
            border-radius: 0 0 0 100%;
        }

        .summary-header {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
            gap: 20px;
        }

        .summary-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--accent-blue), var(--primary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.5rem;
            flex-shrink: 0;
        }

        .summary-content {
            flex-grow: 1;
        }

        .summary-content h3 {
            color: var(--primary-dark);
            margin-bottom: 10px;
        }

        .summary-highlights {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .highlight-card {
            background: var(--white);
            padding: 25px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid var(--light-gray);
        }

        .highlight-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .highlight-card i {
            font-size: 2rem;
            color: var(--accent-blue);
            margin-bottom: 15px;
            display: block;
        }

        .highlight-card h4 {
            color: var(--primary-dark);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        /* Projects Section - UPDATED: Removed third project */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 3rem;
        }

        .project-card {
            background-color: var(--white);
            border-radius: var(--border-radius);
            overflow: hidden;
            transition: var(--transition);
            box-shadow: var(--shadow);
            border: 1px solid var(--light-gray);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-hover);
        }

        .project-img {
            height: 200px;
            background-color: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 3rem;
        }

        .project-card:nth-child(1) .project-img {
            background: linear-gradient(135deg, #E3F2FD, #BBDEFB);
        }

        .project-card:nth-child(2) .project-img {
            background: linear-gradient(135deg, #E8F5E9, #C8E6C9);
        }

        /* Removed third project card styling */

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            margin-bottom: 10px;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 15px 0;
        }

        .project-tag {
            background-color: var(--light-bg);
            color: var(--primary);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            border: 1px solid var(--light-gray);
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 3rem;
        }

        .skill-category h3 {
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-category h3 i {
            color: var(--accent-blue);
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .skill-item {
            background-color: var(--white);
            padding: 15px 20px;
            border-radius: var(--border-radius);
            display: flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
            flex: 1 0 calc(50% - 15px);
            border: 1px solid var(--light-gray);
            box-shadow: var(--shadow);
        }

        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .skill-item i {
            color: var(--accent-blue);
            font-size: 1.2rem;
        }

        /* About Section */
        .about-container {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 50px;
            align-items: center;
            margin-top: 3rem;
        }

        .about-img {
            width: 100%;
            height: 350px;
            background: linear-gradient(135deg, var(--primary), var(--accent-blue));
            border-radius: var(--border-radius);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            color: var(--white);
            box-shadow: var(--shadow);
        }

        .quick-facts {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 2rem;
        }

        .fact {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 15px;
            background-color: var(--light-bg);
            border-radius: var(--border-radius);
            border-left: 4px solid var(--accent-blue);
        }

        .fact i {
            color: var(--accent-blue);
            font-size: 1.2rem;
        }

        /* Education Section */
        .education-timeline {
            max-width: 800px;
            margin: 3rem auto 0;
            position: relative;
        }

        .education-timeline:before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background-color: var(--medium-gray);
        }

        .education-item {
            display: flex;
            align-items: center;
            margin-bottom: 50px;
            position: relative;
        }

        .education-item:nth-child(odd) {
            flex-direction: row-reverse;
        }

        .education-content {
            background-color: var(--white);
            padding: 25px;
            border-radius: var(--border-radius);
            width: 45%;
            box-shadow: var(--shadow);
            border: 1px solid var(--light-gray);
        }

        .education-icon {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--accent-blue), var(--primary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.5rem;
            z-index: 1;
            box-shadow: 0 5px 15px rgba(76, 126, 208, 0.3);
        }

        /* Contact Section - Enhanced with Bold Text */
        .contact-section {
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 100%);
            color: var(--white);
            margin-bottom: 0;
            position: relative;
            overflow: hidden;
        }

        .contact-section:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%234c7ed0' fill-opacity='0.05' fill-rule='evenodd'/%3E%3C/svg%3E");
            opacity: 0.3;
        }

        .contact-section h2,
        .contact-section h3,
        .contact-section h4,
        .contact-section p {
            color: var(--white);
            font-weight: 700 !important; /* Make all text bold */
        }

        .contact-section .section-title h2:after {
            background: linear-gradient(90deg, var(--accent-green), var(--accent-blue));
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
            margin-top: 3rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: var(--border-radius);
            transition: var(--transition);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .contact-item:hover {
            transform: translateY(-5px);
            background-color: rgba(255, 255, 255, 0.15);
            box-shadow: var(--shadow);
        }

        .contact-item i {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--accent-blue), var(--accent-green));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.2rem;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            width: 45px;
            height: 45px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.2rem;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
       
        .social-links a:hover {
            background: linear-gradient(135deg, var(--accent-blue), var(--accent-green));
            color: var(--white);
            transform: scale(1.1);
        }

        .contact-form {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: var(--border-radius);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 700 !important; /* Bold labels */
            color: var(--white);
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: var(--border-radius);
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--white);
            font-family: 'Source Sans Pro', sans-serif;
            transition: var(--transition);
            font-weight: 600; /* Bold input text */
        }

        .form-control::placeholder {
            color: rgba(255, 255, 255, 0.7);
            font-weight: 500;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--accent-blue);
            box-shadow: 0 0 0 3px rgba(76, 126, 208, 0.3);
            background-color: rgba(255, 255, 255, 0.15);
        }

        select.form-control option {
            background-color: var(--primary-dark);
            color: var(--white);
            font-weight: 600;
        }

        /* Footer - Enhanced with Bold Text */
        footer {
            background-color: var(--primary-dark);
            color: var(--white);
            padding: 50px 0 20px;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }

        .footer-links {
            display: flex;
            gap: 20px;
        }

        .footer-links a {
            color: var(--white);
            font-weight: 600 !important; /* Bold footer links */
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--light-gray);
            font-size: 0.9rem;
            font-weight: 600; /* Bold copyright text */
        }

        /* Resume Download Button */
        .download-resume {
            text-align: center;
            margin: 40px 0;
        }

        .resume-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            font-size: 1.1rem;
            font-weight: 600;
        }

        /* Colorful letters for name in hero */
        .name-letters {
            display: inline-block;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            h1 {
                font-size: 3rem;
            }

            h2 {
                font-size: 2.2rem;
            }

            .about-container {
                grid-template-columns: 1fr;
            }

            .education-timeline:before {
                left: 30px;
            }

            .education-item {
                flex-direction: row !important;
                align-items: flex-start;
            }

            .education-content {
                width: calc(100% - 80px);
                margin-left: 80px;
            }

            .education-icon {
                left: 30px;
                transform: translateX(0);
            }

            .professional-summary {
                padding: 30px;
            }

            .summary-highlights {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }

            nav {
                position: fixed;
                top: 80px;
                right: -100%;
                width: 250px;
                height: calc(100vh - 80px);
                background-color: var(--primary-dark);
                transition: var(--transition);
                padding: 30px;
                box-shadow: -5px 0 15px rgba(0, 0, 0, 0.1);
                z-index: 999;
            }

            nav.active {
                right: 0;
            }

            nav ul {
                flex-direction: column;
            }

            nav ul li {
                margin: 15px 0;
            }

            .nav-resume {
                margin-top: 20px;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero-role {
                font-size: 1.5rem;
            }

            .hero-btns {
                flex-direction: column;
                align-items: flex-start;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .skills-container {
                grid-template-columns: 1fr;
            }

            .footer-content {
                flex-direction: column;
                gap: 20px;
                text-align: center;
            }

            .quick-facts {
                grid-template-columns: 1fr;
            }

            .contact-container {
                grid-template-columns: 1fr;
            }

            .summary-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }

            /* Adjust hero text for mobile */
            .hero-content p {
                font-size: 1.1rem;
            }
        }

        @media (max-width: 576px) {
            .container {
                padding: 0 15px;
            }

            section {
                padding: 70px 0;
            }

            .about-img {
                height: 250px;
                font-size: 4rem;
            }

            .professional-summary {
                padding: 20px;
            }

            /* Adjust hero text for smaller screens */
            .hero-content p {
                font-size: 1rem;
            }
        }

        /* Animation Classes */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 1s cubic-bezier(0.4, 0.0, 0.2, 1), transform 1s cubic-bezier(0.4, 0.0, 0.2, 1);
        }

        .fade-in.appear {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <span class="letter-j">J</span><span class="letter-a">a</span><span class="letter-y">y</span><span class="letter-a">a</span><span class="letter-s">s</span><span class="letter-i">i</span><span class="letter-m">m</span><span class="letter-b">b</span><span class="letter-u">u</span>
                <span class="letter-j">J</span><span class="letter-a">a</span><span class="letter-y">y</span><span class="letter-a">a</span><span class="letter-m">m</span><span class="letter-a">a</span><span class="letter-n">n</span><span class="letter-i">i</span>
            </div>
            <nav id="main-nav">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#resume">Resume</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#education">Education</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li class="nav-resume"><a href="Jayasimbu Jayamani (Java).pdf" class="btn btn-resume" download><i class="fas fa-download"></i> Resume</a></li>
                </ul>
            </nav>
            <button class="mobile-menu-btn" id="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content fade-in">
            <h1>Hi, I'm <span class="name-letters">
                <span class="letter-j">J</span><span class="letter-a">a</span><span class="letter-y">y</span><span class="letter-a">a</span><span class="letter-s">s</span><span class="letter-i">i</span><span class="letter-m">m</span><span class="letter-b">b</span><span class="letter-u">u</span>
                <span class="letter-j">J</span><span class="letter-a">a</span><span class="letter-y">y</span><span class="letter-a">a</span><span class="letter-m">m</span><span class="letter-a">a</span><span class="letter-n">n</span><span class="letter-i">i</span>
            </span></h1>
            <div class="hero-role">Java Developer & UI Designer</div>
            <!-- UPDATED: This paragraph now has black bold text -->
            <p>Computer Science Engineering student with strong foundation in Core Java, OOP, and web technologies. Passionate about building efficient, user-friendly software solutions. Seeking internship opportunities for 2026.</p>
            <div class="hero-btns">
                <a href="#projects" class="btn">View Projects</a>
                <a href="#contact" class="btn btn-secondary">Get In Touch</a>
                <a href="Jayasimbu Jayamani (Java).pdf" class="btn btn-resume" download><i class="fas fa-download"></i> Download Resume</a>
            </div>
        </div>
    </section>

    <!-- Resume Download Section with NEW Professional Summary -->
    <section id="resume">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Resume</h2>
                <p>Download my detailed resume for complete professional profile</p>
            </div>
            <div class="download-resume fade-in">
                <a href="Jayasimbu Jayamani (Java).pdf" class="btn resume-btn" download>
                    <i class="fas fa-file-pdf"></i> Download Resume (PDF)
                </a>
                <p style="margin-top: 20px; font-size: 0.9rem; color: var(--medium-text);">
                    <i class="fas fa-info-circle"></i> Includes: Education, Skills, Projects, Certifications, and Contact Information
                </p>
            </div>
            
            <!-- NEW Professional Summary Design -->
            <div class="professional-summary fade-in">
                <div class="summary-header">
                    <div class="summary-icon">
                        <i class="fas fa-user-tie"></i>
                    </div>
                    <div class="summary-content">
                        <h3>Professional Summary</h3>
                        <p>Motivated Computer Science Engineering student with a strong foundation in Core Java, Object-Oriented Programming (OOP), HTML, CSS, and SQL. Hands-on experience in developing web-based applications and using AI-assisted tools to improve application logic and UI flow. Passionate about building efficient, user-friendly software solutions and eager to start a professional career as a Java Developer in a collaborative environment.</p>
                    </div>
                </div>
                
                <div class="summary-highlights">
                    <div class="highlight-card">
                        <i class="fas fa-code"></i>
                        <h4>Technical Expertise</h4>
                        <p>Proficient in Core Java, OOP Concepts, Web Technologies (HTML5, CSS3, JavaScript), and SQL. Experienced with AI-assisted development tools.</p>
                    </div>
                    
                    <div class="highlight-card">
                        <i class="fas fa-paint-brush"></i>
                        <h4>Design Skills</h4>
                        <p>Skilled in UI/UX Design, Wireframing, Prototyping using Figma, Canva, Visily AI, Stitch AI, and Google AI Studio.</p>
                    </div>
                    
                    <div class="highlight-card">
                        <i class="fas fa-project-diagram"></i>
                        <h4>Project Experience</h4>
                        <p>Developed web applications including Fitness Tracking and Elder Care management systems with responsive design and user authentication.</p>
                    </div>
                    
                    <div class="highlight-card">
                        <i class="fas fa-graduation-cap"></i>
                        <h4>Career Objective</h4>
                        <p>Seeking internship opportunities for 2026 to apply technical skills and contribute to innovative software development projects.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section - UPDATED: Removed Chat Application -->
    <section id="projects" style="background-color: var(--light-bg);">
        <div class="container">
            <div class="section-title fade-in">
                <h2>My Projects</h2>
                <p>Showcasing my technical and design capabilities</p>
            </div>
           
            <div class="projects-grid">
                <div class="project-card fade-in">
                    <div class="project-img">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <div class="project-content">
                        <h3>Vechi-Care</h3>
                        <p>A compassionate web application for elder care management with responsive UI and intuitive features for caregivers and family members.</p>
                        <div class="project-tags">
                            <span class="project-tag">HTML5</span>
                            <span class="project-tag">CSS3</span>
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">Responsive Design</span>
                        </div>
                        <a href="#" class="btn">View Details</a>
                    </div>
                </div>
               
                <div class="project-card fade-in">
                    <div class="project-img">
                        <i class="fas fa-dumbbell"></i>
                    </div>
                    <div class="project-content">
                        <h3>Fitness Tracker</h3>
                        <p>AI-powered fitness companion with workout logging, progress tracking, and personalized recommendations using Google AI Studio.</p>
                        <div class="project-tags">
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">AI Integration</span>
                            <span class="project-tag">User Authentication</span>
                            <span class="project-tag">Data Visualization</span>
                        </div>
                        <a href="#" class="btn">View Details</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Skills & Technologies</h2>
                <p>My technical toolkit and design capabilities</p>
            </div>
           
            <div class="skills-container">
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-code"></i> Development</h3>
                    <div class="skills-list">
                        <div class="skill-item">
                            <i class="fab fa-java"></i>
                            <span>Java (HackerRank Certified)</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-html5"></i>
                            <span>HTML5</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-css3-alt"></i>
                            <span>CSS3</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-js"></i>
                            <span>JavaScript</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-database"></i>
                            <span>SQL</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-python"></i>
                            <span>Python</span>
                        </div>
                    </div>
                </div>
               
                <div class="skill-category fade-in">
                    <h3><i class="fas fa-paint-brush"></i> Design & Tools</h3>
                    <div class="skills-list">
                        <div class="skill-item">
                            <i class="fab fa-figma"></i>
                            <span>Figma</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-palette"></i>
                            <span>Canva</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-robot"></i>
                            <span>Stitch AI</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-magic"></i>
                            <span>Visily AI</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-chart-line"></i>
                            <span>Power BI</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-file-excel"></i>
                            <span>Microsoft Excel</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" style="background-color: var(--light-bg);">
        <div class="container">
            <div class="section-title fade-in">
                <h2>About Me</h2>
                <p>Get to know me better</p>
            </div>
           
            <div class="about-container">
                <div class="about-img fade-in">
                    <i class="fas fa-user"></i>
                </div>
                <div class="about-content fade-in">
                    <h3>Developer & Designer Building User-Centered Solutions</h3>
                    <p>Hello! I'm Jayasimbu Jayamani, a Computer Science Engineering student passionate about creating technology that makes a difference in people's lives.</p>
                    <p>I'm fascinated by the intersection of code and design—where technical functionality meets intuitive user experience. My journey in tech has taught me that the best solutions emerge when developers think like designers and designers understand development.</p>
                    <p>Currently pursuing my B.E. in Computer Science, I've developed a strong foundation in web technologies while exploring the creative possibilities of UI/UX design. I'm particularly excited about leveraging AI tools to enhance development workflows and create smarter applications.</p>
                   
                    <div class="quick-facts">
                        <div class="fact">
                            <i class="fas fa-map-marker-alt"></i>
                            <span>Dharmapuri, Tamil Nadu</span>
                        </div>
                        <div class="fact">
                            <i class="fas fa-graduation-cap"></i>
                            <span>B.E. Computer Science</span>
                        </div>
                        <div class="fact">
                            <i class="fas fa-briefcase"></i>
                            <span>Seeking Internships - 2026</span>
                        </div>
                        <div class="fact">
                            <i class="fas fa-star"></i>
                            <span>AI Integration & UI/UX Design</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education">
        <div class="container">
            <div class="section-title fade-in">
                <h2>Education</h2>
                <p>My academic journey and certifications</p>
            </div>
           
            <div class="education-timeline">
                <div class="education-item fade-in">
                    <div class="education-content">
                        <h3>Bachelor of Engineering</h3>
                        <p class="institution">Sri Shanmugha College of Engineering and Technology</p>
                        <p class="duration">2022 - 2026 (Expected)</p>
                        <p class="details">Computer Science and Engineering | CGPA: 7.3/10</p>
                        <p class="courses">Relevant Coursework: Data Structures, Web Technologies, DBMS, Software Engineering, OOP (Java), UI/UX Design</p>
                    </div>
                    <div class="education-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                </div>
               
                <div class="education-item fade-in">
                    <div class="education-content">
                        <h3>Higher Secondary Certificate</h3>
                        <p class="institution">Government Higher Secondary School, Errabaiyanahalli</p>
                        <p class="duration">2020 - 2022</p>
                        <p class="details">Science Stream with Computer Science</p>
                    </div>
                    <div class="education-icon">
                        <i class="fas fa-school"></i>
                    </div>
                </div>
               
                <div class="education-item fade-in">
                    <div class="education-content">
                        <h3>Certifications</h3>
                        <ul style="list-style-type: none;">
                            <li><i class="fas fa-certificate" style="color: var(--accent-blue); margin-right: 10px;"></i> HackerRank Java (Basic) Certification</li>
                            <li><i class="fas fa-certificate" style="color: var(--accent-blue); margin-right: 10px;"></i> IBM SkillsBuild: Artificial Intelligence Fundamentals</li>
                            <li><i class="fas fa-certificate" style="color: var(--accent-blue); margin-right: 10px;"></i> Designing the Web: Front-End Development Immersion</li>
                        </ul>
                    </div>
                    <div class="education-icon">
                        <i class="fas fa-award"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section - Enhanced with Bold Text -->
    <section id="contact" class="contact-section">
        <div class="container">
            <div class="section-title fade-in">
                <h2>GET IN TOUCH</h2>
                <p>LET'S CONNECT AND CREATE SOMETHING AMAZING TOGETHER</p>
            </div>
           
            <div class="contact-container">
                <div class="contact-info fade-in">
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <h4>EMAIL</h4>
                            <p>jayasimbu66@gmail.com</p>
                        </div>
                    </div>
                   
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>LOCATION</h4>
                            <p>Dharmapuri, Tamil Nadu, India</p>
                        </div>
                    </div>
                   
                    <div class="contact-item">
                        <i class="fas fa-user-tie"></i>
                        <div>
                            <h4>STATUS</h4>
                            <p>AVAILABLE FOR INTERNSHIPS - SUMMER 2026</p>
                        </div>
                    </div>
                   
                    <div>
                        <h4>CONNECT WITH ME</h4>
                        <div class="social-links">
                            <a href="https://github.com/jayasimbu" target="_blank"><i class="fab fa-github"></i></a>
                            <a href="https://www.linkedin.com/in/jayasimbu-jayamani-51b1b42a1" target="_blank"><i class="fab fa-linkedin-in"></i></a>
                            <a href="https://www.hackerrank.com/profile/jayasimbu" target="_blank"><i class="fab fa-hackerrank"></i></a>
                            <a href="https://leetcode.com/u/jayasimbu/" target="_blank"><i class="fas fa-code"></i></a>
                            <a href="https://www.figma.com/@jayasimbu" target="_blank"><i class="fab fa-figma"></i></a>
                        </div>
                    </div>
                </div>
               
                <div class="contact-form fade-in">
                    <h3>SEND A MESSAGE</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">NAME</label>
                            <input type="text" id="name" class="form-control" required placeholder="YOUR NAME">
                        </div>
                       
                        <div class="form-group">
                            <label for="email">EMAIL</label>
                            <input type="email" id="email" class="form-control" required placeholder="YOUR EMAIL ADDRESS">
                        </div>
                       
                        <div class="form-group">
                            <label for="subject">SUBJECT</label>
                            <select id="subject" class="form-control" required>
                                <option value="">SELECT A SUBJECT</option>
                                <option value="General Inquiry">GENERAL INQUIRY</option>
                                <option value="Internship Opportunity">INTERNSHIP OPPORTUNITY</option>
                                <option value="Collaboration">COLLABORATION</option>
                                <option value="Other">OTHER</option>
                            </select>
                        </div>
                       
                        <div class="form-group">
                            <label for="message">MESSAGE</label>
                            <textarea id="message" rows="5" class="form-control" required placeholder="YOUR MESSAGE..."></textarea>
                        </div>
                       
                        <button type="submit" class="btn" style="background: linear-gradient(135deg, var(--accent-green), var(--accent-blue)); font-weight: 700;">SEND MESSAGE</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer - Enhanced with Bold Text -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="logo" style="font-weight: 700;">
                    <span class="letter-j">J</span><span class="letter-a">a</span><span class="letter-y">y</span><span class="letter-a">a</span><span class="letter-s">s</span><span class="letter-i">i</span><span class="letter-m">m</span><span class="letter-b">b</span><span class="letter-u">u</span>
                    <span class="letter-j">J</span><span class="letter-a">a</span><span class="letter-y">y</span><span class="letter-a">a</span><span class="letter-m">m</span><span class="letter-a">a</span><span class="letter-n">n</span><span class="letter-i">i</span>
                </div>
                <div class="footer-links">
                    <a href="#home">HOME</a>
                    <a href="#resume">RESUME</a>
                    <a href="#contact">CONTACT</a>
                </div>
            </div>
           
            <div class="copyright">
                <p><strong>&copy; 2026 JAYASIMBU JAYAMANI. ALL RIGHTS RESERVED.</strong></p>
                <p><strong>MADE WITH <i class="fas fa-heart" style="color: var(--accent-red);"></i> USING HTML, CSS & JAVASCRIPT</strong></p>
            </div>
        </div>
    </footer>

    <script>
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mainNav = document.getElementById('main-nav');
        const contactForm = document.getElementById('contactForm');

        // Mobile menu toggle
        mobileMenuBtn.addEventListener('click', () => {
            mainNav.classList.toggle('active');
            const icon = mobileMenuBtn.querySelector('i');
            if (mainNav.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });

        // Close mobile menu when clicking a link
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', () => {
                mainNav.classList.remove('active');
                mobileMenuBtn.querySelector('i').classList.remove('fa-times');
                mobileMenuBtn.querySelector('i').classList.add('fa-bars');
            });
        });

        // Form Submission
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();

            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;

            alert(`Thank you for your message, ${name}! I'll get back to you soon.`);
            contactForm.reset();
        });

        // Fade-in animation on scroll
        const fadeElements = document.querySelectorAll('.fade-in');
        const appearOnScroll = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('appear');
                    appearOnScroll.unobserve(entry.target);
                }
            });
        }, { threshold: 0.1 });

        fadeElements.forEach(element => {
            appearOnScroll.observe(element);
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.padding = '15px 0';
                header.style.boxShadow = '0 5px 20px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.padding = '20px 0';
                header.style.boxShadow = 'none';
            }
        });

        // Function to apply letter colors to any element
        function applyLetterColors(element) {
            const text = element.textContent;
            element.innerHTML = '';
            
            for (let i = 0; i < text.length; i++) {
                const letter = text[i];
                const span = document.createElement('span');
                span.textContent = letter;
                
                if (letter.match(/[a-z]/i)) {
                    const letterClass = 'letter-' + letter.toLowerCase();
                    span.className = letterClass;
                }
                
                element.appendChild(span);
            }
        }

        // Apply letter colors to name in header and footer
        document.addEventListener('DOMContentLoaded', function() {
            const nameElements = document.querySelectorAll('.logo');
            nameElements.forEach(applyLetterColors);
            
            const heroName = document.querySelector('.name-letters');
            if (heroName) applyLetterColors(heroName);
        });
    </script>
</body>
</html>
