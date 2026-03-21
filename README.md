<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>羊山石城 - 浙东千年石境，江南石窟奇观</title>
    <!-- 性能优化：预加载关键资源 -->
    <link rel="preconnect" href="https://cdn.tailwindcss.com">
    <link rel="preconnect" href="https://cdnjs.cloudflare.com">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    
    <!-- 引入Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com" defer></script>
    <!-- 引入Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- 引入谷歌字体：Noto Serif SC (衬线字体提升文化质感) -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- 自定义配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        // 升级配色：更贴合石材质感的大地色系
                        stone: {
                            50: '#F9F7F5',
                            100: '#F1EEE9',
                            200: '#E0D9CF',
                            300: '#C8BCAA',
                            400: '#A89883',
                            500: '#8B7860', // 主色调
                            600: '#73624E',
                            700: '#5A4E3F',
                            800: '#463C30',
                            900: '#332D23',
                        },
                        ink: { // 墨色 - 文本主色
                            100: '#F5F5F5',
                            200: '#E5E5E5',
                            300: '#D4D4D4',
                            400: '#A3A3A3',
                            500: '#737373',
                            600: '#525252',
                            700: '#404040', // 主要文本
                            800: '#262626',
                            900: '#171717',
                        },
                        accent: { // 点缀色 - 朱红
                            100: '#FEE2E2',
                            200: '#FECACA',
                            300: '#FCA5A5',
                            400: '#F87171',
                            500: '#EF4444',
                            600: '#DC2626', // 强调色
                            700: '#B91C1C',
                            800: '#991B1B',
                            900: '#7F1D1D',
                        }
                    },
                    fontFamily: {
                        serif: ['"Noto Serif SC"', 'serif'], // 中文衬线字体
                        sans: ['system-ui', 'sans-serif'],
                    },
                    boxShadow: {
                        'elegant': '0 4px 20px rgba(0, 0, 0, 0.08)',
                        'hover': '0 8px 30px rgba(0, 0, 0, 0.12)',
                    },
                    transitionProperty: {
                        'transform': 'transform 0.4s cubic-bezier(0.25, 0.1, 0.25, 1)',
                        'opacity': 'opacity 0.3s ease-in-out',
                    }
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            /* 自定义工具类 */
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow-elegant {
                text-shadow: 0 2px 8px rgba(0, 0, 0, 0.25);
            }
            .bg-gradient-overlay {
                background: linear-gradient(to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.7));
            }
            .scroll-mt-header {
                scroll-margin-top: 88px;
            }
            .image-hover-zoom {
                overflow: hidden;
            }
            .image-hover-zoom img {
                transition: transform 0.5s ease;
            }
            .image-hover-zoom:hover img {
                transform: scale(1.05);
            }
            /* 自定义滚动条 */
            ::-webkit-scrollbar {
                width: 8px;
            }
            ::-webkit-scrollbar-track {
                background: #f1f1f1;
            }
            ::-webkit-scrollbar-thumb {
                background: #8B7860;
                border-radius: 4px;
            }
            ::-webkit-scrollbar-thumb:hover {
                background: #73624E;
            }
            /* 图片加载占位样式 - 已移除图片，保留样式但不使用 */
            .img-placeholder {
                background-color: #F1EEE9;
                background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='40' height='40' viewBox='0 0 40 40'%3E%3Cg fill-rule='evenodd'%3E%3Cg fill='%23C8BCAA' fill-opacity='0.2'%3E%3Cpath d='M0 38.59l2.83-2.83 1.41 1.41L1.41 40H0v-1.41zM0 1.4l2.83 2.83 1.41-1.41L1.41 0H0v1.41zM38.59 40l-2.83-2.83 1.41-1.41L40 38.59V40h-1.41zM40 1.41l-2.83 2.83-1.41-1.41L38.59 0H40v1.41zM20 18.6l2.83-2.83 1.41 1.41L21.41 20l2.83 2.83-1.41 1.41L20 21.41l-2.83 2.83-1.41-1.41L18.59 20l-2.83-2.83 1.41-1.41L20 18.59z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            }
            /* 骨架屏加载效果 - 已移除图片，保留样式但不使用 */
            .skeleton {
                animation: skeleton-loading 1.5s linear infinite alternate;
            }
            @keyframes skeleton-loading {
                0% {
                    background-color: rgba(168, 152, 131, 0.1);
                }
                100% {
                    background-color: rgba(168, 152, 131, 0.3);
                }
            }
        }
    </style>
</head>
<body class="font-serif text-ink-700 bg-stone-50 antialiased">
    <!-- 导航栏 - 精致化升级 -->
    <header id="header" class="fixed w-full top-0 z-50 bg-white/98 backdrop-blur-sm shadow-elegant transition-all duration-300">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo - 更具文化质感 -->
            <a href="#home" class="flex items-center space-x-2 cursor-pointer">
                <span class="text-stone-500 text-3xl"><i class="fa-solid fa-gopuram"></i></span>
                <span class="text-[clamp(1.25rem,2vw,1.5rem)] font-bold text-stone-800 tracking-wider">羊山石城</span>
            </a>

            <!-- 桌面端导航 - 优化排版和交互 -->
            <nav class="hidden md:flex space-x-8">
                <a href="#home" class="nav-link font-medium text-ink-600 hover:text-stone-500 transition-colors pb-1 border-b-2 border-transparent hover:border-stone-500 cursor-pointer">首页</a>
                <a href="#about" class="nav-link font-medium text-ink-600 hover:text-stone-500 transition-colors pb-1 border-b-2 border-transparent hover:border-stone-500 cursor-pointer">石城溯源</a>
                <a href="#scenic" class="nav-link font-medium text-ink-600 hover:text-stone-500 transition-colors pb-1 border-b-2 border-transparent hover:border-stone-500 cursor-pointer">石窟胜景</a>
                <a href="#guide" class="nav-link font-medium text-ink-600 hover:text-stone-500 transition-colors pb-1 border-b-2 border-transparent hover:border-stone-500 cursor-pointer">游赏指南</a>
                <a href="#contact" class="nav-link font-medium text-ink-600 hover:text-stone-500 transition-colors pb-1 border-b-2 border-transparent hover:border-stone-500 cursor-pointer">预约咨询</a>
            </nav>

            <!-- 移动端汉堡菜单 - 精致化 -->
            <button id="menuBtn" class="md:hidden text-ink-800 text-xl" aria-expanded="false" aria-controls="mobileMenu">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- 移动端导航菜单 - 优化样式 -->
        <div id="mobileMenu" class="md:hidden hidden bg-white shadow-lg absolute w-full border-t border-stone-100" aria-hidden="true">
            <div class="container mx-auto px-6 py-4 flex flex-col space-y-4">
                <a href="#home" class="font-medium text-ink-700 hover:text-stone-500 transition-colors py-2 px-3 rounded-md hover:bg-stone-50 cursor-pointer">首页</a>
                <a href="#about" class="font-medium text-ink-700 hover:text-stone-500 transition-colors py-2 px-3 rounded-md hover:bg-stone-50 cursor-pointer">石城溯源</a>
                <a href="#scenic" class="font-medium text-ink-700 hover:text-stone-500 transition-colors py-2 px-3 rounded-md hover:bg-stone-50 cursor-pointer">石窟胜景</a>
                <a href="#guide" class="font-medium text-ink-700 hover:text-stone-500 transition-colors py-2 px-3 rounded-md hover:bg-stone-50 cursor-pointer">游赏指南</a>
                <a href="#contact" class="font-medium text-ink-700 hover:text-stone-500 transition-colors py-2 px-3 rounded-md hover:bg-stone-50 cursor-pointer">预约咨询</a>
            </div>
        </div>
    </header>

    <!-- 首页hero区 - 视觉升级（移除背景图） -->
    <section id="home" class="pt-24 scroll-mt-header">
        <div class="relative h-[90vh] min-h-[600px] overflow-hidden bg-stone-200">
            <!-- 移除背景图，保留渐变遮罩和布局 -->
            <div class="absolute inset-0 bg-gradient-overlay"></div>
            
            <!-- 文字内容 - 精致排版 -->
            <div class="relative h-full flex items-center justify-center text-center px-4">
                <div class="max-w-4xl">
                    <h1 class="text-[clamp(2.5rem,6vw,4.5rem)] font-bold text-white mb-6 text-shadow-elegant leading-tight">
                        羊山石境<br>
                        <span class="text-[clamp(1.5rem,3vw,2.5rem)] font-medium opacity-90">浙东千年石窟 · 江南采石奇观</span>
                    </h1>
                    <p class="text-[clamp(1rem,2vw,1.25rem)] text-white/90 mb-8 max-w-2xl mx-auto text-shadow-elegant">
                        始于隋唐，盛于明清，千年采石史铸就的地质瑰宝，融自然奇观与人文底蕴于一体
                    </p>
                    <a href="#guide" class="inline-block bg-stone-500 hover:bg-stone-600 text-white px-8 py-3 rounded-lg font-medium transition-all hover:shadow-lg transform hover:-translate-y-1 cursor-pointer">
                        探寻石境 <i class="fa-solid fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
            
            <!-- 向下滚动提示 -->
            <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 text-white animate-bounce cursor-pointer" onclick="document.querySelector('#about').scrollIntoView({behavior:'smooth'})">
                <i class="fa-solid fa-chevron-down text-xl opacity-80"></i>
            </div>
        </div>
    </section>

    <!-- 石城溯源 - 内容和视觉双重升级（移除图片） -->
    <section id="about" class="py-20 bg-white scroll-mt-header content-auto">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <!-- 标题区 - 精致化 -->
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-stone-800 mb-4">石城溯源</h2>
                <div class="w-16 h-1 bg-stone-500 mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-ink-500 text-lg">
                    千年采石史，一斧一凿间，铸就浙东独有的石宕石窟景观
                </p>
            </div>

            <div class="grid md:grid-cols-2 gap-16 items-center">
                <!-- 移除图片区，替换为文字占位 -->
                <div class="rounded-xl overflow-hidden shadow-elegant bg-stone-100 h-[400px] flex items-center justify-center">
                    <div class="text-center p-8">
                        <i class="fa-solid fa-landmark text-stone-400 text-6xl mb-4"></i>
                        <h3 class="text-xl font-semibold text-stone-700">羊山石城摩崖石刻</h3>
                        <p class="text-ink-500 mt-2">千年采石历史的珍贵见证</p>
                    </div>
                </div>
                
                <!-- 文字内容区 - 优化排版和质感 -->
                <div class="space-y-8">
                    <h3 class="text-[clamp(1.25rem,2vw,1.75rem)] font-semibold text-stone-800 border-l-4 border-stone-500 pl-4">
                        千年采石 岁月留痕
                    </h3>
                    
                    <p class="text-ink-600 leading-relaxed text-lg">
                        羊山石城坐落于绍兴市柯桥区齐贤街道，东临杭州湾，北接钱塘。自隋唐始采石，至明清达鼎盛，历经十数朝更迭，千余年开采，形成了如今峰石林立、窟洞相连的独特地貌，被誉为"江南小敦煌"。
                    </p>
                    
                    <p class="text-ink-600 leading-relaxed text-lg">
                        这里不仅是绍兴古城建设的石材之源，更因独特的喀斯特石峰与石窟造像，成为浙东地区自然与人文交融的典范，亦是《西游记》《越王勾践》等经典影视作品的取景地。
                    </p>
                    
                    <!-- 核心信息卡片 - 精致化设计（全部可点击跳转） -->
                    <div class="grid grid-cols-2 gap-4 mt-4">
                        <!-- 隋唐始采石 -->
                        <div class="bg-stone-50 rounded-lg p-4 border border-stone-100 hover:shadow-hover transition-all cursor-pointer group" onclick="document.querySelector('#about').scrollIntoView({behavior:'smooth'})">
                            <div class="flex items-center mb-2">
                                <span class="text-stone-500 text-xl mr-3 group-hover:text-accent-600 transition-colors">
                                    <i class="fa-solid fa-calendar"></i>
                                </span>
                                <h4 class="font-medium text-stone-800">隋唐始采石</h4>
                            </div>
                            <p class="text-ink-500 text-sm">距今1400余年采石史，越州古城建设之基</p>
                        </div>
                        
                        <!-- 面积约800亩 -->
                        <div class="bg-stone-50 rounded-lg p-4 border border-stone-100 hover:shadow-hover transition-all cursor-pointer group" onclick="document.querySelector('#scenic').scrollIntoView({behavior:'smooth'})">
                            <div class="flex items-center mb-2">
                                <span class="text-stone-500 text-xl mr-3 group-hover:text-accent-600 transition-colors">
                                    <i class="fa-solid fa-ruler-combined"></i>
                                </span>
                                <h4 class="font-medium text-stone-800">面积约800亩</h4>
                            </div>
                            <p class="text-ink-500 text-sm">核心景区300亩，大小石峰百余座</p>
                        </div>
                        
                        <!-- 影视取景地 -->
                        <div class="bg-stone-50 rounded-lg p-4 border border-stone-100 hover:shadow-hover transition-all cursor-pointer group" onclick="document.querySelector('#scenic').scrollIntoView({behavior:'smooth'})">
                            <div class="flex items-center mb-2">
                                <span class="text-stone-500 text-xl mr-3 group-hover:text-accent-600 transition-colors">
                                    <i class="fa-solid fa-film"></i>
                                </span>
                                <h4 class="font-medium text-stone-800">影视取景地</h4>
                            </div>
                            <p class="text-ink-500 text-sm">江南第一影视石城，多部经典作品取景</p>
                        </div>
                        
                        <!-- 绍兴柯桥区 -->
                        <div class="bg-stone-50 rounded-lg p-4 border border-stone-100 hover:shadow-hover transition-all cursor-pointer group" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                            <div class="flex items-center mb-2">
                                <span class="text-stone-500 text-xl mr-3 group-hover:text-accent-600 transition-colors">
                                    <i class="fa-solid fa-map-marker"></i>
                                </span>
                                <h4 class="font-medium text-stone-800">绍兴柯桥区</h4>
                            </div>
                            <p class="text-ink-500 text-sm">绍兴北部，融纺织之都与千年石韵于一体</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 石窟胜景 - 画廊式展示升级（移除所有图片） -->
    <section id="scenic" class="py-20 bg-stone-50 scroll-mt-header content-auto">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <!-- 标题区 -->
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-stone-800 mb-4">石窟胜景</h2>
                <div class="w-16 h-1 bg-stone-500 mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-ink-500 text-lg">
                    鬼斧神工的石峰造像，穿越千年的摩崖题刻，每一处皆是历史的印记
                </p>
            </div>

            <!-- 特色分类 - 精致卡片（全部可点击跳转） -->
            <div class="grid md:grid-cols-3 gap-8 mb-16">
                <!-- 石峰造像 -->
                <div class="bg-white rounded-xl shadow-elegant hover:shadow-hover transition-all overflow-hidden cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                    <div class="h-48 bg-stone-100 flex items-center justify-center">
                        <span class="text-stone-500 text-6xl"><i class="fa-solid fa-monument"></i></span>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold text-stone-800 mb-3">石峰造像</h3>
                        <p class="text-ink-600 mb-4">
                            依石而凿的佛造像群，神态各异，工艺精湛，见证了浙东佛教文化的兴盛。
                        </p>
                        <a href="#guide" class="text-stone-500 font-medium hover:text-stone-600 inline-flex items-center cursor-pointer">
                            探寻详情 <i class="fa-solid fa-long-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>

                <!-- 摩崖石刻 -->
                <div class="bg-white rounded-xl shadow-elegant hover:shadow-hover transition-all overflow-hidden cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                    <div class="h-48 bg-stone-100 flex items-center justify-center">
                        <span class="text-stone-500 text-6xl"><i class="fa-solid fa-scroll"></i></span>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold text-stone-800 mb-3">摩崖石刻</h3>
                        <p class="text-ink-600 mb-4">
                            历代文人墨客的题咏石刻，朱红墨迹与苍劲石壁相映，墨香石韵千古流传。
                        </p>
                        <a href="#guide" class="text-stone-500 font-medium hover:text-stone-600 inline-flex items-center cursor-pointer">
                            探寻详情 <i class="fa-solid fa-long-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>

                <!-- 古采石宕 -->
                <div class="bg-white rounded-xl shadow-elegant hover:shadow-hover transition-all overflow-hidden cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                    <div class="h-48 bg-stone-100 flex items-center justify-center">
                        <span class="text-stone-500 text-6xl"><i class="fa-solid fa-hammer"></i></span>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold text-stone-800 mb-3">古采石宕</h3>
                        <p class="text-ink-600 mb-4">
                            保存完好的古采石遗址，清晰的凿痕见证着古代工匠的智慧与汗水。
                        </p>
                        <a href="#guide" class="text-stone-500 font-medium hover:text-stone-600 inline-flex items-center cursor-pointer">
                            探寻详情 <i class="fa-solid fa-long-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>
            </div>

            <!-- 移除所有图片画廊 -->
            <div class="bg-stone-100 rounded-xl p-8 text-center mb-8">
                <i class="fa-solid fa-images text-stone-400 text-5xl mb-4"></i>
                <h3 class="text-xl font-semibold text-stone-800 mb-2">石刻记忆</h3>
                <p class="text-ink-500">镌刻心声，留存印记
写下你的留言与感悟，让旅途印记在此长存，与万千同路人共筑石刻记忆。</p>
                <!-- 修改此处：href改为#contact，添加onclick事件 -->
                <a href="#contact" class="inline-block mt-4 text-stone-500 font-medium hover:text-stone-600 cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                    游客留言入口<i class="fa-solid fa-arrow-right ml-2"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- 游赏指南 - 精致卡片设计（全部可点击跳转） -->
    <section id="guide" class="py-20 bg-white scroll-mt-header content-auto">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <!-- 标题区 -->
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-stone-800 mb-4">游赏指南</h2>
                <div class="w-16 h-1 bg-stone-500 mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-ink-500 text-lg">
                    贴心实用的游玩信息，让您的羊山石城之旅舒心惬意
                </p>
            </div>

            <div class="grid md:grid-cols-2 gap-12">
                <!-- 基本信息卡片 -->
                <div class="bg-stone-50 rounded-xl shadow-elegant p-8 border border-stone-100">
                    <h3 class="text-xl font-semibold text-stone-800 mb-6 flex items-center">
                        <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-stone-500 text-white mr-4">
                            <i class="fa-solid fa-info"></i>
                        </span>
                        基本信息
                    </h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-map-marker text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">地理位置</h4>
                                <p class="text-ink-600">浙江省绍兴市柯桥区齐贤街道羊山风景区</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-clock text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">开放时间</h4>
                                <p class="text-ink-600">全年开放 08:00 - 17:00（16:30停止入园）</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-ticket text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">门票价格</h4>
                                <p class="text-ink-600">成人票 20元/人，学生票 10元/人，60岁以上老人免票</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-phone text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">咨询电话</h4>
                                <p class="text-ink-600">0575-85186888</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 交通指南卡片 -->
                <div class="bg-stone-50 rounded-xl shadow-elegant p-8 border border-stone-100">
                    <h3 class="text-xl font-semibold text-stone-800 mb-6 flex items-center">
                        <span class="inline-flex items-center justify-center w-10 h-10 rounded-full bg-stone-500 text-white mr-4">
                            <i class="fa-solid fa-car"></i>
                        </span>
                        交通指南
                    </h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-car-side text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">自驾前往</h4>
                                <p class="text-ink-600">
                                    绍兴市区：沿群贤路向东，转羊山路即达（车程约20分钟）<br>
                                    杭州市区：杭甬高速柯桥出口下，沿金柯桥大道向北（车程约1小时）
                                </p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-bus text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">公共交通</h4>
                                <p class="text-ink-600">
                                    绍兴市区：18路、807路、815路至羊山公园站下车<br>
                                    柯桥城区：808路、818路至羊山石城站下车
                                </p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-2 mr-4 mt-1">
                                <i class="fa-solid fa-lightbulb text-stone-500"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">游玩建议</h4>
                                <p class="text-ink-600">
                                    建议游玩时长：2-3小时<br>
                                    最佳游玩季节：春秋两季（3-5月、9-11月）<br>
                                    注意事项：部分路段台阶较陡，建议着舒适鞋履
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 预约咨询 - 精致表单设计（全部可点击跳转） -->
    <section id="contact" class="py-20 bg-stone-50 scroll-mt-header content-auto">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <!-- 标题区 -->
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.75rem,3vw,2.5rem)] font-bold text-stone-800 mb-4">预约咨询</h2>
                <div class="w-16 h-1 bg-stone-500 mx-auto mb-6"></div>
                <p class="max-w-2xl mx-auto text-ink-500 text-lg">
                    如有任何疑问或团队预约需求，欢迎随时与我们联系
                </p>
            </div>

            <div class="grid md:grid-cols-2 gap-12">
                <!-- 联系信息 -->
                <div class="space-y-8">
                    <h3 class="text-xl font-semibold text-stone-800">联系方式</h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-3 mr-4">
                                <i class="fa-solid fa-map-marker text-stone-500 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">景区地址</h4>
                                <p class="text-ink-600">浙江省绍兴市柯桥区齐贤街道羊山风景区管理处</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-3 mr-4">
                                <i class="fa-solid fa-phone text-stone-500 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">咨询热线</h4>
                                <p class="text-ink-600">0575-85186888（工作时间：8:00-17:00）</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                            <div class="bg-stone-100 rounded-full p-3 mr-4">
                                <i class="fa-solid fa-envelope text-stone-500 text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-stone-800 mb-1">电子邮箱</h4>
                                <p class="text-ink-600">yangshanshicheng@163.com</p>
                            </div>
                        </div>
                    </div>

                    <!-- 移除公众号二维码图片，替换为文字 -->
                    <div class="bg-white rounded-xl shadow-elegant p-6 inline-block border border-stone-100 cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                        <h4 class="font-medium text-stone-800 mb-3 text-center">景区AR导航</h4>
                        <p class="text-ink-500 text-sm text-center mb-3">扫码关注，开启探索之旅吧！</p>
                        <div class="w-40 h-40 bg-stone-100 rounded mx-auto flex items-center justify-center">
                            <i class="fa-solid fa-qrcode text-stone-400 text-5xl"></i>
                        </div>
                    </div>
                </div>

                <!-- 咨询表单 - 精致化（提交按钮可点击） -->
                <div class="bg-white rounded-xl shadow-elegant p-8 border border-stone-100">
                    <h3 class="text-xl font-semibold text-stone-800 mb-6">在线预约咨询</h3>
                    
                    <form id="contactForm" class="space-y-4">
                        <div>
                            <label for="name" class="block text-ink-700 mb-2 font-medium">姓名 <span class="text-accent-600">*</span></label>
                            <input type="text" id="name" 
                                   class="w-full px-4 py-3 border border-stone-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-stone-500 focus:border-transparent transition-all" 
                                   placeholder="请输入您的姓名" required>
                        </div>
                        
                        <div>
                            <label for="phone" class="block text-ink-700 mb-2 font-medium">联系电话 <span class="text-accent-600">*</span></label>
                            <input type="tel" id="phone" 
                                   class="w-full px-4 py-3 border border-stone-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-stone-500 focus:border-transparent transition-all" 
                                   placeholder="请输入您的手机号码" pattern="^1[3-9]\d{9}$" required>
                            <p class="text-ink-500 text-sm mt-1">请输入有效的11位手机号码</p>
                        </div>
                        
                        <div>
                            <label for="consultType" class="block text-ink-700 mb-2 font-medium">咨询类型</label>
                            <select id="consultType" 
                                    class="w-full px-4 py-3 border border-stone-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-stone-500 focus:border-transparent transition-all">
                                <option value="">请选择咨询类型</option>
                                <option value="ticket">门票咨询</option>
                                <option value="group">团队预约</option>
                                <option value="visit">游玩咨询</option>
                                <option value="other">其他问题</option>
                            </select>
                        </div>
                        
                        <div>
                            <label for="message" class="block text-ink-700 mb-2 font-medium">留言内容 <span class="text-accent-600">*</span></label>
                            <textarea id="message" rows="5" 
                                      class="w-full px-4 py-3 border border-stone-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-stone-500 focus:border-transparent transition-all resize-none" 
                                      placeholder="请详细描述您的问题或需求" required></textarea>
                        </div>
                        
                        <button type="submit" 
                                class="w-full bg-stone-500 hover:bg-stone-600 text-white font-medium py-3 px-6 rounded-lg transition-all hover:shadow-lg transform hover:-translate-y-1">
                            提交咨询 <i class="fa-solid fa-paper-plane ml-2"></i>
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 - 精致化设计（所有链接可点击跳转） -->
    <footer class="bg-stone-800 text-white py-12">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-4 gap-8 mb-8">
                <!-- 品牌区 -->
                <div>
                    <div class="flex items-center space-x-2 mb-4 cursor-pointer" onclick="document.querySelector('#home').scrollIntoView({behavior:'smooth'})">
                        <span class="text-stone-300 text-2xl"><i class="fa-solid fa-gopuram"></i></span>
                        <span class="text-xl font-bold tracking-wider">羊山石城</span>
                    </div>
                    <p class="text-stone-400 mb-4 text-sm">
                        千年采石文化，江南石窟奇观<br>
                        浙东地区独树一帜的自然人文瑰宝
                    </p>
                </div>
                
                <!-- 快速链接 -->
                <div>
                    <h3 class="text-lg font-medium mb-4 text-stone-200">快速链接</h3>
                    <ul class="space-y-2 text-sm">
                        <li><a href="#home" class="text-stone-400 hover:text-white transition-colors cursor-pointer">首页</a></li>
                        <li><a href="#about" class="text-stone-400 hover:text-white transition-colors cursor-pointer">石城溯源</a></li>
                        <li><a href="#scenic" class="text-stone-400 hover:text-white transition-colors cursor-pointer">石窟胜景</a></li>
                        <li><a href="#guide" class="text-stone-400 hover:text-white transition-colors cursor-pointer">游赏指南</a></li>
                    </ul>
                </div>
                
                <!-- 实用信息 -->
                <div>
                    <h3 class="text-lg font-medium mb-4 text-stone-200">实用信息</h3>
                    <ul class="space-y-2 text-sm">
                        <li><a href="#contact" class="text-stone-400 hover:text-white transition-colors cursor-pointer">门票预订</a></li>
                        <li><a href="#contact" class="text-stone-400 hover:text-white transition-colors cursor-pointer">团队接待</a></li>
                        <li><a href="#contact" class="text-stone-400 hover:text-white transition-colors cursor-pointer">景区公告</a></li>
                        <li><a href="#guide" class="text-stone-400 hover:text-white transition-colors cursor-pointer">游客须知</a></li>
                    </ul>
                </div>
                
                <!-- 联系信息 -->
                <div>
                    <h3 class="text-lg font-medium mb-4 text-stone-200">联系我们</h3>
                    <ul class="space-y-2 text-sm">
                        <li class="flex items-start cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                            <i class="fa-solid fa-map-marker text-stone-400 mt-1 mr-2"></i>
                            <span class="text-stone-400">绍兴市柯桥区齐贤街道羊山风景区</span>
                        </li>
                        <li class="flex items-start cursor-pointer" onclick="document.querySelector('#guide').scrollIntoView({behavior:'smooth'})">
                            <i class="fa-solid fa-phone text-stone-400 mt-1 mr-2"></i>
                            <span class="text-stone-400">0575-85186888</span>
                        </li>
                        <li class="flex items-start cursor-pointer" onclick="document.querySelector('#contact').scrollIntoView({behavior:'smooth'})">
                            <i class="fa-solid fa-envelope text-stone-400 mt-1 mr-2"></i>
                            <span class="text-stone-400">yangshanshicheng@163.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <!-- 版权信息 -->
            <div class="border-t border-stone-700 pt-8 text-center text-stone-500 text-sm">
                <p>© 2025 绍兴羊山石城风景区 版权所有 | 浙ICP备12345678号</p>
                <p class="mt-2">本网站已备案，保护知识产权，严禁未经授权的复制与转载</p>
            </div>
        </div>
    </footer>

    <!-- JavaScript - 优化交互体验 -->
    <script>
        // DOM加载完成后执行
        document.addEventListener('DOMContentLoaded', function() {
            // 性能优化：防抖函数
            function debounce(func, wait) {
                let timeout;
                return function() {
                    const context = this;
                    const args = arguments;
                    clearTimeout(timeout);
                    timeout = setTimeout(() => func.apply(context, args), wait);
                };
            }

            // 移动端菜单切换
            const menuBtn = document.getElementById('menuBtn');
            const mobileMenu = document.getElementById('mobileMenu');
            
            if (menuBtn && mobileMenu) {
                menuBtn.addEventListener('click', () => {
                    const isExpanded = menuBtn.getAttribute('aria-expanded') === 'true';
                    mobileMenu.classList.toggle('hidden');
                    menuBtn.setAttribute('aria-expanded', !isExpanded);
                    mobileMenu.setAttribute('aria-hidden', isExpanded);
                    
                    // 切换图标
                    const icon = menuBtn.querySelector('i');
                    if (isExpanded) {
                        icon.classList.replace('fa-times', 'fa-bars');
                    } else {
                        icon.classList.replace('fa-bars', 'fa-times');
                    }
                });
            }

            // 导航栏滚动效果 - 防抖优化
            const header = document.getElementById('header');
            let lastScrollPos = 0;
            
            const handleScroll = debounce(() => {
                const currentScrollPos = window.pageYOffset;
                
                if (header) {
                    // 导航栏样式变化
                    if (currentScrollPos > 50) {
                        header.classList.add('py-2', 'shadow-md');
                        header.classList.remove('py-4');
                    } else {
                        header.classList.add('py-4');
                        header.classList.remove('py-2', 'shadow-md');
                    }
                    
                    // 导航栏当前位置高亮 - 优化逻辑
                    const sections = document.querySelectorAll('section[id]');
                    const navLinks = document.querySelectorAll('.nav-link');
                    
                    // 重置所有链接样式
                    navLinks.forEach(link => {
                        link.classList.remove('text-stone-500', 'border-stone-500');
                        link.classList.add('text-ink-600', 'border-transparent');
                    });
                    
                    // 找到当前可视区域的section并高亮对应链接
                    sections.forEach(section => {
                        const sectionTop = section.offsetTop - 120;
                        const sectionHeight = section.offsetHeight;
                        const sectionId = section.getAttribute('id');
                        
                        if (currentScrollPos >= sectionTop && currentScrollPos < sectionTop + sectionHeight) {
                            navLinks.forEach(link => {
                                if (link.getAttribute('href') === `#${sectionId}`) {
                                    link.classList.remove('text-ink-600', 'border-transparent');
                                    link.classList.add('text-stone-500', 'border-stone-500');
                                }
                            });
                        }
                    });
                    
                    lastScrollPos = currentScrollPos;
                }
            }, 50); // 缩短防抖时间，提升响应性
            
            window.addEventListener('scroll', handleScroll);

            // 平滑滚动 - 统一处理所有跳转
            document.querySelectorAll('a[href^="#"], [onclick*="scrollIntoView"]').forEach(element => {
                element.addEventListener('click', function (e) {
                    // 如果是a标签，阻止默认行为
                    if (this.tagName === 'A') {
                        e.preventDefault();
                        
                        // 获取目标ID并滚动
                        const targetId = this.getAttribute('href').substring(1);
                        const targetElement = document.getElementById(targetId);
                        if (targetElement) {
                            targetElement.scrollIntoView({ behavior: 'smooth' });
                        }
                    }
                    
                    // 关闭移动端菜单（如果打开）
                    if (mobileMenu && !mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                        menuBtn.setAttribute('aria-expanded', 'false');
                        mobileMenu.setAttribute('aria-hidden', 'true');
                        menuBtn.querySelector('i').classList.replace('fa-times', 'fa-bars');
                    }
                });
            });

            // 表单提交处理 - 增强验证和反馈
            const contactForm = document.getElementById('contactForm');
            if (contactForm) {
                contactForm.addEventListener('submit', (e) => {
                    e.preventDefault();
                    
                    // 验证表单
                    if (!contactForm.checkValidity()) {
                        // 显示原生验证提示
                        contactForm.reportValidity();
                        return;
                    }
                    
                    const submitBtn = contactForm.querySelector('button[type="submit"]');
                    if (submitBtn) {
                        // 禁用按钮并显示加载状态
                        submitBtn.disabled = true;
                        submitBtn.innerHTML = '<i class="fa-solid fa-spinner fa-spin mr-2"></i> 提交中...';
                        
                        // 模拟提交
                        setTimeout(() => {
                            // 创建成功提示
                            const successAlert = document.createElement('div');
                            successAlert.className = 'fixed top-20 left-1/2 transform -translate-x-1/2 bg-green-600 text-white px-6 py-3 rounded-lg shadow-lg z-50 animate-fade-in';
                            successAlert.textContent = '您的咨询已提交成功！我们将在1-2个工作日内与您联系。';
                            document.body.appendChild(successAlert);
                            
                            // 添加动画样式
                            successAlert.style.transition = 'opacity 0.5s ease-in-out';
                            
                            // 3秒后移除提示
                            setTimeout(() => {
                                successAlert.style.opacity = '0';
                                setTimeout(() => successAlert.remove(), 500);
                            }, 3000);
                            
                            // 重置表单并恢复按钮状态
                            contactForm.reset();
                            submitBtn.disabled = false;
                            submitBtn.innerHTML = '提交咨询 <i class="fa-solid fa-paper-plane ml-2"></i>';
                        }, 1200);
                    }
                });
                
                // 实时验证手机号
                const phoneInput = document.getElementById('phone');
                if (phoneInput) {
                    phoneInput.addEventListener('input', function() {
                        const phonePattern = /^1[3-9]\d{9}$/;
                        if (this.value && !phonePattern.test(this.value)) {
                            this.setCustomValidity('请输入有效的11位手机号码');
                        } else {
                            this.setCustomValidity('');
                        }
                    });
                }
            }
        });
    </script>
</body>
</html>
