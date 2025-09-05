<!DOCTYPE html>
<html lang="ar" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Oskar - AI Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #7e22ce;
            --accent: #06b6d4;
            --dark: #0f172a;
            --light: #f8fafc;
            --gradient: linear-gradient(135deg, var(--primary), var(--secondary));
            --card-bg: rgba(255, 255, 255, 0.05);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--dark);
            color: var(--light);
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        header {
            text-align: center;
            padding: 40px 0;
            background: var(--card-bg);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            margin-bottom: 20px;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
        }
        
        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 20px;
            border: 4px solid var(--primary);
            background: linear-gradient(45deg, #64FFDA, #009688);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            transition: var(--transition);
        }
        
        .avatar:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px var(--accent);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #94a3b8;
        }
        
        .typing-container {
            height: 60px;
            overflow: hidden;
            position: relative;
            margin: 20px 0;
        }
        
        .typing-text {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            text-align: center;
            opacity: 0;
            animation: typing 4s infinite;
        }
        
        .typing-text:nth-child(2) {
            animation-delay: 4s;
        }
        
        .typing-text:nth-child(3) {
            animation-delay: 8s;
        }
        
        .typing-text:nth-child(4) {
            animation-delay: 12s;
        }
        
        @keyframes typing {
            0%, 100% { opacity: 0; }
            10%, 90% { opacity: 1; }
        }
        
        .section {
            background-color: var(--card-bg);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(10px);
            transition: var(--transition);
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(37, 99, 235, 0.2);
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title i {
            color: var(--primary);
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .skill-category {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            transition: var(--transition);
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(54, 188, 247, 0.2);
        }
        
        .skill-category h3 {
            margin-bottom: 15px;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .badge {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            transition: var(--transition);
        }
        
        .badge:hover {
            background: var(--primary);
            transform: scale(1.05);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
            position: relative;
        }
        
        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--gradient);
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-description {
            color: #94a3b8;
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        
        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
            transition: gap 0.3s ease;
        }
        
        .project-link:hover {
            gap: 10px;
        }
        
        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-around;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            min-width: 200px;
            flex: 1;
            transition: var(--transition);
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(54, 188, 247, 0.2);
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 25px;
            background: var(--gradient);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            transition: var(--transition);
        }
        
        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(54, 188, 247, 0.4);
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .quote {
            font-style: italic;
            border-left: 3px solid var(--primary);
            padding-left: 15px;
            margin: 20px 0;
        }
        
        @media (max-width: 768px) {
            .skills-grid, .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                flex-direction: column;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
        }
        
        /* تأثيرات إضافية */
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .glow {
            text-shadow: 0 0 10px var(--primary), 0 0 20px var(--primary), 0 0 30px var(--primary);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="avatar pulse">O</div>
            <h1>Oskar</h1>
            <p class="tagline">AI Engineer & Software Developer</p>
            
            <div class="typing-container">
                <div class="typing-text">AI Engineer | ML & DL Specialist</div>
                <div class="typing-text">NLP & Computer Vision Developer</div>
                <div class="typing-text">Data Scientist | MLOps Enthusiast</div>
                <div class="typing-text">Open Source Contributor | Problem Solver</div>
            </div>
            
            <p>أبني أنظمة ذكية تستطيع التعلم، الفهم، واتخاذ القرارات</p>
        </header>
        
        <section class="section">
            <h2 class="section-title">
                <i class="fas fa-brain"></i> Areas of Expertise
            </h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-robot"></i> Machine Learning (ML)</h3>
                    <p>التنبؤ، التصنيف، التجميع، النماذج الإحصائية</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-layer-group"></i> Deep Learning (DL)</h3>
                    <p>CNN, RNN, LSTM, Transformers</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-language"></i> Natural Language Processing (NLP)</h3>
                    <p>Chatbots, Sentiment Analysis, Summarization, LLMs</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-eye"></i> Computer Vision (CV)</h3>
                    <p>Face Detection, Emotion Recognition, Image & Video Analysis</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-cogs"></i> MLOps & Deployment</h3>
                    <p>Model optimization, CI/CD, FastAPI, Docker, AWS/GCP</p>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-chart-bar"></i> Big Data Analytics</h3>
                    <p>Pandas, NumPy, Spark for knowledge extraction</p>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <i class="fas fa-tools"></i> Skills & Tools
            </h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-code"></i> Programming Languages</h3>
                    <div class="badges">
                        <span class="badge"><i class="fab fa-python"></i> Python</span>
                        <span class="badge"><i class="fab fa-r-project"></i> R</span>
                        <span class="badge"><i class="fab fa-java"></i> Java</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-network-wired"></i> ML/DL Frameworks</h3>
                    <div class="badges">
                        <span class="bad
