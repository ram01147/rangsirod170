<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>Racing Portfolio - งานส่งครู</title>
    <link href="https://fonts.googleapis.com/css2?family=Teko:wght@400;600;700&family=Titillium+Web:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --f1-red: #e10600;
            --asphalt: #15151e;
            --carbon: #1f1f23;
            --text-light: #f1f1f1;
            --accent-border: #38383f;
        }

        body {
            margin: 0;
            font-family: 'Titillium Web', sans-serif;
            background-color: var(--asphalt);
            background-image: 
                linear-gradient(rgba(21, 21, 30, 0.9), rgba(21, 21, 30, 0.95)),
                repeating-linear-gradient(45deg, #2b2b2b 0, #2b2b2b 1px, transparent 0, transparent 50%);
            background-size: cover;
            color: var(--text-light);
        }

        /* Speed Strip Decoration */
        .speed-strip {
            height: 8px;
            background: repeating-linear-gradient(
                90deg,
                var(--f1-red),
                var(--f1-red) 50px,
                transparent 50px,
                transparent 100px
            );
            border-bottom: 2px solid white;
        }

        header {
            background: #000;
            padding: 40px 20px;
            text-align: center;
            border-bottom: 4px solid var(--f1-red);
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
            margin-bottom: 30px;
        }

        header h1 {
            font-family: 'Teko', sans-serif;
            color: white;
            font-size: 60px;
            text-transform: uppercase;
            letter-spacing: 4px;
            margin: 0;
            font-style: italic; /* ทำให้ตัวเอียงดูพุ่งไปข้างหน้า */
            text-shadow: 4px 4px 0px var(--f1-red);
        }

        header p {
            color: #bbb;
            font-size: 18px;
            margin-top: 5px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .container {
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Card Design - Telemetry Box Style */
        .card {
            background: var(--carbon);
            border-top: 4px solid #444; /* Default border */
            border-radius: 8px 8px 24px 8px; /* มุมขวาล่างตัดมน */
            padding: 25px;
            position: relative;
            box-shadow: 0 10px 20px rgba(0,0,0,0.5);
            transition: all 0.2s ease-out;
            border-left: 1px solid var(--accent-border);
            border-right: 1px solid var(--accent-border);
            border-bottom: 1px solid var(--accent-border);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        /* แถบสีด้านบนการ์ดแต่ละใบ */
        .card:nth-child(1) { border-top-color: var(--f1-red); }
        .card:nth-child(2) { border-top-color: #ffbf00; } /* Yellow Flag */
        .card:nth-child(3) { border-top-color: #00d2be; } /* Mercedes Petronas Green */
        .card:nth-child(4) { border-top-color: #0600f0; } /* Alpine Blue */
        .card:nth-child(5) { border-top-color: #ff8700; } /* McLaren Orange */
        .card:nth-child(6) { border-top-color: #ffffff; } /* Haas White */

        .card:hover {
            transform: translateY(-5px) skewX(-2deg);
            border-top-color: var(--f1-red); /* Hover แล้วเปลี่ยนเป็นสีแดงทั้งหมด */
            box-shadow: 0 15px 30px rgba(225, 6, 0, 0.15);
        }

        .card h2 {
            font-family: 'Teko', sans-serif;
            font-size: 28px;
            margin-top: 0;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-style: italic;
            border-bottom: 1px dashed #555;
            padding-bottom: 10px;
            margin-bottom: 15px;
        }

        .card h2 span {
            color: var(--f1-red);
            font-size: 0.8em;
            margin-right: 10px;
        }

        .card p {
            color: #aaa;
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        /* Button - Pit Lane Style */
        .btn {
            display: block;
            margin-top: 8px;
            padding: 12px 15px;
            background: transparent;
            color: white;
            text-decoration: none;
            font-family: 'Teko', sans-serif;
            font-size: 20px;
            text-transform: uppercase;
            text-align: center;
            border: 2px solid white;
            border-radius: 4px;
            transition: all 0.2s;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0; left: -100%;
            width: 100%; height: 100%;
            background: var(--f1-red);
            z-index: -1;
            transition: left 0.3s;
            transform: skewX(-20deg);
        }

        .btn:hover {
            border-color: var(--f1-red);
            font-weight: bold;
        }

        .btn:hover::before {
            left: 0;
        }

        /* Label for sub-tasks */
        .sub-task-label {
            font-size: 12px;
            color: #666;
            margin-bottom: 2px;
            display: block;
            text-transform: uppercase;
        }

        footer {
            text-align: center;
            padding: 40px;
            background: #000;
            color: #555;
            font-family: 'Teko', sans-serif;
            font-size: 18px;
            text-transform: uppercase;
            border-top: 4px solid var(--f1-red);
            margin-top: 40px;
        }
    </style>
</head>

<body>

<div class="speed-strip"></div>

<header>
    <h1>F1 SEASON WORKS</h1>
    <p>IT Subject | 2026 Championship</p>
</header>

<section class="container">

    <div class="card">
        <div>
            <h2><span>GP 01</span> งานที่ 1</h2>
            <p>จุดเริ่มต้นของฤดูกาล (Foundation Phase)</p>
        </div>
        <a href="https://docs.google.com/document/d/1O91KYmDwk8HKZvV5pODoq0pfXaAPs0byYziNSsEUbK4/edit?tab=t.0" target="_blank" class="btn">START ENGINE</a>
    </div>

    <div class="card">
        <div>
            <h2><span>GP 02</span> ใบปลิวแนะนำตัวเอง</h2>
            <p>Driver Profile & Stats (Canva Design)</p>
        </div>
        <a href="https://www.canva.com/design/DAHA5vepAzc/Mqks2CP2JZCN8wRClk_-XQ/edit?utm_content=DAHA5vepAzc&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton" target="_blank" class="btn">VIEW PROFILE</a>
    </div>

    <div class="card">
        <div>
            <h2><span>GP 03</span> รวมงานออกแบบ</h2>
            <p>Special Liveries Series (3 Tracks)</p>
        </div>
        
        <span class="sub-task-label">Track 1</span>
        <a href="https://www.canva.com/design/DAHA5kBsEfw/KCY2jtD0ArcJPlNi4KYUuQ/edit" target="_blank" class="btn">CHRISTMAS</a>
        
        <span class="sub-task-label">Track 2</span>
        <a href="https://www.canva.com/design/DAG8TzmWIUQ/YCVtDTOzRtrsMZBBhTc0eQ/edit" target="_blank" class="btn">NEW YEAR</a>
        
        <span class="sub-task-label">Track 3</span>
        <a href="https://www.canva.com/design/DAHA5vhKWoo/-98UaJzzuZ1xawf3z-SDOQ/edit?ui=eyJFIjp7IkE_IjoiTiIsIlMiOiJBQUZqLXJUTzlwNCIsIlQiOjN9fQ" target="_blank" class="btn">MAGAZINE</a>
    </div>

    <div class="card">
        <div>
            <h2><span>GP 04</span> HNY Document</h2>
            <p>Technical Regulations Update (Google Docs)</p>
        </div>
        <a href="https://docs.google.com/document/d/1Qk4Yf86uf766g5jxRpGffQfIltKuzjffXZtbkmdVV90/edit?tab=t.0#heading=h.4zsrh2uh5vy3" target="_blank" class="btn">INSPECT</a>
    </div>

    <div class="card">
        <div>
            <h2><span>GP 05</span> นิตยสาร / Magazine</h2>
            <p>Paddock Club Exclusive Content</p>
        </div>
        <a href="https://www.canva.com/design/DAG-RoiRasY/VD3mSzoJ0a_CCK75rH4mmQ/edit" target="_blank" class="btn">READ TELEMETRY</a>
    </div>

    <div class="card">
        <div>
            <h2><span>GP 06</span> ใบปลิว</h2>
            <p>Race Poster Promotion</p>
        </div>
        <a href="https://www.canva.com/design/DAG7uSHrkxU/tephX808PnWbTObCanS0Dw/edit" target="_blank" class="btn">VIEW POSTER</a>
    </div>

</section>

<footer>
    © 2026 Student Racing Team | Ready to Race
</footer>

</body>
</html>
