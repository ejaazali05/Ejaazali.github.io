<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejaaz Ali Hasham | Data Analyst</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* === CSS RESET & VARIABLES === */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #0a0a0a;
            --bg-secondary: #1a1a1a;
            --bg-card: #2d2d2d;
            --accent-primary: #3b82f6;
            --accent-secondary: #10b981;
            --text-primary: #f8fafc;
            --text-secondary: #cbd5e1;
            --border-color: #374151;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.5);
        }

        /* === BASE STYLES === */
        body {
            font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* === HEADER STYLES === */
        header {
            background-color: var(--bg-secondary);
            border-bottom: 1px solid var(--border-color);
            padding: 1.5rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--text-primary);
            text-decoration: none;
        }

        .logo-accent {
            color: var(--accent-primary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: var(--text-secondary);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--accent-primary);
        }

        /* === HERO SECTION === */
        .hero {
            padding: 4rem 0;
            background: linear-gradient(135deg, var(--bg-primary) 0%, var(--bg-secondary) 100%);
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--accent-primary), var(--accent-secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-subtitle {
            font-size: 1.25rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
        }

        /* === MAIN CONTENT GRID === */
        main {
            padding: 4rem 0;
        }

        .grid-layout {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            align-items: start;
        }

        /* === BIO & CONTACT SECTION === */
        .bio-contact {
            background: var(--bg-card);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            box-shadow: var(--shadow);
            position: sticky;
            top: 100px;
        }

        .summary-header {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--text-primary);
            position: relative;
            padding-bottom: 0.75rem;
        }

        .summary-header::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: linear-gradient(90deg, var(--accent-primary), var(--accent-secondary));
            border-radius: 2px;
        }

        .bio-text {
            color: var(--text-secondary);
            margin-bottom: 2rem;
            text-align: left;
        }

        .bio-text p {
            margin-bottom: 1rem;
        }

        .contact-list {
            list-style: none;
            margin-top: 2rem;
        }

        .contact-list li {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            color: var(--text-secondary);
        }

        .contact-list i {
            width: 20px;
            margin-right: 0.75rem;
            color: var(--accent-primary);
        }

        /* === PROJECTS SECTION === */
        .projects-section h2, .skills-section h2 {
            font-size: 2rem;
            margin-bottom: 2rem;
            color: var(--text-primary);
            position: relative;
        }

        .projects-section h2::after, .skills-section h2::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 3px;
            background: linear-gradient(90deg, var(--accent-primary), var(--accent-secondary));
            border-radius: 2px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .project-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 1.5rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: var(--shadow);
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5);
            border-color: var(--accent-primary);
        }

        .project-card h3 {
            color: var(--text-primary);
            margin-bottom: 0.75rem;
            font-size: 1.25rem;
        }

        .project-card p {
            color: var(--text-secondary);
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .project-tag {
            background: var(--bg-secondary);
            color: var(--accent-primary);
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        /* === SKILLS SECTION === */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .skill-category {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: var(--shadow);
        }

        .skill-category h3 {
            color: var(--text-primary);
            margin-bottom: 1rem;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
        }

        .skill-category h3::before {
            content: '▸';
            margin-right: 0.5rem;
            color: var(--accent-primary);
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            color: var(--text-secondary);
            margin-bottom: 0.5rem;
            padding-left: 1rem;
            position: relative;
        }

        .skill-list li::before {
            content: '•';
            position: absolute;
            left: 0;
            color: var(--accent-secondary);
        }

        /* === FOOTER === */
        footer {
            background: var(--bg-secondary);
            border-top: 1px solid var(--border-color);
            padding: 2rem 0;
            text-align: center;
            color: var(--text-secondary);
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--accent-primary);
        }

        /* === RESPONSIVE DESIGN === */
        @media (max-width: 768px) {
            .grid-layout {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            .bio-contact {
                position: static;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container nav-container">
            <a href="#" class="logo">Ejaaz<span class="logo-accent">Hasham</span></a>
            <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Data Analyst</h1>
            <p class="hero-subtitle">Transforming raw data into actionable insights through analytical expertise</p>
        </div>
    </section>

    <main class="container">
        <div class="grid-layout">
            <!-- Bio & Contact Section -->
            <aside class="bio-contact" id="about">
                <h2 class="summary-header">Professional Summary</h2>
                <div class="bio-text">
                    <p>Aspiring data analyst with a strong foundation in SQL, Python, and data visualization tools. Currently pursuing academic studies while developing practical data analysis skills through hands-on projects.</p>
                    
                    <p>Passionate about uncovering insights from data to drive informed decision-making. Skilled in transforming complex datasets into clear, actionable visualizations and reports that help stakeholders understand trends and make data-driven decisions.</p>
                    
                    <p>Eager to apply my analytical skills in a professional environment where I can contribute to business intelligence initiatives while continuing to develop expertise in data analysis methodologies and tools.</p>
                </div>
                
                <h3>Contact</h3>
                <ul class="contact-list">
                    <li>
                        <i class="fas fa-envelope"></i>
                        <span>ejaazali05@gmail.com</span>
                    </li>
                    <li>
                        <i class="fas fa-phone"></i>
                        <span>647-914-4179</span>
                    </li>
                    <li>
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Vaughan, Ontario, Canada</span>
                    </li>
                    <li>
                        <i class="fab fa-linkedin"></i>
                        <span>LinkedIn Profile</span>
                    </li>
                    <li>
                        <i class="fab fa-github"></i>
                        <span>GitHub Profile</span>
                    </li>
                </ul>
            </aside>

            <!-- Main Content Area -->
            <div class="main-content">
                <!-- Featured Projects Section -->
                <section class="projects-section" id="projects">
                    <h2>Data Analysis Projects</h2>
                    <div class="projects-grid">
                        <article class="project-card">
                            <h3>Sales Performance Dashboard</h3>
                            <p>Developed an interactive Power BI dashboard to analyze sales performance across regions, products, and time periods. Implemented DAX calculations for KPIs and created drill-through reports for detailed analysis.</p>
                            <div class="project-tags">
                                <span class="project-tag">Power BI</span>
                                <span class="project-tag">DAX</span>
                                <span class="project-tag">Data Visualization</span>
                            </div>
                        </article>

                        <article class="project-card">
                            <h3>Customer Segmentation Analysis</h3>
                            <p>Used Python and clustering algorithms to segment customers based on purchasing behavior. Performed data cleaning, feature engineering, and visualization to identify distinct customer groups for targeted marketing strategies.</p>
                            <div class="project-tags">
                                <span class="project-tag">Python</span>
                                <span class="project-tag">Pandas</span>
                                <span class="project-tag">Scikit-learn</span>
                                <span class="project-tag">K-means</span>
                            </div>
                        </article>

                        <article class="project-card">
                            <h3>E-commerce Database Analysis</h3>
                            <p>Designed and queried a relational database to analyze e-commerce performance. Created complex SQL queries to extract insights on customer behavior, product performance, and sales trends.</p>
                            <div class="project-tags">
                                <span class="project-tag">SQL</span>
                                <span class="project-tag">Database Design</span>
                                <span class="project-tag">Query Optimization</span>
                            </div>
                        </article>
                    </div>
                </section>

                <!-- Skills & Tools Section -->
                <section class="skills-section" id="skills">
                    <h2>Skills & Tools</h2>
                    <div class="skills-grid">
                        <div class="skill-category">
                            <h3>Data Analysis</h3>
                            <ul class="skill-list">
                                <li>SQL & Database Management</li>
                                <li>Python (Pandas, NumPy)</li>
                                <li>Data Cleaning & Preprocessing</li>
                                <li>Statistical Analysis</li>
                                <li>Exploratory Data Analysis</li>
                            </ul>
                        </div>

                        <div class="skill-category">
                            <h3>Data Visualization</h3>
                            <ul class="skill-list">
                                <li>Power BI & Tableau</li>
                                <li>Matplotlib & Seaborn</li>
                                <li>Dashboard Design</li>
                                <li>KPI Development</li>
                                <li>Storytelling with Data</li>
                            </ul>
                        </div>

                        <div class="skill-category">
                            <h3>Tools & Technologies</h3>
                            <ul class="skill-list">
                                <li>Microsoft Excel (Advanced)</li>
                                <li>Jupyter Notebook</li>
                                <li>Git & GitHub</li>
                                <li>SQL Server / PostgreSQL</li>
                                <li>Data Modeling</li>
                            </ul>
                        </div>
                    </div>
                </section>
            </div>
        </div>
    </main>

    <footer id="contact">
        <div class="container footer-content">
            <p>&copy; 2024 Ejaaz Ali Hasham. All rights reserved.</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i> GitHub</a>
                <a href="#"><i class="fab fa-linkedin"></i> LinkedIn</a>
                <a href="mailto:ejaazali05@gmail.com"><i class="fas fa-envelope"></i> Email</a>
            </div>
        </div>
    </footer>
</body>
</html>
