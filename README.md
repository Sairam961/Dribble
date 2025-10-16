# Project Responsive Web Design using Bootstrap
## Date: 16-10-2025

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble Clone - Showcase & Discover Creative Work</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <!-- Custom CSS -->
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background-color: #f8f9fa;
        }
        
        .navbar {
            background-color: #fff;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            padding: 1rem 0;
        }
        
        .navbar-brand {
            font-weight: 800;
            font-size: 1.5rem;
            color: #ea4c89 !important;
        }
        
        .nav-link {
            color: #6c757d !important;
            font-weight: 500;
            margin: 0 0.5rem;
        }
        
        .nav-link:hover {
            color: #000 !important;
        }
        
        .btn-signup {
            background-color: #ea4c89;
            color: white;
            border: none;
            padding: 0.5rem 1.5rem;
            border-radius: 20px;
            font-weight: 600;
        }
        
        .btn-signup:hover {
            background-color: #d63a7a;
        }
        
        .hero-section {
            background-color: #fef4f8;
            padding: 4rem 0;
            text-align: center;
        }
        
        .hero-section h1 {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 1rem;
        }
        
        .hero-section p {
            font-size: 1.2rem;
            color: #6c757d;
            margin-bottom: 2rem;
        }
        
        .btn-learn {
            background-color: transparent;
            border: 2px solid #6c757d;
            color: #6c757d;
            padding: 0.5rem 1.5rem;
            border-radius: 20px;
            font-weight: 600;
            margin: 0 0.5rem;
        }
        
        .filter-section {
            background-color: white;
            padding: 1.5rem 0;
            border-bottom: 1px solid #dee2e6;
        }
        
        .filter-btn {
            background-color: transparent;
            border: none;
            color: #6c757d;
            font-weight: 600;
            padding: 0.5rem 1rem;
            margin: 0 0.5rem;
        }
        
        .filter-btn.active {
            color: #000;
            border-bottom: 2px solid #ea4c89;
        }
        
        .gallery-section {
            padding: 3rem 0;
        }
        
        .shot-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            margin-bottom: 2rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            transition: transform 0.2s;
        }
        
        .shot-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 16px rgba(0,0,0,0.15);
        }
        
        .shot-image {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1rem;
            font-weight: 600;
        }
        
        .shot-info {
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .author-info {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: #dee2e6;
            margin-right: 0.5rem;
        }
        
        .author-name {
            font-weight: 600;
            color: #000;
            text-decoration: none;
            font-size: 0.9rem;
        }
        
        .shot-stats {
            display: flex;
            gap: 1rem;
            color: #6c757d;
            font-size: 0.9rem;
        }
        
        .footer {
            background-color: #1a1a1a;
            color: white;
            padding: 3rem 0 1rem 0;
            margin-top: 4rem;
        }
        
        .footer h5 {
            font-weight: 700;
            margin-bottom: 1rem;
        }
        
        .footer ul {
            list-style: none;
            padding: 0;
        }
        
        .footer ul li {
            margin-bottom: 0.5rem;
        }
        
        .footer a {
            color: #adb5bd;
            text-decoration: none;
        }
        
        .footer a:hover {
            color: white;
        }
        
        .footer-bottom {
            border-top: 1px solid #343a40;
            margin-top: 2rem;
            padding-top: 1rem;
            color: #6c757d;
        }
    </style>
     </head>
     <body>

    <!-- Navigation Bar -->
    <nav class="navbar navbar-expand-lg sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">Dribbble</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item"><a class="nav-link" href="#">Shots</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Designers</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Teams</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Community</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Jobs</a></li>
                </ul>
                <form class="d-flex me-3">
                    <input class="form-control" type="search" placeholder="Search" style="border-radius: 20px;">
                </form>
                <div>
                    <a href="#" class="nav-link d-inline">Sign in</a>
                    <button class="btn btn-signup">Sign up</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="container">
            <h1>What are you working on?</h1>
            <p>Dribbble is show and tell for designers.</p>
            <button class="btn btn-learn">Learn more</button>
            <button class="btn btn-signup">Sign up</button>
        </div>
    </section>

    <!-- Filter Section -->
    <section class="filter-section">
        <div class="container text-center">
            <button class="filter-btn active">Popular</button>
            <button class="filter-btn">Shots</button>
            <button class="filter-btn">Now</button>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery-section">
        <div class="container">
            <div class="row">
                <!-- Shot Card 1 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image">Design Shot 1</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Famous</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 4k</span>
                                <span>❤️ 290</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 2 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);">Design Shot 2</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Balkan Brothers</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 2.4k</span>
                                <span>❤️ 236</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 3 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);">Design Shot 3</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Jan Losert</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 3.9k</span>
                                <span>❤️ 264</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 4 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #30cfd0 0%, #330867 100%);">Design Shot 4</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Mattias Johansson</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 2.6k</span>
                                <span>❤️ 186</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 5 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);">Design Shot 5</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Ruslan Siiz</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 2.3k</span>
                                <span>❤️ 179</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 6 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);">Design Shot 6</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Paperpillar</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 2k</span>
                                <span>❤️ 160</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 7 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);">Design Shot 7</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">Alfrey Davilla</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 1.8k</span>
                                <span>❤️ 158</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 8 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);">Design Shot 8</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">A Studio-JQ</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 2.1k</span>
                                <span>❤️ 158</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 9 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%);">Design Shot 9</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">RomainTrystram</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 1.8k</span>
                                <span>❤️ 148</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 10 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #fddb92 0%, #d1fdff 100%);">Design Shot 10</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">inFullMobile</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 2.1k</span>
                                <span>❤️ 134</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 11 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #e0c3fc 0%, #8ec5fc 100%);">Design Shot 11</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">FourPlus Studio</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 1.3k</span>
                                <span>❤️ 127</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Shot Card 12 -->
                <div class="col-lg-3 col-md-4 col-sm-6">
                    <div class="shot-card">
                        <div class="shot-image" style="background: linear-gradient(135deg, #fbc2eb 0%, #a6c1ee 100%);">Design Shot 12</div>
                        <div class="shot-info">
                            <div class="author-info">
                                <div class="author-avatar"></div>
                                <a href="#" class="author-name">MUTI</a>
                            </div>
                            <div class="shot-stats">
                                <span>👁 728</span>
                                <span>❤️ 118</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="col-md-3">
                    <h5>Dribbble</h5>
                    <ul>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Support</a></li>
                        <li><a href="#">Media kit</a></li>
                    </ul>
                </div>
                <div class="col-md-3">
                    <h5>Browse</h5>
                    <ul>
                        <li><a href="#">Popular</a></li>
                        <li><a href="#">Recent</a></li>
                        <li><a href="#">Shots</a></li>
                        <li><a href="#">Designers</a></li>
                    </ul>
                </div>
                <div class="col-md-3">
                    <h5>Community</h5>
                    <ul>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Forums</a></li>
                        <li><a href="#">Meetups</a></li>
                        <li><a href="#">Conferences</a></li>
                    </ul>
                </div>
                <div class="col-md-3">
                    <h5>Company</h5>
                    <ul>
                        <li><a href="#">Privacy</a></li>
                        <li><a href="#">Terms</a></li>
                        <li><a href="#">Cookie Policy</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom text-center">
                <p>&copy; 2025 Dribbble Clone. Created by Your Name</p>
            </div>
        </div>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    </body>
    </html>


## OUTPUT:
<img width="1261" height="664" alt="image" src="https://github.com/user-attachments/assets/11df1f74-0456-49b9-8177-723d17561daf" />


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
