<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>My Web Page</title>
    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
            background-color: #E86C6C;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .switch {
            display: inline-block;
            position: relative;
            width: 60px;
            height: 34px;
        }
        .toggle {
            width: 100%;
            height: 100%;
            background-color: #ccc;
            border-radius: 17px;
            position: relative;
        }
        .toggle.active {
            background-color: #2196F3;
        }
        .toggle-button {
            width: 30px;
            height: 30px;
            background-color: white;
            border-radius: 50%;
            position: absolute;
            top: 2px;
            left: 2px;
            transition: transform 0.3s;
        }
        .toggle.active .toggle-button {
            transform: translateX(26px);
        }
        .text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
        }
    </style>
</head>
<body>
    <button><a href="threelines.html" class="button">&#9776;</a></button>
    
    <h1 style="text-align: center; font-weight: bold;">PILOT MODE...</h1>
    
    <div class="switch">
        <div class="toggle" onclick="Animatedtoggle()">
            <div class="toggle-button"></div>
        </div>
        <div class="text">OFF</div>
    </div>
    
    <script>
        function Animatedtoggle(){
            let toggle = document.querySelector(".toggle");
            let text = document.querySelector(".text");
            toggle.classList.toggle("active");
            if(toggle.classList.contains("active")){
                text.innerHTML = "ON";
            }
            else{
                text.innerHTML = "OFF";
            }
        }
    </script>
    
    <p>A website created by me.</p>
</body>
</html>
