# lab6_css_framework

**Nama : Muhammad Iqbal**

**Nim : 312410212**

**kelas : TI.24.A2**

# Langkah 1: Struktur Dasar HTML.
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Modern dengan Bootstrap</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.0/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #4361ee;
            --secondary-color: #3f37c9;
            --accent-color: #4cc9f0;
            --success-color: #4ade80;
            --warning-color: #f59e0b;
        }
        
        .hero-section {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            color: white;
        }
        
        .feature-card {
            transition: transform 0.3s ease;
            border: none;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .navbar-brand {
            font-weight: bold;
            color: var(--primary-color) !important;
        }
        
        .btn-primary {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
        }
        
        .btn-primary:hover {
            background-color: var(--secondary-color);
            border-color: var(--secondary-color);
        }
        
        .widget-header {
            background: linear-gradient(135deg, var(--warning-color), #f97316);
            color: white;
        }
        
        footer {
            background: linear-gradient(135deg, #1e293b, #0f172a);
        }
    </style>
</head>
<body>
    <h1 class="text-center mt-5">Hello World!</h1>
</body>
</html>
```
# Langkah 2: Navbar
```html
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-white shadow-sm sticky-top">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">
                <i class="bi bi-layers-fill me-2"></i>WebFramework
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <a class="nav-link active fw-semibold" href="#" style="color: var(--primary-color);">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-semibold" href="#">Artikel</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-semibold" href="#">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-semibold" href="#">Kontak</a>
                    </li>
                </ul>
                <form class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="Search...">
                    <button class="btn btn-outline-primary" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>

    <h1 class="text-center mt-5">Hello World!</h1>
</body>
```

# Langkah 3: Jumbotron / Hero Section
```html
    <!-- Hero Section -->
    <section class="hero-section py-5">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-8">
                    <h1 class="display-4 fw-bold mb-4">Hello World! 👋</h1>
                    <p class="lead mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, laculis innisi volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
                    <div class="d-flex gap-3">
                        <a class="btn btn-light btn-lg fw-semibold" href="#" role="button">
                            <i class="bi bi-arrow-right-circle me-2"></i>Learn more
                        </a>
                        <a class="btn btn-outline-light btn-lg fw-semibold" href="#" role="button">
                            <i class="bi bi-play-circle me-2"></i>Watch Demo
                        </a>
                    </div>
                </div>
                <div class="col-lg-4 text-center">
                    <div class="bg-white rounded-3 p-4 shadow-lg mt-4 mt-lg-0">
                        <i class="bi bi-code-slash display-1 text-primary"></i>
                        <h4 class="mt-3">Web Framework</h4>
                        <p class="text-muted">Bootstrap 5.3</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
```

# Langkah 4: Grid untuk Konten dan Sidebar
```html
    <!-- Features Section -->
    <div class="container py-5">
        <div class="row g-4">
            <!-- Feature 1 -->
            <div class="col-md-4">
                <div class="feature-card card h-100 border-0 rounded-3">
                    <div class="card-body p-4">
                        <div class="feature-icon bg-primary bg-gradient rounded-circle p-3 mb-3 d-inline-block">
                            <i class="bi bi-lightning-fill text-white fs-4"></i>
                        </div>
                        <h5 class="card-title fw-bold">Fast Performance</h5>
                        <p class="card-text text-muted">Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-outline-primary btn-sm">View detail <i class="bi bi-arrow-right ms-1"></i></a>
                    </div>
                </div>
            </div>
            
            <!-- Feature 2 -->
            <div class="col-md-4">
                <div class="feature-card card h-100 border-0 rounded-3">
                    <div class="card-body p-4">
                        <div class="feature-icon bg-success bg-gradient rounded-circle p-3 mb-3 d-inline-block">
                            <i class="bi bi-shield-check text-white fs-4"></i>
                        </div>
                        <h5 class="card-title fw-bold">Secure & Safe</h5>
                        <p class="card-text text-muted">Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-outline-success btn-sm">View detail <i class="bi bi-arrow-right ms-1"></i></a>
                    </div>
                </div>
            </div>
            
            <!-- Feature 3 -->
            <div class="col-md-4">
                <div class="feature-card card h-100 border-0 rounded-3">
                    <div class="card-body p-4">
                        <div class="feature-icon bg-warning bg-gradient rounded-circle p-3 mb-3 d-inline-block">
                            <i class="bi bi-phone text-white fs-4"></i>
                        </div>
                        <h5 class="card-title fw-bold">Responsive Design</h5>
                        <p class="card-text text-muted">Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-outline-warning btn-sm">View detail <i class="bi bi-arrow-right ms-1"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
```
# Langkah 5: Main Content + Sidebar
```html
    <!-- Main Content -->
    <div class="container py-5">
        <div class="row">
            <!-- Konten Utama -->
            <div class="col-lg-8">
                <article class="mb-5">
                    <h2 class="fw-bold mb-3" style="color: var(--primary-color);">First Featurette Heading</h2>
                    <div class="row align-items-center">
                        <div class="col-md-8">
                            <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, laculis in nisi volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
                        </div>
                        <div class="col-md-4 text-center">
                            <div class="bg-gradient-primary rounded-3 p-4 text-white">
                                <i class="bi bi-star-fill display-4"></i>
                            </div>
                        </div>
                    </div>
                </article>

                <article class="mb-5">
                    <h2 class="fw-bold mb-3" style="color: var(--primary-color);">Second Featurette Heading</h2>
                    <div class="row align-items-center">
                        <div class="col-md-4 text-center">
                            <div class="bg-gradient-success rounded-3 p-4 text-white">
                                <i class="bi bi-award display-4"></i>
                            </div>
                        </div>
                        <div class="col-md-8">
                            <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, laculis in nisi volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
                        </div>
                    </div>
                </article>
            </div>

            <!-- Sidebar -->
            <div class="col-lg-4">
                <div class="card mb-4 border-0 shadow-sm">
                    <div class="card-header widget-header py-3">
                        <strong><i class="bi bi-link-45deg me-2"></i>Widget Header</strong>
                    </div>
                    <ul class="list-group list-group-flush">
                        <li class="list-group-item d-flex align-items-center">
                            <i class="bi bi-arrow-right-circle text-primary me-2"></i>
                            Widget Link 1
                        </li>
                        <li class="list-group-item d-flex align-items-center">
                            <i class="bi bi-arrow-right-circle text-success me-2"></i>
                            Widget Link 2
                        </li>
                        <li class="list-group-item d-flex align-items-center">
                            <i class="bi bi-arrow-right-circle text-warning me-2"></i>
                            Widget Link 3
                        </li>
                        <li class="list-group-item d-flex align-items-center">
                            <i class="bi bi-arrow-right-circle text-info me-2"></i>
                            Widget Link 4
                        </li>
                    </ul>
                </div>
                
                <div class="card border-0 shadow-sm">
                    <div class="card-body">
                        <h5 class="card-title fw-bold">
                            <i class="bi bi-chat-quote text-primary me-2"></i>Widget Text
                        </h5>
                        <p class="card-text text-muted">Vestibulum lorem elit, laculis in nisi volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis.</p>
                        <div class="bg-light rounded-3 p-3 mt-3">
                            <small class="text-muted">
                                <i class="bi bi-info-circle me-1"></i>
                                Integer pharetra est nunc, nec pretium nunc pretium ac.
                            </small>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
```

# Langkah 6 : footer modern
```html
    <!-- Footer -->
    <footer class="text-white py-4 mt-5">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-md-6">
                    <h5 class="fw-bold mb-3">
                        <i class="bi bi-layers-fill me-2"></i>Web Framework
                    </h5>
                    <p class="text-light mb-0">Belajar membuat layout web modern dengan Bootstrap 5</p>
                </div>
                <div class="col-md-6 text-md-end">
                    <div class="social-links mb-3">
                        <a href="#" class="text-white me-3"><i class="bi bi-facebook fs-5"></i></a>
                        <a href="#" class="text-white me-3"><i class="bi bi-twitter fs-5"></i></a>
                        <a href="#" class="text-white me-3"><i class="bi bi-instagram fs-5"></i></a>
                        <a href="#" class="text-white"><i class="bi bi-github fs-5"></i></a>
                    </div>
                    <p class="text-light mb-0">&copy; 2021 - Universitas Pelita Bangsa. All rights reserved.</p>
                </div>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

