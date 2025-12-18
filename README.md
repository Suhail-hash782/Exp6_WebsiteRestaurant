# Ex.06 Restaurant Website
## Date:18-12-2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zaitoon-Al-Sinan | Fine Cuisine</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Plus+Jakarta+Sans:wght@300;400;600&display=swap');

        :root {
            --primary: #c5a059;
            --dark: #0f172a;
        }


        html, body {
            overflow-x: hidden;
            width: 100%;
            margin: 0;
            padding: 0;
            font-size: 16px; 
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            scroll-behavior: smooth;
            background-color: #f8fafc;
        }

        h1, h2, h3, .font-serif {
            font-family: 'Playfair Display', serif;
        }

    
        .hero-bg {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('ZaitoonDine.png');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

    
        .contact-bg {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('Al Zaitoona sherif.jpg');
            background-size: cover;
            background-position: center;
            min-height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .nav-glass {
            background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(8px);
        }

        .card-hover:hover {
            transform: translateY(-8px);
            transition: all 0.3s ease;
        }

    
        .team-portrait {
            width: 160px;
            height: 160px;
            object-fit: cover;
            border-radius: 50%;
            margin: 0 auto 1.5rem;
            border: 3px solid #c5a059;
        }
    </style>
</head>
<body class="text-slate-800">


    <nav class="fixed w-full z-50 nav-glass text-white px-6 py-4">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <a href="#" class="text-xl font-serif font-bold tracking-[0.2em] text-[#c5a059]">Zaitoon-Al-Sinan</a>
            <div class="hidden md:flex space-x-8 uppercase text-[11px] tracking-widest font-semibold">
                <a href="#home" class="hover:text-[#c5a059] transition">Home</a>
                <a href="#about" class="hover:text-[#c5a059] transition">About</a>
                <a href="#menu" class="hover:text-[#c5a059] transition">Menu</a>
                <a href="#contact" class="hover:text-[#c5a059] transition">Contact</a>
                <a href="#team" class="hover:text-[#c5a059] transition">Team</a>
            </div>
            <button class="md:hidden text-2xl" onclick="toggleMenu()">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>


    <div id="mobile-menu" class="fixed inset-0 bg-slate-900 z-[60] flex flex-col items-center justify-center space-y-8 text-white hidden">
        <button class="absolute top-6 right-6 text-3xl" onclick="toggleMenu()">&times;</button>
        <a href="#home" onclick="toggleMenu()" class="text-2xl font-serif">Home</a>
        <a href="#about" onclick="toggleMenu()" class="text-2xl font-serif">About</a>
        <a href="#menu" onclick="toggleMenu()" class="text-2xl font-serif">Menu</a>
        <a href="#contact" onclick="toggleMenu()" class="text-2xl font-serif">Contact</a>
        <a href="#team" onclick="toggleMenu()" class="text-2xl font-serif">Team</a>
    </div>


    <section id="home" class="hero-bg text-center text-white px-4">
        <h1 class="text-5xl md:text-7xl mb-4 font-serif">Zaitoon-Al-Sinan</h1>
        <div class="w-20 h-0.5 bg-[#c5a059] mb-6"></div>
        <p class="text-lg md:text-xl font-light italic opacity-90">Fine MultiCuisine Restaurant & Unforgettable Moments</p>
    </section>


    <section id="about" class="py-24 px-6 bg-white">
        <div class="max-w-5xl mx-auto flex flex-col md:flex-row items-center gap-16">
            <div class="md:w-1/2">
        
                <img src="Al Zaitoona sherif.jpg" alt="About Image" class="rounded shadow-2xl">
            </div>
            <div class="md:w-1/2">
                <span class="text-[#c5a059] uppercase tracking-widest text-xs font-bold">The Experience</span>
                <h2 class="text-4xl my-6">About Our Kitchen</h2>
                <p class="text-slate-600 leading-relaxed mb-6">
                    Zaitoon-Al-Sinan is more than just a restaurant; it is a celebration of culinary heritage. Our kitchen focuses on the purity of ingredients, the art of presentation, and the warmth of hospitality.
                </p>
                <p class="text-slate-600 leading-relaxed">
                    Every recipe is crafted by our award-winning team to ensure that your visit is not just a meal, but a memory that lasts a lifetime.
                </p>
            </div>
        </div>
    </section>


    <section id="menu" class="py-24 bg-slate-50 px-6">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-serif">Our Authentic Signature Menu</h2>
                <div class="w-16 h-1 bg-[#c5a059] mx-auto mt-4"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
            
                <div class="bg-white p-4 rounded-xl shadow-sm card-hover">
                    <img src="Muttonmandi.jpeg" alt="Dish 1" class="h-56 w-full object-cover rounded-lg mb-4">
                    <h3 class="text-xl font-bold">Mutton Mandi</h3>
                    <p class="text-slate-500 text-sm mt-2">Unique smoky flavour basmati rice with juicy Mutton piece .</p>
                </div>
            
                <div class="bg-white p-4 rounded-xl shadow-sm card-hover">
                    <img src="Shawarma.jpeg" alt="Dish 2" class="h-56 w-full object-cover rounded-lg mb-4">
                    <h3 class="text-xl font-bold">Arabian Shawarma</h3>
                    <p class="text-slate-500 text-sm mt-2">Marinated meat stack on a vertical rotisserie.</p>
                </div>
            
                <div class="bg-white p-4 rounded-xl shadow-sm card-hover">
                    <img src="Masalashawaya.jpeg" alt="Dish 3" class="h-56 w-full object-cover rounded-lg mb-4">
                    <h3 class="text-xl font-bold">Masala Shawaya</h3>
                    <p class="text-slate-500 text-sm mt-2">Spicy grill chicken with the sprinkles of Kerala masala.</p>
                </div>
            </div>
        </div>
    </section>


    <section id="contact" class="contact-bg px-6 text-white text-center">
        <div class="max-w-2xl bg-slate-900/70 p-12 rounded-2xl backdrop-blur-md border border-white/10">
            <h2 class="text-4xl mb-8 font-serif">Contact & Reservations</h2>
            <div class="space-y-4 text-lg">
                <p><i class="fas fa-map-marker-alt text-[#c5a059] mr-3"></i> 786 Redhills Road,Chennai</p>
                <p><i class="fas fa-phone text-[#c5a059] mr-3"></i> +91 7826276270</p>
                <p><i class="fas fa-envelope text-[#c5a059] mr-3"></i> contact@ZaitoonDine.com</p>
            </div>
            <div class="mt-8 flex justify-center space-x-6 text-2xl">
                <a href="#" class="hover:text-[#c5a059]"><i class="fab fa-instagram"></i></a>
                <a href="#" class="hover:text-[#c5a059]"><i class="fab fa-facebook"></i></a>
            </div>
        </div>
    </section>


    <section id="team" class="py-24 px-6 bg-white">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-serif">Meet Our Team</h2>
                <p class="text-slate-500 mt-2">The excellence behind every service</p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-y-16 gap-x-8">
            
                <div class="text-center">
                    <img src="Suhail.jpg" alt="CEO" class="team-portrait">
                    <h3 class="text-lg font-bold uppercase tracking-wide">Adam</h3>
                    <p class="text-[#c5a059] font-serif">Chief Executive Officer</p>
                </div>
            
                <div class="text-center">
                    <img src="Messi.jpg" alt="Marketing" class="team-portrait">
                    <h3 class="text-lg font-bold uppercase tracking-wide">Lionel Messi</h3>
                    <p class="text-[#c5a059] font-serif">Marketing Manager</p>
                </div>
            
                <div class="text-center">
                    <img src="Damon.jpg" alt="Operations" class="team-portrait">
                    <h3 class="text-lg font-bold uppercase tracking-wide">Damon Salvatore</h3>
                    <p class="text-[#c5a059] font-serif">Operation Manager</p>
                </div>
            
                <div class="text-center">
                    <img src="Ronaldosheik.jpeg" alt="HR" class="team-portrait">
                    <h3 class="text-lg font-bold uppercase tracking-wide">Sheik Ronaldo</h3>
                    <p class="text-[#c5a059] font-serif">HR Manager</p>
                </div>
            
                <div class="text-center">
                    <img src="Sheikaamir.jpeg" alt="Chef" class="team-portrait">
                    <h3 class="text-lg font-bold uppercase tracking-wide">Khalid-Al-Ameiri</h3>
                    <p class="text-[#c5a059] font-serif">Executive Chef</p>
                </div>
            
                <div class="text-center">
                    <img src="IShowSpeed.jpg" alt="CS" class="team-portrait">
                    <h3 class="text-lg font-bold uppercase tracking-wide">Sheik IShowSpeed</h3>
                    <p class="text-[#c5a059] font-serif">Customer Service Manager</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-slate-900 py-10 text-slate-500 text-sm text-center">
        <p>&copy; 2025 Zaitoon-Al-Sinan. Created for Excellence.</p>
    </footer>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }
    </script>
</body>
</html>
```

## OUTPUT:
![alt text](<Screenshot 2025-12-18 221758.png>)
![alt text](<Screenshot 2025-12-18 221814.png>)
![alt text](<Screenshot 2025-12-18 221826.png>)
![alt text](<Screenshot 2025-12-18 221840.png>)
![alt text](<Screenshot 2025-12-18 221903.png>)
![alt text](<Screenshot 2025-12-18 230504.png>)


## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
