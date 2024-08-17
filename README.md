<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ERP System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            height: 100vh;
            align-items: center;
            justify-content: center;
            background-color: #f0f0f0;
        }

        #login-section {
            width: 300px;
            padding: 20px;
            background-color: #ffffff;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        #login-form input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        #login-form button {
            width: 100%;
            padding: 10px;
            background-color: #2c3e50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        #login-form button:hover {
            background-color: #34495e;
        }

        #dashboard-section {
            display: flex;
            width: 100%;
            height: 100vh;
            display: none;
        }

        .sidebar {
            width: 250px;
            background-color: #2c3e50;
            color: white;
            padding: 15px;
            height: 100vh;
        }

        .sidebar h2 {
            text-align: center;
        }

        .sidebar ul {
            list-style-type: none;
            padding: 0;
        }

        .sidebar ul li {
            margin: 20px 0;
        }

        .sidebar ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            display: block;
        }

        .main-content {
            flex-grow: 1;
            padding: 20px;
        }

        .header h1 {
            font-size: 24px;
            margin-bottom: 20px;
        }

        .content {
            display: flex;
            gap: 20px;
        }

        .card {
            background-color: #ecf0f1;
            padding: 20px;
            border-radius: 8px;
            flex: 1;
            text-align: center;
        }

        #error-message {
            color: red;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div id="login-section">
        <h2>ERP System Login</h2>
        <form id="login-form">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <a href="/index1.html" target="_blank"></a>
            <button type="submit">Login</button>

        </form>
        <p id="error-message"></p>
    </div>

    <div id="dashboard-section">
        <div class="sidebar">
            <h2>ERP System</h2>
            <ul>
                <li><a href="#">Dashboard</a></li>
                <li><a href="#">Inventory</a></li>
                <li><a href="#">Orders</a></li>
                <li><a href="#">Customers</a></li>
                <li><a href="#">Reports</a></li>
                <li><a href="#">Settings</a></li>
            </ul>
        </div>
        <div class="main-content">
            <div class="header">
                <h1>Welcome to the ERP Dashboard</h1>
            </div>
            <div class="content">
                <div class="card">
                    <h3>Inventory Overview</h3>
                    <p>Total Products: 120</p>
                </div>
                <div class="card">
                    <h3>Orders Overview</h3>
                    <p>Pending Orders: 15</p>
                </div>
                <div class="card">
                    <h3>Customer Overview</h3>
                    <p>Active Customers: 320</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Simulated login credentials
        const correctUsername = "admin";
        const correctPassword = "password123";

        document.getElementById('login-form').addEventListener('submit', function(e) {
            e.preventDefault();

            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const errorMessage = document.getElementById('error-message');

            if (username === correctUsername && password === correctPassword) {
                document.getElementById('login-section').style.display = 'none';
                document.getElementById('dashboard-section').style.display = 'flex';
            } else {
                errorMessage.textContent = "Invalid username or password.";
            }
        });
    </script>
</body>
</html>
