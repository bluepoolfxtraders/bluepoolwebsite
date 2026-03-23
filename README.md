<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BLEZOFX | Forex Trading Hub</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;900&display=swap" rel="stylesheet">
<style>
:root {
    --bg-dark: #101012;
    --panel-dark: #141619;
    --section-bg: #1A1C1F;
    --accent-cyan: #00E5FF;
    --accent-orange: #FF8F00;
    --text-white: #FFFFFF;
    --text-grey: #B0BEC5;
    --transition-speed: 0.4s;
}
* { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Poppins', sans-serif; }
body { background: var(--bg-dark); color: var(--text-white); line-height: 1.5; }
a { text-decoration: none; color: inherit; }
button { cursor: pointer; }

/* Header */
header { display: flex; justify-content: space-between; align-items: center; padding: 15px 30px; background: var(--panel-dark); position: sticky; top: 0; z-index: 1000; width: 100%; }
header .logo { display: flex; align-items: center; gap: 10px; color: var(--accent-cyan); font-weight: 900; font-size: 1.5rem; }
header nav { display: flex; gap: 25px; flex-wrap: wrap; }
header nav a { color: var(--text-white); font-weight: 500; transition: color var(--transition-speed); }
header nav a:hover { color: var(--accent-cyan); }
header .actions { display: flex; gap: 10px; flex-wrap: wrap; }
header .actions .login { border: 1px solid var(--accent-cyan); padding: 8px 16px; border-radius: 8px; color: var(--accent-cyan); transition: 0.3s; animation: glow 1.5s infinite alternate; }
header .actions .login:hover { background: var(--accent-cyan); color: var(--text-white); }
header .actions .start { background: var(--accent-orange); padding: 8px 16px; border-radius: 8px; font-weight: 700; transition: 0.3s; animation: glow 1.5s infinite alternate; }
header .actions .start:hover { opacity: 0.9; }

/* Glow animation for buttons */
@keyframes glow {
    0% { box-shadow: 0 0 5px var(--accent-cyan); }
    50% { box-shadow: 0 0 20px var(--accent-cyan); }
    100% { box-shadow: 0 0 5px var(--accent-cyan); }
}

/* Hero Section */
.hero { display: flex; flex-wrap: wrap; align-items: center; justify-content: center; padding: 60px 30px; background: var(--panel-dark); gap: 30px; position: relative; overflow: hidden; border-bottom: 1px solid rgba(0,229,255,0.1); }
.hero::before { content: ''; position: absolute; top:0; left:0; width:100%; height:100%; background: url('https://i.ibb.co/3z3QjZP/trader-desk.png') no-repeat center/cover; opacity: 0.05; z-index:0; }
.hero .hero-left { flex: 1; min-width: 300px; z-index:1; text-align: center; }
.hero .hero-left h1 { font-size: 2.5rem; margin-bottom: 10px; background: linear-gradient(90deg, #00E5FF, #FF8F00); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
.hero .hero-left p { font-size: 1.1rem; color: var(--text-grey); margin-bottom: 20px; }
.hero .hero-left .ticker { display: flex; gap: 10px; padding: 10px; border: 1px solid var(--accent-cyan); border-radius: 10px; overflow-x: auto; margin-bottom: 20px; justify-content: center; }
.ticker div { min-width: 80px; padding: 5px 10px; border-radius: 6px; text-align: center; background: rgba(0,229,255,0.05); color: var(--accent-cyan); font-weight: 600; }
.hero .hero-left .cta { display: flex; gap: 15px; flex-wrap: wrap; justify-content: center; }
.hero .hero-left .cta a { padding: 12px 25px; border-radius: 8px; font-weight: 700; transition: 0.3s; animation: glow 1.5s infinite alternate; }
.hero .hero-left .cta .account { background: var(--accent-cyan); color: var(--text-white); }
.hero .hero-left .cta .markets { color: var(--accent-cyan); background: transparent; border: 1px solid var(--accent-cyan); }
.hero .hero-left .cta .account:hover { opacity: 0.9; }
.hero .hero-left .cta .markets:hover { background: var(--accent-cyan); color: var(--text-white); }
.hero .hero-right { flex: 1; min-width: 300px; text-align: center; z-index:1; }
.hero .hero-right img { width: 100%; border-radius: 15px; box-shadow: 0 0 20px rgba(0,229,255,0.3); }

/* Why Choose Section */
.why { padding: 60px 30px; text-align: center; width: 100%; background: var(--section-bg); border-bottom: 1px solid rgba(0,229,255,0.1); }
.why h2 { font-size: 2rem; margin-bottom: 40px; }
.cards { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
.card { background: var(--panel-dark); padding: 25px 15px; border-radius: 15px; flex: 1; min-width: 220px; max-width: 300px; box-shadow: 0 0 10px rgba(0,229,255,0.3); transition: transform 0.3s, box-shadow 0.3s; }
.card:hover { transform: translateY(-10px); box-shadow: 0 0 25px var(--accent-cyan); }
.card h3 { font-size: 1.2rem; margin-bottom: 10px; color: var(--text-white); }
.card p { color: var(--text-grey); font-size: 0.9rem; }
.card .num { font-size: 2rem; font-weight: 900; color: var(--accent-cyan); margin-bottom: 10px; }

/* Market Watch */
.market-watch { padding: 60px 30px; width: 100%; background: var(--section-bg); border-bottom: 1px solid rgba(0,229,255,0.1); }
.market-watch h2 { text-align: center; margin-bottom: 30px; font-size: 2rem; }
.market-watch table { width: 100%; border-collapse: collapse; text-align: center; }
.market-watch th, .market-watch td { padding: 12px; border-bottom: 1px solid rgba(255,255,255,0.1); }
.market-watch th { color: var(--accent-cyan); font-weight: 700; }
.market-watch td { color: var(--text-grey); }
.market-watch .up { color: #4CAF50; font-weight: 700; }
.market-watch .down { color: #FF5252; font-weight: 700; }
.market-watch button { padding: 6px 12px; border: none; border-radius: 5px; margin: 2px; background: rgba(255,255,255,0.1); color: var(--text-white); transition: 0.3s; animation: glow 1.5s infinite alternate; }
.market-watch button:hover { background: var(--accent-cyan); color: var(--text-white); }

/* Premium PDFs */
.premium { padding: 60px 30px; text-align: center; background: var(--section-bg); width: 100%; border-bottom: 1px solid rgba(0,229,255,0.1); }
.premium h2 { font-size: 2rem; margin-bottom: 20px; }
.premium a { display: inline-block; margin: 10px; padding: 15px 25px; background: var(--accent-cyan); color: var(--text-white); border-radius: 8px; font-weight: 700; transition: 0.3s; animation: glow 1.5s infinite alternate; }
.premium a:hover { opacity: 0.9; }

/* Tips */
.tips { padding: 40px 30px; text-align: center; background: var(--section-bg); border-top: 1px solid rgba(0,229,255,0.1); border-bottom: 1px solid rgba(0,229,255,0.1); width: 100%; }
.tips h2 { margin-bottom: 20px; }
.tips .tip { font-size: 1rem; color: var(--accent-cyan); transition: opacity 0.5s; }

/* Contact / Newsletter */
.contact { padding: 40px 30px; text-align: center; background: var(--panel-dark); border-top: 1px solid rgba(0,229,255,0.1); width: 100%; }
.contact h2 { margin-bottom: 20px; font-size: 1.8rem; color: var(--accent-cyan); }
.contact input[type=email] { padding: 12px 15px; border-radius: 8px; border: 1px solid var(--accent-cyan); width: 250px; max-width: 90%; margin-right: 10px; background: #101012; color: #fff; }
.contact button { padding: 12px 20px; border-radius: 8px; border: none; background: var(--accent-orange); color: var(--text-white); font-weight: 700; animation: glow 1.5s infinite alternate; }

/* Footer */
footer { padding: 30px; display: flex; justify-content: space-between; flex-wrap: wrap; background: var(--panel-dark); color: var(--text-grey); font-size: 0.85rem; border-top: 1px solid rgba(0,229,255,0.1); }
footer .footer-left { flex: 1; min-width: 250px; }
footer .footer-right { flex: 1; min-width: 250px; text-align: right; }
footer .socials { display: flex; gap: 10px; justify-content: flex-end; }
footer .socials a { color: var(--text-grey); transition: 0.3s; }
footer .socials a:hover { color: var(--accent-cyan); }

/* Animations */
.fade-in { opacity: 0; transform: translateY(20px); animation: fadeIn 1s forwards; }
@keyframes fadeIn { to { opacity: 1; transform: translateY(0); } }

/* Responsive */
@media(max-width:900px) { .hero { flex-direction: column; } .cards { flex-direction: column; } footer .footer-right { text-align: left; justify-content: flex-start; } }
@media(max-width:500px) { #chat-box { width: 90%; bottom: 10px; right: 5%; } #chat-messages { max-height: 250px; } .contact input[type=email] { margin-bottom: 10px; } }
</style>
</head>
<body>

<header>
    <div class="logo">BLEZOFX 📈</div>
    <nav>
        <a href="#">Markets</a>
        <a href="#">Platforms</a>
        <a href="#">Accounts</a>
        <a href="#">Tools</a>
        <a href="#">Education</a>
        <a href="#">Live Chat</a>
    </nav>
    <div class="actions">
        <a href="#" class="login">LOG IN</a>
        <a href="#" class="start">START TRADING</a>
    </div>
</header>

<section class="hero fade-in">
    <div class="hero-left">
        <h1>TRADE GLOBAL FOREX WITH <span>BLEZOFX</span></h1>
        <p>Blue Pool Forex Traders</p>
        <div class="ticker">
            <div>EUR/USD</div>
            <div>GBP/USD</div>
            <div>USD/JPY</div>
            <div>Gold/USD</div>
        </div>
        <div class="cta">
            <a href="#" class="account">OPEN YOUR ACCOUNT</a>
            <a href="#" class="markets">EXPLORE MARKETS</a>
        </div>
    </div>
    <div class="hero-right">
        <img src="https://i.ibb.co/3z3QjZP/trader-desk.png" alt="Trader Setup">
    </div>
</section>

<section class="why fade-in">
    <h2>WHY CHOOSE BLEZOFX?</h2>
    <div class="cards">
        <div class="card">
            <div class="num">1</div>
            <h3>BLAZING SPEED EXECUTION</h3>
            <p>Lightning fast speeds, 0.0 spreads for precision.</p>
        </div>
        <div class="card">
            <div class="num">2</div>
            <h3>GLOBAL MARKETS</h3>
            <p>Trade Global Forex, Gold, Oil & Crypto.</p>
        </div>
        <div class="card">
            <div class="num">3</div>
            <h3>ADVANCED TOOLS</h3>
            <p>Interactive charts, MT5 platform, real-time analytics.</p>
        </div>
        <div class="card">
            <div class="num">4</div>
            <h3>INSTITUTIONAL-GRADE TECHNOLOGY</h3>
            <p>Secure, reliable infrastructure with deep liquidity.</p>
        </div>
        <div class="card">
            <div class="num">5</div>
            <h3>EXPERT COMMUNITY SUPPORT</h3>
            <p>Expert analysis, education, and continuous support 24/7.</p>
        </div>
    </div>
</section>

<section class="market-watch fade-in">
    <h2>MARKET WATCH</h2>
    <table>
        <thead>
            <tr>
                <th>Pair</th>
                <th>Price</th>
                <th>Change</th>
                <th>Chart</th>
                <th>Actions</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>EUR/USD</td>
                <td><b>1.0845</b></td>
                <td class="up">+0.12% ▲</td>
                <td>[Chart]</td>
                <td><button>Buy</button><button>Sell</button></td>
            </tr>
            <tr>
                <td>GBP/USD</td>
                <td><b>1.2530</b></td>
                <td class="down">-0.05% ▼</td>
                <td>[Chart]</td>
                <td><button>Buy</button><button>Sell</button></td>
            </tr>
            <tr>
                <td>USD/JPY</td>
                <td><b>151.20</b></td>
                <td class="up">+0.21% ▲</td>
                <td>[Chart]</td>
                <td><button>Buy</button><button>Sell</button></td>
            </tr>
        </tbody>
    </table>
</section>

<section class="premium fade-in">
    <h2>PREMIUM ACCESS</h2>
    <a href="https://payhip.com/b/nwOL4" target="_blank">SMC Guide</a>
    <a href="https://payhip.com/b/nwOL4" target="_blank">Risk Management Guide</a>
    <a href="https://payhip.com/b/nwOL4" target="_blank">ICT Guide</a>
    <a href="https://payhip.com/b/nwOL4" target="_blank">Support & Resistance</a>
</section>

<section class="tips fade-in">
    <h2>Trading Tips</h2>
    <div class="tip" id="tip-text">Welcome to BLEZOFX. Trade smart, trade fast.</div>
</section>

<section class="contact fade-in">
    <h2>Subscribe for Updates</h2>
    <form onsubmit="alert('Subscribed!'); return false;">
        <input type="email" placeholder="Enter your email" required>
        <button type="submit">Subscribe</button>
    </form>
</section>

<footer>
    <div class="footer-left">© 2026 BLEZOFX. All rights reserved.</div>
    <div class="footer-right socials">
        <a href="#">FB</a>
        <a href="#">TW</a>
        <a href="#">IG</a>
    </div>
</footer>

</body>
</html>
