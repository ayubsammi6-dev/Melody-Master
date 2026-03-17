# Melody-Master
A Powerfull Service In The Bangladesh
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Melody Master Official</title>

<style>
body {
    font-family: Arial;
    margin: 0;
    background: #111;
    color: white;
}

/* HEADER */
.header {
    padding: 15px;
    background: #000;
    font-size: 22px;
    font-weight: bold;
}

/* MENU */
.menu {
    display: flex;
    background: #222;
}

.menu button {
    flex: 1;
    padding: 12px;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
}

.menu button:hover {
    background: #444;
}

/* CONTENT */
.content {
    padding: 20px;
}

input, select {
    padding: 10px;
    margin: 10px 0;
    width: 100%;
}

button.order {
    background: green;
    padding: 12px;
    color: white;
    border: none;
    cursor: pointer;
}
</style>

</head>

<body>

<div class="header">
    Melody Master Official
</div>

<div class="menu">
    <button onclick="openTab('services')">Services</button>
    <button onclick="openTab('custom')">Custom Service</button>
    <button onclick="openTab('help')">Help</button>
</div>

<!-- SERVICES -->
<div id="services" class="content">
    <h2>Services</h2>

    <ul>
        <li>Thumbnail Editing</li>
        <li>Video Editing</li>
        <li>Poster Editing</li>
        <li>Live Editing</li>
        <li>Photo Editing</li>
    </ul>

    <h3>Place Order</h3>

    <select id="serviceSelect">
        <option>Thumbnail Editing</option>
        <option>Video Editing</option>
        <option>Poster Editing</option>
        <option>Live Editing</option>
        <option>Photo Editing</option>
    </select>

    <input type="text" id="phone" placeholder="Enter your number">

    <button class="order" onclick="sendOrder()">Place Order</button>
</div>

<!-- CUSTOM -->
<div id="custom" class="content" style="display:none;">
    <h2>Custom Service</h2>
    <p>Need something custom? Contact me!</p>

    <ul>
        <li>Special Thumbnail</li>
        <li>Advanced Video Editing</li>
        <li>Custom Poster Design</li>
    </ul>

    <p>Email: <b>ayubsammi6@gmail.com</b></p>
</div>

<!-- HELP -->
<div id="help" class="content" style="display:none;">
    <h2>Help</h2>
    <p>For any help, contact:</p>
    <p><b>Email: ayubsammi6@gmail.com</b></p>
</div>

<script>
function openTab(tab) {
    document.getElementById("services").style.display = "none";
    document.getElementById("custom").style.display = "none";
    document.getElementById("help").style.display = "none";

    document.getElementById(tab).style.display = "block";
}

function sendOrder() {
    let service = document.getElementById("serviceSelect").value;
    let phone = document.getElementById("phone").value;

    let subject = "New Order";
    let body = "Service: " + service + "%0D%0APhone: " + phone;

    window.location.href =
    "mailto:ayubsammi6@gmail.com?subject=" + subject + "&body=" + body;
}
</script>

</body>
</html>
