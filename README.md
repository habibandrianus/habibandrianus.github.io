<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Habib Furqony Andrianus - Economist & Data Scientist</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            animation: float 20s infinite linear;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }

        /* Header section */
        .header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 25px;
            padding: 60px 40px;
            text-align: center;
            margin-bottom: 40px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.1);
            animation: fadeInUp 1s ease-out;
        }

        .header h1 {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #ff6b6b, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
            animation: textGlow 2s ease-in-out infinite alternate;
        }

        @keyframes textGlow {
            from { filter: drop-shadow(0 0 10px rgba(255, 107, 107, 0.5)); }
            to { filter: drop-shadow(0 0 20px rgba(78, 205, 196, 0.5)); }
        }

        .typing-animation {
            font-size: 1.4rem;
            color: #fff;
            margin-bottom: 30px;
            min-height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .wave {
            font-size: 2.5rem;
            animation: wave 2s infinite;
            display: inline-block;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        /* Card styles */
        .card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease-out;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }

        .card h2 {
            font-size: 2.2rem;
            color: #2c3e50;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 15px;
        }

        .card h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 4px;
            background: linear-gradient(135deg, #ff6b6b, #4ecdc4);
            border-radius: 2px;
        }

        .card h3 {
            color: #34495e;
            font-size: 1.4rem;
            margin-bottom: 15px;
            position: relative;
            padding-left: 20px;
        }

        .card h3::before {
            content: '🚀';
            position: absolute;
            left: 0;
            top: 0;
        }

        /* Skills grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .skill-item {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-item:hover {
            transform: scale(1.05);
            background: linear-gradient(135deg, #764ba2, #667eea);
        }

        /* Awards grid */
        .awards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .award-item {
            background: linear-gradient(135deg, #ffeaa7, #fab1a0);
            padding: 25px;
            border-radius: 15px;
            border-left: 5px solid #e17055;
            transition: all 0.3s ease;
        }

        .award-item:hover {
            transform: translateX(10px);
            box-shadow: -5px 5px 20px rgba(0, 0, 0, 0.1);
        }

        /* Experience timeline */
        .timeline {
            position: relative;
            margin-top: 30px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 30px;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(to bottom, #667eea, #764ba2);
            border-radius: 2px;
        }

        .timeline-item {
            position: relative;
            margin: 30px 0;
            margin-left: 70px;
            background: rgba(255, 255, 255, 0.9);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(102, 126, 234, 0.2);
            transition: all 0.3s ease;
        }

        .timeline-item:hover {
            background: rgba(255, 255, 255, 1);
            transform: translateX(10px);
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -55px;
            top: 25px;
            width: 20px;
            height: 20px;
            background: #667eea;
            border: 4px solid white;
            border-radius: 50%;
            box-shadow: 0 0 10px rgba(102, 126, 234, 0.5);
        }

        /* Contact section */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .contact-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 15px 25px;
            border-radius: 50px;
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .contact-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.4);
            background: linear-gradient(135deg, #764ba2, #667eea);
        }

        /* Projects showcase */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .project-card {
            background: linear-gradient(135deg, #a8e6cf, #88d8c0);
            padding: 30px;
            border-radius: 20px;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transform: rotate(45deg);
            transition: all 0.6s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        /* Animations */
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

        .fade-in {
            animation: fadeInUp 1s ease-out;
        }

        /* Quote section */
        .quote {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 50px;
            border-radius: 25px;
            text-align: center;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }

        .quote::before {
            content: '"';
            font-size: 8rem;
            position: absolute;
            top: -20px;
            left: 30px;
            opacity: 0.2;
            font-family: serif;
        }

        .quote p {
            font-size: 1.5rem;
            font-style: italic;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        /* Responsive design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .header {
                padding: 40px 20px;
            }
            
            .card {
                padding: 25px;
            }
            
            .skills-grid,
            .awards-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <!-- Animated background particles -->
    <div class="particles" id="particles"></div>

    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>Hi there, I'm Habib Furqony Andrianus! <span class="wave">👋</span></h1>
            <div class="typing-animation" id="typing"></div>
        </div>

        <!-- About Section -->
        <div class="card">
            <h2>🚀 About Me</h2>
            <p style="font-size: 1.1rem; color: #555;">I'm a distinguished economist and data scientist currently pursuing my Master of Economics at the National University of Singapore (NUS) on a full LPDP scholarship. With a top 1% Bachelor's degree from IPB University and extensive corporate experience at Philip Morris International and Nutrifood, I specialize in economic research, data analytics, and strategic business insights.</p>
            
            <div class="skills-grid">
                <div class="skill-item">
                    <h4>🎓 Master of Economics</h4>
                    <p>National University of Singapore (Distinction Grade)</p>
                </div>
                <div class="skill-item">
                    <h4>🏆 Top 1% Graduate</h4>
                    <p>IPB University (GPA: 3.95/4.00)</p>
                </div>
                <div class="skill-item">
                    <h4>📊 Area Retail Analyst</h4>
                    <p>Philip Morris International</p>
                </div>
                <div class="skill-item">
                    <h4>🔬 Student Researcher</h4>
                    <p>Institute of Policy Studies, LKYSPP</p>
                </div>
            </div>
        </div>

        <!-- Technical Skills -->
        <div class="card">
            <h2>🛠️ Technical Skills & Tools</h2>
            <div class="skills-grid">
                <div class="skill-item" style="background: linear-gradient(135deg, #276DC3, #1F4E79);">
                    <h4>R Programming</h4>
                    <p>Advanced Statistical Analysis</p>
                </div>
                <div class="skill-item" style="background: linear-gradient(135deg, #1F4E79, #276DC3);">
                    <h4>Stata</h4>
                    <p>Econometric Modeling</p>
                </div>
                <div class="skill-item" style="background: linear-gradient(135deg, #217346, #2F5233);">
                    <h4>Microsoft Excel</h4>
                    <p>Advanced Analytics & Visualization</p>
                </div>
            </div>
        </div>

        <!-- Awards -->
        <div class="card">
            <h2>🎖️ Notable Awards & Honors</h2>
            <div class="awards-grid">
                <div class="award-item">
                    <h4>🥇 World's Top Universities Scholarship</h4>
                    <p>Indonesian Endowment Fund (15% Acceptance Rate) - 2024</p>
                </div>
                <div class="award-item">
                    <h4>🏆 Most Inspiring Student</h4>
                    <p>Economics Department, IPB University - 2022</p>
                </div>
                <div class="award-item">
                    <h4>🥈 Silver Medal</h4>
                    <p>Social Science at National Science Olympiad (OSN SMP) - 2014</p>
                </div>
                <div class="award-item">
                    <h4>📜 Merit-Based Full Tuition Scholarship</h4>
                    <p>Ministry of Education, Republic of Indonesia (2019-2022)</p>
                </div>
            </div>
        </div>

        <!-- Professional Experience -->
        <div class="card">
            <h2>💼 Professional Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <h3>📈 Area Retail Analyst | Philip Morris International</h3>
                    <p><em>August 2023 - April 2024</em></p>
                    <ul>
                        <li>Assembled market data from <strong>10,000+ retailers</strong> driving >5% growth in Sampoerna's volume and profit</li>
                        <li>Managed <strong>3 key sales databases</strong> with real-time survey integration</li>
                        <li>Achieved <strong>10 million sticks</strong> in sales, securing <strong>No.1 Central Java Zone ranking</strong> in Q1 2024</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <h3>🎯 Area Marketing Junior Executive | Nutrifood Indonesia</h3>
                    <p><em>October 2022 - April 2023</em></p>
                    <ul>
                        <li>Led marketing operations across <strong>5 major cities</strong> with team of 10+ members</li>
                        <li>Executed <strong>100+ brand activation</strong> events for 5 brands</li>
                        <li>Drove <strong>10%+ area growth</strong> through strategic multichannel marketing optimization</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <h3>💻 Product Analyst | Lifepal Technologies</h3>
                    <p><em>June 2022 - September 2022</em></p>
                    <ul>
                        <li>Supervised <strong>300+ agents</strong> operations reporting to CPO & CMO</li>
                        <li>Resolved <strong>100+ bug reports</strong> within 24-hour SLA, improving user satisfaction</li>
                        <li>Boosted <strong>customer retention by 75%</strong> through algorithm optimization</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Featured Projects -->
        <div class="card">
            <h2>🎯 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>📊 Economic Impact Analysis - Natural Disasters</h3>
                    <p>Comprehensive econometric analysis of socio-economic impacts of natural disasters in West Sumatra using advanced statistical modeling.</p>
                    <p><strong>Methods:</strong> Panel Data Analysis, Difference-in-Differences, Spatial Econometrics</p>
                    <p><strong>Status:</strong> Published in Q3 Scopus Journal (2025)</p>
                </div>
                
                <div class="project-card">
                    <h3>💰 Redenomination Policy Analysis</h3>
                    <p>Experimental economics approach to analyze determinants of redenomination policy success in Indonesia.</p>
                    <p><strong>Methods:</strong> Online Experiments, Behavioral Economics, Statistical Analysis</p>
                    <p><strong>Funding:</strong> Central Bank of Indonesia Research Program</p>
                </div>
                
                <div class="project-card">
                    <h3>🏪 Retail Analytics Dashboard</h3>
                    <p>Advanced analytics system for optimizing retail channel strategies across 3,000+ retailers.</p>
                    <p><strong>Features:</strong> Real-time Data Integration, Predictive Modeling, Strategic Insights</p>
                    <p><strong>Impact:</strong> Increased PMI sales at Tuban Area to single digits on Q1 2024</p>
                </div>
            </div>
        </div>

        <!-- Current Focus -->
        <div class="card">
            <h2>🌟 Current Focus</h2>
            <div class="skills-grid">
                <div class="skill-item" style="background: linear-gradient(135deg, #e74c3c, #c0392b);">
                    <h4>🔬 Research</h4>
                    <p>Identity and belonging among Indonesians in Singapore (IPS-LKYSPP)</p>
                </div>
                <div class="skill-item" style="background: linear-gradient(135deg, #f39c12, #e67e22);">
                    <h4>📚 Teaching</h4>
                    <p>Digital Business Transformation for MBA students</p>
                </div>
                <div class="skill-item" style="background: linear-gradient(135deg, #9b59b6, #8e44ad);">
                    <h4>🎓 Studies</h4>
                    <p>Master of Economics with Distinction at NUS</p>
                </div>
                <div class="skill-item" style="background: linear-gradient(135deg, #27ae60, #229954);">
                    <h4>🌍 Leadership</h4>
                    <p>Vice-Chairman of LPDP Singapore community</p>
                </div>
            </div>
        </div>

        <!-- Inspirational Quote -->
        <div class="quote">
            <p>"Economics is not just about numbers—it's about understanding human behavior and creating positive impact."</p>
            <p style="font-size: 1rem; opacity: 0.8;">- Habib Furqony Andrianus</p>
        </div>

        <!-- Contact Section -->
        <div class="card">
            <h2>🤝 Let's Connect!</h2>
            <div class="contact-links">
                <a href="https://www.linkedin.com/in/habibandrianus/" class="contact-link">
                    <span>💼</span> LinkedIn
                </a>
                <a href="mailto:andrianus_habib@u.nus.edu" class="contact-link">
                    <span>📧</span> Email
                </a>
                <a href="https://instagram.com/andrianushabib" class="contact-link">
                    <span>📸</span> Instagram
                </a>
            </div>
            <p style="text-align: center; margin-top: 30px; font-style: italic; color: #666;">
                Thanks for visiting my profile! Let's collaborate on impactful research and analytics projects! 🚀
            </p>
        </div>
    </div>

    <script>
        // Create animated particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 20 + 's';
                particle.style.animationDuration = (Math.random() * 10 + 15) + 's';
                particlesContainer.appendChild(particle);
            }
        }

        // Typing animation
        function typeWriter() {
            const texts = [
                'Economist & Data Scientist',
                'NUS Master\'s Student',
                'Research & Analytics Expert',
                'Teaching Assistant',
                'Experienced FMCG Professional'
            ];
            
            const typingElement = document.getElementById('typing');
            let textIndex = 0;
            let charIndex = 0;
            let isDeleting = false;
            
            function type() {
                const currentText = texts[textIndex];
                
                if (isDeleting) {
                    typingElement.textContent = currentText.substring(0, charIndex - 1);
                    charIndex--;
                } else {
                    typingElement.textContent = currentText.substring(0, charIndex + 1);
                    charIndex++;
                }
                
                let typeSpeed = isDeleting ? 50 : 100;
                
                if (!isDeleting && charIndex === currentText.length) {
                    typeSpeed = 2000;
                    isDeleting = true;
                } else if (isDeleting && charIndex === 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % texts.length;
                    typeSpeed = 500;
                }
                
                setTimeout(type, typeSpeed);
            }
            
            type();
        }

        // Intersection Observer for animations
        function observeElements() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animationPlayState = 'running';
                    }
                });
            });

            document.querySelectorAll('.card').forEach(card => {
                observer.observe(card);
            });
        }

        // Initialize everything
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            typeWriter();
            observeElements();
        });

        // Add smooth scrolling
        document.documentElement.style.scrollBehavior = 'smooth';
    </script>
</body>
</html>
