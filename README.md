<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stellar README</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            padding: 40px 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .header h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #fff, #a8edea);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 3s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% { filter: drop-shadow(0 0 20px rgba(255, 255, 255, 0.5)); }
            50% { filter: drop-shadow(0 0 40px rgba(255, 255, 255, 0.8)); }
        }

        .tagline {
            font-size: 1.3em;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 30px;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
            margin: 20px 0;
        }

        .badge {
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9em;
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
        }

        .badge:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .section {
            margin: 40px 0;
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 20px;
            position: relative;
            padding-left: 20px;
        }

        .section h2:before {
            content: '';
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 5px;
            height: 30px;
            background: linear-gradient(180deg, #fff, #a8edea);
            border-radius: 5px;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .feature-card {
            background: rgba(255, 255, 255, 0.15);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .feature-card:hover {
            transform: translateY(-5px) scale(1.02);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .feature-card h3 {
            font-size: 1.5em;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .icon {
            font-size: 1.8em;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 12px 20px;
            border-radius: 10px;
            font-weight: 600;
            border: 2px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
        }

        .tech-item:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.1) rotate(2deg);
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1em;
            margin: 10px;
            border: 2px solid rgba(255, 255, 255, 0.4);
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            background: linear-gradient(45deg, #764ba2, #667eea);
        }

        .stats {
            display: flex;
            justify-content: space-around;
            margin: 40px 0;
            flex-wrap: wrap;
            gap: 20px;
        }

        .stat-item {
            text-align: center;
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            flex: 1;
            min-width: 150px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            background: linear-gradient(45deg, #fff, #a8edea);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            font-size: 1em;
            color: rgba(255, 255, 255, 0.8);
            margin-top: 10px;
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }

        .social-link {
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .social-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.2) rotate(360deg);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>✨ Project Stellar ✨</h1>
            <p class="tagline">Building the future, one commit at a time</p>
            <div class="badges">
                <span class="badge">⭐ MIT License</span>
                <span class="badge">🚀 v2.0.0</span>
                <span class="badge">💚 Open Source</span>
                <span class="badge">🔥 Active</span>
            </div>
        </div>

        <div class="stats">
            <div class="stat-item">
                <div class="stat-number">1.2K</div>
                <div class="stat-label">Stars</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">340</div>
                <div class="stat-label">Forks</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">50+</div>
                <div class="stat-label">Contributors</div>
            </div>
        </div>

        <div class="section">
            <h2>🎯 About</h2>
            <p>Project Stellar is a revolutionary open-source platform designed to empower developers worldwide. With cutting-edge features and a vibrant community, we're redefining what's possible in modern software development.</p>
        </div>

        <div class="section">
            <h2>✨ Features</h2>
            <div class="features">
                <div class="feature-card">
                    <h3><span class="icon">⚡</span> Lightning Fast</h3>
                    <p>Optimized performance with blazing-fast load times and minimal footprint.</p>
                </div>
                <div class="feature-card">
                    <h3><span class="icon">🎨</span> Beautiful UI</h3>
                    <p>Modern, intuitive design that delights users at every interaction.</p>
                </div>
                <div class="feature-card">
                    <h3><span class="icon">🔒</span> Secure</h3>
                    <p>Enterprise-grade security with industry-standard encryption.</p>
                </div>
                <div class="feature-card">
                    <h3><span class="icon">🌐</span> Scalable</h3>
                    <p>Built to grow with your needs from startup to enterprise.</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🛠️ Tech Stack</h2>
            <div class="tech-stack">
                <span class="tech-item">React</span>
                <span class="tech-item">Node.js</span>
                <span class="tech-item">TypeScript</span>
                <span class="tech-item">MongoDB</span>
                <span class="tech-item">Docker</span>
                <span class="tech-item">AWS</span>
            </div>
        </div>

        <div class="section">
            <h2>🚀 Quick Start</h2>
            <p>Get up and running in seconds:</p>
            <div style="background: rgba(0,0,0,0.3); padding: 20px; border-radius: 10px; margin-top: 20px; font-family: monospace;">
                <p>$ git clone https://github.com/yourusername/project-stellar.git</p>
                <p>$ cd project-stellar</p>
                <p>$ npm install</p>
                <p>$ npm start</p>
            </div>
        </div>

        <div class="section" style="text-align: center;">
            <h2>💫 Get Involved</h2>
            <p style="margin-bottom: 30px;">Join our growing community and help shape the future!</p>
            <a href="#" class="cta-button">⭐ Star on GitHub</a>
            <a href="#" class="cta-button">📖 Read Docs</a>
            <a href="#" class="cta-button">🤝 Contribute</a>
        </div>

        <div class="footer">
            <div class="social-links">
                <div class="social-link">🐦</div>
                <div class="social-link">💼</div>
                <div class="social-link">💬</div>
                <div class="social-link">📧</div>
            </div>
            <p>Made with ❤️ by developers, for developers</p>
            <p style="margin-top: 10px; color: rgba(255,255,255,0.6);">© 2025 Project Stellar. All rights reserved.</p>
        </div>
    </div>
</body>
</html>
