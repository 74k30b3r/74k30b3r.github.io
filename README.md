E<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>74k30v3r | Home</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;500;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        orbitron: ['Orbitron', 'sans-serif'],
                        rajdhani: ['Rajdhani', 'sans-serif'],
                    },
                    colors: {
                        neon: {
                            blue: '#068ec4',
                            purple: '#322378',
                            green: '#389e31',
                            silver: '#c0c0c0',
                        },
                        dark: {
                            base: '#1b1b87',
                            surface: 'rgba(15, 15, 30, 0.3)',
                        }
                    },
                    animation: {
                        'pulse-slow': 'pulse 4s cubic-bezier(.09,1.24,.73,-0.99) infinite',
                        'float': 'float 8s ease-in-out infinite',
                        'glow': 'glow 4s ease-in-out infinite alternate',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-24px)' },
                        },
                        glow: {
                            'from': { boxShadow: '0 0 10px #00f3ff, 0 0 20px #00f3ff' },
                            'to': { boxShadow: '0 0 20px #bd00ff, 0 0 30px #bd00ff' },
                        }
                    }
                }
            }
        }
    </script>
    
    <style>
        body {
            /* 3-way center gradient: Black -> Royal Purple -> Black */
            background: radial-gradient(circle at center, #000000 0%, #7851A9 50%, #000000 100%);
            background-attachment: fixed;
            color: #e2e8f0;
            overflow-x: hidden;
            min-height: 100vh;
        }
        
        /* Glassmorphism utilities */
        .glass {
            background: rgba(20, 20, 40, 0.4);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(0, 243, 255, 0.2);
        }

        .glass-card {
            background: linear-gradient(135deg, rgba(20,20,40,0.6) 0%, rgba(10,10,20,0.8) 100%);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(189, 0, 255, 0.3);
            transition: all 0.3s ease;
        }

        .glass-card:hover {
            border-color: rgba(0, 243, 255, 0.8);
            box-shadow: 0 0 25px rgba(0, 243, 255, 0.2);
            transform: translateY(-5px);
        }

        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #000000;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #7851A9, #000000);
            border-radius: 4px;
        }

        /* Glitch text effect on hover */
        .glitch-hover:hover {
            animation: glitch 0.2s linear infinite;
            color: #00f3ff;
            text-shadow: 2px 0 #c0c0c0, -2px 0 #bd00ff;
        }

        @keyframes glitch {
            0% { transform: translate(0) }
            20% { transform: translate(-2px, 2px) }
            40% { transform: translate(-2px, -2px) }
            60% { transform: translate(2px, 2px) }
            80% { transform: translate(2px, -2px) }
            100% { transform: translate(0) }
        }
    </style>
</head>
<body class="font-rajdhani antialiased selection:bg-neon-silver selection:text-white">

    <!-- Fixed particle canvas background -->
    <canvas id="bg-canvas" class="fixed top-0 left-0 w-full h-full -z-10"></canvas>

    <header class="fixed w-full top-0 z-50 glass transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center">
                    <a href="index.html" class="font-orbitron text-3xl font-black tracking-widest text-transparent bg-clip-text bg-gradient-to-r from-neon-blue via-neon-purple to-neon-purple glitch-hover transition-all duration-300">
                        74K30V3R
                    </a>
                </div>
                
                <!-- Desktop Nav -->
                <nav class="hidden md:flex space-x-8">
                    <a href="index.html" class="text-neon-blue font-bold text-lg hover:text-neon-silver transition-colors relative group">
                        HOME
                        <span class="absolute -bottom-1 left-0 w-full h-0.5 bg-neon-blue scale-x-100 transition-transform origin-left"></span>
                    </a>
                    <a href="news.html" class="text-gray-300 hover:text-neon-blue font-medium text-lg transition-colors relative group">
                        NEWS
                        <span class="absolute -bottom-1 left-0 w-full h-0.5 bg-neon-blue scale-x-0 group-hover:scale-x-100 transition-transform origin-left"></span>
                    </a>
                    <a href="products.html" class="text-gray-300 hover:text-neon-blue font-medium text-lg transition-colors relative group">
                        PRODUCTS
                        <span class="absolute -bottom-1 left-0 w-full h-0.5 bg-neon-blue scale-x-0 group-hover:scale-x-100 transition-transform origin-left"></span>
                    </a>
                    <a href="contacts.html" class="text-gray-300 hover:text-neon-blue font-medium text-lg transition-colors relative group">
                        CONTACT
                        <span class="absolute -bottom-1 left-0 w-full h-0.5 bg-neon-blue scale-x-0 group-hover:scale-x-100 transition-transform origin-left"></span>
                    </a>
                </nav>

                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-neon-blue hover:text-white focus:outline-none p-2">
                        <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Nav Menu (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden glass border-t border-neon-blue/20">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 flex flex-col">
                <a href="index.html" class="text-neon-blue block px-3 py-2 rounded-md text-base font-bold bg-white/5">HOME</a>
                <a href="news.html" class="text-gray-300 hover:text-neon-blue block px-3 py-2 rounded-md text-base font-medium">NEWS</a>
                <a href="products.html" class="text-gray-300 hover:text-neon-blue block px-3 py-2 rounded-md text-base font-medium">PRODUCTS</a>
                <a href="contacts.html" class="text-gray-300 hover:text-neon-blue block px-3 py-2 rounded-md text-base font-medium">CONTACT</a>
            </div>
        </div>
    </header>

    <main class="pt-20">
        <!-- Hero -->
        <!-- Removed opaque background classes so the body background gradient shines through -->
        <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
            <!-- Decorative background elements -->
            <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-neon-purple/20 rounded-full filter blur-[100px] animate-pulse-slow"></div>
            <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-neon-blue/20 rounded-full mix-blend-screen filter blur-[100px] animate-pulse-slow" style="animation-delay: 2s;"></div>

            <div class="relative z-10 text-center px-4 max-w-5xl mx-auto">
                <h1 class="font-orbitron text-5xl md:text-7xl lg:text-8xl font-black mb-6 tracking-tight">
                    <span class="block text-transparent bg-clip-text bg-gradient-to-r from-white to-gray-400">INITIATE</span>
                    <span class="block mt-2 text-transparent bg-clip-text bg-gradient-to-r from-neon-blue via-neon-purple to-neon-silver drop-shadow-[0_0_15px_rgba(0,243,255,0.5)]">
                        THE TAKEOVER
                    </span>
                </h1>
                
                <p class="mt-6 text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto font-light leading-relaxed">
                    Step into the next evolution of digital presence. Cozy aesthetics meet cyberpunk reality in a seamless, high-performance environment.
                </p>

                <div class="mt-12 flex flex-col sm:flex-row gap-6 justify-center">
                    <a href="products.html" class="group relative px-8 py-4 font-orbitron font-bold text-lg rounded-lg bg-transparent text-white overflow-hidden border border-neon-blue transition-all duration-300 hover:border-transparent hover:shadow-[0_0_20px_#00f3ff]">
                        <span class="absolute inset-0 w-full h-full bg-gradient-to-r from-neon-blue to-neon-purple opacity-0 group-hover:opacity-100 transition-opacity duration-300 -z-10"></span>
                        EXPLORE TECH
                    </a>
                    <a href="news.html" class="group px-8 py-4 font-orbitron font-bold text-lg rounded-lg bg-white/5 text-gray-300 border border-white/10 hover:bg-white/10 hover:text-white transition-all duration-300 backdrop-blur-sm">
                        LATEST INTEL
                    </a>
                </div>
            </div>

            <!-- Scroll indicator -->
            <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 flex flex-col items-center animate-bounce">
                <span class="text-sm font-orbitron text-gray-400 mb-2 tracking-widest">SCROLL</span>
                <svg class="w-6 h-6 text-neon-blue" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
                </svg>
            </div>
        </section>

        <section class="py-24 relative z-10">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="font-orbitron text-3xl md:text-5xl font-bold text-white mb-4">SYSTEM <span class="text-neon-silver">CAPABILITIES</span></h2>
                    <div class="h-1 w-24 bg-gradient-to-r from-neon-blue to-neon-purple mx-auto rounded-full"></div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Feature Card 1 -->
                    <div class="glass-card p-8 rounded-2xl flex flex-col items-center text-center">
                        <div class="w-16 h-16 rounded-full bg-neon-blue/10 flex items-center justify-center mb-6 text-neon-blue border border-neon-blue/30 shadow-[0_0_15px_rgba(0,243,255,0.2)]">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                        </div>
                        <h3 class="text-2xl font-orbitron font-bold text-white mb-3">Hyper-Speed</h3>
                        <p class="text-gray-400">Optimized rendering and seamless transitions ensure your data is processed at the speed of thought.</p>
                    </div>

                    <!-- Feature Card 2 -->
                    <div class="glass-card p-8 rounded-2xl flex flex-col items-center text-center mt-0 md:mt-12">
                        <div class="w-16 h-16 rounded-full bg-neon-purple/10 flex items-center justify-center mb-6 text-neon-purple border border-neon-purple/30 shadow-[0_0_15px_rgba(189,0,255,0.2)]">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 11c0 3.517-1.009 6.799-2.753 9.571m-3.44-2.04l.054-.09A13.916 13.916 0 008 11a4 4 0 118 0c0 1.017-.07 2.019-.203 3m-2.118 6.844A21.88 21.88 0 0015.171 17m3.839 1.132c.645-2.266.99-4.659.99-7.132A8 8 0 008 4.07M3 15.364c.64-1.319 1-2.8 1-4.364 0-1.457.39-2.823 1.07-4"></path></svg>
                        </div>
                        <h3 class="text-2xl font-orbitron font-bold text-white mb-3">Neural Security</h3>
                        <p class="text-gray-400">Advanced encryption protocols wrapping every interaction in an impenetrable digital fortress.</p>
                    </div>

                    <!-- Feature Card 3 -->
                    <div class="glass-card p-8 rounded-2xl flex flex-col items-center text-center">
                        <div class="w-16 h-16 rounded-full bg-neon-silver/10 flex items-center justify-center mb-6 text-neon-silver border border-neon-silver/30 shadow-[0_0_15px_rgba(192,192,192,0.2)]">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01"></path></svg>
                        </div>
                        <h3 class="text-2xl font-orbitron font-bold text-white mb-3">Adaptive UI</h3>
                        <p class="text-gray-400">Interfaces that learn and adapt to your preferences, creating a cozy yet futuristic user experience.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Multimedia / Content Panels -->
        <section class="py-12 relative z-10 w-full">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-8">
                
                <!-- Panel 1: Channel Info -->
                <div class="glass-card p-6 md:p-8 rounded-2xl flex flex-col md:flex-row items-center justify-between border-t-2 border-t-neon-blue/50">
                    <div class="mb-6 md:mb-0 text-center md:text-left flex flex-col items-center md:items-start">
                        <h3 class="text-2xl font-orbitron font-bold text-white mb-2">SUBSCRIBE TO<span class="text-neon-silver">T4K30V3RS YT</span></h3>
                        <p class="text-gray-400">Content Worth Watching</p>
                    </div>
                    <a href="https://www.youtube.com/@buffsrightout" target="_blank" class="group relative px-6 py-3 font-orbitron font-bold text-sm rounded-lg bg-transparent text-white overflow-hidden border border-neon-silver transition-all duration-300 hover:border-transparent hover:shadow-[0_0_15px_#c0c0c0]">
                        <span class="absolute inset-0 w-full h-full bg-gradient-to-r from-neon-blue to-neon-purple opacity-0 group-hover:opacity-100 transition-opacity duration-300 -z-10"></span>
                        SUBSCRIBE ON YOUTUBE
                    </a>
                </div>

                <!-- Panel 2: Video Player -->
                <div class="glass-card p-4 md:p-8 rounded-2xl flex items-center justify-center border-t-2 border-t-neon-purple/50">
                    <div class="w-full max-w-4xl aspect-video rounded-xl overflow-hidden border border-neon-silver/30 shadow-[0_0_20px_rgba(192,192,192,0.15)] relative bg-black/50">
                        <!-- Updated embed code with user's si parameter, modified for responsive sizing and autoplay -->
                        <iframe 
                            class="absolute top-0 left-0 w-full h-full" 
                            src="https://www.youtube.com/embed/Sp682BqIRss?si=UVg0TQfMxZdD1Q_m&autoplay=1&mute=1" 
                            title="YouTube video player" 
                            frameborder="0" 
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                            referrerpolicy="strict-origin-when-cross-origin" 
                            allowfullscreen>
                        </iframe>
                    </div>
                </div>

                <!-- Panel 3: Status -->
                <div class="glass-card p-6 md:p-8 rounded-2xl flex flex-col md:flex-row items-center justify-between text-center md:text-left border-t-2 border-t-neon-silver/50">
                    <div>
                        <h3 class="text-xl font-orbitron font-bold text-white mb-2">NETWORK SECURE</h3>
                        <p class="text-gray-400 text-sm md:text-base">Streaming encrypted visual data packets successfully.</p>
                    </div>
                    <div class="mt-4 md:mt-0 flex gap-4">
                        <div class="h-2 w-12 bg-neon-purple rounded-full animate-pulse-slow"></div>
                        <div class="h-2 w-12 bg-neon-blue rounded-full animate-pulse-slow" style="animation-delay: 0.5s;"></div>
                        <div class="h-2 w-12 bg-neon-silver rounded-full animate-pulse-slow" style="animation-delay: 1s;"></div>
                    </div>
                </div>
                
            </div>
        </section>

        <!-- Ad Panel Section -->
        <section class="py-12 relative z-10 w-full">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="w-full h-40 md:h-72 rounded-2xl border border-neon-silver/50 flex flex-col items-center justify-center shadow-[0_0_25px_rgba(192,192,192,0.25)] relative overflow-hidden group transition-all duration-300 hover:border-neon-silver hover:shadow-[0_0_35px_rgba(192,192,192,0.4)]" style="background: radial-gradient(circle at center, #7851A9 0%, #c0c0c0 100%);">
                    <div class="absolute inset-0 bg-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                    <span class="font-orbitron font-black tracking-[0.4em] text-black/50 text-lg md:text-2xl z-10">ADVERTISEMENT</span>
                </div>
            </div>
        </section>

    </main>

    <footer class="border-t border-white/10 glass mt-20 relative z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <span class="font-orbitron text-2xl font-bold text-white">74K30V3R<span class="text-neon-silver">.COM</span></span>
                    <p class="text-gray-500 mt-2 text-sm">Forging the future of the web.</p>
                </div>
                <div class="flex space-x-6">
                    <a href="74k30v3r.html" class="text-gray-400 hover:text-neon-blue transition-colors">Home</a>
                    <a href="News.html" class="text-gray-400 hover:text-neon-blue transition-colors">News</a>
                    <a href="Products.html" class="text-gray-400 hover:text-neon-blue transition-colors">Products</a>
                    <a href="Contacts.html" class="text-gray-400 hover:text-neon-blue transition-colors">Contact</a>
                </div>
            </div>
            <div class="mt-8 text-center text-gray-600 text-sm">
                &copy; 2026 74K30V3R Corp. All rights reserved. System Online.
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const btn = document.getElementById('mobile-menu-btn');
        const menu = document.getElementById('mobile-menu');

        btn.addEventListener('click', () => {
            menu.classList.toggle('hidden');
        });

        // Navbar blur effect on scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 20) {
                navbar.classList.add('bg-black/80', 'backdrop-blur-md', 'shadow-lg', 'shadow-neon-blue/5');
                navbar.classList.remove('glass');
            } else {
                navbar.classList.remove('bg-black/80', 'backdrop-blur-md', 'shadow-lg', 'shadow-neon-blue/5');
                navbar.classList.add('glass');
            }
        });

        // --- Interactive Particle Background ---
        const canvas = document.getElementById('bg-canvas');
        const ctx = canvas.getContext('2d');
        
        let width, height, particles;

        function resize() {
            width = canvas.width = window.innerWidth;
            height = canvas.height = window.innerHeight;
        }

        class Particle {
            constructor() {
                this.x = Math.random() * width;
                this.y = Math.random() * height;
                this.vx = (Math.random() - 0.5) * 0.5;
                this.vy = (Math.random() - 0.5) * 0.5;
                this.size = Math.random() * 2 + 0.1;
                // Cyberpunk colors
                const colors = ['#00f3ff', '#bd00ff', '#4a5568'];
                this.color = colors[Math.floor(Math.random() * colors.length)];
                this.alpha = Math.random() * 0.5 + 0.1;
            }

            update(mouseX, mouseY) {
                this.x += this.vx;
                this.y += this.vy;

                // Screen wrap
                if (this.x < 0) this.x = width;
                if (this.x > width) this.x = 0;
                if (this.y < 0) this.y = height;
                if (this.y > height) this.y = 0;

                // Mouse interaction - gentle repulsion
                if (mouseX !== null && mouseY !== null) {
                    const dx = mouseX - this.x;
                    const dy = mouseY - this.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    if (distance < 150) {
                        const force = (150 - distance) / 150;
                        this.x -= (dx / distance) * force * 2;
                        this.y -= (dy / distance) * force * 2;
                    }
                }
            }

            draw() {
                ctx.globalAlpha = this.alpha;
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function initParticles() {
            particles = [];
            const numParticles = Math.floor((width * height) / 15000); // density
            for (let i = 0; i < numParticles; i++) {
                particles.push(new Particle());
            }
        }

        let mouseX = null;
        let mouseY = null;

        window.addEventListener('mousemove', (e) => {
            mouseX = e.clientX;
            mouseY = e.clientY;
        });

        window.addEventListener('mouseout', () => {
            mouseX = null;
            mouseY = null;
        });

        function animate() {
            ctx.clearRect(0, 0, width, height);
            
            // Draw grid background subtle
            ctx.strokeStyle = 'rgba(0, 243, 255, 0.03)';
            ctx.lineWidth = 1;
            
            // Connecting lines between close particles
            for(let i=0; i<particles.length; i++) {
                particles[i].update(mouseX, mouseY);
                particles[i].draw();
                
                for(let j=i+1; j<particles.length; j++) {
                    const dx = particles[i].x - particles[j].x;
                    const dy = particles[i].y - particles[j].y;
                    const dist = dx*dx + dy*dy;
                    
                    if(dist < 10000) { // approx 100px
                        ctx.globalAlpha = ((10000 - dist) / 10000) * 0.2; // fade based on distance
                        ctx.strokeStyle = particles[i].color;
                        ctx.beginPath();
                        ctx.moveTo(particles[i].x, particles[i].y);
                        ctx.lineTo(particles[j].x, particles[j].y);
                        ctx.stroke();
                    }
                }
            }
            
            requestAnimationFrame(animate);
        }

        window.addEventListener('resize', () => {
            resize();
            initParticles();
        });

        // Initialize
        resize();
        initParticles();
        animate();
    </script>
</body>
</html>
