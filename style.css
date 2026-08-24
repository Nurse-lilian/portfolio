/* ============================================
   BRAND COLORS – ROYAL BLUE PALETTE
   ============================================ */
:root {
    --primary: #0D1B4A;
    --primary-light: #2E4AD6;
    --primary-dark: #0A1538;
    --azure: #2E4AD6;
    --azure-light: #5B72E0;
    --white: #FFFFFF;
    --cream: #F8FAFC;
    --gray-light: #E2E8F0;
    --gray-muted: #94A3B8;
    --navy: #0D1B4A;
    --shadow: 0 4px 30px rgba(13, 27, 74, 0.15);
    --shadow-hover: 0 12px 48px rgba(13, 27, 74, 0.08);
    --transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Nunito', sans-serif;
    background: var(--cream);
    color: var(--navy);
    line-height: 1.7;
    overflow-x: hidden;
    cursor: default;
}

.container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 24px;
}

/* ===== PROGRESS BAR ===== */
.progress-bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 0%;
    height: 3px;
    background: linear-gradient(90deg, var(--primary-light), var(--azure-light));
    z-index: 1001;
    transition: width 0.1s ease;
    box-shadow: 0 0 20px rgba(46, 74, 214, 0.3);
}

/* ===== NOISE OVERLAY ===== */
.noise-overlay {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 9999;
    opacity: 0.02;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)'/%3E%3C/svg%3E");
    background-repeat: repeat;
    background-size: 256px 256px;
}

/* ===== GLOW TRAIL ===== */
.glow-trail {
    position: fixed;
    width: 300px;
    height: 300px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(46, 74, 214, 0.06), transparent 70%);
    pointer-events: none;
    z-index: 9998;
    transform: translate(-50%, -50%);
    transition: opacity 0.4s ease;
    opacity: 0;
}
.glow-trail.active {
    opacity: 1;
}

/* ===== CUSTOM CURSOR ===== */
.custom-cursor {
    position: fixed;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    border: 2px solid var(--primary-light);
    pointer-events: none;
    z-index: 99999;
    transform: translate(-50%, -50%);
    transition: width 0.3s ease, height 0.3s ease, background 0.3s ease;
    opacity: 0;
}
.custom-cursor.active {
    opacity: 1;
}
.custom-cursor.hover {
    width: 48px;
    height: 48px;
    background: rgba(46, 74, 214, 0.08);
}

/* ===== MEDICAL CROSS SHAPES (Background) ===== */
.medical-crosses {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
    opacity: 0.04;
}
.medical-crosses .cross {
    position: absolute;
    width: 60px;
    height: 60px;
    border: 2px solid var(--primary-light);
    border-radius: 4px;
    transform: rotate(45deg);
    animation: floatCross 25s infinite alternate ease-in-out;
}
.medical-crosses .cross:nth-child(1) {
    top: 10%;
    left: 5%;
    width: 80px;
    height: 80px;
    animation-duration: 28s;
    border-color: var(--azure-light);
}
.medical-crosses .cross:nth-child(2) {
    bottom: 20%;
    right: 3%;
    width: 100px;
    height: 100px;
    animation-duration: 22s;
}
.medical-crosses .cross:nth-child(3) {
    top: 40%;
    right: 10%;
    width: 60px;
    height: 60px;
    animation-duration: 30s;
    border-color: var(--azure-light);
}
.medical-crosses .cross:nth-child(4) {
    bottom: 10%;
    left: 20%;
    width: 120px;
    height: 120px;
    animation-duration: 35s;
    opacity: 0.5;
}
.medical-crosses .cross:nth-child(5) {
    top: 5%;
    right: 30%;
    width: 70px;
    height: 70px;
    animation-duration: 26s;
}
@keyframes floatCross {
    0% { transform: rotate(45deg) translate(0, 0) scale(1); }
    100% { transform: rotate(65deg) translate(30px, -30px) scale(1.1); }
}

/* ===== NAVIGATION ===== */
.navbar {
    position: fixed;
    top: 24px;
    left: 50%;
    transform: translateX(-50%);
    width: auto;
    max-width: 95%;
    z-index: 1000;
    background: rgba(255, 255, 255, 0.92);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border: 1px solid rgba(13, 27, 74, 0.08);
    border-radius: 60px;
    padding: 10px 24px;
    box-shadow: 0 8px 40px rgba(0, 0, 0, 0.06);
    transition: var(--transition);
}
.navbar.scrolled {
    background: rgba(255, 255, 255, 0.97);
    border-color: rgba(46, 74, 214, 0.15);
    box-shadow: 0 8px 40px rgba(0, 0, 0, 0.1);
    top: 16px;
}
.nav-inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}
.logo {
    font-size: 1.3rem;
    font-weight: 800;
    color: var(--navy);
    letter-spacing: -0.02em;
    text-decoration: none;
    flex-shrink: 0;
}
.logo span {
    color: var(--primary-light);
}
.nav-links {
    display: flex;
    gap: 0.8rem;
    list-style: none;
    align-items: center;
    flex-wrap: nowrap;
}
.nav-links a {
    text-decoration: none;
    color: rgba(13, 27, 74, 0.7);
    font-weight: 600;
    font-size: 0.7rem;
    transition: var(--transition);
    letter-spacing: 0.04em;
    position: relative;
    padding: 4px 6px;
    border-radius: 40px;
    white-space: nowrap;
}
.nav-links a::after {
    content: '';
    position: absolute;
    bottom: -4px;
    left: 50%;
    width: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--primary-light), var(--azure-light));
    transition: var(--transition);
    border-radius: 2px;
    transform: translateX(-50%);
}
.nav-links a:hover {
    color: var(--navy);
}
.nav-links a:hover::after {
    width: 80%;
}
.nav-links a.active {
    color: var(--primary-light);
}
.nav-links a.active::after {
    width: 80%;
}
.nav-toggle {
    display: none;
    flex-direction: column;
    gap: 4px;
    background: none;
    border: none;
    cursor: pointer;
    padding: 4px;
}
.nav-toggle span {
    display: block;
    width: 22px;
    height: 2px;
    background: var(--navy);
    border-radius: 4px;
    transition: var(--transition);
}

/* ===== HERO ===== */
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 100px 0 50px;
    background: linear-gradient(135deg, #F8FAFC 0%, #E2E8F0 100%);
    position: relative;
    overflow: hidden;
}
.hero-glow {
    position: absolute;
    top: -40%;
    left: -20%;
    width: 80%;
    height: 180%;
    background: radial-gradient(circle at 30% 50%, rgba(46, 74, 214, 0.05), transparent 70%);
    pointer-events: none;
    z-index: 1;
}
/* ECG Canvas */
#ecgCanvas {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 80px;
    z-index: 1;
    opacity: 0.3;
    pointer-events: none;
}
/* Floating Medical Icons (particles) */
.particles-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
}
.particle {
    position: absolute;
    bottom: -20px;
    animation: riseParticle var(--duration) linear infinite;
    animation-delay: var(--delay);
    opacity: 0;
    font-size: 1.2rem;
}
@keyframes riseParticle {
    0% { transform: translateY(0) translateX(0) scale(0.8); opacity: 0; }
    10% { opacity: var(--opacity); }
    90% { opacity: var(--opacity); }
    100% { transform: translateY(-110vh) translateX(var(--drift)) scale(1.2); opacity: 0; }
}
.hero-container {
    display: flex;
    gap: 50px;
    align-items: center;
    position: relative;
    z-index: 2;
}
.hero-reverse {
    flex-direction: row-reverse;
}
.hero-content-right {
    flex: 1 1 50%;
}
.hero-badge {
    display: inline-block;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--primary-light);
    background: rgba(46, 74, 214, 0.08);
    padding: 6px 18px;
    border-radius: 40px;
    border: 1.5px solid rgba(46, 74, 214, 0.12);
    margin-bottom: 20px;
}
.hero-title {
    font-family: 'Merriweather', serif;
    font-size: 3.2rem;
    font-weight: 900;
    line-height: 1.05;
    color: var(--navy);
    letter-spacing: -0.02em;
    margin-bottom: 8px;
}
.hero-title span {
    color: var(--primary-light);
}
.typewriter-wrapper {
    display: inline-block;
    position: relative;
}
#typewriterText {
    color: var(--primary-light);
    font-weight: 700;
}
.cursor-blink {
    display: inline-block;
    color: var(--primary-light);
    font-weight: 300;
    animation: blink 0.7s step-end infinite;
}
@keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
}
.hero-subtitle {
    font-size: 1rem;
    color: var(--gray-muted);
    margin-bottom: 20px;
    font-weight: 400;
}
.hero-trust-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 28px;
}
.hero-trust-badges span {
    background: rgba(255, 255, 255, 0.7);
    padding: 5px 16px;
    border-radius: 40px;
    font-size: 0.7rem;
    color: var(--navy);
    border: 1.5px solid rgba(46, 74, 214, 0.06);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.02);
}
.hero-trust-badges span i {
    color: var(--primary-light);
    margin-right: 6px;
}
.hero-actions {
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
}

/* ===== TRUST BADGES ===== */
.trust-badges {
    display: flex;
    gap: 30px;
    margin-top: 24px;
    padding: 12px 20px;
    background: rgba(255, 255, 255, 0.6);
    border-radius: 40px;
    border: 1px solid rgba(46, 74, 214, 0.08);
    backdrop-filter: blur(4px);
    justify-content: center;
    flex-wrap: wrap;
}
.trust-item {
    text-align: center;
}
.trust-item strong {
    display: block;
    font-size: 1.2rem;
    font-weight: 800;
    color: var(--primary-light);
}
.trust-item span {
    font-size: 0.65rem;
    color: var(--gray-muted);
    letter-spacing: 0.04em;
    text-transform: uppercase;
}

/* ===== HERO IMAGE – SPINNING RING ===== */
.hero-image-frame {
    position: relative;
    width: 100%;
    max-width: 380px;
    aspect-ratio: 1/1;
    border-radius: 50%;
    padding: 12px;
    background: linear-gradient(135deg, var(--primary-light), var(--azure-light), var(--primary-light));
    animation: frameRotate 8s linear infinite;
    flex-shrink: 0;
    margin: 0 auto;
}
@keyframes frameRotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
.hero-image-inner {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    overflow: hidden;
    position: relative;
    background: var(--white);
}
.hero-image-inner img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    display: block;
    border-radius: 50%;
}
.hero-image-overlay {
    position: absolute;
    inset: 0;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 40%, transparent 40%, rgba(46, 74, 214, 0.1));
    pointer-events: none;
}
.hero-image-ring {
    position: absolute;
    inset: -6px;
    border-radius: 50%;
    border: 2px solid rgba(91, 114, 224, 0.25);
    animation: ringPulse 3s ease-in-out infinite;
}
@keyframes ringPulse {
    0%, 100% { transform: scale(1); opacity: 0.3; }
    50% { transform: scale(1.05); opacity: 0.8; }
}
.hero-image-dots {
    position: absolute;
    inset: -20px;
    border-radius: 50%;
    background: radial-gradient(circle at 70% 30%, rgba(46, 74, 214, 0.03), transparent 70%);
    pointer-events: none;
}
.hero-image-badge {
    position: absolute;
    bottom: 15px;
    left: 50%;
    transform: translateX(-50%);
    background: var(--primary-light);
    color: var(--white);
    padding: 6px 20px;
    border-radius: 40px;
    font-size: 0.7rem;
    font-weight: 600;
    white-space: nowrap;
    border: 2px solid var(--white);
    z-index: 2;
}

/* ===== STATS BAR ===== */
.hero-stats-bar {
    display: flex;
    gap: 20px;
    padding: 12px 24px;
    background: rgba(255, 255, 255, 0.8);
    border-radius: 60px;
    border: 1.5px solid rgba(46, 74, 214, 0.08);
    width: 100%;
    max-width: 380px;
    justify-content: center;
    flex-wrap: nowrap;
    align-items: center;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.02);
    margin: 0 auto;
}
.hero-stats-bar .stat-item {
    text-align: center;
    flex: 1;
}
.hero-stats-bar .stat-item strong {
    display: block;
    font-size: 1.1rem;
    font-weight: 800;
    color: var(--primary-light);
}
.hero-stats-bar .stat-item span:not(.counter) {
    font-size: 0.55rem;
    color: var(--gray-muted);
    text-transform: uppercase;
    letter-spacing: 0.04em;
    display: block;
    margin-top: 1px;
}
.hero-stats-bar .stat-divider {
    width: 1px;
    background: rgba(46, 74, 214, 0.08);
    flex-shrink: 0;
    height: 30px;
    align-self: center;
}

/* ===== BUTTONS ===== */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 14px 36px;
    border-radius: 40px;
    font-weight: 700;
    font-size: 0.85rem;
    text-decoration: none;
    transition: var(--transition);
    border: none;
    cursor: pointer;
}
.btn-primary {
    background: linear-gradient(135deg, var(--primary-light), var(--azure-light));
    color: var(--white);
    position: relative;
    overflow: hidden;
    box-shadow: 0 4px 16px rgba(46, 74, 214, 0.2);
}
.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(46, 74, 214, 0.4);
}
.btn-outline {
    background: transparent;
    color: var(--navy);
    border: 1.5px solid var(--primary-light);
}
.btn-outline:hover {
    background: var(--primary-light);
    color: var(--white);
    transform: translateY(-3px);
}
.btn-download {
    background: transparent;
    color: var(--primary-light);
    border: 1.5px solid var(--primary-light);
    transition: var(--transition);
}
.btn-download:hover {
    background: var(--primary-light);
    color: var(--white);
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(46, 74, 214, 0.3);
}
.btn-block {
    width: 100%;
    justify-content: center;
}
.btn-ripple {
    position: relative;
    overflow: hidden;
}
.btn-ripple::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.2);
    transform: translate(-50%, -50%);
    transition: width 0.6s ease, height 0.6s ease;
}
.btn-ripple:active::before {
    width: 300px;
    height: 300px;
}

/* ===== 3D TILT ===== */
.tilt-card {
    transition: transform 0.15s cubic-bezier(0.25, 0.46, 0.45, 0.94), box-shadow 0.3s ease;
    will-change: transform;
}
.tilt-card:hover {
    transform: perspective(1000px) rotateX(var(--rotateX, 0deg)) rotateY(var(--rotateY, 0deg)) translateY(-4px);
}

/* ===== SECTION COMMON ===== */
section {
    padding: 80px 0;
}
.section-title {
    font-family: 'Merriweather', serif;
    font-size: 2.4rem;
    font-weight: 900;
    color: var(--navy);
    margin-bottom: 8px;
    line-height: 1.15;
}
.section-title span {
    color: var(--primary-light);
}
.section-tag {
    display: inline-block;
    font-size: 0.65rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--primary-light);
    background: rgba(46, 74, 214, 0.08);
    padding: 4px 16px;
    border-radius: 40px;
    margin-bottom: 8px;
    border: 1.5px solid rgba(46, 74, 214, 0.08);
}
.section-sub {
    font-size: 1rem;
    color: var(--gray-muted);
    font-weight: 400;
    max-width: 500px;
}

/* ===== INTRODUCTORY VIDEO SECTION ===== */
.intro-video {
    padding: 80px 0;
    background: linear-gradient(135deg, #0D1B4A 0%, #1A2F6A 100%);
    position: relative;
    overflow: hidden;
    color: var(--white);
}
.intro-video::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -20%;
    width: 60%;
    height: 200%;
    background: radial-gradient(circle, rgba(46, 74, 214, 0.08), transparent 70%);
    pointer-events: none;
    z-index: 0;
}
.intro-video-container {
    display: flex;
    gap: 50px;
    align-items: center;
    position: relative;
    z-index: 1;
}
.intro-video-wrapper {
    flex: 0 0 48%;
    position: relative;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 20px 60px rgba(13, 27, 74, 0.4);
    background: #0D1B4A;
}
.intro-video-player {
    width: 100%;
    display: block;
    border-radius: 16px;
    aspect-ratio: 16/9;
    object-fit: cover;
    background: #0D1B4A;
}
.video-sound-toggle {
    position: absolute;
    bottom: 16px;
    right: 16px;
    background: rgba(0, 0, 0, 0.6);
    color: #fff;
    border: none;
    border-radius: 50%;
    width: 44px;
    height: 44px;
    font-size: 1.2rem;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: background 0.3s ease, transform 0.2s ease;
    backdrop-filter: blur(4px);
    z-index: 5;
}
.video-sound-toggle:hover {
    background: rgba(0, 0, 0, 0.8);
    transform: scale(1.1);
}
.video-sound-toggle i {
    pointer-events: none;
}
.intro-video-overlay {
    position: absolute;
    bottom: 20px;
    left: 20px;
    color: rgba(255, 255, 255, 0.12);
    font-size: 2rem;
    pointer-events: none;
    z-index: 4;
}
.intro-video-content {
    flex: 1;
}
.intro-video-content .section-tag {
    background: rgba(46, 74, 214, 0.2);
    color: var(--azure-light);
    border-color: rgba(46, 74, 214, 0.15);
}
.intro-video-content .section-title {
    color: var(--white);
    font-size: 2.6rem;
}
.intro-video-content .section-title span {
    color: var(--azure-light);
}
.intro-video-content p {
    color: rgba(255, 255, 255, 0.8);
    font-size: 1rem;
    line-height: 1.8;
    margin-bottom: 14px;
}
.intro-video-actions {
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
    margin-top: 8px;
}
.intro-video-actions .btn-primary {
    background: linear-gradient(135deg, var(--primary-light), var(--azure-light));
    box-shadow: 0 4px 16px rgba(46, 74, 214, 0.4);
}
.intro-video-actions .btn-primary:hover {
    box-shadow: 0 8px 24px rgba(46, 74, 214, 0.6);
}
.intro-video-actions .btn-outline {
    border-color: var(--azure-light);
    color: var(--white);
}
.intro-video-actions .btn-outline:hover {
    background: var(--azure-light);
    color: var(--white);
}

/* ===== ABOUT ===== */
.about {
    background: var(--white);
    padding: 80px 0;
}
.about-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: start;
}
.about-text-side p {
    color: var(--gray-muted);
    font-size: 0.95rem;
    margin-bottom: 14px;
    line-height: 1.8;
}
.about-highlights-cards {
    display: flex;
    flex-direction: column;
    gap: 16px;
}
.highlight-card {
    background: var(--cream);
    padding: 20px 24px;
    border-radius: 16px;
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.04);
    border-left: 4px solid var(--primary-light);
    transition: var(--transition);
}
.highlight-card:hover {
    transform: translateX(6px);
    box-shadow: 0 12px 40px rgba(13, 27, 74, 0.08);
    border-left-color: var(--primary-light);
}
.highlight-card i {
    font-size: 1.6rem;
    color: var(--primary-light);
    margin-bottom: 4px;
    display: block;
}
.highlight-card h4 {
    font-size: 1rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 2px;
}
.highlight-card p {
    font-size: 0.85rem;
    color: var(--gray-muted);
}

/* ===== TOOLS (Expanded) ===== */
.tools-section {
    background: var(--primary);
    padding: 60px 0 70px;
}
.tools-section .section-title {
    color: var(--white);
}
.tools-section .section-tag {
    color: var(--azure-light);
    border-color: rgba(46, 74, 214, 0.3);
}
.tools-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    justify-content: center;
}
.tool-card {
    background: rgba(255, 255, 255, 0.06);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 12px;
    padding: 14px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    transition: var(--transition);
    color: var(--gray-light);
    font-weight: 600;
    font-size: 0.85rem;
}
.tool-card:hover {
    background: rgba(46, 74, 214, 0.15);
    border-color: var(--azure-light);
    transform: translateY(-3px);
}
.tool-card i {
    font-size: 1.2rem;
    color: var(--azure-light);
}

/* ===== SERVICES ===== */
.services {
    background: var(--white);
    padding: 80px 0;
}
.services-header {
    text-align: center;
    margin-bottom: 48px;
}
.services-grid-new {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
}
.service-new {
    background: var(--cream);
    border: 1px solid rgba(13, 27, 74, 0.06);
    padding: 32px 24px;
    border-radius: 16px;
    text-align: center;
    transition: var(--transition);
    position: relative;
    overflow: hidden;
}
.service-new:hover {
    transform: translateY(-6px);
    border-color: var(--primary-light);
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.08);
}
.service-new-icon {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--primary-light), var(--azure-light));
    color: var(--white);
    font-size: 1.8rem;
    margin-bottom: 12px;
    box-shadow: 0 4px 16px rgba(46, 74, 214, 0.15);
}
.service-new h3 {
    font-size: 1rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 4px;
}
.service-new p {
    font-size: 0.85rem;
    color: var(--gray-muted);
    line-height: 1.5;
}
.service-new-number {
    position: absolute;
    top: 12px;
    right: 16px;
    font-size: 0.7rem;
    font-weight: 800;
    color: rgba(46, 74, 214, 0.06);
}

/* ===== EXPERIENCE (with stats on hover) ===== */
.experience {
    background: var(--cream);
    padding: 80px 0;
}
.experience-header {
    margin-bottom: 40px;
}
.experience-grid {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
.exp-item {
    display: flex;
    gap: 20px;
    align-items: flex-start;
}
.exp-marker {
    width: 14px;
    height: 14px;
    min-width: 14px;
    border-radius: 50%;
    background: var(--primary-light);
    border: 3px solid var(--cream);
    box-shadow: 0 0 0 3px var(--primary-light);
    margin-top: 18px;
}
.exp-content {
    flex: 1;
    background: var(--white);
    padding: 24px 28px;
    border-radius: 16px;
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.04);
    transition: var(--transition);
    border: 1px solid transparent;
    position: relative;
    overflow: hidden;
}
.exp-content:hover {
    box-shadow: 0 12px 40px rgba(13, 27, 74, 0.08);
    transform: translateX(6px);
    border-color: var(--primary-light);
}
.exp-header {
    display: flex;
    flex-wrap: wrap;
    align-items: baseline;
    gap: 4px 12px;
    margin-bottom: 4px;
}
.exp-header h3 {
    font-size: 1rem;
    font-weight: 700;
    color: var(--navy);
}
.exp-company {
    font-size: 0.85rem;
    color: var(--gray-muted);
}
.exp-date {
    font-size: 0.7rem;
    color: var(--gray-muted);
    margin-left: auto;
}
.exp-content p {
    font-size: 0.85rem;
    color: var(--gray-muted);
    line-height: 1.6;
    margin-bottom: 8px;
}
.exp-skills {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}
.exp-skills span {
    background: rgba(46, 74, 214, 0.08);
    color: var(--primary-light);
    padding: 2px 14px;
    border-radius: 40px;
    font-size: 0.6rem;
    font-weight: 600;
}
.exp-impact {
    margin-top: 12px;
    padding-top: 10px;
    border-top: 1px dashed rgba(46, 74, 214, 0.15);
    opacity: 0;
    transform: translateY(10px);
    transition: opacity 0.4s ease, transform 0.4s ease;
    display: flex;
    align-items: center;
    gap: 8px;
    color: var(--primary-light);
    font-weight: 600;
    font-size: 0.85rem;
}
.exp-impact i {
    color: var(--azure-light);
}
.exp-content:hover .exp-impact {
    opacity: 1;
    transform: translateY(0);
}

/* ===== WORK (Case Studies) ===== */
.work {
    background: var(--white);
    padding: 80px 0;
}
.work-header {
    text-align: center;
    margin-bottom: 40px;
}
.work-grid-new {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
.work-new {
    background: var(--cream);
    border: 1px solid rgba(13, 27, 74, 0.06);
    padding: 28px 20px;
    border-radius: 16px;
    text-align: center;
    transition: var(--transition);
    cursor: pointer;
}
.work-new:hover {
    transform: translateY(-6px);
    border-color: var(--primary-light);
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.08);
}
.work-new-icon {
    font-size: 2.2rem;
    color: var(--primary-light);
    margin-bottom: 8px;
    display: block;
}
.work-new h3 {
    font-size: 0.9rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 2px;
}
.work-new p {
    font-size: 0.75rem;
    color: var(--gray-muted);
    line-height: 1.4;
    margin-bottom: 8px;
}
.work-new-cta {
    font-size: 0.65rem;
    font-weight: 700;
    color: var(--primary-light);
    transition: var(--transition);
    display: inline-block;
}
.work-new:hover .work-new-cta {
    transform: translateX(4px);
}

/* ===== MODAL ===== */
.modal-overlay {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.85);
    backdrop-filter: blur(12px);
    z-index: 2000;
    align-items: center;
    justify-content: center;
    padding: 24px;
}
.modal-overlay.active {
    display: flex;
}
.modal {
    background: var(--white);
    border: 1px solid rgba(13, 27, 74, 0.15);
    max-width: 700px;
    width: 100%;
    max-height: 90vh;
    overflow-y: auto;
    padding: 40px 44px;
    position: relative;
    border-radius: 20px;
    animation: modalIn 0.4s ease;
}
@keyframes modalIn {
    from { opacity: 0; transform: scale(0.95) translateY(20px); }
    to { opacity: 1; transform: scale(1) translateY(0); }
}
.modal-close {
    position: absolute;
    top: 16px;
    right: 20px;
    background: none;
    border: none;
    font-size: 1.4rem;
    color: var(--gray-muted);
    cursor: pointer;
    transition: var(--transition);
    padding: 4px 8px;
}
.modal-close:hover {
    color: var(--primary-light);
    transform: rotate(90deg);
}
.modal-content h2 {
    font-family: 'Merriweather', serif;
    font-size: 1.6rem;
    font-weight: 900;
    color: var(--navy);
    margin-bottom: 4px;
}
.modal-content .modal-subtitle {
    color: var(--gray-muted);
    font-size: 0.9rem;
    margin-bottom: 20px;
}
.modal-content .modal-section {
    margin-bottom: 16px;
}
.modal-content .modal-section h3 {
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--primary-light);
    text-transform: uppercase;
    letter-spacing: 0.04em;
    margin-bottom: 4px;
}
.modal-content .modal-section p {
    color: var(--gray-muted);
    font-weight: 400;
    line-height: 1.7;
    font-size: 0.9rem;
}
.modal-content .modal-result {
    background: rgba(46, 74, 214, 0.04);
    border: 1px solid rgba(46, 74, 214, 0.08);
    padding: 16px 20px;
    border-radius: 12px;
    margin-top: 8px;
}
.modal-content .modal-result p {
    color: var(--navy);
    font-weight: 400;
    margin: 0;
    font-size: 0.9rem;
}
.modal-content .modal-result strong {
    color: var(--primary-light);
}
.modal-content .modal-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 12px;
}
.modal-content .modal-tags span {
    background: rgba(46, 74, 214, 0.08);
    color: var(--primary-light);
    padding: 4px 14px;
    border-radius: 40px;
    font-size: 0.65rem;
    font-weight: 500;
}

/* ===== WORK SAMPLES – CONTINUOUS CAROUSEL ===== */
.work-samples {
    background: var(--cream);
    padding: 80px 0;
}
.work-samples .section-sub {
    margin-bottom: 32px;
}
.work-samples-carousel-wrapper {
    overflow: hidden;
    position: relative;
}
.work-samples-track {
    display: flex;
    gap: 24px;
    will-change: transform;
}
.work-sample-item {
    flex: 0 0 calc(50% - 12px);
    min-width: 0;
}
.work-sample-image {
    position: relative;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.08);
    aspect-ratio: 16/10;
}
.work-sample-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: var(--transition);
}
.work-sample-image:hover img {
    transform: scale(1.05);
}
.work-sample-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(to top, rgba(13, 27, 74, 0.8), transparent);
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 24px;
    color: var(--white);
}
.work-sample-overlay h3 {
    font-family: 'Merriweather', serif;
    font-size: 1.1rem;
    font-weight: 700;
}
.work-sample-overlay p {
    font-size: 0.8rem;
    opacity: 0.8;
}

/* ===== TESTIMONIALS ===== */
.testimonials {
    background: var(--white);
    padding: 80px 0;
    overflow: hidden;
}
.testimonials-header {
    text-align: center;
    margin-bottom: 40px;
}
.testimonial-carousel-wrapper {
    position: relative;
    overflow: hidden;
}
.testimonial-carousel-track {
    display: flex;
    gap: 30px;
    transition: transform 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    will-change: transform;
}
.testimonial-carousel-item {
    flex: 0 0 calc(33.333% - 20px);
    min-width: 0;
}
.testimonial-carousel-content {
    background: var(--cream);
    padding: 32px 28px;
    border-radius: 20px;
    box-shadow: 0 8px 40px rgba(13, 27, 74, 0.04);
    border-top: 4px solid var(--primary-light);
    height: 100%;
    display: flex;
    flex-direction: column;
}
.testimonial-carousel-quote {
    font-family: 'Merriweather', serif;
    font-size: 2.8rem;
    color: var(--primary-light);
    line-height: 0.8;
    margin-bottom: 8px;
    opacity: 0.3;
}
.testimonial-carousel-content p {
    font-size: 1rem;
    color: var(--gray-muted);
    font-style: italic;
    line-height: 1.7;
    flex: 1;
    margin-bottom: 16px;
}
.testimonial-carousel-author {
    display: flex;
    align-items: center;
    gap: 14px;
}
.testimonial-carousel-avatar {
    width: 48px;
    height: 48px;
    border-radius: 50%;
    background: var(--primary-light);
    color: var(--white);
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 1.1rem;
    flex-shrink: 0;
}
.testimonial-carousel-author strong {
    display: block;
    font-size: 0.9rem;
    color: var(--navy);
}
.testimonial-carousel-author span {
    font-size: 0.75rem;
    color: var(--gray-muted);
}
.testimonial-carousel-dots {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-top: 32px;
}
.testimonial-carousel-dots .dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: rgba(46, 74, 214, 0.15);
    border: none;
    cursor: pointer;
    transition: var(--transition);
    padding: 0;
}
.testimonial-carousel-dots .dot.active {
    background: var(--primary-light);
    width: 30px;
    border-radius: 8px;
}

/* ===== CERTIFICATIONS (Text Only) ===== */
.certifications {
    background: var(--cream);
    padding: 80px 0;
}
.certifications-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    margin-top: 32px;
}
.cert-card {
    background: var(--white);
    padding: 28px 24px;
    border-radius: 16px;
    box-shadow: 0 4px 20px rgba(13, 27, 74, 0.04);
    border: 1px solid rgba(13, 27, 74, 0.06);
    transition: var(--transition);
}
.cert-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.08);
    border-color: var(--primary-light);
}
.cert-icon {
    font-size: 2rem;
    color: var(--primary-light);
    margin-bottom: 12px;
}
.cert-card h3 {
    font-size: 1rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 4px;
}
.cert-card p {
    font-size: 0.85rem;
    color: var(--gray-muted);
    line-height: 1.5;
}

/* ===== WORKFLOW ===== */
.workflow {
    background: var(--white);
    padding: 80px 0;
}
.workflow-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 24px;
    margin-top: 32px;
}
.workflow-step {
    text-align: center;
    padding: 24px;
    background: var(--cream);
    border-radius: 16px;
    border: 1px solid rgba(13, 27, 74, 0.06);
    transition: var(--transition);
}
.workflow-step:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.08);
}
.workflow-number {
    font-size: 2.4rem;
    font-weight: 900;
    color: var(--primary-light);
    opacity: 0.15;
    margin-bottom: 8px;
}
.workflow-step h3 {
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 4px;
}
.workflow-step p {
    font-size: 0.85rem;
    color: var(--gray-muted);
    line-height: 1.5;
}

/* ===== WHY WORK WITH ME ===== */
.why-work {
    background: var(--cream);
    padding: 80px 0;
}
.why-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 20px;
    margin-top: 32px;
}
.why-card {
    text-align: center;
    padding: 24px 16px;
    background: var(--white);
    border-radius: 16px;
    border: 1px solid rgba(13, 27, 74, 0.06);
    transition: var(--transition);
}
.why-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 30px rgba(13, 27, 74, 0.08);
}
.why-card i {
    font-size: 2rem;
    color: var(--primary-light);
    margin-bottom: 8px;
}
.why-card h3 {
    font-size: 0.95rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 2px;
}
.why-card p {
    font-size: 0.8rem;
    color: var(--gray-muted);
}

/* ===== CONTACT ===== */
.contact {
    background: var(--white);
    padding: 80px 0;
}
.contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
    align-items: start;
}
.contact-left p {
    color: var(--gray-muted);
    font-size: 0.95rem;
    margin-bottom: 14px;
    max-width: 400px;
}
.contact-social {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 20px;
}
.contact-social a {
    width: 44px;
    height: 44px;
    border-radius: 50%;
    border: 2px solid rgba(46, 74, 214, 0.08);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--navy);
    transition: var(--transition);
    text-decoration: none;
}
.contact-social a:hover {
    background: var(--primary-light);
    border-color: var(--primary-light);
    color: var(--white);
    transform: translateY(-3px);
}
.contact-right form {
    display: flex;
    flex-direction: column;
    gap: 14px;
    width: 100%;
}
.contact-right input,
.contact-right textarea {
    width: 100%;
    padding: 14px 18px;
    border: 2px solid rgba(46, 74, 214, 0.06);
    border-radius: 12px;
    font-family: 'Nunito', sans-serif;
    font-size: 0.9rem;
    background: var(--cream);
    transition: var(--transition);
    outline: none;
    color: var(--navy);
}
.contact-right input:focus,
.contact-right textarea:focus {
    border-color: var(--primary-light);
    box-shadow: 0 0 0 4px rgba(46, 74, 214, 0.06);
    background: var(--white);
}
.contact-right textarea {
    min-height: 120px;
    resize: vertical;
}

/* ===== BACK TO TOP ===== */
.back-to-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: var(--primary-light);
    color: var(--white);
    border: none;
    font-size: 1.2rem;
    cursor: pointer;
    z-index: 9998;
    opacity: 0;
    visibility: hidden;
    transform: translateY(20px);
    transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    box-shadow: 0 4px 20px rgba(46, 74, 214, 0.3);
    display: flex;
    align-items: center;
    justify-content: center;
}
.back-to-top.visible {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
}
.back-to-top:hover {
    background: var(--azure-light);
    transform: translateY(-4px) scale(1.05);
    box-shadow: 0 8px 30px rgba(46, 74, 214, 0.4);
}

/* ===== FOOTER ===== */
footer {
    padding: 28px 0;
    background: var(--primary);
    border-top: 1px solid rgba(255, 255, 255, 0.04);
    text-align: center;
}
footer p {
    color: var(--gray-muted);
    font-weight: 400;
    font-size: 0.75rem;
    letter-spacing: 0.04em;
}
footer .footer-tagline {
    color: rgba(255, 255, 255, 0.2);
    font-size: 0.7rem;
    margin-top: 2px;
}

/* ===== SCROLLBAR ===== */
::-webkit-scrollbar {
    width: 8px;
}
::-webkit-scrollbar-track {
    background: var(--cream);
}
::-webkit-scrollbar-thumb {
    background: linear-gradient(180deg, var(--primary-light), var(--azure-light));
    border-radius: 4px;
}
::-webkit-scrollbar-thumb:hover {
    background: var(--primary-light);
}

/* ===== RESPONSIVE ===== */
@media (max-width: 1024px) {
    .hero-container {
        flex-direction: column !important;
        text-align: center;
    }
    .hero-content-right {
        order: 1;
    }
    .hero-image-right {
        order: 0;
    }
    .hero-title {
        font-size: 2.8rem;
    }
    .hero-trust-badges {
        justify-content: center;
    }
    .hero-actions {
        justify-content: center;
    }
    .trust-badges {
        justify-content: center;
    }
    .intro-video-container {
        flex-direction: column;
        text-align: center;
        gap: 30px;
    }
    .intro-video-wrapper {
        flex: 0 0 100%;
        width: 100%;
        max-width: 600px;
        margin: 0 auto;
    }
    .intro-video-content .section-title {
        font-size: 2.2rem;
    }
    .intro-video-actions {
        justify-content: center;
    }
    .about-wrapper {
        grid-template-columns: 1fr;
        text-align: center;
    }
    .about-highlights-cards {
        align-items: center;
    }
    .highlight-card {
        width: 100%;
        max-width: 500px;
        text-align: left;
    }
    .services-grid-new {
        grid-template-columns: 1fr 1fr;
    }
    .work-grid-new {
        grid-template-columns: repeat(2, 1fr);
    }
    .certifications-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    .workflow-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    .why-grid {
        grid-template-columns: repeat(3, 1fr);
    }
    .work-sample-item {
        flex: 0 0 calc(50% - 12px);
    }
    .testimonial-carousel-item {
        flex: 0 0 calc(50% - 15px);
    }
    .contact-grid {
        grid-template-columns: 1fr;
        text-align: center;
    }
    .contact-left p {
        margin: 0 auto 14px;
    }
    .contact-social {
        justify-content: center;
    }
    .glow-trail,
    .custom-cursor {
        display: none;
    }
}

@media (max-width: 768px) {
    .navbar {
        top: 12px;
        padding: 8px 16px;
        border-radius: 40px;
        width: calc(100% - 20px);
        background: rgba(255, 255, 255, 0.95);
        max-width: 100%;
    }
    .navbar.scrolled {
        background: rgba(255, 255, 255, 0.98);
        top: 10px;
    }
    .nav-links {
        display: none;
        flex-direction: column;
        gap: 0.8rem;
        width: 100%;
        padding: 16px 0 8px;
        border-top: 1.5px solid rgba(46, 74, 214, 0.08);
        margin-top: 10px;
    }
    .nav-links a {
        font-size: 0.85rem;
        padding: 4px 8px;
        white-space: normal;
    }
    .nav-links.show {
        display: flex;
    }
    .nav-toggle {
        display: flex;
    }
    .hero-title {
        font-size: 2.2rem;
    }
    .hero-actions {
        flex-direction: column;
        align-items: center;
    }
    .hero-actions .btn {
        width: 100%;
        max-width: 280px;
    }
    .hero-trust-badges {
        flex-direction: column;
        align-items: center;
    }
    .trust-badges {
        flex-direction: row;
        flex-wrap: wrap;
        gap: 16px;
    }
    .hero-image-right {
        overflow: hidden;
        width: 100%;
        max-width: 100%;
    }
    .hero-image-frame {
        max-width: 260px;
        margin: 0 auto;
    }
    .hero-stats-bar {
        flex-wrap: nowrap;
        gap: 10px;
        padding: 10px 16px;
        max-width: 100%;
        width: 100%;
        border-radius: 40px;
    }
    .hero-stats-bar .stat-item strong {
        font-size: 0.9rem;
    }
    .hero-stats-bar .stat-item span:not(.counter) {
        font-size: 0.4rem;
    }
    .hero-stats-bar .stat-divider {
        height: 25px;
    }
    .intro-video {
        padding: 60px 0;
    }
    .intro-video-content .section-title {
        font-size: 1.8rem;
    }
    .intro-video-content p {
        font-size: 0.95rem;
    }
    .intro-video-wrapper {
        max-width: 100%;
    }
    .video-sound-toggle {
        width: 38px;
        height: 38px;
        font-size: 1rem;
        bottom: 12px;
        right: 12px;
    }
    .intro-video-overlay {
        font-size: 1.4rem;
        bottom: 14px;
        left: 14px;
    }
    .tools-grid {
        gap: 10px;
    }
    .tool-card {
        padding: 10px 14px;
        font-size: 0.75rem;
    }
    .tool-card i {
        font-size: 1rem;
    }
    .services-grid-new {
        grid-template-columns: 1fr;
    }
    .work-grid-new {
        grid-template-columns: 1fr 1fr;
    }
    .certifications-grid {
        grid-template-columns: 1fr;
    }
    .workflow-grid {
        grid-template-columns: 1fr;
    }
    .why-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    .work-sample-item {
        flex: 0 0 100%;
    }
    .section-title {
        font-size: 1.8rem;
    }
    .testimonial-carousel-item {
        flex: 0 0 100%;
    }
    .exp-header {
        flex-direction: column;
        align-items: flex-start;
        gap: 2px;
    }
    .exp-date {
        margin-left: 0;
    }
    .back-to-top {
        bottom: 20px;
        right: 20px;
        width: 44px;
        height: 44px;
        font-size: 1rem;
    }
    .glow-trail,
    .custom-cursor {
        display: none;
    }
    .noise-overlay {
        opacity: 0.02;
    }
    .contact-right input,
    .contact-right textarea {
        width: 100%;
    }
}

@media (max-width: 480px) {
    .hero-title {
        font-size: 1.8rem;
    }
    .section-title {
        font-size: 1.5rem;
    }
    .hero-image-frame {
        max-width: 200px;
        padding: 8px;
    }
    .hero-image-badge {
        font-size: 0.55rem;
        padding: 4px 12px;
        bottom: 8px;
    }
    .hero-stats-bar {
        gap: 8px;
        padding: 8px 12px;
    }
    .hero-stats-bar .stat-item strong {
        font-size: 0.8rem;
    }
    .hero-stats-bar .stat-item span:not(.counter) {
        font-size: 0.35rem;
    }
    .hero-stats-bar .stat-divider {
        height: 20px;
    }
    .trust-badges {
        gap: 12px;
        padding: 8px 12px;
    }
    .trust-item strong {
        font-size: 1rem;
    }
    .trust-item span {
        font-size: 0.55rem;
    }
    .intro-video {
        padding: 40px 0;
    }
    .intro-video-content .section-title {
        font-size: 1.5rem;
    }
    .intro-video-actions .btn {
        width: 100%;
        max-width: 280px;
        justify-content: center;
    }
    .video-sound-toggle {
        width: 34px;
        height: 34px;
        font-size: 0.9rem;
        bottom: 8px;
        right: 8px;
    }
    .tools-grid {
        gap: 8px;
    }
    .tool-card {
        padding: 8px 12px;
        font-size: 0.7rem;
        gap: 6px;
    }
    .tool-card i {
        font-size: 0.9rem;
    }
    .work-grid-new {
        grid-template-columns: 1fr;
    }
    .why-grid {
        grid-template-columns: 1fr;
    }
    .back-to-top {
        bottom: 16px;
        right: 16px;
        width: 40px;
        height: 40px;
        font-size: 0.9rem;
    }
    .glow-trail,
    .custom-cursor {
        display: none;
    }
    .noise-overlay {
        opacity: 0.01;
    }
    .contact-right input,
    .contact-right textarea {
        width: 100%;
        padding: 12px 14px;
        font-size: 0.85rem;
    }
}
