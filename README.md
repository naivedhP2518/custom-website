:root {
    --white: #ffffff;
    --black: #000000;
    --light-gray: #f0f0f0;
    --dark-gray: #333;
    --primary-color: #007bff;
}

body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: var(--light-gray);
}

.wrapper {
    position: relative;
    width: 750px;
    height: 450px;
    background: var(--white);
    border: 2px solid var(--black);
    border-radius: 10px;
    box-shadow: 0 0 20px var(--black);
    overflow: hidden;
    display: flex;
}

.form-box {
    position: absolute;
    top: 0;
    width: 50%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 0 40px;
    transition: all 0.7s ease;
}

.form-box.Login {
    left: 0;
}

.form-box.register {
    left: 100%;
    opacity: 0;
    z-index: 1;
}

.wrapper.active .form-box.register {
    left: 0;
    opacity: 1;
    z-index: 2;
}

.wrapper.active .form-box.Login {
    left: -100%;
    opacity: 0;
}

.input-box {
    position: relative;
    margin: 20px 0;
    width: 100%;
}

.input-box input {
    width: 100%;
    padding: 10px;
    margin-bottom: 5px;
    border: 1px solid var(--black);
    border-radius: 5px;
    outline: none;
    font-size: 16px;
}

.input-box label {
    position: absolute;
    top: 10px; /* Set the initial position */
    left: 10px;
    color: #aaa;
    font-size: 14px;
    pointer-events: none;
    transition: 0.3s;
}

.input-box input:focus + label,
.input-box input:not(:placeholder-shown) + label {
    top: -10px;
    left: 5px;
    font-size: 12px;
    color: var(--black);
}

button {
    width: 100%;
    padding: 10px;
    background-color: var(--black);
    color: var(--white);
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #333;
}

.switch-text {
    margin-top: 10px;
    font-size: 14px;
}

.switch-text a {
    color: var(--black);
    text-decoration: none;
    font-weight: bold;
    cursor: pointer;
}

.switch-text a:hover {
    text-decoration: underline;
}

.info-text {
    position: absolute;
    top: 0;
    right: 0;
    width: 50%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    padding: 20px;
    background-color: #f8f8f8;
    transition: all 0.7s ease;
}

.info-text .text {
    opacity: 0;
    position: absolute;
    transition: opacity 0.7s ease;
}

.info-text .Login-text {
    font-size: 16px;
    line-height: 1.5;
    opacity: 1;
}

.wrapper.active .info-text .Login-text {
    opacity: 0;
}

.wrapper.active .info-text .register-text {
    opacity: 1;
    font-size: 16px;
    line-height: 1.5;
}
