<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>ZiniaApps - Premium App Store</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #001f3f;
            color: #f5ba42;
            padding: 20px;
            text-align: center;
        }
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
        }
        h1 {
            color: #001f3f;
            text-align: center;
        }
        .app-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }
        .app-item {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin: 15px;
            padding: 20px;
            width: 250px;
            text-align: center;
            transition: transform 0.3s ease;
        }
        .app-item:hover {
            transform: scale(1.05);
        }
        .app-item img {
            width: 100px;
            height: 100px;
            object-fit: contain;
        }
        .app-item h2 {
            font-size: 1.5rem;
            color: #001f3f;
        }
        .app-item p {
            font-size: 1rem;
            color: #555;
        }
        .app-item button {
            background-color: #f5ba42;
            border: none;
            color: white;
            padding: 10px 20px;
            text-transform: uppercase;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        .app-item button:hover {
            background-color: #d79500;
        }
        .confirmation {
            display: none;
            margin-top: 10px;
        }
        .confirmation button {
            margin: 5px;
            padding: 10px;
            background-color: #001f3f;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .confirmation button:hover {
            background-color: #f5ba42;
            color: #001f3f;
        }
        footer {
            background-color: #001f3f;
            color: white;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>

<header>
    <h1>ZiniaApps - Premium Apps at Affordable Prices</h1>
</header>

<div class="container">
    <h1>Daftar Aplikasi Premium</h1>
    <div class="app-list">
        <div class="app-item">
            <img src="netflix.png" alt="Netflix">
            <h2>Netflix</h2>
            <p>Paket Premium untuk film dan serial TV.</p>
            <button onclick="showConfirmation(this)">Beli Sekarang</button>
            <div class="confirmation">
                <p>Apakah kamu yakin ingin membeli Netflix?</p>
                <button onclick="purchase('Netflix')">Yes</button>
                <button onclick="cancel()">No</button>
            </div>
        </div>
        <div class="app-item">
            <img src="canva.png" alt="Canva">
            <h2>Canva</h2>
            <p>Akun Pro untuk desain grafis tanpa batas.</p>
            <button onclick="showConfirmation(this)">Beli Sekarang</button>
            <div class="confirmation">
                <p>Apakah kamu yakin ingin membeli Canva?</p>
                <button onclick="purchase('Canva')">Yes</button>
                <button onclick="cancel()">No</button>
            </div>
        </div>
        <div class="app-item">
            <img src="alight_motion.png" alt="Alight Motion">
            <h2>Alight Motion</h2>
            <p>Pro Version untuk animasi dan editing video.</p>
            <button onclick="showConfirmation(this)">Beli Sekarang</button>
            <div class="confirmation">
                <p>Apakah kamu yakin ingin membeli Alight Motion?</p>
                <button onclick="purchase('Alight Motion')">Yes</button>
                <button onclick="cancel()">No</button>
            </div>
        </div>
        <div class="app-item">
            <img src="remini.png" alt="Remini">
            <h2>Remini</h2>
            <p>Full Features untuk meningkatkan kualitas foto.</p>
            <button onclick="showConfirmation(this)">Beli Sekarang</button>
            <div class="confirmation">
                <p>Apakah kamu yakin ingin membeli Remini?</p>
                <button onclick="purchase('Remini')">Yes</button>
                <button onclick="cancel()">No</button>
            </div>
        </div>
    </div>
</div>

<footer>
    <p>© 2024 ZiniaApps. All rights reserved.</p>
</footer>

<script>
    function showConfirmation(button) {
        // Hide all other confirmation boxes
        document.querySelectorAll('.confirmation').forEach(function(confirmBox) {
            confirmBox.style.display = 'none';
        });
        
        // Show the confirmation box associated with the clicked button
        const confirmationBox = button.nextElementSibling;
        confirmationBox.style.display = 'block';
    }

    function purchase(appName) {
        // Direct to WhatsApp with pre-filled message
        const phoneNumber = '628977384422'; // Replace with your WhatsApp number
        const message = `Saya mau beli ${appName}`;
        const whatsappLink = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
        
        // Redirect to WhatsApp
        window.location.href = whatsappLink;
    }

    function cancel() {
        // Hide all confirmation boxes
        document.querySelectorAll('.confirmation').forEach(function(confirmBox) {
            confirmBox.style.display = 'none';
        });
    }
</script>

</body>
</html>
