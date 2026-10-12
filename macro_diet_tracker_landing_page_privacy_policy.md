<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Macro Diet Tracker | Hit Your Macros & Reach Your Goals</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#ecfdf5',
                            100: '#d1fae5',
                            500: '#10b981',
                            600: '#059669',
                            700: '#047857',
                            900: '#064e3b',
                            dark: '#0b1329',
                            card: '#131c38',
                            border: '#1e294b'
                        }
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .glow-effect {
            box-shadow: 0 0 50px -10px rgba(16, 185, 129, 0.25);
        }
        .glow-button {
            box-shadow: 0 10px 25px -5px rgba(16, 185, 129, 0.4);
        }
    </style>
</head>
<body class="bg-brand-dark text-slate-100 antialiased selection:bg-brand-500 selection:text-white">

    <!-- Navigation Bar -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-brand-dark/80 backdrop-blur-md border-b border-brand-border">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <div class="flex items-center space-x-3 cursor-pointer" onclick="showPage('home')">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-brand-600 to-emerald-400 flex items-center justify-center glow-button">
                    <i class="fa-solid fa-bolt text-white text-lg"></i>
                </div>
                <span class="text-xl font-extrabold tracking-tight bg-gradient-to-r from-white via-slate-200 to-brand-400 bg-clip-text text-transparent">
                    MacroDiet Tracker
                </span>
            </div>
            
            <div class="hidden md:flex items-center space-x-8 text-sm font-medium text-slate-300">
                <button onclick="showPage('home')" class="hover:text-brand-400 transition bg-transparent border-0 cursor-pointer text-slate-300 font-medium text-sm">Home</button>
                <a href="#features" onclick="showPage('home')" class="hover:text-brand-400 transition">Features</a>
                <a href="#calculator" onclick="showPage('home')" class="hover:text-brand-400 transition">Macro Calculator</a>
                <a href="#preview" onclick="showPage('home')" class="hover:text-brand-400 transition">App Preview</a>
                <button onclick="showPage('privacy')" class="hover:text-brand-400 transition bg-transparent border-0 cursor-pointer text-slate-300 font-medium text-sm">Privacy Policy</button>
            </div>

            <div class="flex items-center space-x-4">
                <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="hidden sm:inline-flex items-center space-x-2 bg-brand-600 hover:bg-brand-500 text-white font-semibold px-5 py-2.5 rounded-xl transition glow-button text-sm">
                    <i class="fa-brands fa-google-play text-base"></i>
                    <span>Get App</span>
                </a>
                <button id="mobile-menu-btn" class="md:hidden text-slate-300 hover:text-white text-xl focus:outline-none">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-brand-card border-b border-brand-border px-4 pt-2 pb-6 space-y-3">
            <button onclick="showPage('home'); toggleMobileMenu();" class="block w-full text-left py-2 text-slate-300 hover:text-brand-400 font-medium bg-transparent border-0 cursor-pointer">Home</button>
            <a href="#features" onclick="showPage('home'); toggleMobileMenu();" class="block py-2 text-slate-300 hover:text-brand-400 font-medium">Features</a>
            <a href="#calculator" onclick="showPage('home'); toggleMobileMenu();" class="block py-2 text-slate-300 hover:text-brand-400 font-medium">Macro Calculator</a>
            <a href="#preview" onclick="showPage('home'); toggleMobileMenu();" class="block py-2 text-slate-300 hover:text-brand-400 font-medium">App Preview</a>
            <button onclick="showPage('privacy'); toggleMobileMenu();" class="block w-full text-left py-2 text-slate-300 hover:text-brand-400 font-medium bg-transparent border-0 cursor-pointer">Privacy Policy</button>
            <div class="pt-2">
                <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="w-full flex items-center justify-center space-x-2 bg-brand-600 hover:bg-brand-500 text-white font-semibold px-5 py-3 rounded-xl transition">
                    <i class="fa-brands fa-google-play"></i>
                    <span>Get on Google Play</span>
                </a>
            </div>
        </div>
    </nav>

    <!-- MAIN LANDING PAGE VIEW -->
    <div id="view-home">
        <header class="relative pt-32 pb-20 md:pt-44 md:pb-32 overflow-hidden">
            <!-- Background decorative glow -->
            <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-brand-500/10 blur-[120px] rounded-full pointer-events-none"></div>

            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
                <div class="grid lg:grid-cols-12 gap-12 items-center">
                    <div class="lg:col-span-7 text-center lg:text-left space-y-6">
                        <div class="inline-flex items-center space-x-2 px-3.5 py-1.5 rounded-full bg-brand-500/10 border border-brand-500/20 text-brand-400 text-xs font-semibold tracking-wide uppercase">
                            <span class="w-2 h-2 rounded-full bg-brand-500 animate-pulse"></span>
                            <span>Now Available on Google Play Store</span>
                        </div>
                        
                        <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight text-white leading-tight">
                            Hit Your Macros, Reach Your <span class="bg-gradient-to-r from-brand-400 to-emerald-300 bg-clip-text text-transparent">Goals Effortlessly</span>
                        </h1>
                        
                        <p class="text-lg sm:text-xl text-slate-300 max-w-2xl mx-auto lg:mx-0 font-normal">
                            The ultimate intelligent nutrition companion. Streamline your food logging, optimize your custom macros, and achieve peak body composition with zero guesswork.
                        </p>
                        
                        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start space-y-4 sm:space-y-0 sm:space-x-4 pt-4">
                            <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="w-full sm:w-auto flex items-center justify-center space-x-3 bg-gradient-to-r from-brand-600 to-emerald-500 hover:from-brand-500 hover:to-emerald-400 text-white font-bold px-8 py-4 rounded-2xl transition shadow-xl glow-button transform hover:-translate-y-0.5">
                                <i class="fa-brands fa-google-play text-2xl"></i>
                                <div class="text-left">
                                    <div class="text-[10px] uppercase tracking-wider opacity-80 font-medium">Download on</div>
                                    <div class="text-sm font-bold -mt-0.5">Google Play</div>
                                </div>
                            </a>
                            
                            <a href="#calculator" class="w-full sm:w-auto flex items-center justify-center space-x-2 bg-brand-card hover:bg-brand-border border border-brand-border text-white font-semibold px-8 py-4 rounded-2xl transition">
                                <span>Calculate Macros</span>
                                <i class="fa-solid fa-arrow-down text-sm"></i>
                            </a>
                        </div>

                        <div class="pt-6 flex items-center justify-center lg:justify-start space-x-8 text-slate-400 text-sm">
                            <div class="flex items-center space-x-2">
                                <i class="fa-solid fa-check text-brand-500"></i>
                                <span>Smart AI Logging</span>
                            </div>
                            <div class="flex items-center space-x-2">
                                <i class="fa-solid fa-check text-brand-500"></i>
                                <span>Gluten-Free Support</span>
                            </div>
                            <div class="flex items-center space-x-2">
                                <i class="fa-solid fa-check text-brand-500"></i>
                                <span>100% Free to Use</span>
                            </div>
                        </div>
                    </div>

                    <!-- Hero Graphic / Interactive App Mockup Preview -->
                    <div class="lg:col-span-5 flex justify-center">
                        <div class="relative w-full max-w-sm bg-brand-card border-2 border-brand-border rounded-[3rem] p-4 glow-effect shadow-2xl">
                            <!-- Phone Notch -->
                            <div class="absolute top-4 left-1/2 -translate-x-1/2 w-32 h-5 bg-brand-dark rounded-full z-20"></div>
                            
                            <!-- App Screen Container -->
                            <div class="bg-brand-dark rounded-[2.2rem] p-5 pt-8 space-y-5 text-left border border-brand-border overflow-hidden">
                                <div class="flex justify-between items-center">
                                    <div>
                                        <div class="text-xs text-slate-400">Daily Target</div>
                                        <div class="text-xl font-bold text-white">2,450 kcal</div>
                                    </div>
                                    <div class="w-10 h-10 rounded-full bg-brand-500/10 border border-brand-500/30 flex items-center justify-center text-brand-400 font-bold text-sm">
                                        84%
                                    </div>
                                </div>

                                <!-- Macro Progress Bars -->
                                <div class="space-y-3 bg-brand-card/70 p-4 rounded-2xl border border-brand-border">
                                    <div>
                                        <div class="flex justify-between text-xs mb-1 font-medium">
                                            <span class="text-emerald-400">Protein (180g)</span>
                                            <span class="text-slate-300">152 / 180g</span>
                                        </div>
                                        <div class="w-full bg-brand-dark h-2 rounded-full overflow-hidden">
                                            <div class="bg-emerald-500 h-full rounded-full" style="width: 85%"></div>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between text-xs mb-1 font-medium">
                                            <span class="text-cyan-400">Carbs (220g)</span>
                                            <span class="text-slate-300">190 / 220g</span>
                                        </div>
                                        <div class="w-full bg-brand-dark h-2 rounded-full overflow-hidden">
                                            <div class="bg-cyan-400 h-full rounded-full" style="width: 86%"></div>
                                        </div>
                                    </div>
                                    <div>
                                        <div class="flex justify-between text-xs mb-1 font-medium">
                                            <span class="text-amber-400">Fats (75g)</span>
                                            <span class="text-slate-300">62 / 75g</span>
                                        </div>
                                        <div class="w-full bg-brand-dark h-2 rounded-full overflow-hidden">
                                            <div class="bg-amber-400 h-full rounded-full" style="width: 82%"></div>
                                        </div>
                                    </div>
                                </div>

                                <!-- Recent Meal Log -->
                                <div class="space-y-2">
                                    <div class="text-xs font-semibold text-slate-400 uppercase tracking-wider">Today's Logs</div>
                                    <div class="bg-brand-card/90 p-3 rounded-xl border border-brand-border flex items-center justify-between">
                                        <div class="flex items-center space-x-3">
                                            <div class="w-8 h-8 rounded-lg bg-emerald-500/20 text-emerald-400 flex items-center justify-center text-xs font-bold">
                                                <i class="fa-solid fa-utensils"></i>
                                            </div>
                                            <div>
                                                <div class="text-xs font-semibold text-white">Grilled Chicken Salad</div>
                                                <div class="text-[10px] text-slate-400">Lunch • 450 kcal</div>
                                            </div>
                                        </div>
                                        <span class="text-xs font-bold text-brand-400">42g P</span>
                                    </div>
                                    <div class="bg-brand-card/90 p-3 rounded-xl border border-brand-border flex items-center justify-between">
                                        <div class="flex items-center space-x-3">
                                            <div class="w-8 h-8 rounded-lg bg-cyan-500/20 text-cyan-400 flex items-center justify-center text-xs font-bold">
                                                <i class="fa-solid fa-mug-hot"></i>
                                            </div>
                                            <div>
                                                <div class="text-xs font-semibold text-white">Protein Oats & Berries</div>
                                                <div class="text-[10px] text-slate-400">Breakfast • 380 kcal</div>
                                            </div>
                                        </div>
                                        <span class="text-xs font-bold text-brand-400">30g P</span>
                                    </div>
                                </div>

                                <div class="pt-2">
                                    <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="w-full block text-center py-2.5 bg-brand-600 hover:bg-brand-500 text-white rounded-xl text-xs font-bold transition">
                                        Open App Live Preview
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </header>

        <!-- Features Section -->
        <section id="features" class="py-24 bg-brand-card/40 border-y border-brand-border">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto space-y-4 mb-16">
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Engineered for Results, Designed for Simplicity</h2>
                    <p class="text-slate-300 text-base sm:text-lg">Everything you need to transform your physique, track nutrition accurately, and maintain consistent healthy habits.</p>
                </div>

                <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 space-y-4 hover:border-brand-500/50 transition group">
                        <div class="w-12 h-12 rounded-xl bg-brand-500/10 text-brand-400 flex items-center justify-center text-xl font-bold group-hover:scale-110 transition">
                            <i class="fa-solid fa-brain"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Smart Macro Logging</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Effortlessly log meals with lightning-fast search, barcode scanning, and intelligent AI portion estimators.
                        </p>
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 space-y-4 hover:border-brand-500/50 transition group">
                        <div class="w-12 h-12 rounded-xl bg-cyan-500/10 text-cyan-400 flex items-center justify-center text-xl font-bold group-hover:scale-110 transition">
                            <i class="fa-solid fa-sliders"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Custom Target Splits</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Tailor your protein, fat, and carbohydrate splits perfectly to your fitness goals—whether cutting, bulking, or recomp.
                        </p>
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 space-y-4 hover:border-brand-500/50 transition group">
                        <div class="w-12 h-12 rounded-xl bg-amber-500/10 text-amber-400 flex items-center justify-center text-xl font-bold group-hover:scale-110 transition">
                            <i class="fa-solid fa-chart-line"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Progress Insights</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Visualize daily and weekly streaks, weight trends, and nutrient adherence with clean, interactive analytics charts.
                        </p>
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-6 space-y-4 hover:border-brand-500/50 transition group">
                        <div class="w-12 h-12 rounded-xl bg-purple-500/10 text-purple-400 flex items-center justify-center text-xl font-bold group-hover:scale-110 transition">
                            <i class="fa-solid fa-seedling"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white">Dietary Friendly</h3>
                        <p class="text-slate-300 text-sm leading-relaxed">
                            Built-in filters and guidance for gluten-free lifestyles, keto, low-carb, and clean eating preferences.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Macro Calculator Section -->
        <section id="calculator" class="py-24 relative overflow-hidden">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
                <div class="text-center space-y-4 mb-12">
                    <span class="text-brand-400 text-xs font-bold uppercase tracking-widest px-3 py-1 bg-brand-500/10 rounded-full border border-brand-500/20">Interactive Tool</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Free Daily Macro Calculator</h2>
                    <p class="text-slate-300 text-sm sm:text-base">Input your stats below to instantly discover your optimal daily calorie and macronutrient breakdown.</p>
                </div>

                <div class="bg-brand-card border border-brand-border rounded-3xl p-6 sm:p-10 shadow-2xl">
                    <form id="macro-form" class="grid sm:grid-cols-2 gap-6">
                        <div>
                            <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Weight (lbs)</label>
                            <input type="number" id="weight" value="170" required class="w-full bg-brand-dark border border-brand-border rounded-xl px-4 py-3 text-white focus:outline-none focus:border-brand-500 transition">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Height (inches)</label>
                            <input type="number" id="height" value="70" required class="w-full bg-brand-dark border border-brand-border rounded-xl px-4 py-3 text-white focus:outline-none focus:border-brand-500 transition">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Age (years)</label>
                            <input type="number" id="age" value="28" required class="w-full bg-brand-dark border border-brand-border rounded-xl px-4 py-3 text-white focus:outline-none focus:border-brand-500 transition">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Goal</label>
                            <select id="goal" class="w-full bg-brand-dark border border-brand-border rounded-xl px-4 py-3 text-white focus:outline-none focus:border-brand-500 transition">
                                <option value="lose">Lose Weight (Cutting)</option>
                                <option value="maintain" selected>Maintain Weight</option>
                                <option value="gain">Build Muscle (Bulking)</option>
                            </select>
                        </div>
                        <div class="sm:col-span-2">
                            <label class="block text-xs font-semibold text-slate-300 uppercase mb-2">Activity Level</label>
                            <select id="activity" class="w-full bg-brand-dark border border-brand-border rounded-xl px-4 py-3 text-white focus:outline-none focus:border-brand-500 transition">
                                <option value="1.2">Sedentary (Little or no exercise)</option>
                                <option value="1.375">Lightly Active (Light exercise 1-3 days/week)</option>
                                <option value="1.55" selected>Moderately Active (Moderate exercise 3-5 days/week)</option>
                                <option value="1.725">Very Active (Hard exercise 6-7 days/week)</option>
                            </select>
                        </div>
                        <div class="sm:col-span-2 pt-2">
                            <button type="button" onclick="calculateMacros()" class="w-full bg-brand-600 hover:bg-brand-500 text-white font-bold py-4 rounded-xl transition shadow-lg glow-button cursor-pointer">
                                Calculate My Target Macros
                            </button>
                        </div>
                    </form>

                    <!-- Results Display Box -->
                    <div id="calculator-results" class="mt-8 pt-8 border-t border-brand-border hidden">
                        <div class="text-center mb-6">
                            <div class="text-xs uppercase font-semibold text-slate-400">Your Recommended Daily Target</div>
                            <div id="res-calories" class="text-4xl font-extrabold text-white mt-1">2,450 <span class="text-lg font-normal text-slate-400">Calories/day</span></div>
                        </div>
                        
                        <div class="grid sm:grid-cols-3 gap-4 text-center">
                            <div class="bg-brand-dark p-4 rounded-2xl border border-brand-border">
                                <div class="text-xs text-emerald-400 font-semibold mb-1">PROTEIN</div>
                                <div id="res-protein" class="text-2xl font-bold text-white">180g</div>
                                <div class="text-[10px] text-slate-400 mt-1">Muscle repair & growth</div>
                            </div>
                            <div class="bg-brand-dark p-4 rounded-2xl border border-brand-border">
                                <div class="text-xs text-cyan-400 font-semibold mb-1">CARBS</div>
                                <div id="res-carbs" class="text-2xl font-bold text-white">230g</div>
                                <div class="text-[10px] text-slate-400 mt-1">Energy & performance</div>
                            </div>
                            <div class="bg-brand-dark p-4 rounded-2xl border border-brand-border">
                                <div class="text-xs text-amber-400 font-semibold mb-1">FATS</div>
                                <div id="res-fats" class="text-2xl font-bold text-white">75g</div>
                                <div class="text-[10px] text-slate-400 mt-1">Hormone optimization</div>
                            </div>
                        </div>

                        <div class="mt-6 text-center">
                            <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="inline-flex items-center space-x-2 text-brand-400 hover:text-brand-300 font-semibold text-sm transition">
                                <span>Save these targets directly in the mobile app</span>
                                <i class="fa-solid fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- App Preview Section -->
        <section id="preview" class="py-24 bg-brand-card/40 border-y border-brand-border">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto space-y-4 mb-16">
                    <span class="text-brand-400 text-xs font-bold uppercase tracking-widest px-3 py-1 bg-brand-500/10 rounded-full border border-brand-500/20">Live Web Experience</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Experience Macro Diet Tracker</h2>
                    <p class="text-slate-300 text-sm sm:text-base">Explore the fully functional preview hosted on Google AI Studio right here or open it full screen.</p>
                </div>

                <div class="bg-brand-card border-2 border-brand-border rounded-3xl overflow-hidden shadow-2xl">
                    <div class="bg-brand-dark px-6 py-4 border-b border-brand-border flex items-center justify-between">
                        <div class="flex items-center space-x-2">
                            <div class="w-3 h-3 rounded-full bg-rose-500"></div>
                            <div class="w-3 h-3 rounded-full bg-amber-500"></div>
                            <div class="w-3 h-3 rounded-full bg-emerald-500"></div>
                            <span class="ml-4 text-xs font-mono text-slate-400">Macro Diet Tracker App View</span>
                        </div>
                        <div>
                            <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="text-xs bg-brand-600 hover:bg-brand-500 text-white px-4 py-2 rounded-xl font-semibold transition inline-flex items-center space-x-2">
                                <span>Open Fullscreen</span>
                                <i class="fa-solid fa-external-link-alt text-[10px]"></i>
                            </a>
                        </div>
                    </div>
                    
                    <div class="w-full h-[650px] bg-slate-900 relative">
                        <iframe src="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" class="w-full h-full border-0" title="Macro Diet Tracker App"></iframe>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials Section -->
        <section id="testimonials" class="py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto space-y-4 mb-16">
                    <span class="text-brand-400 text-xs font-bold uppercase tracking-widest px-3 py-1 bg-brand-500/10 rounded-full border border-brand-500/20">Testimonials</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Loved by Fitness Enthusiasts</h2>
                    <p class="text-slate-300 text-sm sm:text-base">See what our beta users and community members are saying about hitting their goals with Macro Diet Tracker.</p>
                </div>

                <div class="grid md:grid-cols-3 gap-8">
                    <div class="bg-brand-card border border-brand-border rounded-2xl p-8 space-y-6 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex text-amber-400 text-sm space-x-1">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <p class="text-slate-300 text-sm leading-relaxed">
                                "This app completely changed how I approach my nutrition. The gluten-free filtering and clean macro tracking make staying on prep effortless!"
                            </p>
                        </div>
                        <div class="flex items-center space-x-3 pt-4 border-t border-brand-border">
                            <div class="w-10 h-10 rounded-full bg-emerald-500/20 text-emerald-400 flex items-center justify-center font-bold">
                                JD
                            </div>
                            <div>
                                <div class="text-sm font-bold text-white">Jason Davis</div>
                                <div class="text-xs text-slate-400">Fitness Coach & Competitor</div>
                            </div>
                        </div>
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-8 space-y-6 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex text-amber-400 text-sm space-x-1">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <p class="text-slate-300 text-sm leading-relaxed">
                                "I've tried every tracker out there. Macro Diet Tracker is by far the cleanest, fastest, and most intuitive app on Google Play. Highly recommend!"
                            </p>
                        </div>
                        <div class="flex items-center space-x-3 pt-4 border-t border-brand-border">
                            <div class="w-10 h-10 rounded-full bg-cyan-500/20 text-cyan-400 flex items-center justify-center font-bold">
                                SM
                            </div>
                            <div>
                                <div class="text-sm font-bold text-white">Sarah Miller</div>
                                <div class="text-xs text-slate-400">Marathon Runner</div>
                            </div>
                        </div>
                    </div>

                    <div class="bg-brand-card border border-brand-border rounded-2xl p-8 space-y-6 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex text-amber-400 text-sm space-x-1">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <p class="text-slate-300 text-sm leading-relaxed">
                                "The custom splits and progress insights helped me drop 15 lbs of fat while keeping my strength up. Incredible tool."
                            </p>
                        </div>
                        <div class="flex items-center space-x-3 pt-4 border-t border-brand-border">
                            <div class="w-10 h-10 rounded-full bg-purple-500/20 text-purple-400 flex items-center justify-center font-bold">
                                MR
                            </div>
                            <div>
                                <div class="text-sm font-bold text-white">Marcus Roberts</div>
                                <div class="text-xs text-slate-400">Software Engineer & Lifter</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- PRIVACY POLICY VIEW (Hidden by default) -->
    <div id="view-privacy" class="hidden pt-32 pb-24 max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="mb-8">
            <button onclick="showPage('home')" class="inline-flex items-center space-x-2 text-brand-400 hover:text-brand-300 font-semibold text-sm bg-transparent border-0 cursor-pointer p-0">
                <i class="fa-solid fa-arrow-left"></i>
                <span>Back to Home</span>
            </button>
        </div>

        <div class="bg-brand-card border border-brand-border rounded-3xl p-8 sm:p-12 shadow-2xl space-y-8">
            <div class="border-b border-brand-border pb-6">
                <span class="text-brand-400 text-xs font-bold uppercase tracking-widest px-3 py-1 bg-brand-500/10 rounded-full border border-brand-500/20">Legal Documentation</span>
                <h1 class="text-3xl sm:text-4xl font-extrabold text-white mt-4">Privacy Policy for Diet Tracker</h1>
                <div class="flex flex-wrap gap-4 mt-4 text-xs text-slate-400 font-mono">
                    <div>Effective Date: October 12, 2026</div>
                    <div>•</div>
                    <div>Last Updated: October 12, 2026</div>
                    <div>•</div>
                    <div class="text-brand-400">App ID: com.aistudio.diettracker.nvkqwz</div>
                </div>
            </div>

            <div class="space-y-6 text-slate-300 text-sm sm:text-base leading-relaxed">
                <div>
                    <h2 class="text-xl font-bold text-white mb-2">1. Introduction</h2>
                    <p>Welcome to Diet Tracker ("we", "our", or "the App"). We are committed to safeguarding your privacy and ensuring your dietary and personal health data remains strictly secure, confidential, and under your control.</p>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">2. Core Privacy Principle: Local-First & Hardware Encrypted</h2>
                    <p class="mb-3">Diet Tracker operates on an on-device privacy model:</p>
                    <ul class="list-disc pl-5 space-y-2 text-slate-300">
                        <li><strong>Local Storage:</strong> Meal logs, macronutrient breakdowns, calorie records, body weight logs, and personal notes are stored locally on your device in a secure SQLite database.</li>
                        <li><strong>Hardware-Backed AES-256-GCM Encryption:</strong> Private notes and sensitive log records are encrypted using the Android KeyStore and hardware-level AES-256-GCM cryptography.</li>
                        <li><strong>No Account Required:</strong> You can use Diet Tracker without creating a third-party account or sharing personal credentials.</li>
                        <li><strong>Zero Data Monetization:</strong> We do not sell, rent, broker, or trade your personal records, dietary information, or photos with advertisers or third-party data brokers.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">3. Information Collected and Processed</h2>
                    <h3 class="font-semibold text-white mt-3 mb-1">A. Information You Provide</h3>
                    <ul class="list-disc pl-5 space-y-1 mb-3">
                        <li><strong>Dietary Records:</strong> Food names, meal types (Breakfast, Lunch, Dinner, Snack), calories, macronutrients (Protein, Carbs, Fat in grams), and personal notes.</li>
                        <li><strong>Body Weight & Target Goals:</strong> Daily calorie goals, target macronutrient ratios, target weight, historical weight records, and measurement units (pounds / kilograms).</li>
                        <li><strong>Preferences:</strong> UI theme settings (System, Calming Light, Forest Dark).</li>
                    </ul>
                    <h3 class="font-semibold text-white mt-3 mb-1">B. Device Permissions</h3>
                    <ul class="list-disc pl-5 space-y-1">
                        <li><strong>Camera (<code class="text-brand-400 text-xs">android.permission.CAMERA</code>):</strong> Optional runtime permission used strictly when you choose to photograph food in the Macro Scanner. Photos are used for real-time nutritional recognition and are never used for facial recognition or identity tracking.</li>
                        <li><strong>Internet (<code class="text-brand-400 text-xs">android.permission.INTERNET</code>):</strong> Used exclusively to retrieve accurate nutritional facts and search grounding via Google Gemini AI when scanning meals or searching the food database.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">4. Third-Party Services & AI Processing</h2>
                    <p class="mb-2">To provide accurate food recognition and search capabilities, the App connects with:</p>
                    <ul class="list-disc pl-5 space-y-2">
                        <li><strong>Google Gemini Generative AI & Google Search Grounding:</strong> Food visual representations or search terms are securely transmitted via HTTPS to Google Gemini services to obtain authoritative nutritional information. For details, refer to <a href="https://policies.google.com/privacy" target="_blank" class="text-brand-400 underline hover:text-brand-300">Google's Privacy Policy</a>.</li>
                    </ul>
                    <p class="mt-3">The App contains no third-party advertising SDKs or cross-app analytics trackers.</p>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">5. User-Initiated Social Sharing</h2>
                    <p>When using the "Share Achievements with Friends" feature, the App generates a plain-text milestone message (such as calorie goal achievements) and opens the standard Android system share sheet. Data is only sent to the recipient or app that you explicitly choose.</p>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">6. Data Retention, Modification & Deletion</h2>
                    <ul class="list-disc pl-5 space-y-2">
                        <li><strong>Editing:</strong> You can edit any logged meal (name, calories, protein, carbs, fat) directly on the Log screen at any time.</li>
                        <li><strong>Deletion:</strong> You can delete individual meal entries or weight records at any time.</li>
                        <li><strong>Complete Removal:</strong> Because all records reside on your local device, uninstalling the App or clearing app data in Android device settings permanently erases all databases and encryption keys.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">7. Children's Privacy</h2>
                    <p>Diet Tracker does not address or knowingly collect personal information from children under the age of 13.</p>
                </div>

                <div>
                    <h2 class="text-xl font-bold text-white mb-2">8. Security Safeguards</h2>
                    <p>We implement industry-standard safeguards including Android's sandbox isolation, hardware-backed AES-256-GCM encryption for private notes, and TLS/HTTPS encrypted network communications.</p>
                </div>

                <div class="bg-brand-dark p-6 rounded-2xl border border-brand-border space-y-2">
                    <h2 class="text-lg font-bold text-white">9. Contact Us</h2>
                    <p>If you have any questions regarding this Privacy Policy, please contact:</p>
                    <p><strong>Developer Email:</strong> <a href="mailto:whitekev2@gmail.com" class="text-brand-400 hover:underline">whitekev2@gmail.com</a></p>
                    <p><strong>Application ID:</strong> <span class="font-mono text-slate-200">com.aistudio.diettracker.nvkqwz</span></p>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-brand-card border-t border-brand-border pt-16 pb-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <!-- Download Banner Box -->
            <div class="bg-gradient-to-r from-brand-600 to-emerald-600 rounded-3xl p-8 sm:p-12 text-center relative overflow-hidden mb-16 shadow-2xl">
                <div class="relative z-10 max-w-2xl mx-auto space-y-6">
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Ready to Transform Your Nutrition?</h2>
                    <p class="text-emerald-100 text-base sm:text-lg">Download Macro Diet Tracker today on the Google Play Store and start hitting your goals effortlessly.</p>
                    <div>
                        <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="inline-flex items-center space-x-3 bg-brand-dark hover:bg-slate-900 text-white font-bold px-8 py-4 rounded-2xl transition shadow-xl transform hover:-translate-y-0.5">
                            <i class="fa-brands fa-google-play text-2xl text-emerald-400"></i>
                            <div class="text-left">
                                <div class="text-[10px] uppercase tracking-wider text-slate-400 font-medium">Download on</div>
                                <div class="text-sm font-bold -mt-0.5">Google Play Store</div>
                            </div>
                        </a>
                    </div>
                </div>
            </div>

            <!-- Footer Links & Copyright -->
            <div class="grid md:grid-cols-4 gap-8 pb-12 border-b border-brand-border">
                <div class="space-y-4 md:col-span-2">
                    <div class="flex items-center space-x-3 cursor-pointer" onclick="showPage('home')">
                        <div class="w-8 h-8 rounded-lg bg-brand-600 flex items-center justify-center text-white">
                            <i class="fa-solid fa-bolt"></i>
                        </div>
                        <span class="text-lg font-bold text-white">Macro Diet Tracker</span>
                    </div>
                    <p class="text-slate-400 text-sm max-w-sm">
                        Empowering individuals to achieve their health, fitness, and nutrition goals through smart macro tracking and effortless food logging.
                    </p>
                </div>

                <div>
                    <h4 class="text-xs font-semibold uppercase tracking-wider text-white mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li><button onclick="showPage('home')" class="hover:text-white transition bg-transparent border-0 cursor-pointer text-slate-400 text-sm p-0">Home</button></li>
                        <li><a href="#features" onclick="showPage('home')" class="hover:text-white transition">Features</a></li>
                        <li><a href="#calculator" onclick="showPage('home')" class="hover:text-white transition">Macro Calculator</a></li>
                        <li><a href="#preview" onclick="showPage('home')" class="hover:text-white transition">App Preview</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-xs font-semibold uppercase tracking-wider text-white mb-4">Support & Legal</h4>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li><button onclick="showPage('privacy')" class="hover:text-white transition bg-transparent border-0 cursor-pointer text-slate-400 text-sm p-0">Privacy Policy</button></li>
                        <li><a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="hover:text-white transition">Google Play App</a></li>
                        <li><a href="mailto:whitekev2@gmail.com" class="hover:text-white transition">Contact Support</a></li>
                    </ul>
                </div>
            </div>

            <div class="pt-8 flex flex-col sm:flex-row items-center justify-between text-xs text-slate-500 space-y-4 sm:space-y-0">
                <div>&copy; 2026 Macro Diet Tracker (com.aistudio.diettracker.nvkqwz). All rights reserved.</div>
                <div class="flex space-x-6">
                    <button onclick="showPage('privacy')" class="hover:text-slate-400 transition bg-transparent border-0 cursor-pointer text-slate-500 text-xs p-0">Privacy Policy</button>
                    <a href="https://aistudio.google.com/apps/7a61dd5d-599f-4a35-ba28-3100c241083d?showPreview=true&showAssistant=true" target="_blank" class="hover:text-slate-400 transition">Google Play Store</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        // Page Router
        function showPage(pageId) {
            const homeView = document.getElementById('view-home');
            const privacyView = document.getElementById('view-privacy');

            if (pageId === 'privacy') {
                homeView.classList.add('hidden');
                privacyView.classList.remove('hidden');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            } else {
                privacyView.classList.add('hidden');
                homeView.classList.remove('hidden');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        // Mobile Menu Toggle
        const menuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        function toggleMobileMenu() {
            mobileMenu.classList.toggle('hidden');
        }

        menuBtn.addEventListener('click', toggleMobileMenu);

        // Macro Calculator Logic
        function calculateMacros() {
            const weight = parseFloat(document.getElementById('weight').value) || 170;
            const height = parseFloat(document.getElementById('height').value) || 70;
            const age = parseFloat(document.getElementById('age').value) || 28;
            const goal = document.getElementById('goal').value;
            const activity = parseFloat(document.getElementById('activity').value) || 1.55;

            // Mifflin-St Jeor Equation for BMR
            const weightKg = weight * 0.453592;
            const heightCm = height * 2.54;
            
            let bmr = (10 * weightKg) + (6.25 * heightCm) - (5 * age) + 5;
            let tdee = bmr * activity;

            if (goal === 'lose') {
                tdee -= 500;
            } else if (goal === 'gain') {
                tdee += 300;
            }

            const calories = Math.round(tdee);
            const protein = Math.round(weight * 1.0); // 1g per lb
            const fats = Math.round((calories * 0.25) / 9); // 25% of calories from fat
            const carbs = Math.round((calories - (protein * 4) - (fats * 9)) / 4);

            document.getElementById('res-calories').innerHTML = `${calories.toLocaleString()} <span class="text-lg font-normal text-slate-400">Calories/day</span>`;
            document.getElementById('res-protein').innerText = `${protein}g`;
            document.getElementById('res-carbs').innerText = `${carbs}g`;
            document.getElementById('res-fats').innerText = `${fats}g`;

            const resultsDiv = document.getElementById('calculator-results');
            resultsDiv.classList.remove('hidden');
            resultsDiv.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }

        // Run initial calculation on load
        window.onload = function() {
            calculateMacros();
        };
    </script>
</body>
</html>