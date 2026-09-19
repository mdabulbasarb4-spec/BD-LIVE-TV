
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ফ্রি লাইভ টিভি - TvWatch Clone</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background-color: #0f172a; color: #f8fafc; padding: 20px; }
        header { text-align: center; margin-bottom: 30px; padding: 20px 0; border-bottom: 1px solid #1e293b; }
        header h1 { color: #38bdf8; font-size: 28px; margin-bottom: 5px; }
        header p { color: #94a3b8; font-size: 14px; }
        .main-container { max-width: 1000px; margin: 0 auto; display: flex; flex-direction: column; gap: 20px; }
        .player-section { background: #1e293b; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 6px -1px rgba(0,0,0,0.5); aspect-ratio: 16/9; width: 100%; display: flex; align-items: center; justify-content: center; position: relative; }
        .player-section iframe { width: 100%; height: 100%; border: none; }
        .player-placeholder { padding: 20px; text-align: center; color: #64748b; font-size: 18px; }
        .grid-title { font-size: 20px; margin-top: 10px; color: #f1f5f9; border-left: 4px solid #38bdf8; padding-left: 10px; }
        .channel-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); gap: 15px; margin-bottom: 4px; }
        .channel-card { background: #1e293b; border: 1px solid #334155; border-radius: 8px; padding: 15px; text-align: center; cursor: pointer; transition: all 0.2s ease; display: flex; flex-direction: column; align-items: center; gap: 10px; }
        .channel-card:hover { transform: translateY(-3px); border-color: #38bdf8; background: #334155; }
        .channel-logo { width: 55px; height: 55px; background: #0f172a; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 24px; }
        .channel-name { font-size: 14px; font-weight: 600; color: #e2e8f0; }
        footer { text-align: center; margin-top: 5px; padding: 20px; color: #475569; font-size: 13px; }
    </style>
</head>
<body>

<header>
    <h1>📺 আমার ফ্রি লাইভ টিভি</h1>
    <p>যেকোনো চ্যানেল সিলেক্ট করে সরাসরি অনলাইনে ফ্রিতে দেখুন</p>
</header>

<div class="main-container">
    <!-- ভিডিও প্লেয়ার স্ক্রিন -->
    <div class="player-section" id="playerWindow">
        <div class="player-placeholder">নিচের যেকোনো একটি চ্যানেলে ক্লিক করে লাইভ স্ট্রিম চালু করুন</div>
    </div>

    <h2 class="grid-title">বাংলাদেশি লাইভ চ্যানেলসমূহ</h2>
    
    <!-- চ্যানেল গ্রিড -->
    <div class="channel-grid">
        <!-- সময় টিভি -->
        <div class="channel-card" onclick="playChannel('https://youtube.com')">
            <div class="channel-logo">⏱️</div>
            <div class="channel-name">সময় টিভি</div>
        </div>

        <!-- যমুনা টিভি -->
        <div class="channel-card" onclick="playChannel('https://youtube.com')">
            <div class="channel-logo">🌊</div>
            <div class="channel-name">যমুনা টিভি</div>
        </div>

        <!-- ডিবিসি নিউজ -->
        <div class="channel-card" onclick="playChannel('https://youtube.com')">
            <div class="channel-logo">📰</div>
            <div class="channel-name">DBC নিউজ</div>
        </div>

        <!-- একাত্তর টিভি -->
        <div class="channel-card" onclick="playChannel('https://youtube.com')">
            <div class="channel-logo">৭১</div>
            <div class="channel-name">একাত্তর টিভি</div>
        </div>

        <!-- চ্যানেল আই -->
        <div class="channel-card" onclick="playChannel('https://youtube.com')">
            <div class="channel-logo">👁️</div>
            <div class="channel-name">চ্যানেল আই</div>
        </div>
    </div>
</div>

<footer>
    <p>&copy; 2026 Free TV App. All Rights Reserved. লিগ্যাল ও ফ্রি ইউটিউব স্ট্রিম দ্বারা চালিত।</p>
</footer>

<script>
    function playChannel(embedUrl) {
        const playerWindow = document.getElementById('playerWindow');
        playerWindow.innerHTML = `<iframe src="${embedUrl}" allow="autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>`;
    }
</script>

</body>
</html>
