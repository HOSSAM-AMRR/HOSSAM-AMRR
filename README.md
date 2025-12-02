<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hossam Amr - Data Analyst & Data Scientist</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 900px;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 30px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            padding: 60px;
            animation: slideIn 0.8s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-10px);
            }
        }

        h1 {
            font-size: 3rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            animation: fadeIn 1s ease-out 0.3s both;
        }

        .subtitle {
            font-size: 1.5rem;
            color: #666;
            margin-bottom: 15px;
            animation: fadeIn 1s ease-out 0.5s both;
        }

        .tagline {
            font-size: 1.1rem;
            color: #888;
            font-style: italic;
            animation: fadeIn 1s ease-out 0.7s both;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .code-block {
            background: #1e1e1e;
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
            font-family: 'Courier New', monospace;
            color: #d4d4d4;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
            animation: slideInLeft 1s ease-out 0.9s both;
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .code-header {
            display: flex;
            gap: 8px;
            margin-bottom: 20px;
        }

        .code-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .dot-red { background: #ff5f56; }
        .dot-yellow { background: #ffbd2e; }
        .dot-green { background: #27c93f; }

        .code-line {
            margin: 8px 0;
            line-height: 1.6;
        }

        .keyword { color: #c586c0; }
        .function { color: #dcdcaa; }
        .string { color: #ce9178; }
        .comment { color: #6a9955; }
        .variable { color: #9cdcfe; }
        .number { color: #b5cea8; }

        .typing-cursor {
            display: inline-block;
            width: 2px;
            height: 1em;
            background: #d4d4d4;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
            animation: fadeInUp 1s ease-out 1.1s both;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .stat-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            color: white;
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 10px;
            display: block;
        }

        .stat-label {
            font-size: 1rem;
            opacity: 0.9;
        }

        .skills-section {
            margin: 40px 0;
            animation: fadeIn 1s ease-out 1.3s both;
        }

        .section-title {
            font-size: 2rem;
            color: #333;
            margin-bottom: 30px;
            text-align: center;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .skill-card {
            background: white;
            border: 2px solid #e0e0e0;
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s;
        }

        .skill-card:hover {
            border-color: #667eea;
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.2);
        }

        .skill-card h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .skill-item {
            background: linear-gradient(135deg, #667eea15 0%, #764ba215 100%);
            padding: 10px 15px;
            border-radius: 8px;
            margin: 8px 0;
            font-weight: 500;
            color: #333;
            transition: all 0.3s;
        }

        .skill-item:hover {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            transform: translateX(5px);
        }

        .contact-section {
            margin-top: 50px;
            text-align: center;
            animation: fadeIn 1s ease-out 1.5s both;
        }

        .contact-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .btn {
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            font-size: 1rem;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.5);
        }

        .btn-secondary {
            background: white;
            color: #667eea;
            border: 2px solid #667eea;
        }

        .btn-secondary:hover {
            background: #667eea;
            color: white;
        }

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
            background: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            animation: float-particle 15s infinite;
        }

        @keyframes float-particle {
            0%, 100% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 30px;
            }

            h1 {
                font-size: 2rem;
            }

            .subtitle {
                font-size: 1.2rem;
            }

            .code-block {
                padding: 20px;
                font-size: 0.9rem;
            }

            .stat-card {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>

    <div class="container">
        <div class="header">
            <div class="profile-image">👨‍💻</div>
            <h1>Hossam Amr</h1>
            <div class="subtitle">Data Analyst & Data Scientist</div>
            <div class="tagline">Turning complex data into clear, actionable business insights</div>
        </div>

        <div class="code-block">
            <div class="code-header">
                <div class="code-dot dot-red"></div>
                <div class="code-dot dot-yellow"></div>
                <div class="code-dot dot-green"></div>
            </div>
            <div class="code-line"><span class="keyword">class</span> <span class="function">DataScientist</span>:</div>
            <div class="code-line">    <span class="keyword">def</span> <span class="function">__init__</span>(<span class="variable">self</span>):</div>
            <div class="code-line">        <span class="variable">self</span>.name = <span class="string">"Hossam Amr"</span></div>
            <div class="code-line">        <span class="variable">self</span>.role = <span class="string">"Data Analyst & Data Scientist"</span></div>
            <div class="code-line">        <span class="variable">self</span>.location = <span class="string">"Beni Suweif, Egypt"</span></div>
            <div class="code-line">        <span class="variable">self</span>.languages = [<span class="string">"Python"</span>, <span class="string">"SQL"</span>, <span class="string">"R"</span>]</div>
            <div class="code-line">        <span class="variable">self</span>.expertise = [</div>
            <div class="code-line">            <span class="string">"Data Analysis & Visualization"</span>,</div>
            <div class="code-line">            <span class="string">"Machine Learning & AI"</span>,</div>
            <div class="code-line">            <span class="string">"Statistical Modeling"</span>,</div>
            <div class="code-line">            <span class="string">"Business Intelligence"</span></div>
            <div class="code-line">        ]</div>
            <div class="code-line"></div>
            <div class="code-line">    <span class="keyword">def</span> <span class="function">say_hi</span>(<span class="variable">self</span>):</div>
            <div class="code-line">        <span class="keyword">return</span> <span class="string">"Thanks for visiting! Let's transform data into insights."</span></div>
            <div class="code-line"></div>
            <div class="code-line"><span class="comment"># Create instance</span></div>
            <div class="code-line"><span class="variable">me</span> = <span class="function">DataScientist</span>()</div>
            <div class="code-line"><span class="keyword">print</span>(<span class="variable">me</span>.<span class="function">say_hi</span>())<span class="typing-cursor"></span></div>
        </div>

        <div class="stats-grid">
            <div class="stat-card">
                <span class="stat-number">5+</span>
                <span class="stat-label">Years Experience</span>
            </div>
            <div class="stat-card">
                <span class="stat-number">50+</span>
                <span class="stat-label">Projects Completed</span>
            </div>
            <div class="stat-card">
                <span class="stat-number">15+</span>
                <span class="stat-label">Tools Mastered</span>
            </div>
        </div>

        <div class="skills-section">
            <h2 class="section-title">🎯 Core Expertise</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>📊 Data Analysis</h3>
                    <div class="skill-item">Python (Advanced)</div>
                    <div class="skill-item">SQL (Expert)</div>
                    <div class="skill-item">R (Advanced)</div>
                    <div class="skill-item">Excel (Advanced)</div>
                </div>

                <div class="skill-card">
                    <h3>📈 Visualization</h3>
                    <div class="skill-item">Power BI (Expert)</div>
                    <div class="skill-item">Tableau (Expert)</div>
                    <div class="skill-item">Plotly</div>
                    <div class="skill-item">Matplotlib & Seaborn</div>
                </div>

                <div class="skill-card">
                    <h3>🤖 Machine Learning</h3>
                    <div class="skill-item">Scikit-learn</div>
                    <div class="skill-item">TensorFlow</div>
                    <div class="skill-item">PyTorch</div>
                    <div class="skill-item">Statistical Modeling</div>
                </div>

                <div class="skill-card">
                    <h3>☁️ Cloud & Databases</h3>
                    <div class="skill-item">Azure</div>
                    <div class="skill-item">MySQL</div>
                    <div class="skill-item">PostgreSQL</div>
                    <div class="skill-item">MongoDB</div>
                </div>
            </div>
        </div>

        <div class="contact-section">
            <h2 class="section-title">📫 Let's Connect</h2>
            <p style="color: #666; font-size: 1.1rem; margin-bottom: 20px;">
                Open to Data Analyst & Data Scientist opportunities
            </p>
            <div class="contact-buttons">
                <a href="https://portfolio-for-hossam.vercel.app/" class="btn btn-primary" target="_blank">
                    🌐 View Portfolio
                </a>
                <a href="https://www.linkedin.com/in/hossamamr2002/" class="btn btn-secondary" target="_blank">
                    💼 LinkedIn
                </a>
                <a href="mailto:hossam.amr2710@gmail.com" class="btn btn-secondary">
                    📧 Email Me
                </a>
            </div>
        </div>
    </div>

    <script>
        // Create floating particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 15 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
            particlesContainer.appendChild(particle);
        }

        // Add click animation to stat cards
        document.querySelectorAll('.stat-card').forEach(card => {
            card.addEventListener('click', function() {
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = 'translateY(-10px) scale(1.05)';
                }, 100);
            });
        });

        // Smooth scroll for any internal links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
