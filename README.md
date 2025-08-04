<!-- index.html --><!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Business Website</title>
  <link rel="stylesheet" href="style.css" />
  <script src="https://js.paypal.com/v1/paypal.js"></script>
</head>
<body>
  <header>
    <h1>Welcome to My Business</h1>
    <input type="text" id="search" placeholder="Search..." />
    <nav>
      <a href="mailto:example@email.com">Email</a>
      <a href="https://wa.me/919999999999" target="_blank">WhatsApp</a>
    </nav>
  </header>  <section id="notifications">
    <h2>Notifications</h2>
    <div id="notification-content">New updates will appear here.</div>
  </section>  <section id="gallery">
    <h2>Gallery</h2>
    <div class="gallery-grid">
      <img src="/content/image1.jpg" alt="Image 1" />
      <img src="/content/image2.jpg" alt="Image 2" />
    </div>
  </section>  <section id="subscription">
    <h2>Subscribe</h2>
    <p>Free for 1 month. Then ₹199/month or ₹599 for 6 months.</p>
    <div class="payment-buttons">
      <button onclick="alert('Redirecting to PhonePe...')">Pay with PhonePe</button>
      <button onclick="alert('Redirecting to Google Pay...')">Pay with Google Pay</button>
      <button onclick="alert('Redirecting to Paytm...')">Pay with Paytm</button>
      <button onclick="alert('Redirecting to PayPal...')">Pay with PayPal</button>
    </div>
  </section>  <footer>
    <p>&copy; 2025 My Business</p>
  </footer>  <script>
    document.getElementById('search').addEventListener('input', function (e) {
      alert('Search feature coming soon: ' + e.target.value);
    });
  </script></body>
</html>/* style.css */ body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f4f4f4; color: #333; } header { background: #222; color: white; padding: 1rem; display: flex; flex-direction: column; align-items: center; } header nav a { margin: 0 10px; color: #0f0; text-decoration: none; } #search { margin-top: 10px; padding: 0.5rem; width: 80%; max-width: 300px; } .gallery-grid { display: flex; gap: 10px; flex-wrap: wrap; padding: 1rem; } .gallery-grid img { width: 150px; height: auto; border-radius: 5px; } section { padding: 1rem; background: white; margin: 1rem; border-radius: 8px; } footer { background: #222; color: white; text-align: center; padding: 1rem; position: fixed; width: 100%; bottom: 0; } .payment-buttons button { margin: 5px; padding: 0.5rem 1rem; background-color: #28a745; color: white; border: none; border-radius: 5px; cursor: pointer; } .payment-buttons button:hover { background-color: #218838; }

admin/config.yml

backend: name: git-gateway branch: main

media_folder: "content" public_folder: "/content"

collections:

name: "gallery" label: "Gallery" folder: "content/gallery" create: true fields:

{ label: "Title", name: "title", widget: "string" }

{ label: "Image", name: "image", widget: "image" }


name: "notifications" label: "Notifications" files:

label: "Notification Message" name: "notification" file: "content/notification.md" fields:

{ label: "Message", name: "body", widget: "markdown" }




content/notification.md


---

title: "Latest Update"

Stay tuned for new product launches and discounts!

