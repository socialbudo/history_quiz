<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>한국사 연도 마스터 퀴즈</title>
    <style>
        body {
            font-family: 'Apple SD Gothic Neo', 'Malgun Gothic', sans-serif;
            background-color: #f4f7f6;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 600px;
        }
        h2 { text-align: center; color: #333; margin-bottom: 20px; }
        .filter-section {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        .filter-section label {
            margin-right: 15px;
            font-weight: bold;
            cursor: pointer;
        }
        .mode-select {
            margin-top: 10px;
            padding-top: 10px;
            border-top: 1px dashed #ddd;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 6px;
            cursor: pointer;
            width: 100%;
            margin-top: 10px;
        }
        button:hover { background-color: #45a049; }
        .btn-secondary {
            background-color: #7f8c8d;
        }
        .btn-secondary:hover {
            background-color: #6c7a89;
        }
        .btn-danger {
            background-color: #e74c3c;
        }
        .btn-danger:hover {
            background-color: #c0392b;
        }
        .quiz-box {
            margin-top: 20px;
            padding: 20px;
            border: 2px dashed #ddd;
            border-radius: 8px;
            text-align: center;
            display: none;
        }
        .counter-badge {
            font-size: 14px;
            font-weight: bold;
            color: #2980b9;
            margin-bottom: 10px;
        }
        .event-text {
            font-size: 20px;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 20px;
            min-height: 60px;
        }
        input[type="number"] {
            padding: 10px;
            font-size: 16px;
            width: 50%;
            border: 1px solid #ccc;
            border-radius: 4px;
            text-align: center;
        }
        .result {
            margin-top: 15px;
            font-size: 18px;
            font-weight: bold;
        }
        .correct { color: #27ae60; }
        .wrong { color: #c0392b; }
        .hidden-answer {
            font-size: 24px;
            color: #e67e22;
            margin-bottom: 15px;
            display: none;
        }
        .nav-buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            gap: 10px;
        }
        .nav-buttons button {
            margin-top: 0;
            width: 50%;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>🇰🇷 한국사 연도 마스터 퀴즈</h2>
    
    <div class="filter-section" id="filterSection">
        <p><strong>📌 시대 선택:</strong></p>
        <label><input type="checkbox" name="era" value="191" checked> 1910년대</label>
        <label><input type="checkbox" name="era" value="192" checked> 1920년대</label>
        <label><input type="checkbox" name="era" value="193" checked> 1930년대</label>
        
        <p style="margin-top: 10px;"><strong>📌 영역 선택:</strong></p>
        <label><input type="checkbox" name="cat" value="국내외 독립 운동" checked> 국내외 독립 운동</label>
        <label><input type="checkbox" name="cat" value="세계사 및 국제 정세" checked> 세계사 및 국제 정세</label>
        
        <div class="mode-select">
            <p><strong>📌 학습 모드 선택:</strong></p>
            <label><input type="radio" name="gameMode" value="input" checked> 연도 직접 입력 모드</label>
            <label><input type="radio" name="gameMode" value="card"> 카드 뒤집기(정답 보기) 모드</label>
        </div>
        
        <button onclick="initQuizSession()">퀴즈 시작하기</button>
    </div>

    <div class="quiz-box" id="quizContainer">
        <div class="counter-badge" id="counterBadge">1 / 10</div>
        <div id="categoryBadge" style="font-size: 12px; color: #7f8c8d; margin-bottom: 5px;"></div>
        <div class="event-text" id="eventDescription">여기에 사건이 나옵니다.</div>
        
        <!-- 입력 모드용 영역 -->
        <div id="inputModeArea">
            <input type="number" id="userYear" placeholder="연도 입력 (예: 1920)">
            <button onclick="checkAnswer()" style="width: auto; display: inline-block; padding: 10px 15px; margin-left: 5px;">정답 확인</button>
        </div>
        
        <!-- 카드 뒤집기 모드용 영역 -->
        <div id="cardModeArea" style="display:none;">
            <div class="hidden-answer" id="hiddenYearDisplay">???</div>
            <button class="btn-secondary" onclick="revealCard()" id="revealBtn">정답 보기</button>
        </div>
        
        <div class="result" id="resultMessage"></div>
        
        <!-- 이전 / 다음 문제 이동 버튼 (답 입력 없어도 이동 가능) -->
        <div class="nav-buttons">
            <button class="btn-secondary" onclick="prevQuestion()">⬅️ 이전 문제</button>
            <button onclick="nextQuestion()">다음 문제 ➡️</button>
        </div>

        <!-- 초기화 및 처음으로 돌아가기 버튼 -->
        <button class="btn-danger" onclick="resetToMenu()">처음 메뉴로 돌아가기 (초기화)</button>
    </div>
</div>

<script>
    // 원본 이미지 연표와 정확히 일치하도록 수정한 전체 데이터셋
    const historyData = [
        // 1910년대
        { year: "1910", cat: "국내외 독립 운동", text: "국권 피탈" },
        { year: "1910", cat: "국내외 독립 운동", text: "조선 총독부 설치" },
        { year: "1910", cat: "국내외 독립 운동", text: "임시 토지 조사국 설치" },
        { year: "1910", cat: "국내외 독립 운동", text: "범죄 즉결례 제정" },
        { year: "1910", cat: "국내외 독립 운동", text: "회사령 제정" },
        { year: "1911", cat: "국내외 독립 운동", text: "어업령 제정" },
        { year: "1911", cat: "국내외 독립 운동", text: "북간도 중광단 조직" },
        { year: "1911", cat: "국내외 독립 운동", text: "105인 사건" },
        { year: "1911", cat: "국내외 독립 운동", text: "서간도 신흥 강습소(신흥무관학교) 설립" },
        { year: "1912", cat: "국내외 독립 운동", text: "조선 태형령 및 경찰범 처벌 규칙 제정" },
        { year: "1912", cat: "국내외 독립 운동", text: "토지 조사령 공포" },
        { year: "1912", cat: "국내외 독립 운동", text: "임병찬, 독립 의군부 조직" },
        { year: "1913", cat: "국내외 독립 운동", text: "송죽회 결성" },
        { year: "1914", cat: "국내외 독립 운동", text: "연해주, 대한 광복군 정부 조직" },
        { year: "1914", cat: "세계사 및 국제 정세", text: "제1차 세계대전 발발" },
        { year: "1915", cat: "국내외 독립 운동", text: "조선 광업령 제정" },
        { year: "1915", cat: "국내외 독립 운동", text: "박상진, 대구에서 대한 광복회 조직" },
        { year: "1915", cat: "세계사 및 국제 정세", text: "일본, 중국에게 21개조 요구 강요" },
        { year: "1917", cat: "세계사 및 국제 정세", text: "러시아 혁명 발생" },
        { year: "1918", cat: "세계사 및 국제 정세", text: "제1차 세계대전 종전" },
        { year: "1919", cat: "국내외 독립 운동", text: "고종 사망" },
        { year: "1919", cat: "국내외 독립 운동", text: "2·8 독립 선언" },
        { year: "1919", cat: "국내외 독립 운동", text: "연해주 대한 국민 의회 설립" },
        { year: "1919", cat: "국내외 독립 운동", text: "3·1 운동 발생" },
        { year: "1919", cat: "국내외 독립 운동", text: "화성 제암리 학살 사건" },
        { year: "1919", cat: "국내외 독립 운동", text: "대한민국 임시정부(상하이) 설립" },
        { year: "1919", cat: "국내외 독립 운동", text: "한성 정부(경성) 설립" },
        { year: "1919", cat: "국내외 독립 운동", text: "대한민국 임시정부 통합" },
        { year: "1919", cat: "국내외 독립 운동", text: "강우규 의거" },
        { year: "1919", cat: "국내외 독립 운동", text: "김원봉 의열단 결성" },
        { year: "1919", cat: "세계사 및 국제 정세", text: "파리 강화 회의 개최" },
        { year: "1919", cat: "세계사 및 국제 정세", text: "중국 5·4 운동" },

        // 1920년대
        { year: "1920", cat: "국내외 독립 운동", text: "《동아일보》, 《조선일보》 창간" },
        { year: "1920", cat: "국내외 독립 운동", text: "산미증식계획 실시, 회사령 폐지" },
        { year: "1920", cat: "국내외 독립 운동", text: "조선 물산 장려회 조직" },
        { year: "1920", cat: "국내외 독립 운동", text: "봉오동 전투 승리" },
        { year: "1920", cat: "국내외 독립 운동", text: "청산리 전투 승리" },
        { year: "1920", cat: "국내외 독립 운동", text: "간도 참변 발생" },
        { year: "1920", cat: "국내외 독립 운동", text: "대한 독립 군단 창설" },
        { year: "1921", cat: "국내외 독립 운동", text: "자유시 참변 발생" },
        { year: "1921", cat: "국내외 독립 운동", text: "김익상 의거" },
        { year: "1921", cat: "국내외 독립 운동", text: "부산 부두 노동자 총파업" },
        { year: "1921", cat: "세계사 및 국제 정세", text: "워싱턴 회의 개최" },
        { year: "1922", cat: "국내외 독립 운동", text: "조선 민립 대학 기성회 조직" },
        { year: "1922", cat: "세계사 및 국제 정세", text: "소비에트 사회주의 공화국 연방(소련) 수립" },
        { year: "1923", cat: "국내외 독립 운동", text: "일본 상품 관세 철폐" },
        { year: "1923", cat: "국내외 독립 운동", text: "관동 대지진 발생" },
        { year: "1923", cat: "국내외 독립 운동", text: "국민 대표 회의 실시" },
        { year: "1923", cat: "국내외 독립 운동", text: "김상옥 의거" },
        { year: "1923", cat: "국내외 독립 운동", text: "암태도 소작 쟁의 발생" },
        { year: "1924", cat: "국내외 독립 운동", text: "경성제국대학 설립" },
        { year: "1925", cat: "국내외 독립 운동", text: "조선공산당 결성" },
        { year: "1925", cat: "국내외 독립 운동", text: "박은식 임시 대통령 취임" },
        { year: "1925", cat: "국내외 독립 운동", text: "미쓰야 협정 체결" },
        { year: "1925", cat: "국내외 독립 운동", text: "남자현 의거" },
        { year: "1925", cat: "세계사 및 국제 정세", text: "치안 유지법 제정" },
        { year: "1926", cat: "국내외 독립 운동", text: "순종 사망" },
        { year: "1926", cat: "국내외 독립 운동", text: "6·10 만세 운동 발생" },
        { year: "1926", cat: "국내외 독립 운동", text: "조선 민흥회 결성" },
        { year: "1926", cat: "국내외 독립 운동", text: "정우회 선언 발표" },
        { year: "1926", cat: "국내외 독립 운동", text: "나석주 의거" },
        { year: "1927", cat: "국내외 독립 운동", text: "신간회 결성" },
        { year: "1927", cat: "국내외 독립 운동", text: "조선 농민 총동맹 결성" },
        { year: "1929", cat: "국내외 독립 운동", text: "광주 학생 항일 운동 발생" },
        { year: "1929", cat: "국내외 독립 운동", text: "원산 총파업 발생" },
        { year: "1929", cat: "세계사 및 국제 정세", text: "대공황 발생" },

        // 1930년대 (이미지 기준 한인애국단은 1931년!)
        { year: "1931", cat: "국내외 독립 운동", text: "한인 애국단 결성" }, //[span_1](start_span)[span_1](end_span) 수정 완료
        { year: "1931", cat: "국내외 독립 운동", text: "신간회 해소" },
        { year: "1931", cat: "국내외 독립 운동", text: "평원 고무 공장 여직공 파업(을밀대 고공농성)" },
        { year: "1931", cat: "세계사 및 국제 정세", text: "만보산 사건 발생" },
        { year: "1931", cat: "세계사 및 국제 정세", text: "만주사변 발생" },
        { year: "1932", cat: "국내외 독립 운동", text: "이봉창 의거" },
        { year: "1932", cat: "국내외 독립 운동", text: "윤봉길 의거" },
        { year: "1932", cat: "국내외 독립 운동", text: "조선 혁명 간부학교 설립" },
        { year: "1937", cat: "세계사 및 국제 정세", text: "연해주 한인 강제 이주" },
        { year: "1937", cat: "세계사 및 국제 정세", text: "중일 전쟁 발발" }
    ];

    let currentSessionList = [];
    let currentIndex = 0;
    let gameMode = "input";

    function initQuizSession() {
        const selectedEras = Array.from(document.querySelectorAll('input[name="era"]:checked')).map(el => el.value);
        const selectedCats = Array.from(document.querySelectorAll('input[name="cat"]:checked')).map(el => el.value);
        gameMode = document.querySelector('input[name="gameMode"]:checked').value;

        if (selectedEras.length === 0 || selectedCats.length === 0) {
            alert("시대와 영역을 최소 하나 이상 선택해주세요!");
            return;
        }

        const filtered = historyData.filter(item => {
            const eraMatch = selectedEras.some(era => item.year.startsWith(era));
            const catMatch = selectedCats.includes(item.cat);
            return eraMatch && catMatch;
        });

        if (filtered.length === 0) {
            alert("선택한 조건에 해당하는 사건이 없습니다!");
            return;
        }

        currentSessionList = shuffleArray([...filtered]);
        currentIndex = 0;

        document.getElementById("filterSection").style.display = "none";
        document.getElementById("quizContainer").style.display = "block";

        renderQuestion();
    }

    function shuffleArray(array) {
        for (let i = array.length - 1; i > 0; i--) {
            const j = Math.floor(Math.random() * (i + 1));
            [array[i], array[j]] = [array[j], array[i]];
        }
        return array;
    }

    function renderQuestion() {
        const item = currentSessionList[currentIndex];

        document.getElementById("counterBadge").innerText = `${currentIndex + 1} / ${currentSessionList.length}`;
        document.getElementById("categoryBadge").innerText = `[${item.cat}]`;
        document.getElementById("eventDescription").innerText = item.text;
        document.getElementById("resultMessage").innerText = "";

        if (gameMode === "input") {
            document.getElementById("inputModeArea").style.display = "block";
            document.getElementById("cardModeArea").style.display = "none";
            document.getElementById("userYear").value = "";
        } else {
            document.getElementById("inputModeArea").style.display = "none";
            document.getElementById("cardModeArea").style.display = "block";
            document.getElementById("hiddenYearDisplay").style.display = "none";
            document.getElementById("hiddenYearDisplay").innerText = `${item.year}년`;
            document.getElementById("revealBtn").style.display = "inline-block";
        }
    }

    function nextQuestion() {
        if (currentIndex < currentSessionList.length - 1) {
            currentIndex++;
            renderQuestion();
        } else {
            alert("마지막 문제입니다!");
        }
    }

    function prevQuestion() {
        if (currentIndex > 0) {
            currentIndex--;
            renderQuestion();
        } else {
            alert("첫 번째 문제입니다!");
        }
    }

    function checkAnswer() {
        const userVal = document.getElementById("userYear").value.trim();
        const msg = document.getElementById("resultMessage");
        const item = currentSessionList[currentIndex];

        if (!userVal) {
            alert("연도를 입력해주세요!");
            return;
        }

        if (userVal === item.year) {
            msg.innerHTML = `<span class="correct">정답입니다! 🎉 (연도: ${item.year}년)</span>`;
        } else {
            msg.innerHTML = `<span class="wrong">틀렸습니다! 🥲 정답은 ${item.year}년 입니다.</span>`;
        }
    }

    function revealCard() {
        const item = currentSessionList[currentIndex];
        document.getElementById("hiddenYearDisplay").innerText = `${item.year}년`;
        document.getElementById("hiddenYearDisplay").style.display = "block";
        document.getElementById("revealBtn").style.display = "none";
    }

    function resetToMenu() {
        document.getElementById("quizContainer").style.display = "none";
        document.getElementById("filterSection").style.display = "block";
    }
</script>

</body>
</html>
