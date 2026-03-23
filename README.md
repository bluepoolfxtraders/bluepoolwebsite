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
header { display: flex; justify-content: space-between; align-items: center; padding: 15px 30px; background: var(--panel-dark); position: sticky; top: 0; z-index: 1000; }
header .logo { display: flex; align-items: center; gap: 10px; color: var(--accent-cyan); font-weight: 900; font-size: 1.5rem; }
header nav { display: flex; gap: 25px; }
header nav a { color: var(--text-white); font-weight: 500; transition: color var(--transition-speed); }
header nav a:hover { color: var(--accent-cyan); }
header .actions { display: flex; gap: 10px; }
header .actions .login { border: 1px solid var(--accent-cyan); padding: 8px 16px; border-radius: 8px; color: var(--accent-cyan); transition: 0.3s; }
header .actions .login:hover { background: var(--accent-cyan); color: var(--text-white); }
header .actions .start { background: var(--accent-orange); padding: 8px 16px; border-radius: 8px; font-weight: 700; transition: 0.3s; }
header .actions .start:hover { opacity: 0.9; }

/* Hero Section */
.hero { display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; padding: 60px 30px; background: var(--panel-dark); gap: 30px; position: relative; overflow: hidden; }
.hero::before { content: ''; position: absolute; top:0; left:0; width:100%; height:100%; background: url('https://i.ibb.co/3z3QjZP/trader-desk.png') no-repeat center/cover; opacity: 0.05; z-index:0; }
.hero .hero-left { flex: 1; min-width: 300px; z-index:1; }
.hero .hero-left h1 { font-size: 2.5rem; margin-bottom: 10px; }
.hero .hero-left h1 span { color: var(--accent-cyan); font-weight: 900; }
.hero .hero-left p { font-size: 1.1rem; color: var(--text-grey); margin-bottom: 20px; }
.hero .hero-left .ticker { display: flex; gap: 10px; padding: 10px; border: 1px solid var(--accent-cyan); border-radius: 10px; overflow-x: auto; margin-bottom: 20px; }
.ticker div { min-width: 80px; padding: 5px 10px; border-radius: 6px; text-align: center; background: rgba(0,229,255,0.05); color: var(--accent-cyan); font-weight: 600; }
.hero .hero-left .cta { display: flex; gap: 15px; flex-wrap: wrap; }
.hero .hero-left .cta a { padding: 12px 25px; border-radius: 8px; font-weight: 700; transition: 0.3s; }
.hero .hero-left .cta .account { background: var(--accent-cyan); color: var(--text-white); }
.hero .hero-left .cta .markets { color: var(--accent-cyan); background: transparent; border: 1px solid var(--accent-cyan); }
.hero .hero-left .cta .account:hover { opacity: 0.9; }
.hero .hero-left .cta .markets:hover { background: var(--accent-cyan); color: var(--text-white); }
.hero .hero-right { flex: 1; min-width: 300px; text-align: center; z-index:1; }
.hero .hero-right img { width: 100%; border-radius: 15px; box-shadow: 0 0 20px rgba(0,229,255,0.3); }

/* Why Choose Section */
.why { padding: 60px 30px; text-align: center; }
.why h2 { font-size: 2rem; margin-bottom: 40px; }
.cards { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
.card { background: var(--panel-dark); padding: 25px 15px; border-radius: 15px; flex: 1; min-width: 220px; max-width: 300px; box-shadow: 0 0 10px rgba(0,229,255,0.3); transition: transform 0.3s; }
.card:hover { transform: translateY(-5px); }
.card h3 { font-size: 1.2rem; margin-bottom: 10px; color: var(--text-white); }
.card p { color: var(--text-grey); font-size: 0.9rem; }
.card .num { font-size: 2rem; font-weight: 900; color: var(--accent-cyan); margin-bottom: 10px; }

/* Market Watch */
.market-watch { padding: 60px 30px; }
.market-watch h2 { text-align: center; margin-bottom: 30px; font-size: 2rem; }
.market-watch table { width: 100%; border-collapse: collapse; text-align: center; }
.market-watch th, .market-watch td { padding: 12px; border-bottom: 1px solid rgba(255,255,255,0.1); }
.market-watch th { color: var(--accent-cyan); font-weight: 700; }
.market-watch td { color: var(--text-grey); }
.market-watch .up { color: #4CAF50; font-weight: 700; }
.market-watch .down { color: #FF5252; font-weight: 700; }
.market-watch button { padding: 6px 12px; border: none; border-radius: 5px; margin: 2px; background: rgba(255,255,255,0.1); color: var(--text-white); transition: 0.3s; }
.market-watch button:hover { background: var(--accent-cyan); color: var(--text-white); }

/* Premium PDFs */
.premium { padding: 60px 30px; text-align: center; background: var(--panel-dark); }
.premium h2 { font-size: 2rem; margin-bottom: 20px; }
.premium a { display: inline-block; margin: 10px; padding: 15px 25px; background: var(--accent-cyan); color: var(--text-white); border-radius: 8px; font-weight: 700; transition: 0.3s; }
.premium a:hover { opacity: 0.9; }

/* Rotating Tips */
.tips { padding: 40px 30px; text-align: center; background: var(--panel-dark); border-top: 1px solid rgba(0,229,255,0.1); }
.tips h2 { margin-bottom: 20px; }
.tips .tip { font-size: 1rem; color: var(--accent-cyan); transition: opacity 0.5s; }

/* Newsletter / Contact */
.contact { padding: 40px 30px; text-align: center; background: var(--panel-dark); border-top: 1px solid rgba(0,229,255,0.1); }
.contact h2 { margin-bottom: 20px; }
.contact input[type=email] { padding: 10px 15px; border-radius: 6px; border: none; width: 250px; margin-right: 10px; }
.contact button { padding: 10px 15px; border-radius: 6px; border: none; background: var(--accent-cyan); color: var(--text-white); font-weight: 700; }

/* Footer */
footer { padding: 20px 30px; display: flex; justify-content: space-between; flex-wrap: wrap; background: var(--panel-dark); color: var(--text-grey); font-size: 0.85rem; }
footer .socials a { margin-left: 10px; color: var(--text-grey); transition: 0.3s; }
footer .socials a:hover { color: var(--accent-cyan); }

/* Animations */
.fade-in { opacity: 0; transform: translateY(20px); animation: fadeIn 1s forwards; }
@keyframes fadeIn { to { opacity: 1; transform: translateY(0); } }

/* Responsive */
@media(max-width:900px) { .hero { flex-direction: column; } .cards { flex-direction: column; } }
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
    <h2>Contact / Report</h2>
    <form onsubmit="return false;">
        <input type="email" placeholder="Your Email" value="blezofxacademy@gmail.com">
        <button>Subscribe</button>
    </form>
</section>

<footer>
    <div>&copy; 2026 BLEZOFX | All rights reserved</div>
    <div class="socials">
        <a href="#" target="_blank">Facebook</a>
        <a href="#" target="_blank">Twitter</a>
        <a href="#" target="_blank">LinkedIn</a>
    </div>
</footer>

<script>
// Live Ticker Simulation
setInterval(() => {
    const ticker = document.querySelectorAll('.ticker div');
    ticker.forEach(t => {
        let change = (Math.random()*0.02-0.01).toFixed(4);
        t.textContent = t.textContent.split(' ')[0] + ' ' + change;
    });
}, 2000);

// Rotating Tips
const tips = [
    "Trade smart, trade fast.",
    "Risk management is key.",
    "Stay updated with market news.",
    "Analyze charts before buying or selling."
];
let tipIndex = 0;
setInterval(() => {
    document.getElementById('tip-text').style.opacity = 0;
    setTimeout(()=>{
        document.getElementById('tip-text').textContent = tips[tipIndex];
        document.getElementById('tip-text').style.opacity = 1;
        tipIndex = (tipIndex+1) % tips.length;
    },500);
}, 5000);

// Fade-in on scroll
const faders = document.querySelectorAll('.fade-in');
window.addEventListener('scroll', () => {
    faders.forEach(f => {
        const top = f.getBoundingClientRect().top;
        const height = window.innerHeight;
        if(top < height - 100) { f.style.opacity = 1; f.style.transform = 'translateY(0)'; }
    });
});
</script>

</body>
</html>
