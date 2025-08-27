# username.github.io
web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FortifyOps - Security Work Operations Made Simple</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-dark: #0f172a;
            --primary-blue: #0066ff;
            --primary-blue-hover: #0052cc;
            --text-dark: #1e293b;
            --text-light: #64748b;
            --bg-light: #f8fafc;
            --bg-white: #ffffff;
            --accent-gradient: linear-gradient(135deg, #0066ff 0%, #00d4ff 100%);
            --success-green: #10b981;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            scroll-behavior: smooth;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            padding: 1rem 0;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-dark);
        }

        .nav-links {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .nav-cta {
            background: var(--primary-blue);
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .nav-cta:hover {
            background: var(--primary-blue-hover);
            transform: translateY(-2px);
        }

        .nav-secondary {
            color: var(--primary-blue);
            padding: 0.75rem 1.5rem;
            text-decoration: none;
            font-weight: 600;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            padding: 4rem 2rem 3rem;
            background: linear-gradient(to bottom, #ffffff, #f8fafc);
            text-align: center;
        }

        .hero-content {
            max-width: 900px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            color: var(--primary-dark);
        }

        .hero-highlight {
            background: var(--accent-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-subtitle {
            font-size: 1.375rem;
            color: var(--text-light);
            margin-bottom: 2.5rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-cta {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .primary-btn {
            background: var(--primary-blue);
            color: white;
            padding: 1rem 2rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.125rem;
            transition: all 0.3s ease;
        }

        .primary-btn:hover {
            background: var(--primary-blue-hover);
            transform: translateY(-2px);
        }

        .secondary-btn {
            background: transparent;
            color: var(--primary-blue);
            padding: 1rem 2rem;
            border: 2px solid var(--primary-blue);
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.125rem;
            transition: all 0.3s ease;
        }

        .secondary-btn:hover {
            background: var(--primary-blue);
            color: white;
        }

        /* Metrics Bar */
        .metrics-bar {
            display: flex;
            justify-content: center;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .metric-item {
            text-align: center;
        }

        .metric-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-blue);
            display: block;
        }

        .metric-label {
            font-size: 0.875rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Benefits Ticker */
        .benefits-ticker {
            background: var(--primary-dark);
            color: white;
            padding: 1rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker-content {
            display: inline-block;
            padding-left: 100%;
            animation: ticker 30s linear infinite;
        }

        .ticker-item {
            display: inline;
            padding: 0 3rem;
            font-weight: 500;
        }

        @keyframes ticker {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-100%, 0); }
        }

        /* Simple Steps */
        .steps-section {
            padding: 4rem 2rem;
            background: white;
        }

        .section-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title {
            font-size: 2.25rem;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        .section-subtitle {
            color: var(--text-light);
            font-size: 1.125rem;
        }

        .steps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .step-card {
            background: var(--bg-light);
            padding: 2rem;
            border-radius: 1rem;
            text-align: center;
        }

        .step-number {
            width: 50px;
            height: 50px;
            background: var(--accent-gradient);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0 auto 1rem;
        }

        .step-card h3 {
            font-size: 1.25rem;
            margin-bottom: 0.75rem;
            color: var(--primary-dark);
        }

        .step-card p {
            color: var(--text-light);
        }

        /* Comparison */
        .comparison-section {
            padding: 4rem 2rem;
            background: var(--bg-light);
        }

        .comparison-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            max-width: 900px;
            margin: 0 auto;
        }

        .comparison-card {
            background: white;
            padding: 2rem;
            border-radius: 1rem;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        .comparison-card.without {
            border: 2px solid #fee2e2;
        }

        .comparison-card.with {
            border: 2px solid #d1fae5;
        }

        .comparison-card h3 {
            font-size: 1.25rem;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        .comparison-card ul {
            list-style: none;
            padding: 0;
        }

        .comparison-card li {
            padding: 0.5rem 0;
            color: var(--text-light);
            display: flex;
            align-items: flex-start;
        }

        .comparison-card li::before {
            margin-right: 0.5rem;
            flex-shrink: 0;
        }

        .comparison-card.without li::before {
            content: "✗";
            color: #ef4444;
        }

        .comparison-card.with li::before {
            content: "✓";
            color: var(--success-green);
        }

        /* For Teams */
        .teams-section {
            padding: 4rem 2rem;
            background: white;
        }

        .teams-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            max-width: 1000px;
            margin: 0 auto;
        }

        .team-card {
            padding: 2rem;
        }

        .team-card h3 {
            font-size: 1.75rem;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        .team-card p {
            color: var(--text-light);
            margin-bottom: 1.5rem;
        }

        .team-card ul {
            list-style: none;
            padding: 0;
        }

        .team-card li {
            padding: 0.5rem 0;
            color: var(--text-dark);
            display: flex;
            align-items: flex-start;
        }

        .team-card li::before {
            content: "•";
            color: var(--primary-blue);
            margin-right: 0.75rem;
            font-weight: bold;
        }

        /* Vision */
        .vision-section {
            padding: 4rem 2rem;
            background: var(--bg-light);
            text-align: center;
        }

        .vision-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .vision-content h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        .vision-text {
            font-size: 1.5rem;
            color: var(--primary-blue);
            font-weight: 600;
            font-style: italic;
            margin-bottom: 2rem;
        }

        .mission-text {
            color: var(--text-light);
            font-size: 1.125rem;
            line-height: 1.8;
        }

        /* CTA Section */
        .cta-section {
            padding: 5rem 2rem;
            background: var(--primary-dark);
            text-align: center;
            color: white;
        }

        .cta-content h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .cta-content p {
            font-size: 1.25rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .cta-white {
            background: white;
            color: var(--primary-blue);
            padding: 1rem 2rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.125rem;
            transition: all 0.3s ease;
        }

        .cta-white:hover {
            transform: translateY(-2px);
        }

        .cta-outline {
            background: transparent;
            color: white;
            border: 2px solid white;
            padding: 1rem 2rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.125rem;
            transition: all 0.3s ease;
        }

        .cta-outline:hover {
            background: white;
            color: var(--primary-dark);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .comparison-grid,
            .teams-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-cta,
            .cta-buttons {
                flex-direction: column;
                width: 100%;
                max-width: 300px;
                margin: 0 auto;
            }
            
            .primary-btn,
            .secondary-btn,
            .cta-white,
            .cta-outline {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">FortifyOps</div>
            <div class="nav-links">
                <a href="#partnership" class="nav-secondary">Join Partnership</a>
                <a href="#access" class="nav-cta">Request Early Access</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Security Work Operations<br><span class="hero-highlight">Made Simple</span></h1>
            <p class="hero-subtitle">Connect security requests to the right people and resources at the right time. Get faster, consistent and quality structured resolutions while showing your value clearly.</p>
            <div class="hero-cta">
                <a href="#access" class="primary-btn">Request Early Access</a>
                <a href="#partnership" class="secondary-btn">Join Partnership</a>
            </div>
            <div class="metrics-bar">
                <div class="metric-item">
                    <span class="metric-value">Smart</span>
                    <span class="metric-label">Request Routing</span>
                </div>
                <div class="metric-item">
                    <span class="metric-value">70%</span>
                    <span class="metric-label">Faster Resolutions</span>
                </div>
                <div class="metric-item">
                    <span class="metric-value">High-Precision</span>
                    <span class="metric-label">Expert Matching</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Ticker -->
    <section class="benefits-ticker">
        <div class="ticker-content">
            <span class="ticker-item">• Serve Intently</span>
            <span class="ticker-item">• Govern Smarter</span>
            <span class="ticker-item">• Scale Intelligently</span>
            <span class="ticker-item">• Expand Capabilities</span>
            <span class="ticker-item">• Justify Clearly</span>
            <span class="ticker-item">• Accelerate Business</span>
            <span class="ticker-item">• Serve Intently</span>
            <span class="ticker-item">• Govern Smarter</span>
            <span class="ticker-item">• Scale Intelligently</span>
            <span class="ticker-item">• Expand Capabilities</span>
            <span class="ticker-item">• Justify Clearly</span>
            <span class="ticker-item">• Accelerate Business</span>
        </div>
    </section>

    <!-- Simple Steps Section -->
    <section class="steps-section">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">Simple as 1-2-3</h2>
                <p class="section-subtitle">Our operational strength: connecting security work to the best people and resources with full business context for faster, consistent, and quality structured resolutions.</p>
            </div>
            <div class="steps-grid">
                <div class="step-card">
                    <div class="step-number">1</div>
                    <h3>Capture & Route Intelligently</h3>
                    <p>Security requests come from everywhere. We capture them all and instantly route to the right expert based on type, urgency, and expertise needed.</p>
                </div>
                <div class="step-card">
                    <div class="step-number">2</div>
                    <h3>Execute & Govern</h3>
                    <p>Workspaces collect business context from your existing systems, facilitate resolution, and maintain complete records. Every action tracked with full organizational context.</p>
                </div>
                <div class="step-card">
                    <div class="step-number">3</div>
                    <h3>Tell Your Story</h3>
                    <p>Insights transforms your work into compelling narratives. Show what happened, predict what's coming, and prove your value clearly.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section class="comparison-section">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">The Power of Right Connections</h2>
                <p class="section-subtitle">Your security requests are complex. Getting them to the right person with the right context for consistent, structured deliverables shouldn't be.</p>
            </div>
            <div class="comparison-grid">
                <div class="comparison-card without">
                    <h3>Without FortifyOps</h3>
                    <ul>
                        <li>Requests get lost in Email, Slack, Teams, Jira, Zendesk etc.</li>
                        <li>Wrong person handles critical issues</li>
                        <li>Expertise sits idle while work piles up</li>
                        <li>Response times measured in days</li>
                        <li>Inconsistent deliverables and resolution formats</li>
                        <li>No business context from existing systems</li>
                    </ul>
                </div>
                <div class="comparison-card with">
                    <h3>With FortifyOps</h3>
                    <ul>
                        <li>Every request tracked and routed instantly</li>
                        <li>Intelligent matching of work to best available expert</li>
                        <li>Resources utilized based on real expertise</li>
                        <li>Response times measured in minutes</li>
                        <li>Consistent, structured deliverables every time</li>
                        <li>Full business context from integrated systems</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- For Teams Section -->
    <section class="teams-section">
        <div class="section-container">
            <div class="section-header">
                <h2 class="section-title">Built for Teams Like Yours</h2>
                <p class="section-subtitle">Whether you're protecting your company or helping others protect theirs, we've got you covered.</p>
            </div>
            <div class="teams-grid">
                <div class="team-card">
                    <h3>For Security Teams</h3>
                    <p>Get ahead of business decisions by understanding stakeholder priorities early. Stop losing critical security conversations across emails, Slack/Teams, tickets, and project documents.</p>
                    <ul>
                        <li>Timely engage with business requests and insights before critical decisions are made</li>
                        <li>Enable identification of true business intent upfront</li>
                        <li>Match the right skills and talent to each security challenge</li>
                        <li>Better collaboration integration with your business stakeholders</li>
                    </ul>
                </div>
                <div class="team-card">
                    <h3>For Security Providers</h3>
                    <p>Turn dormant capacity into revenue by getting discovered by organizations actively seeking your expertise. Understand what businesses actually need to reduce acquisition costs.</p>
                    <ul>
                        <li>Get promoted to businesses actively seeking your specific expertise</li>
                        <li>Fill capacity gaps with opportunities that match your capabilities</li>
                        <li>Lower acquisition costs by targeting pre-qualified opportunities</li>
                        <li>Build reputation and lifetime value through proven outcomes</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Vision Section -->
    <section class="vision-section">
        <div class="vision-content">
            <h2>Our North Star</h2>
            <p class="vision-text">"Bring clarity and confidence to every information security guardian to protect and prosper"</p>
            <p class="mission-text">Help create a world where information security professionals bring clarity to their clients and confidence to their practice, transforming overwhelming compliance into simple protection that works.</p>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section" id="access">
        <div class="cta-content">
            <h2>Ready to Make Security Simple?</h2>
            <p>Be among the first to experience a better way to do security governance.</p>
            <div class="cta-buttons">
                <a href="#" class="cta-white">Request Early Access</a>
                <a href="#partnership" class="cta-outline">Join Partnership</a>
            </div>
        </div>
    </section>
</body>
</html>
