<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plantillas de Ingeniería Civil</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary-color);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.8)), url('https://via.placeholder.com/1200x600') no-repeat center center/cover;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #c0392b;
        }
        
        /* Products Section */
        .products {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 36px;
            color: var(--primary-color);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-image {
            height: 200px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            color: #777;
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-title {
            font-size: 20px;
            margin-bottom: 10px;
            color: var(--primary-color);
        }
        
        .product-description {
            margin-bottom: 15px;
            color: #666;
        }
        
        .product-price {
            font-size: 24px;
            font-weight: bold;
            color: var(--accent-color);
            margin-bottom: 15px;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 20px;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 10px;
        }
        
        .footer-section ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section ul li a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #bbb;
            font-size: 14px;
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            max-width: 500px;
            width: 90%;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .modal-title {
            font-size: 24px;
            color: var(--primary-color);
        }
        
        .close-modal {
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: #777;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        .form-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        
        .payment-methods {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .payment-method {
            flex: 1;
            text-align: center;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .payment-method.active {
            border-color: var(--secondary-color);
            background-color: rgba(52, 152, 219, 0.1);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">Ingeniería Civil Pro</div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#productos">Productos</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="container">
            <h1>Plantillas Profesionales de Ingeniería Civil</h1>
            <p>Optimiza tu trabajo con nuestras plantillas especializadas. Diseñadas por profesionales para profesionales.</p>
            <a href="#productos" class="btn">Ver Productos</a>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="productos">
        <div class="container">
            <h2 class="section-title">Nuestras Plantillas</h2>
            <div class="product-grid">
                <!-- Producto 1 -->
                <div class="product-card">
                    <div class="product-image">Imagen Plantilla 1</div>
                    <div class="product-info">
                        <h3 class="product-title">Plantilla para Cálculo Estructural</h3>
                        <p class="product-description">Completa plantilla Excel para cálculos estructurales avanzados con gráficos integrados.</p>
                        <div class="product-price">$29.99</div>
                        <button class="btn comprar-btn" data-product="Plantilla para Cálculo Estructural" data-price="29.99">Comprar Ahora</button>
                    </div>
                </div>
                
                <!-- Producto 2 -->
                <div class="product-card">
                    <div class="product-image">Imagen Plantilla 2</div>
                    <div class="product-info">
                        <h3 class="product-title">Plantilla para Presupuestos de Obra</h3>
                        <p class="product-description">Sistema completo para elaboración de presupuestos con base de datos de materiales.</p>
                        <div class="product-price">$24.99</div>
                        <button class="btn comprar-btn" data-product="Plantilla para Presupuestos de Obra" data-price="24.99">Comprar Ahora</button>
                    </div>
                </div>
                
                <!-- Producto 3 -->
                <div class="product-card">
                    <div class="product-image">Imagen Plantilla 3</div>
                    <div class="product-info">
                        <h3 class="product-title">Plantilla para Planos y Diseños</h3>
                        <p class="product-description">Colección de bloques y plantillas CAD para proyectos de ingeniería civil.</p>
                        <div class="product-price">$34.99</div>
                        <button class="btn comprar-btn" data-product="Plantilla para Planos y Diseños" data-price="34.99">Comprar Ahora</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contacto">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Contacto</h3>
                    <p>Email: info@ingenieriacivilpro.com</p>
                    <p>Teléfono: +1 234 567 890</p>
                </div>
                <div class="footer-section">
                    <h3>Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#productos">Productos</a></li>
                        <li><a href="#">Términos y Condiciones</a></li>
                        <li><a href="#">Política de Privacidad</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Síguenos</h3>
                    <ul>
                        <li><a href="#">Facebook</a></li>
                        <li><a href="#">Instagram</a></li>
                        <li><a href="#">LinkedIn</a></li>
                        <li><a href="#">YouTube</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Ingeniería Civil Pro. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- Modal de Pago -->
    <div class="modal" id="paymentModal">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title">Completar Compra</h3>
                <button class="close-modal">&times;</button>
            </div>
            <form id="paymentForm">
                <div class="form-group">
                    <label for="productName">Producto:</label>
                    <input type="text" id="productName" readonly>
                </div>
                <div class="form-group">
                    <label for="productPrice">Precio:</label>
                    <input type="text" id="productPrice" readonly>
                </div>
                <div class="form-group">
                    <label for="customerName">Nombre Completo:</label>
                    <input type="text" id="customerName" required>
                </div>
                <div class="form-group">
                    <label for="customerEmail">Email:</label>
                    <input type="email" id="customerEmail" required>
                </div>
                
                <h4>Método de Pago</h4>
                <div class="payment-methods">
                    <div class="payment-method active" data-method="paypal">
                        PayPal
                    </div>
                    <div class="payment-method" data-method="card">
                        Tarjeta de Crédito
                    </div>
                </div>
                
                <div id="paypalFields">
                    <div class="form-group">
                        <label for="paypalEmail">Email de PayPal:</label>
                        <input type="email" id="paypalEmail">
                    </div>
                </div>
                
                <div id="cardFields" style="display: none;">
                    <div class="form-group">
                        <label for="cardNumber">Número de Tarjeta:</label>
                        <input type="text" id="cardNumber" placeholder="1234 5678 9012 3456">
                    </div>
                    <div class="form-group">
                        <label for="cardExpiry">Fecha de Expiración:</label>
                        <input type="text" id="cardExpiry" placeholder="MM/AA">
                    </div>
                    <div class="form-group">
                        <label for="cardCVC">CVC:</label>
                        <input type="text" id="cardCVC" placeholder="123">
                    </div>
                </div>
                
                <button type="submit" class="btn" style="width: 100%;">Pagar y Descargar</button>
            </form>
        </div>
    </div>

    <script>
        // Elementos del DOM
        const comprarBtns = document.querySelectorAll('.comprar-btn');
        const paymentModal = document.getElementById('paymentModal');
        const closeModal = document.querySelector('.close-modal');
        const productNameInput = document.getElementById('productName');
        const productPriceInput = document.getElementById('productPrice');
        const paymentForm = document.getElementById('paymentForm');
        const paymentMethods = document.querySelectorAll('.payment-method');
        const paypalFields = document.getElementById('paypalFields');
        const cardFields = document.getElementById('cardFields');

        // Abrir modal al hacer clic en comprar
        comprarBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                const product = this.getAttribute('data-product');
                const price = this.getAttribute('data-price');
                
                productNameInput.value = product;
                productPriceInput.value = `$${price}`;
                
                paymentModal.style.display = 'flex';
            });
        });

        // Cerrar modal
        closeModal.addEventListener('click', function() {
            paymentModal.style.display = 'none';
        });

        // Cerrar modal al hacer clic fuera de él
        window.addEventListener('click', function(event) {
            if (event.target === paymentModal) {
                paymentModal.style.display = 'none';
            }
        });

        // Cambiar método de pago
        paymentMethods.forEach(method => {
            method.addEventListener('click', function() {
                // Remover clase active de todos
                paymentMethods.forEach(m => m.classList.remove('active'));
                
                // Agregar clase active al seleccionado
                this.classList.add('active');
                
                // Mostrar campos correspondientes
                const paymentType = this.getAttribute('data-method');
                
                if (paymentType === 'paypal') {
                    paypalFields.style.display = 'block';
                    cardFields.style.display = 'none';
                } else {
                    paypalFields.style.display = 'none';
                    cardFields.style.display = 'block';
                }
            });
        });

        // Procesar pago
        paymentForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Aquí normalmente integrarías con una pasarela de pago real
            // Por ahora simularemos el proceso
            
            const productName = productNameInput.value;
            const customerName = document.getElementById('customerName').value;
            const customerEmail = document.getElementById('customerEmail').value;
            
            // Simular procesamiento de pago
            alert(`¡Gracias por tu compra, ${customerName}!\n\nProducto: ${productName}\nSe ha enviado un enlace de descarga a: ${customerEmail}`);
            
            // Cerrar modal
            paymentModal.style.display = 'none';
            
            // Limpiar formulario
            paymentForm.reset();
        });
    </script>
</body>
</html>
