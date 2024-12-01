<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>Watch Ads & Earn Money</title>
    <style>
        /* General reset */
        * {
            margin: 0;
            padding: 4;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f4f6f7;
            color: #34495e;
            padding: 20px;
            -webkit-user-select: none; /* Safari */
            -moz-user-select: none;    /* Firefox */
            -ms-user-select: none;     /* IE/Edge */
            user-select: none;         /* Standard syntax */
        }

        button {
            -webkit-user-select: text;
            -moz-user-select: text;
            -ms-user-select: text;
            user-select: text;
        }

        /* Button Styling */
        .category-button {
            padding: 14px 28px;
            background: linear-gradient(145deg, #3498db, #2980b9);
            color: white;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            white-space: nowrap; /* Prevent text from wrapping */
            overflow: hidden; /* Prevent overflow */
            text-overflow: ellipsis; /* Add "..." if text overflows */
        }

        .category-button:hover {
            background: linear-gradient(145deg, #2980b9, #3498db);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }

        .category-button:active {
            transform: translateY(0);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }

        /* Ads Section */
        .ads-section {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .ad-box {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            border: 1px solid #3498db;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .ad-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .ad-box h2 {
            font-size: 1.2rem;
            color: #2980b9;
        }

        .ad-box p {
            margin: 10px 0;
            font-size: 0.9rem;
            color: #34495e;
        }

        .ad-box button {
            padding: 12px 24px;
            font-size: 1.1rem;
            background: linear-gradient(145deg, #2ecc71, #27ae60);
            color: white;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .ad-box button:hover {
            background: linear-gradient(145deg, #27ae60, #2ecc71);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .ad-box button:active {
            transform: translateY(0);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }

        /* Redeem Section */
        .redeem-section {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border: 1px solid #3498db;
        }

        .redeem-section button {
            padding: 15px 30px;
            background: linear-gradient(145deg, #f39c12, #e67e22);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .redeem-section button:hover {
            background: linear-gradient(145deg, #e67e22, #f39c12);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .redeem-section button:active {
            transform: translateY(0);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }

        .redeem-message {
            margin-top: 15px;
            font-size: 1rem;
            font-weight: bold;
            color: #e74c3c;
            padding: 10px;
            background-color: #fbe4e4;
            border-radius: 5px;
            display: none; /* Hidden initially */
        }

        .redeem-message.success {
            color: #27ae60;
            background-color: #e0f7e0;
        }

        /* Scrollable Earning History */
        .history-section {
            margin-top: 30px;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border: 1px solid #3498db;
        }

        .history-list {
            list-style: none;
            max-height: 200px; /* Set a max height for the scrollable area */
            overflow-y: auto; /* Enables vertical scrolling */
            padding: 10px;
            border: 1px solid #2980b9;
            border-radius: 8px;
            background-color: #f9f9f9;
            margin-top: 20px;
        }

        .history-list li {
            padding: 8px 0;
            border-bottom: 1px solid #ddd;
            font-size: 0.9rem;
        }

        .history-list li:last-child {
            border-bottom: none;
        }

        footer {
            text-align: center;
            margin-top: 50px;
            color: #7f8c8d;
        }

    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Monetag Mini App</h1>
            <p>get High Ecpm from 3 PM to 10 AM Next Update for Telegram Channel</p>
        </header>

        <!-- Telegram Group Section -->
        <section class="telegram-section" style="text-align: center; margin-top: 0px;">
            <a href="https://t.me/MdreamBoss" target="_blank">
                <button class="category-button">Telegram</button>
            </a>
        </section>

        <section class="ads-section" id="ads-section">
            <!-- Ads will be dynamically listed here -->
            <div class="ad-box">
                <h2>Sample Ad</h2>
                <p>Watch this ad and earn 10 points!</p>
                <button onclick="showAd()">Watch Ad</button>
            </div>
        </section>

        <!-- Redeem Section -->
        <section class="redeem-section">
            <h3>Redeem Your Earnings</h3>
            <p>Current Points: <span id="points">0</span> | Cash: $<span id="cash">0.00</span></p>
            <button onclick="redeemCash()">Redeem Cash</button>
            <p id="redeem-message" class="redeem-message"></p>
        </section>

        <!-- Earning History Section with Scrollable View -->
        <section class="history-section">
            <h3>Earning History</h3>
            <ul class="history-list" id="history-list">
                <!-- History will be displayed here -->
            </ul>
        </section>
    </div>

    <footer>
        <p>© 2024 Watch Ads & Monetag</p>
    </footer>

    <!-- Include the ad script -->
    <script src="//niphaumeenses.net/vignette.min.js" data-zone="8555463" data-sdk="show_8555463"></script>

    <script>
        let points = 0;
        let cash = 0;
        let earningHistory = [];

        // Function to show ad
        function showAd() {
            show_8555463().then(() => {
                // After ad is shown, user gets rewards
                points += 10;
                document.getElementById('points').textContent = points;
                earningHistory.push({ adId: 1, date: new Date() });
                displayEarningHistory();
                alert('You have seen the ad and earned 10 points!');
            }).catch((error) => {
                alert('Error displaying ad: ' + error.message);
            });
        }

        // Function to redeem points for cash
        function redeemCash() {
            if (points >= 100) {
                cash += 10;
                points -= 100;
                document.getElementById('points').textContent = points;
                document.getElementById('cash').textContent = cash.toFixed(2);
                showRedeemMessage('success', 'Redeemed successfully!');
            } else {
                showRedeemMessage('error', 'Not enough points to redeem.');
            }
        }

        // Function to show redeem message
        function showRedeemMessage(type, message) {
            const redeemMessage = document.getElementById('redeem-message');
            redeemMessage.classList.remove('success', 'error');
            redeemMessage.classList.add(type);
            redeemMessage.textContent = message;
            redeemMessage.style.display = 'block';
        }

        // Function to display earning history
        function displayEarningHistory() {
            const historyList = document.getElementById('history-list');
            historyList.innerHTML = ''; // Clear previous history
            earningHistory.forEach(entry => {
                const listItem = document.createElement('li');
                listItem.textContent = `Ad ID: ${entry.adId} - Date: ${entry.date.toLocaleString()}`;
                historyList.appendChild(listItem);
            });
        }

        // Initialize the page
        displayEarningHistory();
    </script>
</body>
</html>
