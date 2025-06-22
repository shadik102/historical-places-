<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Historical Places in India</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 20px 0;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 20px;
        }

        .card {
            background-color: white;
            margin: 15px;
            padding: 15px;
            width: 250px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            text-align: center;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.2s ease;
        }

        .card:hover {
            transform: scale(1.05);
        }

        .card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 6px;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 999;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.7);
        }

        .modal-content {
            background-color: white;
            margin: 10% auto;
            padding: 20px;
            width: 70%;
            border-radius: 10px;
            max-width: 500px;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover {
            color: #000;
        }
    </style>
</head>
<body>

    <header>
        <h1>Historical Places in India</h1>
    </header>

    <div class="container">
        <div class="card" onclick="showInfo('Taj Mahal', 'Located in Agra, built by Shah Jahan in memory of Mumtaz Mahal.')">
            <img src="C:\Users\Aiesha\Downloads\tajmahal.jpg" alt="Taj Mahal">
            <h2>Taj Mahal</h2>
        </div>

        <div class="card" onclick="showInfo('mysure palace', 'Located in karnataka, built by wadiyar dynasty in 14th century.')">
            <img src="C:\Users\Aiesha\Downloads\mysure palace.jpeg" alt="mysure palace">
            <h2>mysure palace</h2>
        </div>

        <div class="card" onclick="showInfo('indiagate', 'Located in Delhi, built by Sir Edwin Lutyens.')">
            <img src="C:\Users\Aiesha\Downloads\india gate.jpeg" alt="india gate">
            <h2>india gate</h2>
        </div>

        <div class="card" onclick="showInfo('charminar', 'Located in hyderabad,built by Sultan muhammad Quli Qutub sha.')">
            <img src="C:\Users\Aiesha\Downloads\charminar.jpg" alt="charminar">
            <h2>charminar</h2>
        </div>
    </div>

    <!-- Modal -->
    <div id="modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2 id="place-title"></h2>
            <p id="place-description"></p>
        </div>
    </div>

    <script>
        function showInfo(title, description) {
            document.getElementById("place-title").innerText = title;
            document.getElementById("place-description").innerText = description;
            document.getElementById("modal").style.display = "block";
        }

        function closeModal() {
            document.getElementById("modal").style.display = "none";
        }
    </script>

</body>
</html>
