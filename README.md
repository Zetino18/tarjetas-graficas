<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proyecto Zetino - Tarjetas Gráficas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#2563eb',
                        secondary: '#1e40af',
                        accent: '#3b82f6',
                        dark: '#111827',
                        light: '#f3f4f6'
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        .product-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .product-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        .badge-pulse {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { opacity: 0.8; }
            50% { opacity: 1; }
            100% { opacity: 0.8; }
        }
        .survey-input:checked + label {
            border-color: #3b82f6;
            background-color: #eff6ff;
            transform: scale(1.02);
        }
        .gpu-feature {
            background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
            transition: all 0.3s ease;
        }
        .gpu-feature:hover {
            transform: translateY(-4px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Header -->
    <header class="bg-gradient-to-r from-dark to-gray-900 text-white sticky top-0 z-50 shadow-lg">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center py-4">
                <div class="flex items-center mb-4 md:mb-0">
                    <i class="fas fa-microchip text-accent text-3xl mr-3"></i>
                    <div>
                        <h1 class="text-2xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-white to-accent">PROYECTO ZETINO</h1>
                        <p class="text-gray-300 text-sm">Tarjetas gráficas de alto rendimiento</p>
                    </div>
                </div>
                <nav class="hidden md:flex space-x-6">
                    <a href="#products" class="hover:text-accent transition-colors">Productos</a>
                    <a href="#features" class="hover:text-accent transition-colors">Características</a>
                    <a href="#survey" class="hover:text-accent transition-colors">Encuesta</a>
                    <a href="#contact" class="hover:text-accent transition-colors">Contacto</a>
                </nav>
                <div class="flex items-center space-x-4">
                    <a href="tel:9615689589" class="flex items-center hover:text-accent transition-colors">
                        <i class="fas fa-phone mr-2"></i>
                        <span class="hidden sm:inline">961 568 9589</span>
                    </a>
                    <a href="mailto:cesarzetinozetino@gmail.com" class="flex items-center hover:text-accent transition-colors">
                        <i class="fas fa-envelope mr-2"></i>
                        <span class="hidden sm:inline">Contacto</span>
                    </a>
                    <button class="md:hidden text-white focus:outline-none">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-gradient-to-br from-dark to-gray-800 text-white py-20 overflow-hidden">
        <div class="absolute inset-0 opacity-20">
            <div class="absolute top-0 left-0 w-64 h-64 bg-accent rounded-full filter blur-3xl opacity-30"></div>
            <div class="absolute bottom-0 right-0 w-64 h-64 bg-accent rounded-full filter blur-3xl opacity-20"></div>
        </div>
        <div class="container mx-auto px-4 z-10 relative">
            <div class="max-w-3xl mx-auto text-center">
                <span class="inline-block mb-4 px-4 py-2 bg-accent/10 rounded-full text-accent border border-accent/30 text-sm font-medium">ÚLTIMAS NOVEDADES</span>
                <h2 class="text-4xl md:text-5xl font-bold mb-6 leading-tight">Potencia tu experiencia con nuestras <span class="text-accent">GPU</span> de alto rendimiento</h2>
                <p class="text-xl text-gray-300 mb-8">Descubre la mejor selección de tarjetas gráficas para gaming, diseño y renderizado profesional.</p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#products" class="px-8 py-3 bg-accent hover:bg-primary rounded-lg font-medium transition-all transform hover:scale-105 shadow-lg shadow-accent/30">Explorar productos</a>
                    <a href="#features" class="px-8 py-3 border border-gray-600 hover:border-accent rounded-lg font-medium transition-all hover:text-accent">Ver características</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats -->
    <div class="relative bg-gray-100 overflow-hidden">
        <div class="relative container mx-auto px-4 py-8">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                <div class="bg-white p-6 rounded-xl shadow-sm text-center">
                    <div class="text-3xl font-bold text-dark mb-2">5+</div>
                    <div class="text-gray-600">Años en el mercado</div>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-sm text-center">
                    <div class="text-3xl font-bold text-dark mb-2">500+</div>
                    <div class="text-gray-600">Clientes satisfechos</div>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-sm text-center">
                    <div class="text-3xl font-bold text-dark mb-2">15+</div>
                    <div class="text-gray-600">Marcas disponibles</div>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-sm text-center">
                    <div class="text-3xl font-bold text-dark mb-2">24/7</div>
                    <div class="text-gray-600">Soporte técnico</div>
                </div>
            </div>
        </div>
    </div>

    <!-- Features Section -->
    <section id="features" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="max-w-3xl mx-auto text-center mb-12">
                <h2 class="text-3xl font-bold mb-4 text-dark">¿Por qué elegir nuestras GPU?</h2>
                <p class="text-gray-600">Ofrecemos las mejores soluciones gráficas para todas tus necesidades</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="gpu-feature p-6 rounded-xl">
                    <div class="w-14 h-14 bg-accent/10 rounded-lg flex items-center justify-center text-accent mb-4">
                        <i class="fas fa-tachometer-alt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Alto Rendimiento</h3>
                    <p class="text-gray-600">GPUs diseñadas para ofrecer el máximo rendimiento en juegos y aplicaciones profesionales.</p>
                </div>
                
                <div class="gpu-feature p-6 rounded-xl">
                    <div class="w-14 h-14 bg-accent/10 rounded-lg flex items-center justify-center text-accent mb-4">
                        <i class="fas fa-snowflake text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Enfriamiento Avanzado</h3>
                    <p class="text-gray-600">Sistemas de refrigeración eficientes que mantienen temperaturas óptimas incluso bajo carga intensa.</p>
                </div>
                
                <div class="gpu-feature p-6 rounded-xl">
                    <div class="w-14 h-14 bg-accent/10 rounded-lg flex items-center justify-center text-accent mb-4">
                        <i class="fas fa-shield-alt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Garantía Extendida</h3>
                    <p class="text-gray-600">Todas nuestras tarjetas gráficas incluyen garantía de 3 años y soporte técnico especializado.</p>
                </div>
                
                <div class="gpu-feature p-6 rounded-xl">
                    <div class="w-14 h-14 bg-accent/10 rounded-lg flex items-center justify-center text-accent mb-4">
                        <i class="fas fa-dollar-sign text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Precios Competitivos</h3>
                    <p class="text-gray-600">Ofrecemos las mejores tarifas del mercado con financiamiento disponible.</p>
                </div>
                
                <div class="gpu-feature p-6 rounded-xl">
                    <div class="w-14 h-14 bg-accent/10 rounded-lg flex items-center justify-center text-accent mb-4">
                        <i class="fas fa-bolt text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Eficiencia Energética</h3>
                    <p class="text-gray-600">Tecnologías de ahorro de energía que reducen el consumo sin sacrificar rendimiento.</p>
                </div>
                
                <div class="gpu-feature p-6 rounded-xl">
                    <div class="w-14 h-14 bg-accent/10 rounded-lg flex items-center justify-center text-accent mb-4">
                        <i class="fas fa-headset text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Soporte Personalizado</h3>
                    <p class="text-gray-600">Asesoramiento experto para ayudarte a elegir la mejor GPU para tus necesidades específicas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="max-w-3xl mx-auto text-center mb-12">
                <h2 class="text-3xl font-bold mb-4 text-dark">NUESTROS PRODUCTOS DESTACADOS</h2>
                <p class="text-gray-600">Selección premium de las mejores tarjetas gráficas del mercado</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Product 1 -->
                <div class="product-card group bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1591488320449-011701bb6704?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" 
                             alt="NVIDIA RTX 4090" class="w-full h-64 object-cover group-hover:opacity-90 transition-opacity">
                        <div class="absolute top-4 left-4">
                            <span class="bg-accent text-white px-3 py-1 rounded-full text-xs font-bold badge-pulse">NUEVO</span>
                        </div>
                        <div class="absolute top-4 right-4">
                            <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-gray-100 transition-colors">
                                <i class="far fa-heart text-gray-600"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex items-center mb-2">
                            <div class="w-3 h-3 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-gray-500">EN STOCK</span>
                        </div>
                        <h3 class="text-xl font-bold mb-2 text-dark">NVIDIA RTX 4090</h3>
                        <div class="flex items-center text-yellow-400 mb-3">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                            <span class="text-gray-500 text-sm ml-2">(24 reviews)</span>
                        </div>
                        <p class="text-gray-600 mb-5 text-sm">La tarjeta gráfica más potente del mercado con 24GB GDDR6X para gaming 8K y creación 3D profesional.</p>
                        <div class="flex items-end justify-between">
                            <div>
                                <span class="text-2xl font-bold text-dark">$9,899.99</span>
                                <span class="block text-xs text-gray-500">Costo producción: $600</span>
                            </div>
                            <button class="px-6 py-2 bg-dark text-white rounded-lg font-medium hover:bg-gray-800 transition-all transform hover:scale-105 active:scale-95">
                                <i class="fas fa-shopping-cart mr-2"></i> Comprar
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Product 2 -->
                <div class="product-card group bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative">
                        <img src="img/rtx.png.jpg"
                             alt="AMD RX 7900 XTX" class="w-full h-64 object-cover group-hover:opacity-90 transition-opacity">
                        <div class="absolute top-4 left-4">
                            <span class="bg-red-500 text-white px-3 py-1 rounded-full text-xs font-bold">OFERTA</span>
                            <span class="block mt-2 bg-blue-500 text-white px-3 py-1 rounded-full text-xs font-bold">-15%</span>
                        </div>
                        <div class="absolute top-4 right-4">
                            <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-gray-100 transition-colors">
                                <i class="far fa-heart text-gray-600"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex items-center mb-2">
                            <div class="w-3 h-3 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-gray-500">ÚLTIMAS UNIDADES</span>
                        </div>
                        <h3 class="text-xl font-bold mb-2 text-dark">AMD RX 7900 XTX</h3>
                        <div class="flex items-center text-yellow-400 mb-3">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="far fa-star"></i>
                            <span class="text-gray-500 text-sm ml-2">(18 reviews)</span>
                        </div>
                        <p class="text-gray-600 mb-5 text-sm">Rendimiento premium para gamers exigentes con 24GB GDDR6 y arquitectura RDNA 3.</p>
                        <div class="flex items-end justify-between">
                            <div>
                                <span class="text-2xl font-bold text-dark">$9,899.99</span>
                                <span class="block text-xs text-gray-500">Costo producción: $450</span>
                            </div>
                            <button class="px-6 py-2 bg-dark text-white rounded-lg font-medium hover:bg-gray-800 transition-all transform hover:scale-105 active:scale-95">
                                <i class="fas fa-shopping-cart mr-2"></i> Comprar
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Product 3 -->
                <div class="product-card group bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative">
                        <img src="img/NVIDIA RTX 3080 Ti.png.png"
                             alt="NVIDIA RTX 3080 Ti" class="w-full h-64 object-cover group-hover:opacity-90 transition-opacity">
                        <div class="absolute top-4 right-4">
                            <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-gray-100 transition-colors">
                                <i class="far fa-heart text-gray-600"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex items-center mb-2">
                            <div class="w-3 h-3 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-gray-500">DISPONIBLE</span>
                        </div>
                        <h3 class="text-xl font-bold mb-2 text-dark">NVIDIA RTX 3080 Ti</h3>
                        <div class="flex items-center text-yellow-400 mb-3">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <span class="text-gray-500 text-sm ml-2">(36 reviews)</span>
                        </div>
                        <p class="text-gray-600 mb-5 text-sm">Excelente relación calidad-precio para gaming en 4K con 12GB GDDR6X y ray tracing.</p>
                        <div class="flex items-end justify-between">
                            <div>
                                <span class="text-2xl font-bold text-dark">$9,899.99</span>
                                <span class="block text-xs text-gray-500">Costo producción: $350</span>
                            </div>
                            <button class="px-6 py-2 bg-dark text-white rounded-lg font-medium hover:bg-gray-800 transition-all transform hover:scale-105 active:scale-95">
                                <i class="fas fa-shopping-cart mr-2"></i> Comprar
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <button class="px-8 py-3 border border-dark text-dark rounded-lg font-medium hover:bg-dark hover:text-white transition-all">
                    Ver todo el catálogo <i class="fas fa-arrow-right ml-2"></i>
                </button>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="max-w-3xl mx-auto text-center mb-12">
                <h2 class="text-3xl font-bold mb-4 text-dark">COMPARATIVA DE PRODUCTOS</h2>
                <p class="text-gray-600">Toda la información que necesitas para tomar la mejor decisión</p>
            </div>
            
            <div class="overflow-x-auto">
                <table class="w-full">
                    <thead>
                        <tr class="border-b border-gray-200">
                            <th class="py-4 px-6 text-left">Especificaciones</th>
                            <th class="py-4 px-6 text-center">RTX 4090</th>
                            <th class="py-4 px-6 text-center">RX 7900 XTX</th>
                            <th class="py-4 px-6 text-center">RTX 3080 Ti</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="border-b border-gray-200">
                            <td class="py-4 px-6 text-gray-600">Memoria</td>
                            <td class="py-4 px-6 text-center font-medium">24GB GDDR6X</td>
                            <td class="py-4 px-6 text-center font-medium">24GB GDDR6</td>
                            <td class="py-4 px-6 text-center font-medium">12GB GDDR6X</td>
                        </tr>
                        <tr class="border-b border-gray-200">
                            <td class="py-4 px-6 text-gray-600">Velocidad memoria</td>
                            <td class="py-4 px-6 text-center font-medium">21 Gbps</td>
                            <td class="py-4 px-6 text-center font-medium">20 Gbps</td>
                            <td class="py-4 px-6 text-center font-medium">19 Gbps</td>
                        </tr>
                        <tr class="border-b border-gray-200">
                            <td class="py-4 px-6 text-gray-600">Ancho de banda</td>
                            <td class="py-4 px-6 text-center font-medium">1 TB/s</td>
                            <td class="py-4 px-6 text-center font-medium">960 GB/s</td>
                            <td class="py-4 px-6 text-center font-medium">912 GB/s</td>
                        </tr>
                        <tr class="border-b border-gray-200">
                            <td class="py-4 px-6 text-gray-600">Núcleos CUDA/Stream</td>
                            <td class="py-4 px-6 text-center font-medium">16,384</td>
                            <td class="py-4 px-6 text-center font-medium">6,144</td>
                            <td class="py-4 px-6 text-center font-medium">10,240</td>
                        </tr>
                        <tr class="border-b border-gray-200">
                            <td class="py-4 px-6 text-gray-600">Potencia (TDP)</td>
                            <td class="py-4 px-6 text-center font-medium">450W</td>
                            <td class="py-4 px-6 text-center font-medium">355W</td>
                            <td class="py-4 px-6 text-center font-medium">350W</td>
                        </tr>
                        <tr>
                            <td class="py-4 px-6 text-gray-600">Precio</td>
                            <td class="py-4 px-6 text-center font-bold text-accent">$1,899.99</td>
                            <td class="py-4 px-6 text-center font-bold text-accent">$999.99</td>
                            <td class="py-4 px-6 text-center font-bold text-accent">$799.99</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- Survey Section -->
    <section id="survey" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="max-w-3xl mx-auto text-center mb-12">
                <h2 class="text-3xl font-bold mb-4 text-dark">PARTICIPA EN NUESTRA ENCUESTA</h2>
                <p class="text-gray-600">Tu opinión nos ayuda a mejorar nuestros productos y servicios</p>
            </div>
            
            <div class="max-w-3xl mx-auto bg-white p-8 rounded-xl shadow-md">
                <form id="survey-form">
                    <div class="mb-8">
                        <h3 class="text-xl font-semibold mb-4 flex items-center">
                            <span class="bg-dark text-white w-8 h-8 rounded-full flex items-center justify-center mr-3">1</span>
                            Según tu experiencia, ¿qué tarjeta gráfica consideras la mejor?
                        </h3>
                        <div class="space-y-3">
                            <input type="radio" id="survey-1" name="best-gpu" value="RTX 4090" class="survey-input hidden">
                            <label for="survey-1" class="block p-4 border rounded-lg cursor-pointer transition-all hover:border-blue-400">
                                <div class="flex justify-between">
                                    <span>NVIDIA RTX 4090</span>
                                    <span class="text-gray-500 text-sm">Costo producción: $600</span>
                                </div>
                            </label>
                            
                            <input type="radio" id="survey-2" name="best-gpu" value="RX 7900 XTX" class="survey-input hidden">
                            <label for="survey-2" class="block p-4 border rounded-lg cursor-pointer transition-all hover:border-blue-400">
                                <div class="flex justify-between">
                                    <span>AMD RX 7900 XTX</span>
                                    <span class="text-gray-500 text-sm">Costo producción: $450</span>
                                </div>
                            </label>
                            
                            <input type="radio" id="survey-3" name="best-gpu" value="RTX 3080 Ti" class="survey-input hidden">
                            <label for="survey-3" class="block p-4 border rounded-lg cursor-pointer transition-all hover:border-blue-400">
                                <div class="flex justify-between">
                                    <span>NVIDIA RTX 3080 Ti</span>
                                    <span class="text-gray-500 text-sm">Costo producción: $350</span>
                                </div>
                            </label>
                        </div>
                    </div>
                    
                    <div class="mb-8">
                        <h3 class="text-xl font-semibold mb-4 flex items-center">
                            <span class="bg-dark text-white w-8 h-8 rounded-full flex items-center justify-center mr-3">2</span>
                            ¿Qué características valoras más en una tarjeta gráfica?
                        </h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div class="flex items-center bg-gray-50 p-4 rounded-lg">
                                <input type="checkbox" id="feature-1" class="rounded text-accent focus:ring-accent mr-3">
                                <label for="feature-1" class="cursor-pointer">Rendimiento en gaming</label>
                            </div>
                            <div class="flex items-center bg-gray-50 p-4 rounded-lg">
                                <input type="checkbox" id="feature-2" class="rounded text-accent focus:ring-accent mr-3">
                                <label for="feature-2" class="cursor-pointer">Compatibilidad con software 3D</label>
                            </div>
                            <div class="flex items-center bg-gray-50 p-4 rounded-lg">
                                <input type="checkbox" id="feature-3" class="rounded text-accent focus:ring-accent mr-3">
                                <label for="feature-3" class="cursor-pointer">Consumo energético</label>
                            </div>
                            <div class="flex items-center bg-gray-50 p-4 rounded-lg">
                                <input type="checkbox" id="feature-4" class="rounded text-accent focus:ring-accent mr-3">
                                <label for="feature-4" class="cursor-pointer">Relación precio-rendimiento</label>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mb-8">
                        <h3 class="text-xl font-semibold mb-4 flex items-center">
                            <span class="bg-dark text-white w-8 h-8 rounded-full flex items-center justify-center mr-3">3</span>
                            Comentarios adicionales sobre costos de producción y productos
                        </h3>
                        <textarea class="w-full px-4 py-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-accent focus:border-transparent bg-gray-50" 
                                  rows="4" placeholder="Escribe tus comentarios sobre costos, margen de ganancia o sugerencias..."></textarea>
                    </div>
                    
                    <button type="submit" class="w-full bg-dark text-white py-3 rounded-lg font-medium hover:bg-gray-800 transition-all transform hover:scale-[1.01] flex items-center justify-center">
                        Enviar Encuesta <i class="fas fa-paper-plane ml-2"></i>
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="py-16 bg-gradient-to-r from-dark to-gray-800 text-white">
        <div class="container mx-auto px-4">
            <div class="max-w-3xl mx-auto text-center mb-12">
                <h2 class="text-3xl font-bold mb-4">OPINIONES DE CLIENTES</h2>
                <p class="text-gray-300">Lo que dicen nuestros clientes sobre nuestros productos</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white/10 p-6 rounded-xl backdrop-blur-sm">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full overflow-hidden mr-4">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Usuario" class="w-full h-full object-cover">
                        </div>
                        <div>
                            <h4 class="font-bold">Carlos Mendoza</h4>
                            <div class="flex text-yellow-400 text-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-300">"La RTX 4090 superó todas mis expectativas. El rendimiento en 8K es increíble y el servicio postventa excelente."</p>
                </div>
                
                <div class="bg-white/10 p-6 rounded-xl backdrop-blur-sm">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full overflow-hidden mr-4">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Usuario" class="w-full h-full object-cover">
                        </div>
                        <div>
                            <h4 class="font-bold">Ana Fernández</h4>
                            <div class="flex text-yellow-400 text-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-300">"La RX 7900 XTX es perfecta para mi trabajo de diseño 3D. La relación calidad-precio es inmejorable y el envío llegó antes de lo esperado."</p>
                </div>
                
                <div class="bg-white/10 p-6 rounded-xl backdrop-blur-sm">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full overflow-hidden mr-4">
                            <img src="https://randomuser.me/api/portraits/men/68.jpg" alt="Usuario" class="w-full h-full object-cover">
                        </div>
                        <div>
                            <h4 class="font-bold">Luis García</h4>
                            <div class="flex text-yellow-400 text-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="far fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-300">"Compré la RTX 3080 Ti para mi setup de streaming y es simplemente increíble. El soporte técnico de Proyecto Zetino resolvió rápidamente todas mis dudas."</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="bg-gradient-to-r from-accent to-primary rounded-2xl p-8 md:p-12 text-white">
                <div class="flex flex-col md:flex-row items-center justify-between">
                    <div class="mb-6 md:mb-0">
                        <h2 class="text-2xl md:text-3xl font-bold mb-2">¿Listo para potenciar tu setup?</h2>
                        <p class="text-accent-100 max-w-lg">Consulta con nuestros expertos para encontrar la mejor tarjeta gráfica según tus necesidades y presupuesto.</p>
                    </div>
                    <button class="px-8 py-3 bg-white text-dark rounded-lg font-bold hover:bg-gray-100 transition-all shadow-lg transform hover:scale-105">
                        Contactar asesor <i class="fas fa-arrow-right ml-2"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact" class="bg-dark text-white pt-16 pb-8">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-8">
                <div>
                    <div class="flex items-center mb-4">
                        <i class="fas fa-microchip text-accent text-3xl mr-3"></i>
                        <h2 class="text-2xl font-bold">PROYECTO ZETINO</h2>
                    </div>
                    <p class="text-gray-400 mb-4">Especialistas en hardware de alto rendimiento y soluciones gráficas profesionales.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-accent transition-colors">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-accent transition-colors">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-accent transition-colors">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-accent transition-colors">
                            <i class="fab fa-youtube"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="text-lg font-bold mb-4">Productos</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Tarjetas NVIDIA</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Tarjetas AMD</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Refrigeración</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Accesorios</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Ofertas especiales</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-lg font-bold mb-4">Soporte</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Preguntas frecuentes</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Guías de instalación</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Garantías</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Política de devoluciones</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Soporte técnico</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-lg font-bold mb-4">Contacto</h3>
                    <ul class="space-y-3">
                        <li class="flex items-center">
                            <i class="fas fa-map-marker-alt text-accent mr-3"></i>
                            <span class="text-gray-400">ESCUINTLA CHIAPAS</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone text-accent mr-3"></i>
                            <a href="tel:9615689589" class="text-gray-400 hover:text-white transition-colors">961 568 9589</a>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope text-accent mr-3"></i>
                            <a href="mailto:cesarzetinozetino@gmail.com" class="text-gray-400 hover:text-white transition-colors">cesarzetinozetino@gmail.com</a>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-clock text-accent mr-3"></i>
                            <span class="text-gray-400">Lun-Vie: 9am - 7pm</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-400 text-sm mb-4 md:mb-0">© 2025 Proyecto Zetino. Muchas gracias profesor Ricardo Olivera.</p>
                    <div class="flex space-x-6">
                        <a href="#" class="text-gray-400 hover:text-white text-sm transition-colors">Términos de servicio</a>
                        <a href="#" class="text-gray-400 hover:text-white text-sm transition-colors">Política de privacidad</a>
                        <a href="#" class="text-gray-400 hover:text-white text-sm transition-colors">Aviso legal</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to top button -->
    <button id="back-to-top" class="fixed bottom-8 right-8 w-12 h-12 bg-dark text-white rounded-full flex items-center justify-center shadow-lg hover:bg-gray-800 transition-colors hidden">
        <i class="fas fa-arrow-up"></i>
    </button>

    <script>
        // Survey form submission with better feedback
        document.getElementById('survey-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Create feedback element
            const feedback = document.createElement('div');
            feedback.className = 'fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50';
            feedback.innerHTML = `
                <div class="bg-white rounded-xl p-8 max-w-md mx-4 text-center">
                    <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-check text-green-500 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">¡Gracias por tu participación!</h3>
                    <p class="text-gray-600 mb-4">Tu opinión es muy valiosa para nosotros. Hemos registrado tus respuestas.</p>
                    <button class="px-6 py-2 bg-dark text-white rounded-lg font-medium hover:bg-gray-800 transition-colors" onclick="this.parentElement.parentElement.remove()">
                        Cerrar
                    </button>
                </div>
            `;
            
            document.body.appendChild(feedback);
            this.reset();
        });
        
        // Back to top button
        const backToTopButton = document.getElementById('back-to-top');
        
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.remove('hidden');
            } else {
                backToTopButton.classList.add('hidden');
            }
        });
        
        backToTopButton.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Add to cart animation
        document.querySelectorAll('button').forEach(button => {
            if (button.textContent.includes('Comprar') || button.textContent.includes('Añadir')) {
                button.addEventListener('click', function() {
                    const cartIcon = this.querySelector('i') || document.createElement('i');
                    const iconClone = cartIcon.cloneNode(true);
                    
                    const animation = iconClone.animate([
                        { transform: 'scale(1)', opacity: 1 },
                        { transform: 'scale(1.5)', opacity: 0.8 },
                        { transform: 'scale(0.5) translate(100px, -100px)', opacity: 0 }
                    ], {
                        duration: 1000,
                        easing: 'cubic-bezier(0.4, 0, 0.2, 1)'
                    });
                    
                    iconClone.style.position = 'fixed';
                    iconClone.style.pointerEvents = 'none';
                    iconClone.style.fontSize = '20px';
                    iconClone.style.color = '#3b82f6';
                    iconClone.style.left = `${this.getBoundingClientRect().left + this.offsetWidth / 2 - 10}px`;
                    iconClone.style.top = `${this.getBoundingClientRect().top}px`;
                    iconClone.style.zIndex = '1000';
                    
                    document.body.appendChild(iconClone);
                    
                    animation.onfinish = () => {
                        iconClone.remove();
                    };
                    
                    // Button feedback
                    this.style.transform = 'scale(0.95)';
                    setTimeout(() => {
                        this.style.transform = 'scale(1)';
                    }, 100);
                });
            }
        });
    </script>
</body>
</html>
