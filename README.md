import qrcode

# HTML code to be encoded into a QR code
html_code = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guru's Collection</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0e68c; /* light yellow background */
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #800080; /* purple */
            color: #fff;
            padding: 1rem;
            text-align: center;
        }
        nav {
            background-color: #ff69b4; /* pink */
            padding: 1rem;
            text-align: center;
        }
        nav a {
            color: #fff;
            margin: 0 1rem;
            text-decoration: none;
        }
        nav a:hover {
            text-decoration: underline.
        }
        main {
            padding: 2rem;
        }
        footer {
            background-color: #800080; /* purple */
            color: #fff;
            text-align: center;
            padding: 1rem;
            position: fixed;
            width: 100%;
            bottom: 0.
        }
        .product {
            border: 2px solid #ff69b4; /* pink */
            padding: 1rem;
            margin: 1rem 0;
            background-color: #fff.
        }
        .product img {
            max-width: 100%.
        }
        .product h2 {
            color: #800080; /* purple */
        }
        .product p {
            color: #ff69b4; /* pink */
        }
    </style>
</head>
<body>
    <header>
        <h1>Guru's Collection</h1>
        <p>Your one-stop shop for the latest fashion trends!</p>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#shop">Shop</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>
    <main>
        <section id="home">
            <h2>Welcome to Guru's Collection</h2>
            <p>Discover our latest arrivals and exclusive collections. Shop now to stay ahead of the trends!</p>
        </section>
        <section id="shop">
            <h2>Shop Our Collection</h2>
            <div class="product">
                <h3>Product 1</h3>
                <img src="https://via.placeholder.com/150" alt="Product 1">
                <p>Description of Product 1.</p>
                <p>Price: $50</p>
            </div>
            <div class="product">
                <h3>Product 2</h3>
                <img src="https://via.placeholder.com/150" alt="Product 2">
                <p>Description of Product 2.</p>
                <p>Price: $75</p>
            </div>
        </section>
        <section id="about">
            <h2>About Us</h2>
            <p>Guru's Collection is dedicated to bringing you the finest clothing options with a touch of elegance and style. Founded in 2023, we strive to provide quality and fashion-forward pieces for every occasion.</p>
        </section>
        <section id="contact">
            <h2>Contact Us</h2>
            <p>Email: contact@guruscollection.com</p>
            <p>Phone: (123) 456-7890</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Guru's Collection. All rights reserved.</p>
    </footer>
</body>
</html>
"""

# Generate QR code
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
)
qr.add_data(html_code)
qr.make(fit=True)

# Create an image
img = qr.make_image(fill='black', back_color='white')
img_path = "/mnt/data/gurus_collection_qr.png"
img.save(img_path)

img_path
