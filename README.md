<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login and Signup Page</title>
    <link rel="stylesheet" href="./login.css">
</head>
<body>
    <div class="wrapper">
        <!-- Login Form -->
        <div class="form-box Login">
            <h2>Login</h2>
            <form>
                <div class="input-box">
                    <input type="text" name="username" required>
                    <label>Username</label>
                </div>
                <div class="input-box">
                    <input type="password" name="password" required>
                    <label>Password</label>
                </div>
                <button type="submit">Login</button>
                <p class="switch-text">Don't have an account? <a href="#" onclick="switchToRegister()">Sign up</a></p>
            </form>
        </div>

        <!-- Register Form -->
        <div class="form-box register">
            <h2>Sign Up</h2>
            <form>
                <div class="input-box">
                    <input type="text" name="username" required>
                    <label>Username</label>
                </div>
                <div class="input-box">
                    <input type="email" name="email" required>
                    <label>Email</label>
                </div>
                <div class="input-box">
                    <input type="password" name="password" required>
                    <label>Password</label>
                </div>
                <button type="submit">Sign Up</button>
                <p class="switch-text">Already have an account? <a href="#" onclick="switchToLogin()">Log in</a></p>
            </form>
        </div>

        <!-- Info Text -->
        <div class="info-text">
            <div class="text Login-text">
                <h2>Welcome Back!</h2>
                <p>Please log in to continue 
                    enjoying our services.</p>
            </div>
            <div class="text register-text">
                <h2>Welcome to Our Platform!</h2>
                <p>Sign up today to access exclusive
                    <br> features and content!</p>
            </div>
        </div>
    </div>

    <script>
        function switchToRegister() {
            document.querySelector('.wrapper').classList.add('active');
        }

        function switchToLogin() {
            document.querySelector('.wrapper').classList.remove('active');
        }
    </script>
</body>
</html>
