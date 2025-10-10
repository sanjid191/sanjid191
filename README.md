<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub README</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            padding: 40px 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .title {
            font-size: 3.5em;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            animation: fadeInDown 1s ease-out;
        }

        .subtitle {
            font-size: 1.3em;
            color: #666;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .wave {
            display: inline-block;
            animation: wave 2s infinite;
            transform-origin: 70% 70%;
            font-size: 1.2em;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            40% { transform: rotate(-4deg); }
            50% { transform: rotate(10deg); }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
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

        .section {
            margin: 40px 0;
            animation: fadeIn 1s ease-out 0.6s both;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        h2 {
            font-size: 2em;
            color: #333;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 2px;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .tech-badge {
            padding: 12px 24px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 30px;
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .tech-badge:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.4);
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .stat-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            color: #666;
            margin-top: 10px;
            font-size: 1.1em;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5em;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
            text-decoration: none;
        }

        .social-btn:hover {
            transform: rotate(360deg) scale(1.2);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.5);
        }

        .highlight {
            background: linear-gradient(135deg, #667eea20 0%, #764ba220 100%);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #667eea;
            margin: 20px 0;
        }

        .typing-text {
            font-family: 'Courier New', monospace;
            color: #333;
            font-size: 1.1em;
        }

        .cursor {
            display: inline-block;
            width: 3px;
            height: 1.2em;
            background: #667eea;
            margin-left: 5px;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            color: #666;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="title">Hi there! <span class="wave">👋</span></h1>
            <p class="subtitle">I'm a Passionate Developer & Creative Problem Solver</p>
        </div>

        <div class="section">
            <h2>🚀 About Me</h2>
            <div class="highlight">
                <p class="typing-text">const developer = {
    name: "Your Name",
    role: "Full Stack Developer",
    location: "Your Location",
    passion: "Building amazing things with code"
};<span class="cursor"></span></p>
            </div>
            <p style="margin-top: 20px; color: #555; line-height: 1.8;">
                I'm a developer who loves turning ideas into reality through clean, efficient code. 
                Currently focused on building scalable web applications and exploring new technologies. 
                Always learning, always growing! 🌱
            </p>
        </div>

        <div class="section">
            <h2>💻 Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-badge">JavaScript</div>
                <div class="tech-badge">React</div>
                <div class="tech-badge">Node.js</div>
                <div class="tech-badge">Python</div>
                <div class="tech-badge">TypeScript</div>
                <div class="tech-badge">Docker</div>
                <div class="tech-badge">MongoDB</div>
                <div class="tech-badge">Git</div>
            </div>
        </div>

        <div class="section">
            <h2>📊 GitHub Stats</h2>
            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">50+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1000+</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">15+</div>
                    <div class="stat-label">Contributions</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🌟 Featured Projects</h2>
            <div style="margin-top: 20px;">
                <div class="highlight" style="margin-bottom: 15px;">
                    <h3 style="color: #667eea; margin-bottom: 10px;">🎯 Project Alpha</h3>
                    <p style="color: #555;">A revolutionary app that does amazing things. Built with React and Node.js.</p>
                </div>
                <div class="highlight">
                    <h3 style="color: #764ba2; margin-bottom: 10px;">🔥 Project Beta</h3>
                    <p style="color: #555;">An innovative solution for modern problems. Powered by AI and machine learning.</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🤝 Connect With Me</h2>
            <div class="social-links">
                <a href="#" class="social-btn">💼</a>
                <a href="#" class="social-btn">🐦</a>
                <a href="#" class="social-btn">📧</a>
                <a href="#" class="social-btn">🔗</a>
            </div>
        </div>

        <div class="footer">
            <p>⭐ Star my repos if you find them interesting! | 📫 Always open to collaborate</p>
            <p style="margin-top: 10px;">Made with ❤️ and lots of ☕</p>
        </div>
    </div>
</body>
</html>
