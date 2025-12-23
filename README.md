# Huyen_Speaking_101-200
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Luyện Speaking Part 1 - Red Edition Pro</title>
    <style>
        :root {
            --primary-color: #d32f2f;
            --secondary-color: #b71c1c;
            --accent-light: #ffebee;
            --bg-color: #fdf2f2;
            --card-bg: #ffffff;
            --text-color: #333333;
            --success-color: #2e7d32;
            --warning-color: #f57f17;
            --gray-color: #757575;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            color: var(--text-color);
            padding: 10px;
            box-sizing: border-box;
        }

        .container {
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(211, 47, 47, 0.15);
            width: 100%;
            max-width: 600px;
            text-align: center;
            border-top: 5px solid var(--primary-color);
            position: relative;
            box-sizing: border-box;
        }

        /* Header & Progress */
        .header-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .header-controls {
            display: flex;
            gap: 10px;
        }

        .btn-icon {
            background: none;
            border: none;
            font-size: 22px; 
            cursor: pointer;
            color: var(--primary-color);
            padding: 5px;
            transition: transform 0.2s;
        }
        .btn-icon:hover { transform: scale(1.1); }

        .progress-bar {
            color: #ef5350;
            font-weight: 600;
            font-size: 14px;
            letter-spacing: 1px;
        }

        /* Card Area */
        .card {
            min-height: 320px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            padding: 10px;
        }

        .vietnamese-text {
            font-size: 22px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #2c3e50;
            line-height: 1.5;
            word-wrap: break-word; 
        }

        .hidden-content {
            display: none;
            animation: fadeIn 0.5s ease-out;
            width: 100%;
        }

        .english-row {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin: 10px 0;
            flex-wrap: wrap;
        }

        .english-word {
            font-size: 24px;
            color: var(--primary-color);
            font-weight: 700;
            text-shadow: 1px 1px 0px rgba(0,0,0,0.05);
            margin: 0;
            word-break: break-word; 
            line-height: 1.4;
            text-align: center;
        }

        .ipa-text {
            font-family: 'Lucida Sans Unicode', 'Arial Unicode MS', sans-serif;
            font-size: 16px;
            color: #757575;
            margin-bottom: 15px;
            font-weight: 400;
            line-height: 1.4;
        }

        .btn-audio-replay {
            background: white;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            width: 40px; 
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.2s;
            flex-shrink: 0;
            -webkit-tap-highlight-color: transparent; 
        }
        .btn-audio-replay:hover {
            background: var(--primary-color);
            color: white;
            transform: scale(1.1);
        }

        .part-of-speech {
            font-style: normal;
            font-weight: 600;
            color: #c62828;
            margin-bottom: 8px;
            font-size: 14px;
            background: var(--accent-light);
            padding: 5px 12px;
            border-radius: 15px;
            display: inline-block;
            border: 1px solid #ffcdd2;
        }

        /* Buttons */
        .btn {
            border: none;
            padding: 14px 20px; 
            font-size: 16px;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            color: white;
            -webkit-tap-highlight-color: transparent;
        }
        
        .btn:hover { transform: translateY(-2px); box-shadow: 0 6px 12px rgba(0,0,0,0.15); }
        .btn:active { transform: translateY(1px); }
        .btn:disabled { background: #bdbdbd !important; cursor: not-allowed; transform: none; box-shadow: none; color: #fff;}

        .btn-reveal {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            width: 100%;
            margin-top: 20px;
            font-size: 18px;
        }

        .nav-row {
            display: flex;
            justify-content: space-between;
            margin-top: 25px;
            gap: 15px;
        }

        .btn-nav {
            background-color: white;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
            width: 55px; 
            height: 55px;
            border-radius: 50%;
            font-size: 22px;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 0;
        }

        .review-actions {
            display: flex;
            gap: 10px;
            margin-top: 20px;
            justify-content: center;
        }

        .btn-learn { background-color: var(--warning-color); flex: 1; }
        .btn-success { background-color: var(--success-color); flex: 1; }

        .status-badge {
            font-size: 12px;
            padding: 4px 8px;
            border-radius: 4px;
            margin-bottom: 10px;
            display: inline-block;
            font-weight: bold;
        }
        .status-new { color: var(--gray-color); background: #eee; }
        .status-learned { color: var(--success-color); background: #e8f5e9; border: 1px solid #c8e6c9; }
        .status-learning { color: var(--warning-color); background: #fff3e0; border: 1px solid #ffe0b2; }

        .status-msg {
            font-size: 13px;
            margin-top: 10px;
            color: #e53935;
            font-style: italic;
            height: 20px;
        }

        /* Modal Global */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.6);
            z-index: 100;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(2px);
        }

        .modal-content {
            background: white;
            width: 90%;
            max-width: 400px;
            max-height: 85vh; 
            border-radius: 15px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 20px 50px rgba(0,0,0,0.3);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }

        .list-container {
            overflow-y: auto;
            flex: 1;
            -webkit-overflow-scrolling: touch; 
        }

        .list-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 10px; 
            border-bottom: 1px solid #f5f5f5;
            cursor: pointer;
            text-align: left;
            align-items: center;
        }
        .list-item:hover { background-color: #fce4ec; }
        .list-item.active { background-color: #ffcdd2; font-weight: bold; }

        .stats-summary {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
            text-align: center;
        }
        .stat-box {
            padding: 10px;
            border-radius: 10px;
            width: 30%;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .stat-val { font-size: 20px; font-weight: bold; display: block; }
        .stat-label { font-size: 12px; }
        
        .bg-learned { background: #e8f5e9; color: var(--success-color); }
        .bg-learning { background: #fff3e0; color: var(--warning-color); }
        .bg-new { background: #f5f5f5; color: var(--gray-color); }

        .recommend-section {
            text-align: left;
            margin-top: 10px;
            flex: 1;
            overflow-y: auto;
            -webkit-overflow-scrolling: touch;
        }
        .recommend-item {
            padding: 12px 8px;
            border-bottom: 1px solid #eee;
            cursor: pointer;
            color: var(--warning-color);
            font-weight: 500;
        }
        .recommend-item:hover { background: #fff3e0; }
        
        .settings-row {
            margin-bottom: 15px;
            text-align: left;
        }
        .settings-label {
            font-weight: 600;
            margin-bottom: 5px;
            display: block;
            color: #555;
        }
        select.settings-input {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: 1px solid #ccc;
            font-size: 14px;
            background: #fff;
        }
        input[type=range] {
            width: 100%;
            margin-top: 5px;
        }

        @media (max-width: 480px) {
            .container { padding: 20px; }
            .vietnamese-text { font-size: 18px; }
            .english-word { font-size: 22px; }
            .card { min-height: 240px; }
            .btn { font-size: 15px; padding: 12px; }
            .btn-nav { width: 45px; height: 45px; font-size: 18px; }
            .header-controls { gap: 8px; }
            .btn-icon { font-size: 22px; }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header-row">
        <div class="header-controls">
            <button class="btn-icon" onclick="toggleList()" title="Danh sách">☰</button>
            <button class="btn-icon" onclick="toggleStats()" title="Thống kê">📊</button>
            <button class="btn-icon" onclick="toggleSettings()" title="Cài đặt">⚙️</button>
            <button class="btn-icon" onclick="shuffleVocabulary()" title="Trộn">🔀</button>
        </div>
        <div id="progress" class="progress-bar"></div>
    </div>

    <div id="current-status" class="status-badge status-new">Mới</div>
    
    <div class="card">
        <div id="question-area">
            <div class="vietnamese-text" id="vn-text">Đang tải dữ liệu...</div>
        </div>

        <div id="answer-area" class="hidden-content">
            <div class="part-of-speech" id="pos-text"></div>
            
            <div class="english-row">
                <div class="english-word" id="en-text"></div>
                <button class="btn-audio-replay" onclick="playCurrentAudio()" title="Nghe lại">🔊</button>
            </div>
            
            <div class="ipa-text" id="ipa-text"></div>
        </div>
    </div>

    <div id="status-msg" class="status-msg"></div>

    <div id="main-actions">
        <button id="btn-reveal" class="btn btn-reveal" onclick="revealAnswer()">XEM ĐÁP ÁN</button>
    </div>

    <div id="review-actions" class="review-actions" style="display: none;">
        <button class="btn btn-learn" onclick="markStatus('learning')">Chưa thuộc 😕</button>
        <button class="btn btn-success" onclick="markStatus('learned')">Đã thuộc 😎</button>
    </div>

    <div class="nav-row">
        <button class="btn btn-nav" onclick="changeCard(-1)">❮</button>
        <button class="btn btn-nav" onclick="changeCard(1)">❯</button>
    </div>
</div>

<!-- Modal Danh Sách -->
<div id="list-modal" class="modal-overlay">
    <div class="modal-content">
        <div class="modal-header">
            <h3 style="margin:0; color:var(--primary-color)">Danh Sách Câu</h3>
            <button onclick="toggleList()" style="border:none; background:none; font-size:24px; cursor:pointer;">&times;</button>
        </div>
        <div class="list-container" id="vocab-list-content"></div>
    </div>
</div>

<!-- Modal Thống Kê -->
<div id="stats-modal" class="modal-overlay">
    <div class="modal-content">
        <div class="modal-header">
            <h3 style="margin:0; color:var(--primary-color)">Thống Kê</h3>
            <button onclick="toggleStats()" style="border:none; background:none; font-size:24px; cursor:pointer;">&times;</button>
        </div>
        
        <div class="stats-summary">
            <div class="stat-box bg-learned">
                <span class="stat-val" id="stat-learned">0</span>
                <span class="stat-label">Đã thuộc</span>
            </div>
            <div class="stat-box bg-learning">
                <span class="stat-val" id="stat-learning">0</span>
                <span class="stat-label">Chưa thuộc</span>
            </div>
            <div class="stat-box bg-new">
                <span class="stat-val" id="stat-new">0</span>
                <span class="stat-label">Mới</span>
            </div>
        </div>

        <hr style="border:0; border-top:1px solid #eee; width:100%; margin: 10px 0;">
        <h4 style="margin: 0 0 10px 0; color: #555;">💡 Cần ôn tập ngay:</h4>
        <div class="recommend-section" id="recommend-list"></div>
    </div>
</div>

<!-- Modal Cài Đặt -->
<div id="settings-modal" class="modal-overlay">
    <div class="modal-content">
        <div class="modal-header">
            <h3 style="margin:0; color:var(--primary-color)">Cài Đặt Âm Thanh</h3>
            <button onclick="toggleSettings()" style="border:none; background:none; font-size:24px; cursor:pointer;">&times;</button>
        </div>
        
        <div style="padding: 10px 0;">
            <div class="settings-row">
                <label class="settings-label">Chọn Giọng Đọc (Hệ thống):</label>
                <select id="voice-select" class="settings-input" onchange="updateVoiceSettings()">
                    <option value="-1">Tự động chọn (Tốt nhất)</option>
                </select>
                <p style="font-size: 12px; color: #666; margin-top: 5px;">* Ưu tiên giọng "Google UK English Female" hoặc giọng Anh.</p>
            </div>
            
            <div class="settings-row">
                <label class="settings-label">Tốc Độ Đọc: <span id="speed-display" style="color:var(--primary-color)">0.8</span></label>
                <input type="range" id="speed-range" min="0.4" max="1.5" step="0.1" value="0.8" oninput="updateSpeedSettings()">
                <div style="display:flex; justify-content:space-between; font-size:12px; color:#999; margin-top:5px;">
                    <span>Chậm (0.4)</span>
                    <span>Nhanh (1.5)</span>
                </div>
            </div>
            
            <button class="btn" style="width:100%; margin-top:10px;" onclick="testVoice()">🔊 Nghe thử</button>
        </div>
    </div>
</div>

<script>
    // === DỮ LIỆU TỪ VỰNG MỚI (88 items) ===
    const initialVocabulary = [
        { id: 1, en: "Currently, I am a senior at a high school in my hometown.", vi: "Hiện tại, em đang là học sinh năm cuối (lớp 12) tại một trường cấp 3 ở quê.", ipa: "/ˈkʌr.ənt.li aɪ æm ə ˈsiː.ni.ər æt ə haɪ skuːl ɪn maɪ ˈhəʊm.taʊn/", pos: "Senior (n)" },
        { id: 2, en: "To be honest, I am very busy right now because I am in the middle of preparing for the national entrance exam.", vi: "Thành thật mà nói, hiện tại em rất bận vì đang trong giai đoạn chuẩn bị cho kỳ thi THPT Quốc gia.", ipa: "/tu bi ˈɒn.ɪst aɪ æm ˈver.i ˈbɪz.i raɪt naʊ bɪˈkɒz aɪ æm ɪn ðə ˈmɪd.əl əv prɪˈpeər.ɪŋ fɔː ðə ˈnæʃ.ən.əl ˈen.trəns ɪɡˈzæm/", pos: "In the middle of + V-ing" },
        { id: 3, en: "I decided to focus on social sciences because I have always been keen on learning languages.", vi: "Em quyết định tập trung vào các môn xã hội vì em luôn thích học ngôn ngữ.", ipa: "/aɪ dɪˈsaɪ.dɪd tu ˈfəʊ.kəs ɒn ˈsəʊ.ʃəl ˈsaɪ.ən.sɪz bɪˈkɒz aɪ hæv ˈɔːl.weɪz biːn kiːn ɒn ˈlɜːn.ɪŋ ˈlæŋ.ɡwɪdʒ.ɪz/", pos: "Keen on (adj)" },
        { id: 4, en: "I want to pursue a career as an interpreter in the future, so this path suits me best.", vi: "Em muốn theo đuổi nghề phiên dịch viên trong tương lai, nên con đường này phù hợp nhất với em.", ipa: "/aɪ wɒnt tu pəˈsjuː ə kəˈrɪər æz ən ɪnˈtɜː.prə.tər ɪn ðə ˈfjuː.tʃər səʊ ðɪs pɑːθ suːts miː best/", pos: "Pursue a career" },
        { id: 5, en: "To be honest, the only thing I dislike is the heavy workload.", vi: "Thú thật, điều duy nhất em không thích là khối lượng bài vở quá nặng.", ipa: "/tu bi ˈɒn.ɪst ði ˈəʊn.li θɪŋ aɪ dɪsˈlaɪk ɪz ðə ˈhev.i ˈwɜːk.ləʊd/", pos: "Heavy workload (n)" },
        { id: 6, en: "As a 12th grader, I have to study day in, day out to memorize a lot of knowledge.", vi: "Là học sinh lớp 12, em phải học ngày qua ngày để ghi nhớ rất nhiều kiến thức.", ipa: "/æz ə twelfθ ˈɡreɪ.dər aɪ hæv tu ˈstʌd.i deɪ ɪn deɪ aʊt tu ˈmem.ə.raɪz ə lɒt əv ˈnɒl.ɪdʒ/", pos: "Day in, day out (idm)" },
        { id: 7, en: "It makes me feel under pressure sometimes.", vi: "Đôi khi điều đó làm em cảm thấy bị áp lực.", ipa: "/ɪt meɪks miː fiːl ˈʌn.dər ˈpreʃ.ər ˈsʌm.taɪmz/", pos: "Under pressure (phrase)" },
        { id: 8, en: "Actually, what I enjoy most is the supportive environment at my school.", vi: "Thực ra, điều em thích nhất là môi trường hỗ trợ lẫn nhau ở trường em.", ipa: "/ˈæk.tʃu.ə.li wɒt aɪ ɪnˈdʒɔɪ məʊst ɪz ðə səˈpɔː.tɪv ɪnˈvaɪ.rən.mənt æt maɪ skuːl/", pos: "Supportive (adj)" },
        { id: 9, en: "My friends and I always help each other with difficult homework.", vi: "Bạn bè và em luôn giúp đỡ nhau làm những bài tập khó.", ipa: "/maɪ frendz ənd aɪ ˈɔːl.weɪz help iːtʃ ˈʌð.ər wɪð ˈdɪf.ɪ.kəlt ˈhəʊm.wɜːk/", pos: "Help each other" },
        { id: 10, en: "Plus, we have a lot of fun together during break times, which really helps me let my hair down.", vi: "Thêm nữa, chúng em rất vui vẻ trong giờ giải lao, điều đó thực sự giúp em xả hơi.", ipa: "/plʌs wi hæv ə lɒt əv fʌn təˈɡeð.ər ˈdʒʊə.rɪŋ breɪk taɪmz wɪtʃ ˈrɪə.li helps miː let maɪ heər daʊn/", pos: "Let hair down (idm)" },
        { id: 11, en: "My immediate plan is to pass the upcoming exam with flying colors.", vi: "Kế hoạch trước mắt của em là vượt qua kỳ thi sắp tới với điểm số cao.", ipa: "/maɪ ɪˈmiː.di.ət plæn ɪz tu pɑːs ði ˈʌpˌkʌm.ɪŋ ɪɡˈzæm wɪð ˈflaɪ.ɪŋ ˈkʌl.əz/", pos: "Flying colors (idm)" },
        { id: 12, en: "I hope to major in English at a prestigious university in Ho Chi Minh City.", vi: "Em hy vọng sẽ học chuyên ngành tiếng Anh tại một trường đại học danh tiếng ở TP.HCM.", ipa: "/aɪ həʊp tu ˈmeɪ.dʒər ɪn ˈɪŋ.ɡlɪʃ æt ə presˈtɪdʒ.əs ˌjuː.nɪˈvɜː.sə.ti ɪn həʊ tʃiː mɪn ˈsɪt.i/", pos: "Prestigious (adj)" },
        { id: 13, en: "Personally, I prefer studying alone because I find it easier to concentrate.", vi: "Cá nhân em thích học một mình hơn vì em thấy dễ tập trung hơn.", ipa: "/ˈpɜː.sən.əl.i aɪ prɪˈfɜː ˈstʌd.i.ɪŋ əˈləʊn bɪˈkɒz aɪ faɪnd ɪt ˈiː.zi.ər tu ˈkɒn.sən.treɪt/", pos: "Concentrate (v)" },
        { id: 14, en: "Studying in a group can be fun, but sometimes I get distracted by chatting with my friends.", vi: "Học nhóm có thể vui, nhưng đôi khi em bị xao nhãng do nói chuyện với bạn bè.", ipa: "/ˈstʌd.i.ɪŋ ɪn ə ɡruːp kæn bi fʌn bʌt ˈsʌm.taɪmz aɪ ɡet dɪˈstræk.tɪd baɪ ˈtʃæt.ɪŋ wɪð maɪ frendz/", pos: "Distracted (adj)" },
        { id: 15, en: "I would say I am a night owl, so I work more effectively in the evening.", vi: "Em có thể nói mình là \"cú đêm\", nên em làm việc hiệu quả hơn vào buổi tối.", ipa: "/aɪ wʊd seɪ aɪ æm ə naɪt aʊl səʊ aɪ wɜːk mɔːr ɪˈfek.tɪv.li ɪn ði ˈiːv.nɪŋ/", pos: "Night owl (n)" },
        { id: 16, en: "It is usually much quieter at night, which helps me stay focused on my homework.", vi: "Ban đêm thường yên tĩnh hơn nhiều, giúp em tập trung vào bài tập về nhà.", ipa: "/ɪt ɪz ˈjuː.ʒu.ə.li mʌtʃ ˈkwaɪ.ə.tər æt naɪt wɪtʃ helps miː steɪ ˈfəʊ.kəst ɒn maɪ ˈhəʊm.wɜːk/", pos: "Stay focused" },
        { id: 17, en: "English is actually one of my favorite subjects, but mastering it is quite challenging.", vi: "Tiếng Anh thực sự là một trong những môn yêu thích của em, nhưng để giỏi nó thì khá thử thách.", ipa: "/ˈɪŋ.ɡlɪʃ ɪz ˈæk.tʃu.ə.li wʌn əv maɪ ˈfeɪ.vər.ɪt ˈsʌb.dʒekts bʌt ˈmɑː.stər.ɪŋ ɪt ɪz kwaɪt ˈtʃæl.ɪn.dʒɪŋ/", pos: "Mastering (v)" },
        { id: 18, en: "For me, grammar rules are confusing, and I sometimes struggle to remember new vocabulary.", vi: "Với em, các quy tắc ngữ pháp khá rối rắm, và đôi khi em gặp khó khăn trong việc nhớ từ vựng mới.", ipa: "/fɔː miː ˈɡræm.ər ruːlz ɑː kənˈfjuː.zɪŋ ənd aɪ ˈsʌm.taɪmz ˈstrʌɡ.əl tu rɪˈmem.bər njuː vəˈkæb.jə.lər.i/", pos: "Struggle (v)" },
        { id: 19, en: "However, I try to practice every day to improve.", vi: "Tuy nhiên, em cố gắng luyện tập mỗi ngày để cải thiện.", ipa: "/haʊˈev.ər aɪ traɪ tu ˈpræk.tɪs ˈev.ri deɪ tu ɪmˈpruːv/", pos: "Improve (v)" },
        { id: 20, en: "My teachers are very dedicated and knowledgeable.", vi: "Các thầy cô của em rất tận tâm và uyên bác.", ipa: "/maɪ ˈtiː.tʃərz ɑː ˈver.i ˈded.ɪ.keɪ.tɪd ənd ˈnɒl.ɪdʒ.ə.bəl/", pos: "Dedicated (adj)" },
        { id: 21, en: "They always try to make the lessons engaging and easy to understand.", vi: "Họ luôn cố gắng làm cho bài học hấp dẫn và dễ hiểu.", ipa: "/ðeɪ ˈɔːl.weɪz traɪ tu meɪk ðə ˈles.ənz ɪnˈɡeɪ.dʒɪŋ ənd ˈiː.zi tu ˌʌn.dəˈstænd/", pos: "Engaging (adj)" },
        { id: 22, en: "My classroom is equipped with a modern projector and air conditioner.", vi: "Phòng học của em được trang bị máy chiếu hiện đại và máy lạnh.", ipa: "/maɪ ˈklɑːs.ruːm ɪz ɪˈkwɪpt wɪð ə ˈmɒd.ən prəˈdʒek.tər ənd eər kənˈdɪʃ.ən.ər/", pos: "Equipped with" },
        { id: 23, en: "I believe that education is the key to success in the future.", vi: "Em tin rằng giáo dục là chìa khóa dẫn đến thành công trong tương lai.", ipa: "/aɪ bɪˈliːv ðæt ˌed.jʊˈkeɪ.ʃən ɪz ðə kiː tu səkˈses ɪn ðə ˈfjuː.tʃər/", pos: "Key to success" },
        { id: 24, en: "Besides English, I am also interested in Literature because I love reading stories.", vi: "Ngoài tiếng Anh, em cũng thích Văn học vì em thích đọc truyện.", ipa: "/bɪˈsaɪdz ˈɪŋ.ɡlɪʃ aɪ æm ˈɔːl.səʊ ˈɪn.trə.stɪd ɪn ˈlɪt.rə.tʃər bɪˈkɒz aɪ lʌv ˈriː.dɪŋ ˈstɔː.riz/", pos: "Interested in" },
        { id: 25, en: "I am not very good with numbers, so Math is a bit tricky for me.", vi: "Em không giỏi với các con số lắm, nên môn Toán hơi khó nhằn với em.", ipa: "/aɪ æm nɒt ˈver.i ɡʊd wɪð ˈnʌm.bərz səʊ mæθ ɪz ə bɪt ˈtrɪk.i fɔː miː/", pos: "Tricky (adj)" },
        { id: 26, en: "During the break, I usually go to the canteen to grab a snack with my classmates.", vi: "Trong giờ giải lao, em thường xuống căn tin ăn vặt với bạn cùng lớp.", ipa: "/'dʒʊə.rɪŋ ðə breɪk aɪ ˈjuː.ʒu.ə.li ɡəʊ tu ðə kænˈtiːn tu ɡræb ə snæk wɪð maɪ ˈklɑːs.meɪts/", pos: "Grab a snack" },
        { id: 27, en: "I prefer offline learning because I can interact directly with my teachers.", vi: "Em thích học trực tiếp hơn vì em có thể tương tác trực tiếp với giáo viên.", ipa: "/aɪ prɪˈfɜː ˌɒfˈlaɪn ˈlɜː.nɪŋ bɪˈkɒz aɪ kæn ˌɪn.təˈrækt daɪˈrekt.li wɪð maɪ ˈtiː.tʃərz/", pos: "Offline learning" },
        { id: 28, en: "Online learning is convenient, but it can be quite boring sometimes.", vi: "Học online thì tiện lợi, nhưng đôi khi khá nhàm chán.", ipa: "/ˈɒn.laɪn ˈlɜː.nɪŋ ɪz kənˈviː.ni.ənt bʌt ɪt kæn bi kwaɪt ˈbɔː.rɪŋ ˈsʌm.taɪmz/", pos: "Convenient (adj)" },
        { id: 29, en: "I have to attend extra classes in the evening to prepare for the exams.", vi: "Em phải đi học thêm vào buổi tối để chuẩn bị cho các kỳ thi.", ipa: "/aɪ hæv tu əˈtend ˈek.strə ˈklɑː.sɪz ɪn ði ˈiːv.nɪŋ tu prɪˈpeər fɔː ði ɪɡˈzæmz/", pos: "Extra classes" },
        { id: 30, en: "I always try to finish my assignments before the deadline.", vi: "Em luôn cố gắng hoàn thành bài tập trước hạn chót.", ipa: "/aɪ ˈɔːl.weɪz traɪ tu ˈfɪn.ɪʃ maɪ əˈsaɪn.mənts bɪˈfɔː ðə ˈded.laɪn/", pos: "Deadline (n)" },
        { id: 31, en: "Learning a foreign language opens up many opportunities for me.", vi: "Học ngoại ngữ mở ra nhiều cơ hội cho em.", ipa: "/ˈlɜː.nɪŋ ə ˈfɒr.ən ˈlæŋ.ɡwɪdʒ ˈəʊ.pənz ʌp ˈmen.i ˌɒp.əˈtjuː.nə.tiz fɔː miː/", pos: "Opportunity (n)" },
        { id: 32, en: "I really admire my English teacher; she inspires me a lot.", vi: "Em rất ngưỡng mộ cô giáo tiếng Anh của em; cô truyền cảm hứng cho em rất nhiều.", ipa: "/aɪ ˈrɪə.li ədˈmaɪər maɪ ˈɪŋ.ɡlɪʃ ˈtiː.tʃər ʃiː ɪnˈspaɪəz miː ə lɒt/", pos: "Inspire (v)" },
        { id: 33, en: "The school facilities are quite modern and comfortable.", vi: "Cơ sở vật chất của trường khá hiện đại và thoải mái.", ipa: "/ðə skuːl fəˈsɪl.ə.tiz ɑː kwaɪt ˈmɒd.ən ənd ˈkʌm.fə.tə.bəl/", pos: "Facilities (n)" },
        { id: 34, en: "I have a lot in common with my classmates.", vi: "Em có rất nhiều điểm chung với các bạn cùng lớp.", ipa: "/aɪ hæv ə lɒt ɪn ˈkɒm.ən wɪð maɪ ˈklɑːs.meɪts/", pos: "In common" },
        { id: 35, en: "I was born and raised in a small coastal city located in the central part of my country.", vi: "Em sinh ra và lớn lên ở một thành phố biển nhỏ nằm ở miền Trung đất nước.", ipa: "/aɪ wɒz bɔːn ənd reɪzd ɪn ə smɔːl ˈkəʊ.stəl ˈsɪt.i ləʊˈkeɪ.tɪd ɪn ðə ˈsen.trəl pɑːt əv maɪ ˈkʌn.tri/", pos: "Coastal city" },
        { id: 36, en: "What I love most about my hometown is its picturesque landscapes.", vi: "Điều em yêu nhất ở quê mình là phong cảnh đẹp như tranh vẽ.", ipa: "/wɒt aɪ lʌv məʊst əˈbaʊt maɪ ˈhəʊm.taʊn ɪz ɪts ˌpɪk.tʃərˈesk ˈlænd.skeɪps/", pos: "Picturesque (adj)" },
        { id: 37, en: "It has breathtaking views of the ocean.", vi: "Nơi đây có những cảnh biển đẹp ngoạn mục.", ipa: "/ɪt hæz ˈbreθˌteɪ.kɪŋ vjuːz əv ði ˈəʊ.ʃən/", pos: "Breathtaking (adj)" },
        { id: 38, en: "Unlike the hustle and bustle of big cities, the pace of life here is quite tranquil.", vi: "Không giống sự xô bồ của thành phố lớn, nhịp sống ở đây khá yên bình.", ipa: "/ʌnˈlaɪk ðə ˈhʌs.əl ənd ˈbʌs.əl əv bɪɡ ˈsɪt.iz ðə peɪs əv laɪf hɪər ɪz kwaɪt ˈtræŋ.kwɪl/", pos: "Tranquil (adj)" },
        { id: 39, en: "Living here allows me to enjoy the fresh air every morning.", vi: "Sống ở đây cho phép em tận hưởng không khí trong lành mỗi sáng.", ipa: "/ˈlɪv.ɪŋ hɪər əˈlaʊz miː tu ɪnˈdʒɔɪ ðə freʃ eər ˈev.ri ˈmɔː.nɪŋ/", pos: "Fresh air" },
        { id: 40, en: "My hometown has undergone dramatic changes recently.", vi: "Quê hương em đã trải qua những thay đổi mạnh mẽ gần đây.", ipa: "/maɪ ˈhəʊm.taʊn hæz ˌʌn.dəˈɡɒn drəˈmæt.ɪk ˈtʃeɪn.dʒɪz ˈriː.sənt.li/", pos: "Undergo changes" },
        { id: 41, en: "It has become a famous tourist attraction with many modern amenities.", vi: "Nó đã trở thành một điểm du lịch nổi tiếng với nhiều tiện ích hiện đại.", ipa: "/ɪt hæz bɪˈkʌm ə ˈfeɪ.məs ˈtʊə.rɪst əˈtræk.ʃən wɪð ˈmen.i ˈmɒd.ən əˈmiː.nə.tiz/", pos: "Tourist attraction" },
        { id: 42, en: "However, the local people remain very hospitable and friendly.", vi: "Tuy nhiên, người dân địa phương vẫn rất hiếu khách và thân thiện.", ipa: "/haʊˈev.ər ðə ˈləʊ.kəl ˈpiː.pəl rɪˈmeɪn ˈver.i hɒsˈpɪt.ə.bəl ənd ˈfrend.li/", pos: "Hospitable (adj)" },
        { id: 43, en: "You should definitely try the local delicacies sold at street food stalls.", vi: "Bạn nhất định phải thử các món đặc sản địa phương bán ở các quầy hàng rong.", ipa: "/juː ʃʊd ˈdef.ɪ.nət.li traɪ ðə ˈləʊ.kəl ˈdel.ɪ.kə.siz səʊld æt striːt fuːd stɔːlz/", pos: "Delicacies (n)" },
        { id: 44, en: "The street food here is incredibly delicious and affordable.", vi: "Đồ ăn đường phố ở đây cực kỳ ngon và giá cả phải chăng.", ipa: "/ðə striːt fuːd hɪər ɪz ɪnˈkred.ə.bli dɪˈlɪʃ.əs ənd əˈfɔː.də.bəl/", pos: "Affordable (adj)" },
        { id: 45, en: "To be honest, my hometown is not really a good place for young people to build a career.", vi: "Thành thật mà nói, quê em không thực sự là nơi tốt để người trẻ xây dựng sự nghiệp.", ipa: "/tu bi ˈɒn.ɪst maɪ ˈhəʊm.taʊn ɪz nɒt ˈrɪə.li ə ɡʊd pleɪs fɔː jʌŋ ˈpiː.pəl tu bɪld ə kəˈrɪər/", pos: "Build a career" },
        { id: 46, en: "There are not many job opportunities for young people like me.", vi: "Không có nhiều cơ hội việc làm cho người trẻ như em.", ipa: "/ðeər ɑː nɒt ˈmen.i dʒɒb ˌɒp.əˈtjuː.nə.tiz fɔː jʌŋ ˈpiː.pəl laɪk miː/", pos: "Job opportunities" },
        { id: 47, en: "The nightlife is quite dull compared to big cities like Saigon.", vi: "Cuộc sống về đêm khá buồn tẻ so với các thành phố lớn như Sài Gòn.", ipa: "/ðə ˈnaɪt.laɪf ɪz kwaɪt dʌl kəmˈpeəd tu bɪɡ ˈsɪt.iz laɪk saɪˈɡɒn/", pos: "Dull (adj)" },
        { id: 48, en: "I think it is more suitable for elderly people who want to retire.", vi: "Em nghĩ nó phù hợp hơn với người lớn tuổi muốn nghỉ hưu.", ipa: "/aɪ θɪŋk ɪt ɪz mɔːr ˈsuː.tə.bəl fɔː ˈel.də.li ˈpiː.pəl huː wɒnt tu rɪˈtaɪər/", pos: "Retire (v)" },
        { id: 49, en: "The weather in my hometown is usually hot and humid.", vi: "Thời tiết ở quê em thường nóng và ẩm.", ipa: "/ðə ˈweð.ər ɪn maɪ ˈhəʊm.taʊn ɪz ˈjuː.ʒu.ə.li hɒt ənd ˈhjuː.mɪd/", pos: "Humid (adj)" },
        { id: 50, en: "We have two distinct seasons: the rainy season and the dry season.", vi: "Chúng em có hai mùa rõ rệt: mùa mưa và mùa khô.", ipa: "/wi hæv tuː dɪˈstɪŋkt ˈsiː.zənz ðə ˈreɪ.ni ˈsiː.zən ənd ðə draɪ ˈsiː.zən/", pos: "Distinct (adj)" },
        { id: 51, en: "Traffic congestion is becoming a serious problem during rush hours.", vi: "Ùn tắc giao thông đang trở thành vấn đề nghiêm trọng vào giờ cao điểm.", ipa: "/ˈtræf.ɪk kənˈdʒes.tʃən ɪz bɪˈkʌm.ɪŋ ə ˈsɪə.ri.əs ˈprɒb.ləm ˈdʒʊə.rɪŋ rʌʃ ˈaʊərz/", pos: "Traffic congestion" },
        { id: 52, en: "Most people in my hometown get around by motorbike.", vi: "Hầu hết mọi người ở quê em đi lại bằng xe máy.", ipa: "/məʊst ˈpiː.pəl ɪn maɪ ˈhəʊm.taʊn ɡet əˈraʊnd baɪ ˈməʊ.tə.baɪk/", pos: "Get around" },
        { id: 53, en: "Public transport is not very developed in my area.", vi: "Giao thông công cộng không phát triển lắm ở khu vực của em.", ipa: "/ˈpʌb.lɪk ˈtræn.spɔːt ɪz nɒt ˈver.i dɪˈvel.əpt ɪn maɪ ˈeə.ri.ə/", pos: "Public transport" },
        { id: 54, en: "I have many fond memories of playing in the local park when I was a child.", vi: "Em có nhiều ký ức đẹp về việc chơi ở công viên địa phương khi còn nhỏ.", ipa: "/aɪ hæv ˈmen.i fɒnd ˈmem.ər.iz əv ˈpleɪ.ɪŋ ɪn ðə ˈləʊ.kəl pɑːk wen aɪ wɒz ə tʃaɪld/", pos: "Fond memories" },
        { id: 55, en: "It is a small town, so you can easily go from one end to the other.", vi: "Đó là một thị trấn nhỏ, nên bạn có thể dễ dàng đi từ đầu này sang đầu kia.", ipa: "/ɪt ɪz ə smɔːl taʊn səʊ juː kæn ˈiː.zəl.i ɡəʊ frɒm wʌn end tu ði ˈʌð.ər/", pos: "From one end to..." },
        { id: 56, en: "Everyone knows each other in my neighborhood.", vi: "Mọi người đều biết nhau trong khu phố của em.", ipa: "/ˈev.ri.wʌn nəʊz iːtʃ ˈʌð.ər ɪn maɪ ˈneɪ.bə.hʊd/", pos: "Neighborhood (n)" },
        { id: 57, en: "It is a great place to escape from the stress of daily life.", vi: "Đó là nơi tuyệt vời để thoát khỏi sự căng thẳng của cuộc sống thường ngày.", ipa: "/ɪt ɪz ə ɡreɪt pleɪs tu ɪˈskeɪp frɒm ðə stres əv ˈdeɪ.li laɪf/", pos: "Escape (v)" },
        { id: 58, en: "The beaches are pristine and very beautiful in the summer.", vi: "Các bãi biển còn nguyên sơ và rất đẹp vào mùa hè.", ipa: "/ðə ˈbiː.tʃɪz ɑː ˈprɪs.tiːn ənd ˈver.i ˈbjuː.tɪ.fəl ɪn ðə ˈsʌm.ər/", pos: "Pristine (adj)" },
        { id: 59, en: "I feel a strong sense of belonging when I am in my hometown.", vi: "Em cảm thấy sự thuộc về mạnh mẽ khi ở quê hương mình.", ipa: "/aɪ fiːl ə strɒŋ sens əv bɪˈlɒŋ.ɪŋ wen aɪ æm ɪn maɪ ˈhəʊm.taʊn/", pos: "Sense of belonging" },
        { id: 60, en: "There are many historical sites that attract foreign tourists.", vi: "Có nhiều di tích lịch sử thu hút du khách nước ngoài.", ipa: "/ðeər ɑː ˈmen.i hɪˈstɒr.ɪ.kəl saɪts ðæt əˈtrækt ˈfɒr.ən ˈtʊə.rɪsts/", pos: "Historical sites" },
        { id: 61, en: "The cost of living here is much lower than in major cities.", vi: "Chi phí sinh hoạt ở đây thấp hơn nhiều so với các thành phố lớn.", ipa: "/ðə kɒst əv ˈlɪv.ɪŋ hɪər ɪz mʌtʃ ˈləʊ.ər ðæn ɪn ˈmeɪ.dʒər ˈsɪt.iz/", pos: "Cost of living" },
        { id: 62, en: "It is famous for its seafood, which is fresh and cheap.", vi: "Nó nổi tiếng với hải sản, vừa tươi vừa rẻ.", ipa: "/ɪt ɪz ˈfeɪ.məs fɔːr ɪts ˈsiː.fuːd wɪtʃ ɪz freʃ ənd tʃiːp/", pos: "Famous for" },
        { id: 63, en: "I usually go for a walk along the beach to relax.", vi: "Em thường đi dạo dọc bãi biển để thư giãn.", ipa: "/aɪ ˈjuː.ʒu.ə.li ɡəʊ fɔːr ə wɔːk əˈlɒŋ ðə biːtʃ tu rɪˈlæks/", pos: "Go for a walk" },
        { id: 64, en: "The atmosphere is always calm and peaceful.", vi: "Bầu không khí luôn êm đềm và yên bình.", ipa: "/ðə ˈæt.mə.sfɪər ɪz ˈɔːl.weɪz kɑːm ənd ˈpiːs.fəl/", pos: "Atmosphere (n)" },
        { id: 65, en: "I am very proud of the traditions and culture of my hometown.", vi: "Em rất tự hào về truyền thống và văn hóa của quê hương.", ipa: "/aɪ æm ˈver.i praʊd əv ðə trəˈdɪʃ.ənz ənd ˈkʌl.tʃər əv maɪ ˈhəʊm.taʊn/", pos: "Proud of" },
        { id: 66, en: "Currently, I am living in a terraced house with my family.", vi: "Hiện tại, em đang sống trong một ngôi nhà phố (nhà liền kề) với gia đình.", ipa: "/ˈkʌr.ənt.li aɪ æm ˈlɪv.ɪŋ ɪn ə ˈter.əst haʊs wɪð maɪ ˈfæm.əl.i/", pos: "Terraced house" },
        { id: 67, en: "It is located in a quiet residential area right in the heart of my town.", vi: "Nó nằm trong một khu dân cư yên tĩnh ngay trung tâm thị trấn của em.", ipa: "/ɪt ɪz ləʊˈkeɪ.tɪd ɪn ə ˈkwaɪ.ət ˌrez.ɪˈden.ʃəl ˈeə.ri.ə raɪt ɪn ðə hɑːt əv maɪ taʊn/", pos: "Residential area" },
        { id: 68, en: "My favorite room is definitely my own bedroom.", vi: "Căn phòng yêu thích của em chắc chắn là phòng ngủ của riêng em.", ipa: "/maɪ ˈfeɪ.vər.ɪt ruːm ɪz ˈdef.ɪ.nət.li maɪ əʊn ˈbed.ruːm/", pos: "Favorite (adj)" },
        { id: 69, en: "That is where I spend most of my time studying and sleeping.", vi: "Đó là nơi em dành phần lớn thời gian để học và ngủ.", ipa: "/ðæt ɪz weər aɪ spend məʊst əv maɪ taɪm ˈstʌd.i.ɪŋ ənd ˈsliː.pɪŋ/", pos: "Spend time + V-ing" },
        { id: 70, en: "Although it is not very spacious, it is quite cozy and airy.", vi: "Mặc dù nó không rộng rãi lắm, nhưng nó khá ấm cúng và thoáng đãng.", ipa: "/ɔːlˈðəʊ ɪt ɪz nɒt ˈver.i ˈspeɪ.ʃəs ɪt ɪz kwaɪt ˈkəʊ.zi ənd ˈeə.ri/", pos: "Spacious / Cozy" },
        { id: 71, en: "There is a big window overlooking the garden.", vi: "Có một cửa sổ lớn nhìn ra khu vườn.", ipa: "/ðeər ɪz ə bɪɡ ˈwɪn.dəʊ ˌəʊ.vəˈlʊk.ɪŋ ðə ˈɡɑː.dən/", pos: "Overlooking" },
        { id: 72, en: "It gives me privacy to unwind after a long day at school.", vi: "Nó mang lại cho em sự riêng tư để thư giãn sau một ngày dài ở trường.", ipa: "/ɪt ɡɪvz miː ˈprɪv.ə.si tu ʌnˈwaɪnd ˈɑːf.tər ə lɒŋ deɪ æt skuːl/", pos: "Privacy / Unwind" },
        { id: 73, en: "My house is in a prime location, very close to the market and supermarket.", vi: "Nhà em ở vị trí đắc địa, rất gần chợ và siêu thị.", ipa: "/maɪ haʊs ɪz ɪn ə praɪm ləʊˈkeɪ.ʃən ˈver.i kləʊs tu ðə ˈmɑː.kɪt ənd ˌsuː.pəˈmɑː.kɪt/", pos: "Prime location" },
        { id: 74, en: "Actually, it is within walking distance of my school.", vi: "Thực ra, nó nằm trong khoảng cách có thể đi bộ đến trường em.", ipa: "/ˈæk.tʃu.ə.li ɪt ɪz wɪˈðɪn ˈwɔː.kɪŋ ˈdɪs.təns əv maɪ skuːl/", pos: "Walking distance" },
        { id: 75, en: "I don’t have to spend much time commuting every day.", vi: "Em không phải tốn nhiều thời gian đi lại mỗi ngày.", ipa: "/aɪ dəʊnt hæv tu spend mʌtʃ taɪm kəˈmjuː.tɪŋ ˈev.ri deɪ/", pos: "Commute (v)" },
        { id: 76, en: "I am planning to move to Ho Chi Minh City next year for my university studies.", vi: "Em đang định chuyển đến TP.HCM vào năm tới để học đại học.", ipa: "/aɪ æm ˈplæn.ɪŋ tu muːv tu həʊ tʃiː mɪn ˈsɪt.i nekst jɪər fɔː maɪ ˌjuː.nɪˈvɜː.sə.ti ˈstʌd.iz/", pos: "Plan to + V" },
        { id: 77, en: "I will probably rent a small apartment near the university.", vi: "Có lẽ em sẽ thuê một căn hộ nhỏ gần trường đại học.", ipa: "/aɪ wɪl ˈprɒb.ə.bli rent ə smɔːl əˈpɑːt.mənt nɪər ðə ˌjuː.nɪˈvɜː.sə.ti/", pos: "Rent (v)" },
        { id: 78, en: "My living room is where my family gathers to watch TV every evening.", vi: "Phòng khách là nơi gia đình em tụ họp xem TV mỗi tối.", ipa: "/maɪ ˈlɪv.ɪŋ ruːm ɪz weər maɪ ˈfæm.əl.i ˈɡæð.ərz tu wɒtʃ ˌtiːˈviː ˈev.ri ˈiːv.nɪŋ/", pos: "Gather (v)" },
        { id: 79, en: "The walls in my room are painted in a soothing blue color.", vi: "Những bức tường trong phòng em được sơn màu xanh dương dịu nhẹ.", ipa: "/ðə wɔːlz ɪn maɪ ruːm ɑː ˈpeɪn.tɪd ɪn ə ˈsuː.ðɪŋ bluː ˈkʌl.ər/", pos: "Soothing (adj)" },
        { id: 80, en: "I like to decorate my walls with posters of my favorite bands.", vi: "Em thích trang trí tường bằng áp phích của các ban nhạc yêu thích.", ipa: "/aɪ laɪk tu ˈdek.ə.reɪt maɪ wɔːlz wɪð ˈpəʊ.stərz əv maɪ ˈfeɪ.vər.ɪt bændz/", pos: "Decorate (v)" },
        { id: 81, en: "Our kitchen is quite small, but it has everything we need.", vi: "Bếp nhà em khá nhỏ, nhưng có mọi thứ chúng em cần.", ipa: "/aʊər ˈkɪtʃ.ɪn ɪz kwaɪt smɔːl bʌt ɪt hæz ˈev.ri.θɪŋ wi niːd/", pos: "Kitchen (n)" },
        { id: 82, en: "We have a small garden where my mother grows fresh vegetables.", vi: "Chúng em có một khu vườn nhỏ nơi mẹ em trồng rau sạch.", ipa: "/wi hæv ə smɔːl ˈɡɑː.dən weər maɪ ˈmʌð.ər ɡrəʊz freʃ ˈvedʒ.tə.bəlz/", pos: "Grow (v)" },
        { id: 83, en: "My neighborhood is very safe; we rarely lock our doors during the day.", vi: "Khu phố em rất an toàn; chúng em hiếm khi khóa cửa vào ban ngày.", ipa: "/maɪ ˈneɪ.bə.hʊd ɪz ˈver.i seɪf wi ˈreə.li lɒk aʊər dɔːrz ˈdʒʊə.rɪŋ ðə deɪ/", pos: "Safe (adj)" },
        { id: 84, en: "My neighbors are very helpful and kind.", vi: "Hàng xóm của em rất hay giúp đỡ và tốt bụng.", ipa: "/maɪ ˈneɪ.bərz ɑː ˈver.i ˈhelp.fəl ənd kaɪnd/", pos: "Neighbor (n)" },
        { id: 85, en: "We often have a small party with our neighbors on weekends.", vi: "Chúng em thường tổ chức tiệc nhỏ với hàng xóm vào cuối tuần.", ipa: "/wi ˈɒf.ən hæv ə smɔːl ˈpɑː.ti wɪð aʊər ˈneɪ.bərz ɒn ˌwiːkˈendz/", pos: "Party (n)" },
        { id: 86, en: "I help my mother with house chores like doing the laundry and cleaning the floor.", vi: "Em giúp mẹ làm việc nhà như giặt giũ và lau nhà.", ipa: "/aɪ help maɪ ˈmʌð.ər wɪð haʊs tʃɔːrz laɪk ˈduː.ɪŋ ðə ˈlɔːn.dri ənd ˈkliːn.ɪŋ ðə flɔːr/", pos: "House chores" },
        { id: 87, en: "I want to buy a big house with a swimming pool in the future.", vi: "Em muốn mua một ngôi nhà lớn có hồ bơi trong tương lai.", ipa: "/aɪ wɒnt tu baɪ ə bɪɡ haʊs wɪð ə ˈswɪm.ɪŋ puːl ɪn ðə ˈfjuː.tʃər/", pos: "Swimming pool" },
        { id: 88, en: "My dream house would be a modern villa by the sea.", vi: "Ngôi nhà mơ ước của em sẽ là một biệt thự hiện đại bên bờ biển.", ipa: "/maɪ driːm haʊs wūd bi ə ˈmɒd.ən ˈvɪl.ə baɪ ðə siː/", pos: "Dream house" },
        { id: 89, en: "I prefer living in a house rather than a flat because it is more spacious.", vi: "Em thích sống ở nhà đất hơn là căn hộ vì nó rộng rãi hơn.", ipa: "/aɪ prɪˈfɜː ˈlɪv.ɪŋ ɪn ə haʊs ˈrɑː.ðər ðæn ə flæt bɪˈkɒz ɪt ɪz mɔːr ˈspeɪ.ʃəs/", pos: "Prefer ... rather than" },
        { id: 90, en: "Living in an apartment block offers better security services.", vi: "Sống trong chung cư cung cấp dịch vụ an ninh tốt hơn.", ipa: "/ˈlɪv.ɪŋ ɪn ən əˈpɑːt.mənt blɒk ˈɒf.ərz ˈbet.ər sɪˈkjʊə.rɪ.ti ˈsɜː.vɪ.sɪz/", pos: "Apartment block" },
        { id: 91, en: "My house has been renovated recently, so it looks quite new.", vi: "Nhà em mới được sửa sang lại gần đây, nên trông khá mới.", ipa: "/maɪ haʊs hæz biːn ˈren.ə.veɪ.tɪd ˈriː.sənt.li səʊ ɪt lʊks kwaɪt njuː/", pos: "Renovate (v)" },
        { id: 92, en: "There is a bookshelf in my room where I keep all my favorite books.", vi: "Có một giá sách trong phòng em, nơi em giữ tất cả những cuốn sách yêu thích.", ipa: "/ðeər ɪz ə ˈbʊk.ʃelf ɪn maɪ ruːm weər aɪ kiːp ɔːl maɪ ˈfeɪ.vər.ɪt bʊks/", pos: "Bookshelf (n)" },
        { id: 93, en: "I feel very comfortable and safe when I am at home.", vi: "Em cảm thấy rất thoải mái và an toàn khi ở nhà.", ipa: "/aɪ fiːl ˈver.i ˈkʌm.fə.tə.bəl ənd seɪf wen aɪ æm æt həʊm/", pos: "Comfortable (adj)" },
        { id: 94, en: "It is the place where I can truly be myself.", vi: "Đó là nơi em có thể thực sự là chính mình.", ipa: "/ɪt ɪz ðə pleɪs weər aɪ kæn ˈtruː.li bi maɪˈself/", pos: "Be myself" },
        { id: 95, en: "The internet connection in my house is very fast.", vi: "Kết nối internet ở nhà em rất nhanh.", ipa: "/ði ˈɪn.tə.net kəˈnek.ʃən ɪn maɪ haʊs ɪz ˈver.i fɑːst/", pos: "Connection (n)" },
        { id: 96, en: "We have a spacious balcony where we can sit and drink tea.", vi: "Chúng em có một ban công rộng rãi nơi có thể ngồi uống trà.", ipa: "/wi hæv ə ˈspeɪ.ʃəs ˈbæl.kə.ni weər wi kæn sɪt ənd drɪŋk tiː/", pos: "Balcony (n)" },
        { id: 97, en: "I don't like moving house because packing things is very tiring.", vi: "Em không thích chuyển nhà vì đóng gói đồ đạc rất mệt.", ipa: "/aɪ dəʊnt laɪk ˈmuː.vɪŋ haʊs bɪˈkɒz ˈpæk.ɪŋ θɪŋz ɪz ˈver.i ˈtaɪə.rɪŋ/", pos: "Move house" },
        { id: 98, en: "My parents have lived in this house for over 20 years.", vi: "Bố mẹ em đã sống ở ngôi nhà này hơn 20 năm rồi.", ipa: "/maɪ ˈpeə.rənts hæv lɪvd ɪn ðɪs haʊs fɔːr ˈəʊ.vər ˈtwen.ti jɪərz/", pos: "For over..." },
        { id: 99, en: "It is not just a house; it is a home full of love.", vi: "Nó không chỉ là một ngôi nhà (vật chất); nó là tổ ấm tràn đầy tình yêu thương.", ipa: "/ɪt ɪz nɒt dʒʌst ə haʊs ɪt ɪz ə həʊm fʊl əv lʌv/", pos: "Home full of love" },
        { id: 100, en: "I will miss my home a lot when I go to university.", vi: "Em sẽ nhớ nhà rất nhiều khi đi học đại học.", ipa: "/aɪ wɪl mɪs maɪ həʊm ə lɒt wen aɪ ɡəʊ tu ˌjuː.nɪˈvɜː.sə.ti/", pos: "Miss (v)" }
    ];

    let vocabularyList = initialVocabulary.map(item => ({...item, status: 'new'}));
    
    let currentIndex = 0;
    let isRevealed = false;
    let availableVoices = [];
    
    // Global settings for audio
    let selectedVoiceIndex = -1; // -1 means auto-detect
    let readingRate = 0.8; // Default slow speed

    // Elements
    const elements = {
        vnText: document.getElementById('vn-text'),
        enText: document.getElementById('en-text'),
        ipaText: document.getElementById('ipa-text'), // New element for IPA
        posText: document.getElementById('pos-text'),
        answerArea: document.getElementById('answer-area'),
        btnReveal: document.getElementById('btn-reveal'),
        reviewActions: document.getElementById('review-actions'),
        statusMsg: document.getElementById('status-msg'),
        progress: document.getElementById('progress'),
        currentStatus: document.getElementById('current-status'),
        listModal: document.getElementById('list-modal'),
        listContent: document.getElementById('vocab-list-content'),
        statsModal: document.getElementById('stats-modal'),
        statLearned: document.getElementById('stat-learned'),
        statLearning: document.getElementById('stat-learning'),
        statNew: document.getElementById('stat-new'),
        recommendList: document.getElementById('recommend-list'),
        settingsModal: document.getElementById('settings-modal'),
        voiceSelect: document.getElementById('voice-select'),
        speedRange: document.getElementById('speed-range'),
        speedDisplay: document.getElementById('speed-display')
    };

    // === SETUP AUDIO (PURE SYSTEM SPEECH) ===
    function loadVoices() {
        availableVoices = window.speechSynthesis.getVoices();
        
        // Populate Dropdown
        elements.voiceSelect.innerHTML = '';
        
        // Option Mặc định
        const defaultOption = document.createElement('option');
        defaultOption.value = -1;
        defaultOption.text = "Tự động chọn (Tốt nhất)";
        elements.voiceSelect.appendChild(defaultOption);
        
        // Select Google UK English Female as default if available
        let defaultSelectedIndex = -1;

        availableVoices.forEach((voice, index) => {
            // Chỉ hiện các giọng có tiếng Anh để đỡ rối
            if(voice.lang.includes('en')) {
                const option = document.createElement('option');
                option.value = index;
                option.text = `${voice.name} (${voice.lang})`;
                // Đánh dấu nếu đang được chọn
                if (index === selectedVoiceIndex) option.selected = true;
                
                // Check for preferred voice
                if (voice.name.includes("Google UK English Female")) {
                    defaultSelectedIndex = index;
                }
                
                elements.voiceSelect.appendChild(option);
            }
        });
        
        // Auto select preferred voice if user hasn't selected anything yet
        if (selectedVoiceIndex === -1 && defaultSelectedIndex !== -1) {
            elements.voiceSelect.value = defaultSelectedIndex;
            selectedVoiceIndex = defaultSelectedIndex;
        }
    }
    
    if (speechSynthesis.onvoiceschanged !== undefined) {
        speechSynthesis.onvoiceschanged = loadVoices;
    }
    // Gọi lần đầu (đôi khi trình duyệt đã load xong rồi)
    setTimeout(loadVoices, 100);

    function playAudio(text) {
        window.speechSynthesis.cancel();
        const utterance = new SpeechSynthesisUtterance(text);
        
        // Xác định giọng đọc
        if (selectedVoiceIndex !== -1 && availableVoices[selectedVoiceIndex]) {
            // Người dùng đã chọn giọng cụ thể
            utterance.voice = availableVoices[selectedVoiceIndex];
        } else {
            // Tự động chọn (Ưu tiên Google UK English Female / Premium / UK)
            let preferredVoice = availableVoices.find(voice => voice.name.includes("Google UK English Female"));
            
            if (!preferredVoice) {
                preferredVoice = availableVoices.find(voice => 
                    (voice.name.includes('Google') && voice.lang.includes('en')) || 
                    (voice.name.includes('Premium') && voice.lang.includes('en')) ||
                    (voice.name.includes('Samantha') && voice.lang.includes('en'))
                );
            }

            if (!preferredVoice) {
                preferredVoice = availableVoices.find(voice => voice.lang === 'en-GB' || voice.lang === 'en_GB');
            }
            if (!preferredVoice) {
                preferredVoice = availableVoices.find(voice => voice.lang.includes('en'));
            }

            if (preferredVoice) utterance.voice = preferredVoice;
        }
        
        // Áp dụng tốc độ
        utterance.rate = readingRate; 
        utterance.pitch = 1.0;
        utterance.volume = 1.0;

        utterance.onerror = (e) => console.log('Speech error:', e);
        window.speechSynthesis.speak(utterance);
    }

    // --- SETTINGS FUNCTIONS ---
    function toggleSettings() {
        const isHidden = elements.settingsModal.style.display === 'none' || elements.settingsModal.style.display === '';
        if (isHidden) {
            elements.settingsModal.style.display = 'flex';
            // Refresh voice list in case it wasn't loaded
            if(availableVoices.length === 0) loadVoices();
        } else {
            elements.settingsModal.style.display = 'none';
        }
    }

    function updateVoiceSettings() {
        selectedVoiceIndex = parseInt(elements.voiceSelect.value);
        // Lưu ý: Không cần lưu localStorage vì đề bài không yêu cầu, 
        // nhưng biến selectedVoiceIndex là toàn cục nên sẽ áp dụng cho mọi từ.
    }

    function updateSpeedSettings() {
        readingRate = parseFloat(elements.speedRange.value);
        elements.speedDisplay.innerText = readingRate;
    }
    
    function testVoice() {
        playAudio("Hello, this is a test for English voice.");
    }

    // --- OTHER LOGIC ---
    function shuffleVocabulary() {
        for (let i = vocabularyList.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [vocabularyList[i], vocabularyList[j]] = [vocabularyList[j], vocabularyList[i]];
        }
        currentIndex = 0;
        loadCard(0);
        elements.statusMsg.innerText = "🔀 Đã đảo thứ tự từ vựng!";
        setTimeout(() => elements.statusMsg.innerText = "", 2000);
    }

    function loadCard(index) {
        if (index < 0) currentIndex = vocabularyList.length - 1;
        else if (index >= vocabularyList.length) currentIndex = 0;
        else currentIndex = index;

        const item = vocabularyList[currentIndex];

        elements.vnText.innerText = item.vi;
        elements.enText.innerText = item.en;
        elements.posText.innerText = item.pos;
        
        // Cập nhật IPA
        if (item.ipa) {
            elements.ipaText.innerText = item.ipa;
            elements.ipaText.style.display = 'block';
        } else {
            elements.ipaText.style.display = 'none';
        }
        
        elements.answerArea.style.display = 'none';
        elements.reviewActions.style.display = 'none';
        elements.btnReveal.style.display = 'block';
        elements.btnReveal.disabled = false;
        elements.btnReveal.innerText = "XEM ĐÁP ÁN";
        elements.statusMsg.innerText = "";
        
        elements.progress.innerText = `CÂU ${currentIndex + 1} / ${vocabularyList.length}`;
        updateStatusBadge(item.status);
        
        isRevealed = false;
    }

    function updateStatusBadge(status) {
        elements.currentStatus.className = 'status-badge';
        if (status === 'learned') {
            elements.currentStatus.innerText = "Đã thuộc";
            elements.currentStatus.classList.add('status-learned');
        } else if (status === 'learning') {
            elements.currentStatus.innerText = "Chưa thuộc";
            elements.currentStatus.classList.add('status-learning');
        } else {
            elements.currentStatus.innerText = "Mới";
            elements.currentStatus.classList.add('status-new');
        }
    }

    function revealAnswer() {
        isRevealed = true;
        elements.btnReveal.disabled = true;
        elements.answerArea.style.display = 'block';
        playAudio(vocabularyList[currentIndex].en);
        elements.btnReveal.style.display = 'none'; 
        elements.reviewActions.style.display = 'flex'; 
    }

    function playCurrentAudio() {
        playAudio(vocabularyList[currentIndex].en);
    }

    function markStatus(status) {
        vocabularyList[currentIndex].status = status;
        updateStatusBadge(status);
        setTimeout(() => { changeCard(1); }, 300);
    }

    function changeCard(step) {
        loadCard(currentIndex + step);
    }

    function toggleList() {
        const isHidden = elements.listModal.style.display === 'none' || elements.listModal.style.display === '';
        if (isHidden) {
            renderList();
            elements.listModal.style.display = 'flex';
        } else {
            elements.listModal.style.display = 'none';
        }
    }

    function renderList() {
        elements.listContent.innerHTML = '';
        vocabularyList.forEach((item, index) => {
            const div = document.createElement('div');
            div.className = `list-item ${index === currentIndex ? 'active' : ''}`;
            let statusIcon = '⚪';
            if (item.status === 'learned') statusIcon = '✅';
            if (item.status === 'learning') statusIcon = '🔸';
            div.innerHTML = `<div style="display:flex; align-items:center;"><span style="margin-right:8px; font-size: 12px;">${statusIcon}</span><strong>${item.en}</strong></div><div style="font-size:12px; color:#666;">${index + 1}</div>`;
            div.onclick = () => { currentIndex = index; loadCard(currentIndex); toggleList(); };
            elements.listContent.appendChild(div);
        });
    }

    function toggleStats() {
        const isHidden = elements.statsModal.style.display === 'none' || elements.statsModal.style.display === '';
        if (isHidden) { renderStats(); elements.statsModal.style.display = 'flex'; } else { elements.statsModal.style.display = 'none'; }
    }

    function renderStats() {
        const learnedCount = vocabularyList.filter(i => i.status === 'learned').length;
        const learningCount = vocabularyList.filter(i => i.status === 'learning').length;
        const newCount = vocabularyList.filter(i => i.status === 'new').length;
        elements.statLearned.innerText = learnedCount;
        elements.statLearning.innerText = learningCount;
        elements.statNew.innerText = newCount;
        let recommendItems = vocabularyList.map((item, index) => ({ ...item, originalIndex: index })).filter(i => i.status === 'learning');
        elements.recommendList.innerHTML = '';
        if (recommendItems.length === 0) {
            const newItems = vocabularyList.map((item, index) => ({ ...item, originalIndex: index })).filter(i => i.status === 'new').slice(0, 5);
            if (newItems.length > 0) {
                elements.recommendList.innerHTML = '<div style="color:#777; font-style:italic; padding:10px;">Bạn đã thuộc hết các từ cần ôn. Hãy học từ mới:</div>';
                newItems.forEach(item => createRecommendItem(item));
            } else {
                elements.recommendList.innerHTML = '<div style="color:green; padding:10px; text-align:center;">🎉 Tuyệt vời! Bạn đã thuộc hết toàn bộ danh sách.</div>';
            }
        } else {
            recommendItems.forEach(item => createRecommendItem(item));
        }
    }

    function createRecommendItem(item) {
        const div = document.createElement('div');
        div.className = 'recommend-item';
        div.innerHTML = `🔸 <strong>${item.en}</strong> <span style="font-size:12px; color:#999;">(${item.vi})</span>`;
        div.onclick = () => { currentIndex = item.originalIndex; loadCard(currentIndex); toggleStats(); };
        elements.recommendList.appendChild(div);
    }

    loadCard(0);
</script>

</body>
</html>
