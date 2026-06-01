# Ex02 Commercial Website
## Date:

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
# index.html:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NovaCart</title>
    <link rel="stylesheet" href="style.css">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>

    <!-- NAVBAR -->
    <header>
        <nav class="navbar">
            <div class="logo">NovaCart</div>

            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">Products</a></li>
                <li><a href="#">Deals</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HERO SECTION -->
    <section class="hero">

        <div class="hero-text">
            <h1>Discover Tech That<br>Defines Your Lifestyle</h1>

            <p>
                Explore premium gadgets, accessories, and smart devices 
                curated for modern living.
            </p>

            <div class="hero-buttons">
                <button class="primary-btn">Shop Now</button>
                <button class="secondary-btn">View Deals</button>
            </div>
        </div>

        <div class="hero-image">
            <img src="images/apple.jpg" alt="Premium Gadget Showcase">
        </div>

    </section>

    <!-- PRODUCTS -->
    <section class="products">
        <h2>Trending Products</h2>

        <div class="product-container">

            <div class="product-card">
                <img src="images/headphones.jpeg" alt="Wireless Headphones">
                <h3>Wireless Headphones</h3>
                <p>₹2,999</p>
                <button>Buy Now</button>
            </div>

            <div class="product-card">
                <img src="images/smartwatch.jpg" alt="Smart Watch">
                <h3>Smart Watch</h3>
                <p>₹4,499</p>
                <button>Buy Now</button>
            </div>

            <div class="product-card">
                <img src="images/mouse.jpg" alt="Gaming Mouse">
                <h3>Gaming Mouse</h3>
                <p>₹1,499</p>
                <button>Buy Now</button>
            </div>

            <div class="product-card">
                <img src="images/speaker.jpg" alt="Bluetooth Speaker">
                <h3>Bluetooth Speaker</h3>
                <p>₹3,299</p>
                <button>Buy Now</button>
            </div>

        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>© 2026 NovaCart. Crafted with Flexbox.</p>
    </footer>

</body>
</html>
# style.css

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    background:#0f172a;
    color:white;
}

/* NAVBAR */
.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:20px 8%;
    background:rgba(15,23,42,0.95);
    position:sticky;
    top:0;
    z-index:100;
}

.logo{
    font-size:1.8rem;
    font-weight:700;
    color:#38bdf8;
}

.nav-links{
    display:flex;
    gap:30px;
    list-style:none;
}

.nav-links a{
    color:white;
    text-decoration:none;
    transition:0.3s;
}

.nav-links a:hover{
    color:#38bdf8;
}

/* HERO */
.hero{
    min-height:90vh;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:60px 8%;
    background:linear-gradient(135deg,#0f172a,#1e293b);
    gap:50px;
    flex-wrap:wrap;
}

.hero-text{
    flex:1;
    min-width:300px;
}

.hero-text h1{
    font-size:4rem;
    line-height:1.2;
    margin-bottom:20px;
}

.hero-text p{
    font-size:1.15rem;
    color:#cbd5e1;
    margin-bottom:30px;
    max-width:500px;
}

.hero-buttons{
    display:flex;
    gap:15px;
    flex-wrap:wrap;
}

.primary-btn,
.secondary-btn{
    padding:14px 30px;
    border:none;
    border-radius:30px;
    font-weight:600;
    cursor:pointer;
    transition:0.3s;
}

.primary-btn{
    background:#38bdf8;
    color:#0f172a;
}

.secondary-btn{
    background:transparent;
    border:2px solid #38bdf8;
    color:#38bdf8;
}

.primary-btn:hover,
.secondary-btn:hover{
    transform:translateY(-3px);
}

.hero-image{
    flex:1;
    display:flex;
    justify-content:center;
    min-width:300px;
}

.hero-image img{
    width:100%;
    max-width:500px;
    filter:drop-shadow(0 20px 30px rgba(56,189,248,0.25));
}

/* PRODUCTS */
.products{
    padding:80px 8%;
    text-align:center;
}

.products h2{
    font-size:2.5rem;
    margin-bottom:40px;
}

.product-container{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:30px;
}

.product-card{
    background:#1e293b;
    width:260px;
    padding:20px;
    border-radius:20px;
    transition:0.3s;
    box-shadow:0 8px 20px rgba(0,0,0,0.3);
}

.product-card:hover{
    transform:translateY(-10px);
}

.product-card img{
    width:100%;
    height:220px;
    object-fit:cover;
    border-radius:15px;
    margin-bottom:15px;
}

.product-card h3{
    margin-bottom:10px;
}

.product-card p{
    color:#38bdf8;
    margin-bottom:15px;
    font-weight:600;
}

.product-card button{
    padding:10px 20px;
    border:none;
    border-radius:25px;
    background:#38bdf8;
    color:#0f172a;
    cursor:pointer;
    font-weight:600;
}

/* FOOTER */
footer{
    background:#020617;
    text-align:center;
    padding:20px;
    color:#94a3b8;
}

/* RESPONSIVE */
@media(max-width:768px){

    .navbar{
        flex-direction:column;
        gap:15px;
    }

    .nav-links{
        flex-direction:column;
        align-items:center;
    }

    .hero{
        flex-direction:column;
        text-align:center;
        padding-top:40px;
    }

    .hero-text h1{
        font-size:2.5rem;
    }

    .hero-text p{
        margin:auto auto 30px;
    }

    .hero-buttons{
        justify-content:center;
    }
}


## OUTPUT


<img width="1900" height="923" alt="Screenshot 2026-05-01 134321" src="https://github.com/user-attachments/assets/15bb29ca-8e76-42c9-96e4-8f14f9028336" />

<img width="1900" height="929" alt="Screenshot 2026-05-01 134340" src="https://github.com/user-attachments/assets/a9ee8bbf-c3d3-4e17-9966-90323fceba6c" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
