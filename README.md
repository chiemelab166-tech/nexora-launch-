# nexora-launch-
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nexora | Boost Your Social Presence</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #050505;
            color: #e5e5e5;
            overflow-x: hidden;
        }
        .neon-text {
            text-shadow: 0 0 10px rgba(139, 92, 246, 0.5), 0 0 20px rgba(59, 130, 246, 0.3);
        }
        .neon-border {
            box-shadow: 0 0 15px rgba(139, 92, 246, 0.2);
            border: 1px solid rgba(139, 92, 246, 0.3);
        }
        .gradient-bg {
            background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
        }
        .glass {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        .service-card:hover {
            transform: translateY(-5px);
            transition: all 0.3s ease;
            border-color: #8b5cf6;
        }
        .tab-active {
            border-bottom: 2px solid #8b5cf6;
            color: #8b5cf6;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #050505;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e1b4b;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #312e81;
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav class="fixed top-0 w-full z-50 glass border-b border-white/5 px-6 py-4 flex justify-between items-center">
        <div class="flex items-center gap-2 cursor-pointer" onclick="showPage('home')">
            <div class="w-10 h-10 bg-indigo-600 rounded-lg flex items-center justify-center shadow-lg shadow-indigo-500/30">
                <i data-lucide="zap" class="text-white"></i>
            </div>
            <span class="text-2xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 to-purple-500">NEXORA</span>
        </div>
        <div class="hidden md:flex gap-8 items-center text-sm font-medium uppercase tracking-wider">
            <a href="#" onclick="showPage('home')" class="hover:text-indigo-400 transition">Home</a>
            <a href="#" onclick="showPage('services')" class="hover:text-indigo-400 transition">Services</a>
            <a href="#" onclick="showPage('order')" class="hover:text-indigo-400 transition text-indigo-400">Order Now</a>
            <button onclick="showAdminLogin()" class="opacity-50 hover:opacity-100 transition text-xs">Admin</button>
        </div>
        <div class="flex items-center gap-4">
            <a href="https://wa.me/2348103627127" target="_blank" class="p-2 bg-green-600/20 text-green-400 rounded-full hover:bg-green-600/30 transition">
                <i data-lucide="phone"></i>
            </a>
            <button class="md:hidden" onclick="toggleMobileMenu()">
                <i data-lucide="menu"></i>
            </button>
        </div>
    </nav>

    <!-- Mobile Menu Overlay -->
    <div id="mobileMenu" class="fixed inset-0 z-[60] bg-black/95 hidden flex-col items-center justify-center gap-8 text-2xl font-bold">
        <button class="absolute top-6 right-6" onclick="toggleMobileMenu()">
            <i data-lucide="x" class="w-10 h-10"></i>
        </button>
        <a href="#" onclick="showPage('home'); toggleMobileMenu()" class="hover:text-indigo-400">Home</a>
        <a href="#" onclick="showPage('services'); toggleMobileMenu()" class="hover:text-indigo-400">Services</a>
        <a href="#" onclick="showPage('order'); toggleMobileMenu()" class="hover:text-indigo-400 text-indigo-400">Order Now</a>
    </div>

    <!-- Main Content -->
    <main class="pt-24 min-h-screen">

        <!-- Page: Home -->
        <section id="homePage" class="page-section">
            <div class="container mx-auto px-6 py-12 md:py-24 text-center">
                <h1 class="text-5xl md:text-7xl font-extrabold mb-6 leading-tight">
                    Boost Your <span class="text-indigo-500">Social Presence</span> <br>with Nexora
                </h1>
                <p class="text-gray-400 text-lg md:text-xl max-w-2xl mx-auto mb-10">
                    Fast, reliable and affordable social media growth services. Join thousands of creators and businesses scaling their reach today.
                </p>
                <div class="flex flex-wrap justify-center gap-4 mb-20">
                    <button onclick="showPage('order')" class="px-8 py-4 bg-indigo-600 hover:bg-indigo-700 text-white rounded-full font-bold transition shadow-xl shadow-indigo-600/20">
                        Get Started Now
                    </button>
                    <button onclick="showPage('services')" class="px-8 py-4 glass border-white/10 hover:border-indigo-500/50 rounded-full font-bold transition">
                        View Pricing
                    </button>
                </div>

                <!-- Platform Grid -->
                <div class="grid grid-cols-2 md:grid-cols-5 gap-4 md:gap-8">
                    <div class="glass p-6 rounded-2xl flex flex-col items-center gap-3 grayscale hover:grayscale-0 transition cursor-pointer" onclick="selectPlatform('TikTok')">
                        <i data-lucide="music" class="w-10 h-10 text-pink-500"></i>
                        <span class="font-semibold">TikTok</span>
                    </div>
                    <div class="glass p-6 rounded-2xl flex flex-col items-center gap-3 grayscale hover:grayscale-0 transition cursor-pointer" onclick="selectPlatform('Instagram')">
                        <i data-lucide="instagram" class="w-10 h-10 text-purple-500"></i>
                        <span class="font-semibold">Instagram</span>
                    </div>
                    <div class="glass p-6 rounded-2xl flex flex-col items-center gap-3 grayscale hover:grayscale-0 transition cursor-pointer" onclick="selectPlatform('YouTube')">
                        <i data-lucide="youtube" class="w-10 h-10 text-red-500"></i>
                        <span class="font-semibold">YouTube</span>
                    </div>
                    <div class="glass p-6 rounded-2xl flex flex-col items-center gap-3 grayscale hover:grayscale-0 transition cursor-pointer" onclick="selectPlatform('X')">
                        <i data-lucide="twitter" class="w-10 h-10 text-blue-400"></i>
                        <span class="font-semibold">X (Twitter)</span>
                    </div>
                    <div class="glass p-6 rounded-2xl flex flex-col items-center gap-3 grayscale hover:grayscale-0 transition cursor-pointer" onclick="selectPlatform('Facebook')">
                        <i data-lucide="facebook" class="w-10 h-10 text-blue-600"></i>
                        <span class="font-semibold">Facebook</span>
                    </div>
                </div>
            </div>

            <!-- Testimonials -->
            <div class="bg-indigo-900/10 py-20">
                <div class="container mx-auto px-6">
                    <h2 class="text-3xl font-bold text-center mb-12">Trusted by Influencers</h2>
                    <div class="grid md:grid-cols-3 gap-8">
                        <div class="glass p-8 rounded-2xl">
                            <div class="flex text-yellow-500 mb-4">
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                            </div>
                            <p class="text-gray-300 italic mb-6">"Nexora delivered 10k followers within 24 hours. My engagement has skyrocketed since then!"</p>
                            <div class="font-bold text-indigo-400">@david_creativ</div>
                        </div>
                        <div class="glass p-8 rounded-2xl">
                            <div class="flex text-yellow-500 mb-4">
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                            </div>
                            <p class="text-gray-300 italic mb-6">"The views service is very high quality. No drops and fast delivery. Best in Nigeria."</p>
                            <div class="font-bold text-indigo-400">Sarah M.</div>
                        </div>
                        <div class="glass p-8 rounded-2xl">
                            <div class="flex text-yellow-500 mb-4">
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                                <i data-lucide="star" class="fill-current w-4 h-4"></i>
                            </div>
                            <p class="text-gray-300 italic mb-6">"Support team is very responsive. Helped me setup my campaign in minutes. 10/10!"</p>
                            <div class="font-bold text-indigo-400">Business Hub Lagos</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- FAQ -->
            <div class="container mx-auto px-6 py-20">
                <h2 class="text-3xl font-bold text-center mb-12">Frequently Asked Questions</h2>
                <div class="max-w-3xl mx-auto space-y-4">
                    <div class="glass p-4 rounded-xl cursor-pointer" onclick="toggleFaq(1)">
                        <div class="flex justify-between items-center">
                            <h3 class="font-semibold">Is this safe for my account?</h3>
                            <i data-lucide="chevron-down" id="faq-icon-1"></i>
                        </div>
                        <p id="faq-content-1" class="hidden mt-4 text-gray-400 text-sm">Yes, our methods are fully compliant with social media policies. We use organic delivery systems that don't put your account at risk.</p>
                    </div>
                    <div class="glass p-4 rounded-xl cursor-pointer" onclick="toggleFaq(2)">
                        <div class="flex justify-between items-center">
                            <h3 class="font-semibold">How long does delivery take?</h3>
                            <i data-lucide="chevron-down" id="faq-icon-2"></i>
                        </div>
                        <p id="faq-content-2" class="hidden mt-4 text-gray-400 text-sm">Most orders start within 1-3 hours. Full delivery depends on the quantity, but followers and likes are usually completed within 24 hours.</p>
                    </div>
                    <div class="glass p-4 rounded-xl cursor-pointer" onclick="toggleFaq(3)">
                        <div class="flex justify-between items-center">
                            <h3 class="font-semibold">What is the payment process?</h3>
                            <i data-lucide="chevron-down" id="faq-icon-3"></i>
                        </div>
                        <p id="faq-content-3" class="hidden mt-4 text-gray-400 text-sm">Once you place an order, you will receive our Opay bank details. After making the transfer, your order will be activated automatically once we confirm.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Page: Services -->
        <section id="servicesPage" class="page-section hidden">
            <div class="container mx-auto px-6 py-12">
                <h2 class="text-4xl font-bold text-center mb-4">Our Premium Services</h2>
                <p class="text-gray-400 text-center mb-12 max-w-lg mx-auto">Choose from our list of high-quality engagement services tailored for your growth.</p>
                
                <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
                    <!-- Views -->
                    <div class="glass p-6 rounded-2xl service-card">
                        <div class="w-12 h-12 bg-blue-500/20 rounded-xl flex items-center justify-center mb-6">
                            <i data-lucide="play" class="text-blue-500"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">High Quality Views</h3>
                        <p class="text-gray-400 text-sm mb-6">Boost your reach and go viral with authentic views from real users.</p>
                        <div class="text-indigo-400 font-bold text-2xl mb-6">₦3,000 <span class="text-sm text-gray-500">/ 1,000 views</span></div>
                        <button onclick="startOrder('Views')" class="w-full py-3 bg-white/5 hover:bg-indigo-600 transition rounded-xl font-semibold">Order Views</button>
                    </div>
                    <!-- Followers -->
                    <div class="glass p-6 rounded-2xl service-card">
                        <div class="w-12 h-12 bg-purple-500/20 rounded-xl flex items-center justify-center mb-6">
                            <i data-lucide="users" class="text-purple-500"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">Organic Followers</h3>
                        <p class="text-gray-400 text-sm mb-6">Build credibility and an audience that sticks with your content.</p>
                        <div class="text-indigo-400 font-bold text-2xl mb-6">₦1,500 <span class="text-sm text-gray-500">/ 100 followers</span></div>
                        <button onclick="startOrder('Followers')" class="w-full py-3 bg-white/5 hover:bg-indigo-600 transition rounded-xl font-semibold">Order Followers</button>
                    </div>
                    <!-- Likes -->
                    <div class="glass p-6 rounded-2xl service-card">
                        <div class="w-12 h-12 bg-red-500/20 rounded-xl flex items-center justify-center mb-6">
                            <i data-lucide="heart" class="text-red-500"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">Instant Likes</h3>
                        <p class="text-gray-400 text-sm mb-6">Increase your post popularity and signal quality to algorithms.</p>
                        <div class="text-indigo-400 font-bold text-2xl mb-6">₦3,500 <span class="text-sm text-gray-500">/ 100 likes</span></div>
                        <button onclick="startOrder('Likes')" class="w-full py-3 bg-white/5 hover:bg-indigo-600 transition rounded-xl font-semibold">Order Likes</button>
                    </div>
                    <!-- Comments -->
                    <div class="glass p-6 rounded-2xl service-card">
                        <div class="w-12 h-12 bg-green-500/20 rounded-xl flex items-center justify-center mb-6">
                            <i data-lucide="message-circle" class="text-green-500"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-2">Custom Comments</h3>
                        <p class="text-gray-400 text-sm mb-6">Spark conversations and boost engagement rate with real replies.</p>
                        <div class="text-indigo-400 font-bold text-2xl mb-6">₦4,000 <span class="text-sm text-gray-500">/ 20 comments</span></div>
                        <button onclick="startOrder('Comments')" class="w-full py-3 bg-white/5 hover:bg-indigo-600 transition rounded-xl font-semibold">Order Comments</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Page: Order Form -->
        <section id="orderPage" class="page-section hidden">
            <div class="container mx-auto px-6 py-12">
                <div class="max-w-2xl mx-auto glass p-8 md:p-12 rounded-3xl neon-border">
                    <h2 class="text-3xl font-bold mb-8 text-center">Place Your Order</h2>
                    
                    <form id="orderForm" onsubmit="handleOrderSubmit(event)" class="space-y-6">
                        <div class="grid md:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-sm text-gray-400 mb-2">Platform</label>
                                <select id="orderPlatform" class="w-full bg-white/5 border border-white/10 rounded-xl p-3 focus:outline-none focus:border-indigo-500 transition" required>
                                    <option value="" disabled selected>Select Platform</option>
                                    <option value="TikTok">TikTok</option>
                                    <option value="Instagram">Instagram</option>
                                    <option value="YouTube">YouTube</option>
                                    <option value="Facebook">Facebook</option>
                                    <option value="X">X (Twitter)</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm text-gray-400 mb-2">Service Type</label>
                                <select id="orderService" onchange="calculatePrice()" class="w-full bg-white/5 border border-white/10 rounded-xl p-3 focus:outline-none focus:border-indigo-500 transition" required>
                                    <option value="" disabled selected>Select Service</option>
                                    <option value="Views">Views</option>
                                    <option value="Followers">Followers</option>
                                    <option value="Likes">Likes</option>
                                    <option value="Comments">Comments</option>
                                </select>
                            </div>
                        </div>

                        <div>
                            <label class="block text-sm text-gray-400 mb-2">Link / Username</label>
                            <input type="text" id="orderLink" placeholder="e.g. https://instagram.com/p/..." class="w-full bg-white/5 border border-white/10 rounded-xl p-3 focus:outline-none focus:border-indigo-500 transition" required>
                        </div>

                        <div>
                            <label class="block text-sm text-gray-400 mb-2">Quantity</label>
                            <input type="number" id="orderQty" oninput="calculatePrice()" min="1" placeholder="Enter quantity" class="w-full bg-white/5 border border-white/10 rounded-xl p-3 focus:outline-none focus:border-indigo-500 transition" required>
                            <p id="qtyHelp" class="text-xs text-gray-500 mt-1 italic"></p>
                        </div>

                        <div class="bg-indigo-600/10 p-6 rounded-2xl flex justify-between items-center border border-indigo-500/20">
                            <span class="font-bold text-gray-300">Total Price:</span>
                            <span id="totalPrice" class="text-3xl font-extrabold text-indigo-400">₦0</span>
                        </div>

                        <button type="submit" class="w-full py-4 bg-indigo-600 hover:bg-indigo-700 text-white rounded-xl font-bold text-lg shadow-lg shadow-indigo-600/30 transition">
                            Proceed to Payment
                        </button>
                    </form>
                </div>
            </div>
        </section>

        <!-- Page: Order Success / Payment Details -->
        <section id="successPage" class="page-section hidden">
            <div class="container mx-auto px-6 py-12">
                <div class="max-w-md mx-auto glass p-8 rounded-3xl text-center border border-green-500/30">
                    <div class="w-16 h-16 bg-green-500/20 rounded-full flex items-center justify-center mx-auto mb-6">
                        <i data-lucide="check" class="text-green-500 w-8 h-8"></i>
                    </div>
                    <h2 class="text-2xl font-bold mb-2">Order Submitted!</h2>
                    <p class="text-gray-400 mb-8">Please complete the payment below to activate your service.</p>
                    
                    <div class="bg-black/40 p-6 rounded-2xl text-left space-y-4 mb-8">
                        <div>
                            <div class="text-xs text-gray-500 uppercase font-bold mb-1">Bank Name</div>
                            <div class="font-bold text-lg">Opay</div>
                        </div>
                        <div>
                            <div class="text-xs text-gray-500 uppercase font-bold mb-1">Account Number</div>
                            <div class="flex justify-between items-center">
                                <span class="font-bold text-xl tracking-wider text-indigo-400">8103627127</span>
                                <button onclick="copyToClipboard('8103627127')" class="text-gray-500 hover:text-white transition">
                                    <i data-lucide="copy" class="w-4 h-4"></i>
                                </button>
                            </div>
                        </div>
                        <div>
                            <div class="text-xs text-gray-500 uppercase font-bold mb-1">Account Name</div>
                            <div class="font-bold">Bright Chinalu Chiemela</div>
                        </div>
                        <div class="pt-4 border-t border-white/5">
                            <div class="text-xs text-gray-500 uppercase font-bold mb-1">Amount to Pay</div>
                            <div id="finalAmount" class="font-extrabold text-2xl text-green-400">₦0</div>
                        </div>
                    </div>

                    <div class="space-y-4">
                        <a id="whatsappConfirm" href="#" target="_blank" class="block w-full py-4 bg-green-600 hover:bg-green-700 text-white rounded-xl font-bold transition flex items-center justify-center gap-2">
                            <i data-lucide="send" class="w-5 h-5"></i>
                            Send Proof on WhatsApp
                        </a>
                        <button onclick="showPage('home')" class="text-gray-500 hover:text-white transition text-sm">Return to Home</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Page: Admin Login -->
        <section id="adminLoginPage" class="page-section hidden">
            <div class="container mx-auto px-6 py-20 flex justify-center">
                <div class="w-full max-w-sm glass p-8 rounded-3xl border border-white/10">
                    <h2 class="text-2xl font-bold mb-6 text-center">Admin Access</h2>
                    <form onsubmit="handleAdminLogin(event)" class="space-y-4">
                        <input type="password" id="adminPin" placeholder="Enter Access PIN" class="w-full bg-white/5 border border-white/10 rounded-xl p-3 focus:outline-none focus:border-indigo-500" required>
                        <button type="submit" class="w-full py-3 bg-indigo-600 hover:bg-indigo-700 rounded-xl font-bold transition">Login</button>
                        <button type="button" onclick="showPage('home')" class="w-full text-gray-500 text-sm">Cancel</button>
                    </form>
                </div>
            </div>
        </section>

        <!-- Page: Admin Dashboard -->
        <section id="adminDashboardPage" class="page-section hidden">
            <div class="container mx-auto px-6 py-12">
                <div class="flex justify-between items-center mb-8">
                    <h2 class="text-3xl font-bold">Admin Dashboard</h2>
                    <button onclick="logoutAdmin()" class="px-4 py-2 bg-red-500/20 text-red-400 rounded-lg text-sm">Logout</button>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
                    <div class="glass p-6 rounded-2xl">
                        <div class="text-gray-400 text-sm mb-1">Total Orders</div>
                        <div id="statTotalOrders" class="text-3xl font-bold">0</div>
                    </div>
                    <div class="glass p-6 rounded-2xl">
                        <div class="text-gray-400 text-sm mb-1">Pending Revenue</div>
                        <div id="statRevenue" class="text-3xl font-bold text-green-400">₦0</div>
                    </div>
                    <div class="glass p-6 rounded-2xl">
                        <div class="text-gray-400 text-sm mb-1">System Status</div>
                        <div class="text-3xl font-bold text-indigo-400">Live</div>
                    </div>
                </div>

                <div class="glass rounded-3xl overflow-hidden overflow-x-auto">
                    <table class="w-full text-left">
                        <thead class="bg-white/5">
                            <tr>
                                <th class="px-6 py-4 text-xs font-bold uppercase text-gray-500">Order ID</th>
                                <th class="px-6 py-4 text-xs font-bold uppercase text-gray-500">Platform/Service</th>
                                <th class="px-6 py-4 text-xs font-bold uppercase text-gray-500">Target</th>
                                <th class="px-6 py-4 text-xs font-bold uppercase text-gray-500">Qty</th>
                                <th class="px-6 py-4 text-xs font-bold uppercase text-gray-500">Price</th>
                                <th class="px-6 py-4 text-xs font-bold uppercase text-gray-500">Status</th>
                            </tr>
                        </thead>
                        <tbody id="adminOrderTable" class="divide-y divide-white/5">
                            <!-- Orders dynamic -->
                        </tbody>
                    </table>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="glass border-t border-white/5 py-12 mt-20">
        <div class="container mx-auto px-6 grid md:grid-cols-4 gap-12">
            <div class="col-span-2">
                <div class="flex items-center gap-2 mb-6">
                    <div class="w-8 h-8 bg-indigo-600 rounded flex items-center justify-center">
                        <i data-lucide="zap" class="text-white w-4 h-4"></i>
                    </div>
                    <span class="text-xl font-bold">NEXORA</span>
                </div>
                <p class="text-gray-500 text-sm max-w-sm mb-6">The #1 choice for social media growth in Nigeria. Fast delivery, high retention, and organic results.</p>
                <div class="flex gap-4">
                    <a href="#" class="w-10 h-10 glass rounded-full flex items-center justify-center hover:bg-indigo-600 transition"><i data-lucide="instagram" class="w-4 h-4"></i></a>
                    <a href="#" class="w-10 h-10 glass rounded-full flex items-center justify-center hover:bg-indigo-600 transition"><i data-lucide="twitter" class="w-4 h-4"></i></a>
                    <a href="#" class="w-10 h-10 glass rounded-full flex items-center justify-center hover:bg-indigo-600 transition"><i data-lucide="facebook" class="w-4 h-4"></i></a>
                </div>
            </div>
            <div>
                <h4 class="font-bold mb-6">Services</h4>
                <ul class="text-gray-500 text-sm space-y-3">
                    <li><a href="#" onclick="showPage('services')" class="hover:text-indigo-400 transition">TikTok Growth</a></li>
                    <li><a href="#" onclick="showPage('services')" class="hover:text-indigo-400 transition">Instagram Marketing</a></li>
                    <li><a href="#" onclick="showPage('services')" class="hover:text-indigo-400 transition">YouTube Promotion</a></li>
                    <li><a href="#" onclick="showPage('services')" class="hover:text-indigo-400 transition">X Engagement</a></li>
                </ul>
            </div>
            <div>
                <h4 class="font-bold mb-6">Company</h4>
                <ul class="text-gray-500 text-sm space-y-3">
                    <li><a href="#" class="hover:text-indigo-400 transition">About Us</a></li>
                    <li><a href="#" class="hover:text-indigo-400 transition">Privacy Policy</a></li>
                    <li><a href="#" class="hover:text-indigo-400 transition">Terms of Service</a></li>
                    <li><a href="https://wa.me/2348103627127" class="hover:text-indigo-400 transition">Contact Support</a></li>
                </ul>
            </div>
        </div>
        <div class="container mx-auto px-6 pt-12 text-center text-gray-600 text-xs">
            © 2024 Nexora Media. All rights reserved.
        </div>
    </footer>

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-6 left-1/2 -translate-x-1/2 glass px-6 py-3 rounded-full text-sm font-medium z-[100] transform translate-y-20 transition-all duration-300 opacity-0 pointer-events-none">
        Message here
    </div>

    <script>
        // State Management
        let currentPrice = 0;
        let orders = JSON.parse(localStorage.getItem('nexora_orders') || '[]');
        let isAdmin = false;

        // Pricing Rates
        const RATES = {
            'Views': { rate: 3000, per: 1000 },
            'Followers': { rate: 1500, per: 100 },
            'Likes': { rate: 3500, per: 100 },
            'Comments': { rate: 4000, per: 20 }
        };

        // Initialize Icons
        lucide.createIcons();

        // Navigation
        function showPage(pageId) {
            window.scrollTo({ top: 0, behavior: 'smooth' });
            document.querySelectorAll('.page-section').forEach(p => p.classList.add('hidden'));
            document.getElementById(pageId + 'Page').classList.remove('hidden');
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
            menu.classList.toggle('flex');
        }

        // Service Selection Logic
        function selectPlatform(platform) {
            document.getElementById('orderPlatform').value = platform;
            showPage('order');
        }

        function startOrder(service) {
            document.getElementById('orderService').value = service;
            calculatePrice();
            showPage('order');
        }

        // Calculator
        function calculatePrice() {
            const service = document.getElementById('orderService').value;
            const qty = document.getElementById('orderQty').value;
            const help = document.getElementById('qtyHelp');
            const priceEl = document.getElementById('totalPrice');

            if (!service || !qty) {
                currentPrice = 0;
                priceEl.innerText = "₦0";
                help.innerText = "";
                return;
            }

            const config = RATES[service];
            currentPrice = Math.ceil((qty / config.per) * config.rate);
            
            priceEl.innerText = "₦" + currentPrice.toLocaleString();
            help.innerText = `Pricing: ₦${config.rate.toLocaleString()} per ${config.per.toLocaleString()} ${service.toLowerCase()}`;
        }

        // Order Submission
        function handleOrderSubmit(event) {
            event.preventDefault();
            
            const platform = document.getElementById('orderPlatform').value;
            const service = document.getElementById('orderService').value;
            const link = document.getElementById('orderLink').value;
            const qty = document.getElementById('orderQty').value;

            if (!platform || !service || !link || !qty) {
                showToast("Please fill all fields correctly.");
                return;
            }

            const orderId = 'NX' + Math.random().toString(36).substr(2, 6).toUpperCase();
            const newOrder = {
                id: orderId,
                platform,
                service,
                link,
                qty,
                price: currentPrice,
                status: 'Pending Payment',
                date: new Date().toLocaleString()
            };

            orders.unshift(newOrder);
            localStorage.setItem('nexora_orders', JSON.stringify(orders));

            // Setup Success Page
            document.getElementById('finalAmount').innerText = "₦" + currentPrice.toLocaleString();
            const waMsg = encodeURIComponent(`Hi Nexora, I just placed an order!\n\nOrder ID: ${orderId}\nService: ${qty} ${service} on ${platform}\nLink: ${link}\nTotal: ₦${currentPrice.toLocaleString()}\n\nI am sending proof of payment now.`);
            document.getElementById('whatsappConfirm').href = `https://wa.me/2348103627127?text=${waMsg}`;
            
            showPage('success');
            showToast("Order saved! Please make payment.");
        }

        // Admin System
        function showAdminLogin() {
            showPage('adminLogin');
        }

        function handleAdminLogin(event) {
            event.preventDefault();
            const pin = document.getElementById('adminPin').value;
            if (pin === "1234") { // Mock admin PIN
                isAdmin = true;
                renderAdminDashboard();
                showPage('adminDashboard');
                showToast("Welcome Admin");
            } else {
                showToast("Invalid Admin PIN");
            }
        }

        function logoutAdmin() {
            isAdmin = false;
            showPage('home');
        }

        function renderAdminDashboard() {
            const table = document.getElementById('adminOrderTable');
            const totalOrders = document.getElementById('statTotalOrders');
            const totalRevenue = document.getElementById('statRevenue');
            
            table.innerHTML = "";
            let revenue = 0;

            orders.forEach(order => {
                revenue += order.price;
                table.innerHTML += `
                    <tr>
                        <td class="px-6 py-4 text-xs font-mono text-indigo-400">${order.id}</td>
                        <td class="px-6 py-4 text-sm">
                            <span class="block font-bold">${order.platform}</span>
                            <span class="text-xs text-gray-500">${order.service}</span>
                        </td>
                        <td class="px-6 py-4 text-xs text-gray-400 truncate max-w-[150px]">${order.link}</td>
                        <td class="px-6 py-4 text-sm font-bold">${order.qty}</td>
                        <td class="px-6 py-4 text-sm font-bold">₦${order.price.toLocaleString()}</td>
                        <td class="px-6 py-4">
                            <span class="px-3 py-1 bg-yellow-500/10 text-yellow-500 text-xs rounded-full font-bold">${order.status}</span>
                        </td>
                    </tr>
                `;
            });

            totalOrders.innerText = orders.length;
            totalRevenue.innerText = "₦" + revenue.toLocaleString();
        }

        // UI Helpers
        function showToast(msg) {
            const toast = document.getElementById('toast');
            toast.innerText = msg;
            toast.classList.remove('translate-y-20', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
                toast.classList.remove('translate-y-0', 'opacity-100');
            }, 3000);
        }

        function toggleFaq(id) {
            const content = document.getElementById(`faq-content-${id}`);
            const icon = document.getElementById(`faq-icon-${id}`);
            const isHidden = content.classList.contains('hidden');
            
            content.classList.toggle('hidden');
            icon.style.transform = isHidden ? 'rotate(180deg)' : 'rotate(0deg)';
        }

        function copyToClipboard(text) {
            const el = document.createElement('textarea');
            el.value = text;
            document.body.appendChild(el);
            el.select();
            document.execCommand('copy');
            document.body.removeChild(el);
            showToast("Copied to clipboard!");
        }

    </script>
</body>
</html>

```
