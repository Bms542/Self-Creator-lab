<?xml version="1.0" encoding="UTF-8" ?>

<!DOCTYPE html>

<html xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>

<head>

    <meta charset='UTF-8'/>

    <meta content='width=device-width, initial-scale=1.0, user-scalable=no' name='viewport'/>

    <title>Monetag Mini App</title>

    <style>

        /* General reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f4f6f7;
            color: #34495e;
            padding: 20px;
            user-select: none;
        }

        button {
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
            white-space: nowrap;
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

        /* Beautiful Auto Ad Button */
        .auto-ad-button {
            padding: 15px 30px;
            background: linear-gradient(145deg, #f39c12, #e67e22);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            margin: 10px;
            display: inline-block;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .auto-ad-button:hover {
            background: linear-gradient(145deg, #e67e22, #f39c12);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }

        .auto-ad-button:active {
            transform: translateY(0);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }

        /* Ads Section */
        .ads-section {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
            gap: 20px;
            margin-top: 30px;
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
            display: none;
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
            max-height: 200px;
            overflow-y: auto;
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

        /* Auto Ad Section */
        .auto-ad {
            display: none;
            padding: 15px;
            background-color:  #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }

    </style>

    <b:skin><![CDATA[

        /* Add any additional styles for the skin here */

    ]]></b:skin>

</head>

<body>

    <div class='container'>

        <header>

            <h1>Monetag Mini App</h1>
            <p>Get High Ecpm from 3 PM to 10 AM Next Update for Telegram Channel</p>

        </header>

        <!-- Main Section -->
        <b:section id='main' showaddelement='yes'>

            <b:widget id='HTML1' locked='false' title='Watch Ads  Earn Money' type='HTML' version='1'>

                <b:widget-settings>
                    <b:widget-setting name='content'/>
                </b:widget-settings>

                <b:includable id='main'>
                    <div class='widget-content'>
                        <data:content/>
                    </div>
                    <b:include name='quickedit'/>
                </b:includable>

            </b:widget>

        </b:section>

        <section class='telegram-section' style='text-align: center; margin-top: 20px;'>
            <a href='https://t.me/SelfCreatorLab' target='_blank'>
                <button class='category-button'>Telegram</button>
            </a>
        </section>

        <section class='ads-section' id='ads-section'>
            <div class='ad-box'>
                <h2>High Ecpm Ads</h2>
                <p>Hacking...</p>
                <button onclick='showAd()'>Watch Ad</button>
            </div>
        </section>

        <!-- Auto Ad Toggle Button -->
        <section class='auto-ad-section' style='text-align: center; margin-top: 20px;'>
            <div style="display:inline-block; margin: 10px; border: 2px solid #e67e22; border-radius: 10px; padding: 20px;">
                <button class='auto-ad-button' onclick='startAutoAds()'>Start Auto Ads</button>
                <button class='category-button' onclick='stopAutoAds()' style='display:none;' id='stop-auto-ads'>Stop Auto Ads</button>
            </div>
        </section>

        <!-- Auto Ad Section -->
        <div class='auto-ad' id='auto-ad'>
            <h3>Auto Ad</h3>
            <p>Ads Loding every 2 seconds...</p>
        </div>

        <!-- Redeem Section -->
        <section class='redeem-section'>
            <h3>Redeem Your Earnings</h3>
            <p>Total Ads: <span id='points'>0</span> | Cash: $<span id='cash'>0.00</span></p>
            <button onclick='redeemCash()'>Redeem Cash</button>
            <p class='redeem-message' id='redeem-message'></p>
        </section>

        <!-- Earning History Section with Scrollable View -->
        <section class='history-section'>
            <h3>Earning History</h3>
            <ul class='history-list' id='history-list'>
                <!-- History will be displayed here -->
            </ul>
        </section>

    </div>

    <footer>
        <p>&#169; 2024 Watch Ads Monetag</p>
    </footer>

    <script data-sdk='show_8555463' data-zone='8555463' src='//niphaumeenses.net/vignette.min.js'></script>
    <script>

        let points = 0;
        let cash = 0;
        let earningHistory = [];
        let autoAdInterval;

        // Function to show ad
        function showAd() {
            show_8555463().then(() => {
                points += 01;
                document.getElementById('points').textContent = points;
                earningHistory.push({ adId: 1, date: new Date() });
                displayEarningHistory();
            }).catch((error) => {
                console.error('Error displaying ad:', error.message);
            });
        }

        // Function to redeem points for cash
        function redeemCash() {
            if (points >= 100) {
                cash += 01;
                points -= 100;
                document.getElementById('points').textContent = points;
                document.getElementById('cash').textContent = cash.toFixed(2);
                showRedeemMessage('success', 'Redeemed successfully!');
            } else {
                showRedeemMessage('error', 'Not enough Ads 100 to redeem.');
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

        // Function to start automatic ads
        function startAutoAds() {
            autoAdInterval = setInterval(showAd, 2000); // Show ad every 2 seconds
            document.getElementById('auto-ad').style.display = 'block';
            document.getElementById('stop-auto-ads').style.display = 'inline-block';
            document.querySelector('.auto-ad-section .auto-ad-button').style.display = 'none'; // Hide Start button
        }

        // Function to stop automatic ads
        function stopAutoAds() {
            clearInterval(autoAdInterval);
            document.getElementById('auto-ad').style.display = 'none';
            document.getElementById('stop-auto-ads').style.display = 'none';
            document.querySelector('.auto-ad-section .auto-ad-button').style.display = 'inline-block'; // Show Start button
        }

        // Initialize the page
        displayEarningHistory();

    </script>

</body>

</html>
