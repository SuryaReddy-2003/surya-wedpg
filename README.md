# surya-wedpg
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign In Page</title>
  
    <script>
        function validateLogin(event) {
            event.preventDefault();
            let username = document.getElementById("username").value;
            let password = document.getElementById("password").value;
            let message = document.getElementById("message");
            
            if (username === "admin" && password === "password123") {
                message.style.color = "green";
                message.innerText = "Login successful!";
            } else {
                message.style.color = "red";
                message.innerText = "Invalid username or password.";
            }
        }
    </script>
</head>
<body>
    <div class="container">
        <h2>Sign In</h2>
        <form onsubmit="validateLogin(event)">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>
        <p id="message"></p>
    </div>
</body>
</html>
