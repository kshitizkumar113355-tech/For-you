DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>For You</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body, html { width: 100%; height: 100%; overflow: hidden; background: #000; }
        
        .slide {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            transition: all 0.8s ease-in-out;
            z-index: 1;
        }

        .instruction {
            position: absolute;
            bottom: 30px;
            font-size: 0.8rem;
            opacity: 0.6;
            animation: blink 1.5s infinite;
        }

        @keyframes blink { 50% { opacity: 0.1; } }

        /* Slide 1: Red */
        #slide1 { background: #ff4d4d; color: white; }
        .crumble { transform: scale(0) rotate(15deg); opacity: 0; border-radius: 50%; }

        /* Slide 2: Yellow */
        #slide2 { background: #ffdb58; left: -100%; color: #5d4037; }
        #slide2.active { left: 0; }
        .choco-img { font-size: 80px; margin-bottom: 20px; }

        /* Slide 3: Teal */
        #slide3 { background: #008080; color: white; clip-path: circle(0% at 50% 50%); }
        #slide3.active { clip-path: circle(150% at 50% 50%); }

        /* Slide 4: Blackout */
        #slide4 { background: black; color: white; display: none; }
        .bottom-to-center {
            position: relative;
            bottom: -100px;
            opacity: 0;
            transition: all 1s ease-out;
        }
        .bottom-to-center.show { bottom: 0; opacity: 1; }
        
        .btn-group { margin-top: 20px; display: none; }
        .btn {
            background: white; color: black; border: none;
            padding: 10px 20px; margin: 5px; border-radius: 20px; font-weight: bold;
        }

        /* Slide 5: Rabbit */
        #slide5 { background: #fce4ec; display: none; overflow: hidden; }
        .rabbit { font-size: 50px; position: absolute; left: -60px; bottom: 40%; transition: all 3s linear; }
        .text-card {
            position: absolute; right: -100%; background: white;
            padding: 15px; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            width: 80%; transition: all 1s ease-out; color: #ad1457;
        }

        /* Slide 6: Filmy */
        #slide6 { background: #e1f5fe; display: none; color: #0277bd; }

        /* Slide 7: Final */
        #slide7 { background: #fff3e0; display: none; }
        .grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; font-size: 40px; }
    </style>
</head>
<body>

    <div id="slide1" class="slide" onclick="toSlide2()">
        <h1>tumhe chocolates to pasand ni jyada</h1>
        <p class="instruction">Tap the screen</p>
    </div>

    <div id="slide2" class="slide" onclick="toSlide3()">
        <div class="choco-img">🍫</div>
        <h1>online ye chocolate rakh lo</h1>
    </div>

    <div id="slide3" class="slide" onclick="toSlide4()">
        <h1>baad me hm fastfood date pr chalenge 🍟</h1>
    </div>

    <div id="slide4" class="slide">
        <h1 id="secretText" class="bottom-to-center">tmhe ek baat batau?</h1>
        <div class="btn-group" id="btnGroup">
            <button class="btn" onclick="toSlide5()">Yes</button>
            <button class="btn" onclick="toSlide5()">Of course</button>
        </div>
    </div>

    <div id="slide5" class="slide" onclick="toSlide6()">
        <div id="rabbit" class="rabbit">🐰</div>
        <div id="textCard" class="text-card">"I can't eat you but you are my sweet chocolate"</div>
    </div>

    <div id="slide6" class="slide" onclick="toSlide7()">
        <div style="font-size: 60px;">🙈</div>
        <p>thoda sa filmy ho gaya par you will understand one day what does it mean</p>
    </div>

    <div id="slide7" class="slide">
        <div class="grid">
            <span>🍫</span><span>🍬</span><span>🍭</span>
            <span>🍫</span><span>🍩</span><span>🍫</span>
            <span>🍭</span><span>🍬</span><span>🍫</span>
        </div>
        <h1 style="margin-top:20px; color: #e65100;">HAPPY CHOCOLATE DAY GAHDEE</h1>
    </div>

    <script>
        function toSlide2() {
            document.getElementById('slide1').classList.add('crumble');
            document.getElementById('slide2').classList.add('active');
        }

        function toSlide3() {
            document.getElementById('slide3').classList.add('active');
        }

        function toSlide4() {
            document.getElementById('slide4').style.display = 'flex';
            setTimeout(() => {
                document.getElementById('secretText').classList.add('show');
                setTimeout(() => {
                    document.getElementById('btnGroup').style.display = 'block';
                }, 1000);
            }, 3000);
        }

        function toSlide5() {
            document.getElementById('slide4').style.display = 'none';
            document.getElementById('slide5').style.display = 'flex';
            const rabbit = document.getElementById('rabbit');
            const card = document.getElementById('textCard');
            
            // Rabbit walks in
            setTimeout(() => {
                rabbit.style.left = '20%';
                // Card pulls in
                setTimeout(() => {
                    card.style.right = '10%';
                    // Rabbit runs away
                    setTimeout(() => {
                        rabbit.style.left = '110%';
                    }, 2000);
                }, 1000);
            }, 500);
        }

        function toSlide6() {
            document.getElementById('slide5').style.display = 'none';
            document.getElementById('slide6').style.display = 'flex';
        }

        function toSlide7() {
            document.getElementById('slide6').style.display = 'none';
            document.getElementById('slide7').style.display = 'flex';
        }
    </script>
</body>
</html>
