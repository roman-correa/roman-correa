## Hi there 👋

<!--
**roman-correa/roman-correa** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Programador Snacker</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Roboto:wght@400;700&display=swap');
        
        .banner-container {
            width: 800px;
            height: 400px;
            background: linear-gradient(135deg, #2c3e50, #1a1f2d);
            font-family: 'Roboto', sans-serif;
            position: relative;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 15px 30px rgba(0,0,0,0.4);
        }
        
        /* Escritorio */
        .desk {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 35%;
            background: linear-gradient(to top, #3e2723, #5d4037);
            border-top: 15px solid #4e342e;
        }
        
        /* Silla */
        .chair {
            position: absolute;
            bottom: 35%;
            left: 10%;
            width: 200px;
            height: 150px;
            background: #455a64;
            border-radius: 10px 10px 0 0;
            transform: perspective(300px) rotateX(20deg);
            z-index: 2;
        }
        
        /* Personaje */
        .programmer {
            position: absolute;
            bottom: 35%;
            left: 20%;
            z-index: 5;
        }
        
        /* Cabeza */
        .head {
            width: 120px;
            height: 120px;
            background: #ffcc80;
            border-radius: 50%;
            position: relative;
            z-index: 10;
        }
        
        /* Calvicie */
        .bald-spot {
            position: absolute;
            top: -5px;
            left: 30px;
            width: 60px;
            height: 40px;
            background: #f5d7b3;
            border-radius: 50% 50% 0 0;
            box-shadow: 0 -2px 5px rgba(0,0,0,0.1);
        }
        
        /* Pelo lateral */
        .side-hair {
            position: absolute;
            top: 20px;
            width: 20px;
            height: 40px;
            background: #333;
            border-radius: 10px;
        }
        
        .side-hair.left { left: 5px; transform: rotate(-10deg); }
        .side-hair.right { right: 5px; transform: rotate(10deg); }
        
        /* Cuerpo */
        .body {
            position: absolute;
            top: 100px;
            left: 10px;
            width: 160px;
            height: 200px;
        }
        
        /* Pecho */
        .chest {
            position: absolute;
            width: 140px;
            height: 90px;
            background: #ffb74d;
            border-radius: 70px 70px 40px 40px;
            top: 0;
            left: 10px;
            z-index: 5;
            box-shadow: inset -5px -5px 10px rgba(0,0,0,0.1);
        }
        
        /* Panza */
        .belly {
            position: absolute;
            width: 180px;
            height: 140px;
            background: #ffb74d;
            border-radius: 90px;
            top: 60px;
            left: -10px;
            z-index: 4;
            box-shadow: inset 0 -10px 15px rgba(0,0,0,0.1);
        }
        
        /* Camiseta */
        .tshirt {
            position: absolute;
            width: 160px;
            height: 100px;
            background: #e53935;
            border-radius: 20px 20px 80px 80px;
            top: 40px;
            left: 0;
            z-index: 6;
        }
        
        .tshirt:before {
            content: "";
            position: absolute;
            width: 80px;
            height: 80px;
            background: #1a237e;
            border-radius: 50%;
            top: 10px;
            left: 40px;
        }
        
        /* Brazos */
        .arm {
            position: absolute;
            background: #ffcc80;
            z-index: 3;
        }
        
        .arm.left {
            width: 40px;
            height: 120px;
            border-radius: 20px;
            top: 50px;
            left: -20px;
            transform: rotate(15deg);
        }
        
        .arm.right {
            width: 40px;
            height: 100px;
            border-radius: 20px;
            top: 60px;
            right: -20px;
            transform: rotate(-25deg);
        }
        
        /* Manos */
        .hand {
            position: absolute;
            width: 40px;
            height: 30px;
            background: #ffcc80;
            border-radius: 10px;
        }
        
        .hand.left {
            bottom: -10px;
            left: 0;
        }
        
        .hand.right {
            bottom: -10px;
            right: 0;
        }
        
        /* Monitor */
        .monitor {
            position: absolute;
            width: 300px;
            height: 200px;
            background: #37474f;
            border-radius: 15px;
            bottom: 40%;
            right: 20%;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            z-index: 8;
        }
        
        .screen {
            position: absolute;
            width: 90%;
            height: 80%;
            background: #0d1b2a;
            border-radius: 8px;
            top: 10%;
            left: 5%;
            overflow: hidden;
            font-family: 'Courier New', monospace;
            color: #00ff41;
            padding: 15px;
            box-sizing: border-box;
        }
        
        .code-line {
            animation: typing 4s steps(40) infinite;
            white-space: nowrap;
            overflow: hidden;
            margin-bottom: 5px;
            font-size: 14px;
        }
        
        /* Papitas */
        .chip {
            position: absolute;
            background: #ffd54f;
            width: 20px;
            height: 8px;
            border-radius: 4px;
            transform: rotate(var(--rot));
            z-index: 20;
            box-shadow: 0 2px 3px rgba(0,0,0,0.2);
        }
        
        /* Bolsa de papitas */
        .chip-bag {
            position: absolute;
            width: 80px;
            height: 100px;
            background: #e53935;
            bottom: 40%;
            left: 50%;
            border-radius: 5px 5px 30px 5px;
            z-index: 7;
            transform: rotate(-10deg);
        }
        
        .chip-bag:before {
            content: "";
            position: absolute;
            top: 15px;
            left: 10px;
            width: 60px;
            height: 40px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 20px;
        }
        
        /* Texto del banner */
        .banner-text {
            position: absolute;
            top: 20px;
            left: 0;
            width: 100%;
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            color: white;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
            font-size: 32px;
            animation: glow 2s infinite alternate;
        }
        
        /* Animaciones */
        @keyframes typing {
            0% { width: 0 }
            50% { width: 100% }
            100% { width: 100% }
        }
        
        @keyframes glow {
            from { text-shadow: 0 0 5px #fff; }
            to { text-shadow: 0 0 20px #00b0ff, 0 0 30px #0086c3; }
        }
        
        .arm.right, .hand.right {
            animation: eating 3s infinite;
        }
        
        @keyframes eating {
            0% { transform: rotate(-25deg); }
            50% { transform: rotate(10deg) translateY(-20px); }
            100% { transform: rotate(-25deg); }
        }
        
        /* Detalles adicionales */
        .keyboard {
            position: absolute;
            width: 250px;
            height: 30px;
            background: #212121;
            bottom: 38%;
            right: 22%;
            border-radius: 5px;
            z-index: 7;
        }
        
        .cable {
            position: absolute;
            height: 250px;
            width: 8px;
            background: #bdbdbd;
            bottom: 0;
            right: 28%;
            z-index: 1;
        }
    </style>
</head>
<body>
    <div class="banner-container">
        <div class="banner-text">RENDIMIENTO SIN PRETENSIONES</div>
        
        <div class="desk"></div>
        <div class="cable"></div>
        <div class="chair"></div>
        
        <div class="programmer">
            <div class="head">
                <div class="bald-spot"></div>
                <div class="side-hair left"></div>
                <div class="side-hair right"></div>
            </div>
            
            <div class="body">
                <div class="chest"></div>
                <div class="belly"></div>
                <div class="tshirt"></div>
                <div class="arm left"></div>
                <div class="arm right"></div>
                <div class="hand left"></div>
                <div class="hand right"></div>
            </div>
        </div>
        
        <div class="monitor">
            <div class="screen">
                <div class="code-line">while (snacks > 0) {</div>
                <div class="code-line">&nbsp;&nbsp;codeQuality++;</div>
                <div class="code-line">&nbsp;&nbsp;snacks--;</div>
                <div class="code-line">}</div>
                <div class="code-line">// Rendimiento garantizado</div>
            </div>
        </div>
        
        <div class="keyboard"></div>
        <div class="chip-bag"></div>
        
        <!-- Papitas esparcidas -->
        <div class="chip" style="--rot: 25deg; bottom: 38%; left: 53%;"></div>
        <div class="chip" style="--rot: -15deg; bottom: 37%; left: 56%;"></div>
        <div class="chip" style="--rot: 40deg; bottom: 36%; left: 50%;"></div>
        <div class="chip" style="--rot: 5deg; bottom: 40%; left: 58%;"></div>
        <div class="chip" style="--rot: -30deg; bottom: 42%; right: 25%;"></div>
    </div>
</body>
</html>
