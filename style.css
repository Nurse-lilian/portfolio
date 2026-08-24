// ============================================
// PROGRESS BAR
// ============================================
window.addEventListener('scroll', () => {
    const scrollTop = window.scrollY;
    const docHeight = document.documentElement.scrollHeight - window.innerHeight;
    const progress = (scrollTop / docHeight) * 100;
    document.getElementById('progressBar').style.width = progress + '%';
});

// ============================================
// NAVBAR
// ============================================
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => {
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});

// ============================================
// MOBILE NAV TOGGLE
// ============================================
const navToggle = document.getElementById('navToggle');
const navLinks = document.getElementById('navLinks');
if (navToggle && navLinks) {
    navToggle.addEventListener('click', () => navLinks.classList.toggle('show'));
    navLinks.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', () => {
            if (window.innerWidth <= 768) navLinks.classList.remove('show');
        });
    });
}

// ============================================
// SMOOTH SCROLL
// ============================================
document.querySelectorAll('a[href^="#"]').forEach(link => {
    link.addEventListener('click', function(e) {
        const targetId = this.getAttribute('href');
        if (targetId && targetId !== '#') {
            const target = document.querySelector(targetId);
            if (target) {
                e.preventDefault();
                const offset = 80;
                const targetPosition = target.getBoundingClientRect().top + window.pageYOffset - offset;
                window.scrollTo({ top: targetPosition, behavior: 'smooth' });
            }
        }
    });
});

// ============================================
// TYPEWRITER
// ============================================
const typewriterElement = document.getElementById('typewriterText');
const phrases = [
    'Deliver Patient-Centered Care',
    'Support Maternal & Child Health',
    'Transition to Telehealth',
    'Provide Remote Clinical Support',
    'Coordinate Seamless Care'
];
let phraseIndex = 0;
let charIndex = 0;
let isDeleting = false;
let typewriterTimeout;

function typeWriterEffect() {
    const currentPhrase = phrases[phraseIndex];

    if (!isDeleting) {
        typewriterElement.textContent = currentPhrase.substring(0, charIndex + 1);
        charIndex++;

        if (charIndex === currentPhrase.length) {
            typewriterTimeout = setTimeout(() => {
                isDeleting = true;
                typeWriterEffect();
            }, 2000);
            return;
        }
        typewriterTimeout = setTimeout(typeWriterEffect, 80);
    } else {
        typewriterElement.textContent = currentPhrase.substring(0, charIndex - 1);
        charIndex--;

        if (charIndex === 0) {
            isDeleting = false;
            phraseIndex = (phraseIndex + 1) % phrases.length;
            typewriterTimeout = setTimeout(typeWriterEffect, 400);
            return;
        }
        typewriterTimeout = setTimeout(typeWriterEffect, 40);
    }
}

setTimeout(typeWriterEffect, 800);

// ============================================
// GLOW TRAIL
// ============================================
const glowTrail = document.getElementById('glowTrail');
let glowTimeout;

document.addEventListener('mousemove', (e) => {
    if (window.innerWidth <= 768) return;
    glowTrail.style.left = e.clientX + 'px';
    glowTrail.style.top = e.clientY + 'px';
    glowTrail.classList.add('active');

    clearTimeout(glowTimeout);
    glowTimeout = setTimeout(() => {
        glowTrail.classList.remove('active');
    }, 3000);
});

document.addEventListener('mouseleave', () => {
    glowTrail.classList.remove('active');
});

// ============================================
// CUSTOM CURSOR
// ============================================
const customCursor = document.getElementById('customCursor');
let cursorTimeout;

if (customCursor) {
    document.addEventListener('mousemove', (e) => {
        if (window.innerWidth <= 768) return;
        customCursor.style.left = e.clientX + 'px';
        customCursor.style.top = e.clientY + 'px';
        customCursor.classList.add('active');

        clearTimeout(cursorTimeout);
        cursorTimeout = setTimeout(() => {
            customCursor.classList.remove('active');
        }, 2000);
    });

    document.addEventListener('mouseleave', () => {
        customCursor.classList.remove('active');
    });

    document.querySelectorAll('a, .btn, .work-new, .service-new, .testimonial-carousel-item, .tilt-card, .work-sample-item')
        .forEach(el => {
            el.addEventListener('mouseenter', () => {
                customCursor.classList.add('hover');
            });
            el.addEventListener('mouseleave', () => {
                customCursor.classList.remove('hover');
            });
        });
}

// ============================================
// ECG / HEARTBEAT CANVAS ANIMATION
// ============================================
function initECG() {
    const canvas = document.getElementById('ecgCanvas');
    if (!canvas) return;
    const ctx = canvas.getContext('2d');
    let width = canvas.width = window.innerWidth;
    let height = canvas.height = Math.min(80, window.innerHeight * 0.08);
    let time = 0;

    function resize() {
        width = canvas.width = window.innerWidth;
        height = canvas.height = Math.min(80, window.innerHeight * 0.08);
    }

    window.addEventListener('resize', resize);

    function draw() {
        ctx.clearRect(0, 0, width, height);
        ctx.beginPath();
        ctx.strokeStyle = '#2E4AD6';
        ctx.lineWidth = 2;
        ctx.shadowBlur = 10;
        ctx.shadowColor = 'rgba(46, 74, 214, 0.15)';

        const startY = height / 2;
        ctx.moveTo(0, startY);

        for (let i = 0; i < width; i += 1.5) {
            const t = (i / width) * 20 + time;
            let y = startY;

            const phase = t % (2 * Math.PI);
            if (phase < 0.2) {
                y -= 8 * Math.sin(phase * 30);
            } else if (phase < 0.35) {
                const qrs = (phase - 0.2) / 0.15;
                y -= 25 * Math.sin(qrs * Math.PI);
            } else if (phase < 0.6) {
                const tw = (phase - 0.35) / 0.25;
                y -= 12 * Math.sin(tw * Math.PI);
            } else {
                y -= 2 * Math.sin(phase * 2);
            }

            y += (Math.random() - 0.5) * 1.5;
            ctx.lineTo(i, y);
        }

        ctx.stroke();
        ctx.shadowBlur = 0;
        time += 0.03;
        requestAnimationFrame(draw);
    }

    draw();
}

// ============================================
// FLOATING MEDICAL ICONS (Rising from bottom)
// ============================================
function createParticles() {
    const container = document.getElementById('particlesContainer');
    if (!container) return;
    if (window.innerWidth < 768) return;

    const icons = [
        'fa-heartbeat', 'fa-stethoscope', 'fa-pills',
        'fa-syringe', 'fa-hospital', 'fa-user-md',
        'fa-ambulance', 'fa-medkit', 'fa-baby', 'fa-bandage'
    ];

    const particleCount = 25;

    for (let i = 0; i < particleCount; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        const icon = icons[Math.floor(Math.random() * icons.length)];
        const size = Math.random() * 14 + 10;
        const duration = Math.random() * 15 + 10;
        const delay = Math.random() * 12;
        const drift = (Math.random() - 0.5) * 250;
        const opacity = Math.random() * 0.15 + 0.05;
        const color = ['#0D1B4A', '#2E4AD6', '#5B72E0'][Math.floor(Math.random() * 3)];

        particle.innerHTML = `<i class="fas ${icon}" style="color:${color};font-size:${size}px;"></i>`;
        particle.style.cssText = `
            left: ${Math.random() * 100}%;
            --duration: ${duration}s;
            --delay: ${delay}s;
            --drift: ${drift}px;
            --opacity: ${opacity};
            animation-delay: ${delay}s;
        `;

        container.appendChild(particle);
    }
}

// ============================================
// 3D TILT
// ============================================
document.querySelectorAll('.tilt-card').forEach(card => {
    card.addEventListener('mousemove', (e) => {
        if (window.innerWidth <= 768) return;
        const rect = card.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;
        const centerX = rect.width / 2;
        const centerY = rect.height / 2;
        const rotateX = ((y - centerY) / centerY) * -8;
        const rotateY = ((x - centerX) / centerX) * 8;

        card.style.setProperty('--rotateX', rotateX + 'deg');
        card.style.setProperty('--rotateY', rotateY + 'deg');
    });

    card.addEventListener('mouseleave', () => {
        card.style.setProperty('--rotateX', '0deg');
        card.style.setProperty('--rotateY', '0deg');
    });
});

// ============================================
// BUTTON RIPPLE
// ============================================
document.querySelectorAll('.btn-ripple').forEach(btn => {
    btn.addEventListener('click', function(e) {
        const rect = this.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;
        const ripple = document.createElement('span');
        ripple.style.cssText = `
            position: absolute;
            top: ${y}px;
            left: ${x}px;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255,255,255,0.3);
            transform: translate(-50%, -50%);
            pointer-events: none;
            transition: width 0.6s ease, height 0.6s ease;
        `;
        this.appendChild(ripple);
        setTimeout(() => {
            ripple.style.width = '300px';
            ripple.style.height = '300px';
        }, 10);
        setTimeout(() => {
            ripple.remove();
        }, 700);
    });
});

// ============================================
// ACTIVE NAV LINK
// ============================================
const sections = document.querySelectorAll('section');
const navLinkItems = document.querySelectorAll('.nav-links a');

window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(section => {
        const sectionTop = section.offsetTop - 120;
        if (scrollY >= sectionTop) {
            current = section.getAttribute('id');
        }
    });
    navLinkItems.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === `#${current}`) {
            link.classList.add('active');
        }
    });
});

// ============================================
// STATS COUNTER (Hero stats)
// ============================================
const counters = document.querySelectorAll('.counter');

const counterObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            const target = parseInt(entry.target.getAttribute('data-target'));
            const suffix = entry.target.getAttribute('data-suffix') || '';
            const duration = 2000;
            const startTime = performance.now();

            function updateCounter(currentTime) {
                const elapsed = currentTime - startTime;
                const progress = Math.min(elapsed / duration, 1);
                const eased = 1 - Math.pow(1 - progress, 3);
                const current = Math.floor(eased * target);
                entry.target.textContent = current + suffix;

                if (progress < 1) {
                    requestAnimationFrame(updateCounter);
                } else {
                    entry.target.textContent = target + suffix;
                }
            }
            requestAnimationFrame(updateCounter);
            counterObserver.unobserve(entry.target);
        }
    });
}, { threshold: 0.3 });

counters.forEach(counter => {
    counterObserver.observe(counter);
});

// ============================================
// TRUST BADGE COUNTERS
// ============================================
const trustNumbers = document.querySelectorAll('.trust-number');

const trustObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            const target = parseInt(entry.target.getAttribute('data-count'));
            const suffix = entry.target.getAttribute('data-suffix') || '';
            const duration = 1800;
            const startTime = performance.now();

            function updateTrustNumber(currentTime) {
                const elapsed = currentTime - startTime;
                const progress = Math.min(elapsed / duration, 1);
                const eased = 1 - Math.pow(1 - progress, 3);
                const current = Math.floor(eased * target);
                entry.target.textContent = current + suffix;

                if (progress < 1) {
                    requestAnimationFrame(updateTrustNumber);
                } else {
                    entry.target.textContent = target + suffix;
                }
            }
            requestAnimationFrame(updateTrustNumber);
            trustObserver.unobserve(entry.target);
        }
    });
}, { threshold: 0.3 });

trustNumbers.forEach(num => {
    trustObserver.observe(num);
});

// ============================================
// CASE STUDY MODAL
// ============================================
const caseStudies = {
    telehealth: {
        title: "Telehealth Patient Triage System",
        subtitle: "Virtual triage and intake for a busy maternal health clinic",
        problem: "A maternal health clinic was overwhelmed with patient inquiries and had no structured system for triaging urgent vs. routine cases. Patients experienced long wait times, and critical cases were sometimes missed.",
        process: "Developed a structured triage protocol for virtual patient intake. Implemented a system for categorizing patient concerns (urgent, semi-urgent, routine) and escalated critical cases immediately to the attending physician. Created patient communication templates to streamline follow-ups.",
        result: "✅ Reduced patient wait times by 40%. Ensured urgent cases were prioritized and attended to within 30 minutes. Improved patient satisfaction scores significantly.",
        tools: ["Telehealth Platforms", "Patient Triage", "Communication Protocols"]
    },
    maternal: {
        title: "Maternal Health Education Program",
        subtitle: "Patient education and support for new mothers",
        problem: "New mothers in the clinic's catchment area had limited access to postnatal education and support, leading to anxiety, low breastfeeding rates, and missed follow-up appointments.",
        process: "Designed and implemented a structured patient education program covering newborn care, breastfeeding support, postnatal recovery, and warning signs. Created easy-to-understand educational materials and conducted virtual follow-up sessions.",
        result: "✅ Increased breastfeeding initiation rates by 35%. Improved postnatal follow-up attendance by 50%. Received positive feedback from mothers on the clarity and support provided.",
        tools: ["Patient Education", "Virtual Support", "Health Literacy"]
    },
    documentation: {
        title: "SOAP Documentation System",
        subtitle: "Standardized clinical documentation workflow for telehealth",
        problem: "The telehealth team lacked a standardized documentation format, leading to inconsistent records, missed clinical details, and challenges in care coordination.",
        process: "Implemented a SOAP (Subjective, Objective, Assessment, Plan) documentation framework across the team. Created templates and provided training to ensure consistency. Integrated the system into existing telehealth workflows.",
        result: "✅ Achieved 100% compliance with SOAP documentation within 4 weeks. Improved care coordination and reduced errors in patient records. Enhanced team communication and handover efficiency.",
        tools: ["SOAP Documentation", "EHR Systems", "Clinical Workflow"]
    }
};

const modalOverlay = document.getElementById('caseModal');
const modalContent = document.getElementById('modalContent');
const modalClose = document.getElementById('modalClose');

document.querySelectorAll('.work-new').forEach(card => {
    card.addEventListener('click', function() {
        const caseKey = this.dataset.case;
        const study = caseStudies[caseKey];
        if (!study) return;

        modalContent.innerHTML = `
            <h2>${study.title}</h2>
            <p class="modal-subtitle">${study.subtitle}</p>

            <div class="modal-section">
                <h3><i class="fas fa-exclamation-triangle" style="color:var(--primary-light);"></i> The Challenge</h3>
                <p>${study.problem}</p>
            </div>

            <div class="modal-section">
                <h3><i class="fas fa-cogs" style="color:var(--primary-light);"></i> What I Did</h3>
                <p>${study.process}</p>
            </div>

            <div class="modal-section">
                <h3><i class="fas fa-chart-line" style="color:var(--primary-light);"></i> The Outcome</h3>
                <div class="modal-result">
                    <p>${study.result.replace(/\n/g, '<br>')}</p>
                </div>
            </div>

            <div class="modal-section" style="margin-bottom:0;">
                <h3><i class="fas fa-tools" style="color:var(--primary-light);"></i> Tools Used</h3>
                <div class="modal-tags">
                    ${study.tools.map(tool => `<span>${tool}</span>`).join('')}
                </div>
            </div>
        `;

        modalOverlay.classList.add('active');
        document.body.style.overflow = 'hidden';
    });
});

function closeModal() {
    modalOverlay.classList.remove('active');
    document.body.style.overflow = 'auto';
}

modalClose.addEventListener('click', closeModal);

modalOverlay.addEventListener('click', function(e) {
    if (e.target === this) {
        closeModal();
    }
});

document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') {
        closeModal();
    }
});

// ============================================
// WORK SAMPLES – SMOOTH CONTINUOUS CAROUSEL
// ============================================
(function initContinuousCarousel() {
    const track = document.getElementById('workSamplesTrack');
    if (!track) return;

    let scrollPos = 0;
    let animationId = null;
    let isPaused = false;
    let speed = 0.7;
    let totalScrollWidth = 0;
    let itemWidth = 0;
    const gap = 24;
    const ORIGINAL_ITEM_COUNT = 10;

    function getItems() {
        return track.querySelectorAll('.work-sample-item');
    }

    function calculateDimensions() {
        const items = getItems();
        if (items.length === 0) return;
        const firstItem = items[0];
        if (!firstItem) return;
        itemWidth = firstItem.offsetWidth;
        totalScrollWidth = (itemWidth + gap) * ORIGINAL_ITEM_COUNT;
    }

    function animate() {
        if (!isPaused && totalScrollWidth > 0) {
            scrollPos += speed;
            if (scrollPos >= totalScrollWidth) {
                scrollPos = 0;
            }
            track.style.transform = 'translateX(-' + scrollPos + 'px)';
        }
        animationId = requestAnimationFrame(animate);
    }

    function startCarousel() {
        calculateDimensions();
        if (animationId) cancelAnimationFrame(animationId);
        scrollPos = 0;
        animate();
    }

    setTimeout(startCarousel, 150);

    const wrapper = document.querySelector('.work-samples-carousel-wrapper');
    if (wrapper) {
        wrapper.addEventListener('mouseenter', function() {
            isPaused = true;
        });
        wrapper.addEventListener('mouseleave', function() {
            isPaused = false;
        });
    }

    let resizeTimer;
    window.addEventListener('resize', function() {
        clearTimeout(resizeTimer);
        resizeTimer = setTimeout(function() {
            calculateDimensions();
            if (scrollPos >= totalScrollWidth) {
                scrollPos = 0;
            }
        }, 300);
    });

    const section = document.getElementById('work-samples');
    if (section && 'IntersectionObserver' in window) {
        const obs = new IntersectionObserver(function(entries) {
            entries.forEach(function(entry) {
                if (entry.isIntersecting) {
                    setTimeout(calculateDimensions, 200);
                }
            });
        }, { threshold: 0.1 });
        obs.observe(section);
    }

    window.__carousel = {
        setSpeed: function(s) { speed = s; },
        getSpeed: function() { return speed; },
        pause: function() { isPaused = true; },
        resume: function() { isPaused = false; }
    };
})();

// ============================================
// TESTIMONIALS AUTO CAROUSEL (2 Items)
// ============================================
const track = document.getElementById('testimonialCarouselTrack');
const dotsContainer = document.getElementById('testimonialDots');
const items = track ? track.querySelectorAll('.testimonial-carousel-item') : [];
const totalItems = items.length;
let currentIndex = 0;
let autoSlideInterval;
let isTransitioning = false;

function getItemsPerView() {
    if (window.innerWidth < 768) return 1;
    if (window.innerWidth < 1024) return 2;
    return 2; // Max 2 items since we only have 2 testimonials
}

function createDots() {
    if (!dotsContainer) return;
    const itemsPerView = getItemsPerView();
    const totalDots = Math.ceil(totalItems / itemsPerView);
    dotsContainer.innerHTML = '';
    for (let i = 0; i < totalDots; i++) {
        const dot = document.createElement('button');
        dot.className = 'dot' + (i === 0 ? ' active' : '');
        dot.addEventListener('click', function() {
            goToSlide(i * itemsPerView);
            resetAutoSlide();
        });
        dotsContainer.appendChild(dot);
    }
}

function goToSlide(index) {
    if (!track) return;
    if (isTransitioning) return;
    isTransitioning = true;

    const itemsPerView = getItemsPerView();
    const maxIndex = totalItems - itemsPerView;
    currentIndex = Math.min(index, maxIndex);
    if (currentIndex < 0) currentIndex = 0;

    const gap = 30;
    const itemWidth = items[0] ? items[0].offsetWidth : 300;
    const offset = currentIndex * (itemWidth + gap);
    track.style.transform = 'translateX(-' + offset + 'px)';

    const dots = dotsContainer ? dotsContainer.querySelectorAll('.dot') : [];
    const activeDotIndex = Math.floor(currentIndex / itemsPerView);
    dots.forEach(function(dot, i) {
        dot.classList.toggle('active', i === activeDotIndex);
    });

    setTimeout(function() {
        isTransitioning = false;
    }, 800);
}

function nextSlide() {
    const itemsPerView = getItemsPerView();
    const maxIndex = totalItems - itemsPerView;
    if (currentIndex + itemsPerView >= maxIndex) {
        goToSlide(0);
    } else {
        goToSlide(currentIndex + itemsPerView);
    }
}

function startAutoSlide() {
    if (autoSlideInterval) clearInterval(autoSlideInterval);
    autoSlideInterval = setInterval(nextSlide, 4000);
}

function resetAutoSlide() {
    if (autoSlideInterval) {
        clearInterval(autoSlideInterval);
        startAutoSlide();
    }
}

if (track && items.length > 0) {
    createDots();
    startAutoSlide();

    let resizeTimeout;
    window.addEventListener('resize', function() {
        clearTimeout(resizeTimeout);
        resizeTimeout = setTimeout(function() {
            createDots();
            goToSlide(currentIndex);
            resetAutoSlide();
        }, 300);
    });

    const carouselWrapper = document.querySelector('.testimonial-carousel-wrapper');
    if (carouselWrapper) {
        carouselWrapper.addEventListener('mouseenter', function() {
            clearInterval(autoSlideInterval);
        });
        carouselWrapper.addEventListener('mouseleave', function() {
            startAutoSlide();
        });
    }
}

// ============================================
// VIDEO SECTION FADE-IN ON SCROLL
// ============================================
const videoSection = document.querySelector('.intro-video');
if (videoSection) {
    const videoObserver = new IntersectionObserver(function(entries) {
        entries.forEach(function(entry) {
            if (entry.isIntersecting) {
                videoSection.style.opacity = '1';
                videoSection.style.transform = 'translateY(0)';
            }
        });
    }, { threshold: 0.2 });
    videoSection.style.opacity = '0';
    videoSection.style.transform = 'translateY(30px)';
    videoSection.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
    videoObserver.observe(videoSection);
}

// ============================================
// VIDEO SOUND TOGGLE
// ============================================
const video = document.getElementById('introVideo');
const soundToggle = document.getElementById('soundToggle');

if (video && soundToggle) {
    function updateSoundIcon() {
        const icon = soundToggle.querySelector('i');
        if (video.muted) {
            icon.className = 'fas fa-volume-mute';
        } else {
            icon.className = 'fas fa-volume-up';
        }
    }

    soundToggle.addEventListener('click', function(e) {
        e.stopPropagation();
        video.muted = !video.muted;
        updateSoundIcon();
    });

    video.play().catch(function() {
        document.addEventListener('click', function playOnClick() {
            video.play();
            document.removeEventListener('click', playOnClick);
        }, { once: true });
    });

    updateSoundIcon();
}

// ============================================
// CONTACT FORM – AJAX (fetch) with auto-reset
// ============================================
const form = document.getElementById('contactForm');
if (form) {
    form.addEventListener('submit', function(e) {
        e.preventDefault();
        const btn = this.querySelector('.btn');
        const originalText = btn.innerHTML;
        btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Sending...';
        btn.disabled = true;

        fetch(this.action, {
            method: 'POST',
            body: new FormData(this),
            headers: { 'Accept': 'application/json' }
        })
        .then(response => {
            if (response.ok) {
                alert('✅ Message sent successfully! I\'ll get back to you soon.');
                this.reset();
            } else {
                alert('❌ Something went wrong. Please try again.');
            }
        })
        .catch(() => {
            alert('❌ Network error. Please check your connection and try again.');
        })
        .finally(() => {
            btn.innerHTML = originalText;
            btn.disabled = false;
        });
    });
}

// ============================================
// BACK TO TOP
// ============================================
const backToTopBtn = document.getElementById('backToTop');

if (backToTopBtn) {
    window.addEventListener('scroll', function() {
        if (window.scrollY > 400) {
            backToTopBtn.classList.add('visible');
        } else {
            backToTopBtn.classList.remove('visible');
        }
    });

    backToTopBtn.addEventListener('click', function() {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
    });
}

// ============================================
// INITIALIZE
// ============================================
document.addEventListener('DOMContentLoaded', function() {
    createParticles();
    setTimeout(initECG, 500);

    let particleTimeout;
    window.addEventListener('resize', function() {
        clearTimeout(particleTimeout);
        particleTimeout = setTimeout(function() {
            const container = document.getElementById('particlesContainer');
            if (container) container.innerHTML = '';
            createParticles();
        }, 500);
    });
});

console.log('🩺 Lilian Nyong · Registered Nurse · Telehealth Portfolio with continuous carousel ready!');
