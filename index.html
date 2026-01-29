<!DOCTYPE html>
<html lang="si">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chemistry Smart Learner Pro</title>
    <style>
        :root {
            --bg: #0a0a0a;
            --card: #161616;
            --primary: #3498db;
            --success: #2ecc71;
            --error: #e74c3c;
            --text: #ffffff;
            --text-dim: #b0b0b0;
            --opt-bg: #222222;
        }

        body { font-family: 'Segoe UI', sans-serif; background: var(--bg); color: var(--text); margin: 0; padding: 20px; display: flex; justify-content: center; }
        .container { width: 100%; max-width: 850px; }
        .step { display: none; background: var(--card); padding: 35px; border-radius: 20px; box-shadow: 0 15px 40px rgba(0,0,0,0.6); }
        .active { display: block; }

        /* Navigation Buttons */
        .btn-row { display: flex; gap: 15px; margin-top: 30px; }
        .btn-next { background: var(--primary); color: white; border: none; padding: 14px 30px; border-radius: 12px; cursor: pointer; flex: 2; font-weight: bold; font-size: 16px; }
        .btn-back { background: #27ae60; color: white; border: none; padding: 14px 30px; border-radius: 12px; cursor: pointer; flex: 1; font-weight: bold; font-size: 16px; }

        /* Selection UI */
        .option-card { background: #222; border: 2px solid #333; padding: 20px; margin: 12px 0; border-radius: 12px; cursor: pointer; transition: 0.3s; }
        .option-card:hover { border-color: var(--primary); background: #282828; }
        input, select { width: 100%; padding: 15px; border-radius: 10px; border: 1px solid #444; background: #222; color: white; font-size: 16px; margin-top: 15px; }

        /* Quiz UI */
        .header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; }
        .progress-bar { flex-grow: 1; height: 5px; background: #333; margin: 0 20px; border-radius: 3px; position: relative; }
        .progress-fill { height: 100%; background: var(--primary); width: 0%; border-radius: 3px; transition: 0.5s; }
        .score-pill { padding: 5px 15px; border-radius: 20px; font-weight: bold; font-size: 0.9em; margin-left: 8px; }
        .s-wrong { background: rgba(231, 76, 60, 0.2); color: var(--error); border: 1px solid var(--error); }
        .s-right { background: rgba(46, 204, 113, 0.2); color: var(--success); border: 1px solid var(--success); }

        .q-text { font-size: 1.4em; margin-bottom: 30px; line-height: 1.6; }
        .mcq-opt { background: var(--opt-bg); padding: 18px; border-radius: 12px; cursor: pointer; margin-bottom: 15px; border: 1px solid transparent; transition: 0.2s; }
        .correct-final { border-color: var(--success) !important; background: rgba(46, 204, 113, 0.05) !important; }
        .wrong-final { border-color: var(--error) !important; background: rgba(231, 76, 60, 0.05) !important; }

        .fb-tag { font-size: 0.9em; font-weight: bold; margin-top: 10px; display: flex; align-items: center; gap: 8px; }
        .exp-text { font-size: 0.95em; color: var(--text-dim); margin-top: 6px; line-height: 1.5; }

        .hint-section { background: #222; padding: 15px; border-radius: 10px; border-left: 4px solid #f1c40f; margin: 25px 0; display: none; }
    </style>
</head>
<body>

<div class="container">
    <div id="step1" class="step active">
        <h2>පියවර 1: විෂය තෝරන්න</h2>
        <div class="option-card" onclick="goToStep(2)">රසායන විද්‍යාව (Chemistry)</div>
        <div class="option-card" style="opacity: 0.4; cursor: not-allowed;">භෞතික විද්‍යාව (ළඟදීම)</div>
    </div>

    <div id="step2" class="step">
        <h2>පියවර 2: කාල රාමුව</h2>
        <p>විභාගයට තව දින කීයක් ඉතිරිව තිබේද?</p>
        <input type="number" id="daysInput" placeholder="උදා: 100">
        <div class="btn-row">
            <button class="btn-back" onclick="goToStep(1)">Back</button>
            <button class="btn-next" onclick="goToStep(3)">Next</button>
        </div>
    </div>

    <div id="step3" class="step">
        <h2>පියවර 3: රසායන විද්‍යා අංශය</h2>
        <select id="branchSelect">
            <option value="general">සාමාන්‍ය රසායනය (General)</option>
            <option value="inorganic">අකාබනික රසායනය (Inorganic)</option>
            <option value="physical">භෞතික රසායනය (Physical)</option>
            <option value="organic">කාබනික රසායනය (Organic)</option>
        </select>
        <div class="btn-row">
            <button class="btn-back" onclick="goToStep(2)">Back</button>
            <button class="btn-next" onclick="showPlanner()">වැඩපිළිවෙල පෙන්වන්න</button>
        </div>
    </div>

    <div id="step4" class="step">
        <h2>ඔබේ ඉලක්කය</h2>
        <div id="plannerResult" style="text-align:center; font-size: 1.3em; padding: 30px; border: 1px dashed var(--primary); border-radius: 15px;"></div>
        <div class="btn-row">
            <button class="btn-back" onclick="goToStep(3)">සංස්කරණය</button>
            <button class="btn-next" onclick="startQuiz()">MCQ ආරම්භ කරන්න</button>
        </div>
    </div>

    <div id="quizStep" class="step">
        <div class="header">
            <span id="qInfo" style="color: var(--text-dim);">1 / 1</span>
            <div class="progress-bar"><div class="progress-fill" id="pFill"></div></div>
            <div style="display:flex;">
                <div class="score-pill s-wrong">✕ <span id="wScore">0</span></div>
                <div class="score-pill s-right">✓ <span id="rScore">0</span></div>
            </div>
        </div>

        <div id="qDisplay" class="q-text"></div>
        <div id="optionsDisplay"></div>

        <div id="hintBox" class="hint-section"></div>

        <div class="btn-row" style="justify-content: flex-end;">
            <button onclick="toggleHint()" style="background:none; border:none; color:var(--primary); cursor:pointer; font-weight:bold;">Show hint ⌃</button>
            <button id="doneBtn" class="btn-next" style="display:none; flex:unset; padding: 10px 40px; border-radius: 25px;" onclick="nextQuestion()">Done</button>
        </div>
    </div>
</div>

<script>
    const questionsDB = {
        "general": [{
            q: "5. ක්වොන්ටම් අංක කට්ටලයක් පිළිබඳ පහත සඳහන් කුමන ප්‍රකාශය වැරදිද?",
            o: ["ms සඳහා +1/2 හෝ -1/2 යන අගයන් තිබිය හැක.", "l හි අගය සැමවිටම n ට වඩා කුඩා විය යුතුය.", "n = 3 විට l සඳහා විය හැකි අගයන් වන්නේ 0, 1, 2 ය.", "ml මගින් කාක්ෂිකයේ හැඩය තීරණය කරයි."],
            c: 3, h: "කාක්ෂිකයක හැඩය සහ දිශානතිය තීරණය කරන අංක සිහිපත් කරන්න.",
            exps: ["ms අගය භ්‍රමණය පෙන්වන අතර එය සැමවිටම +1/2 හෝ -1/2 වේ.", "l අගය 0 සිට n-1 දක්වා පරාසයක පවතින බැවින් එය සැමවිටම n ට වඩා කුඩාය.", "l අගය 0 සිට n-1 දක්වා වන බැවින් n=3 විට 0, 1, 2 (s,p,d) නිවැරදිය.", "කාක්ෂිකයේ හැඩය තීරණය කරන්නේ l අගයයි. ml මගින් දිශානතිය පෙන්වයි."]
        }],
        "inorganic": [{
            q: "වාතයේ වැඩිපුරම අඩංගු වායුව කුමක්ද?",
            o: ["ඔක්සිජන්", "හයිඩ්‍රජන්", "නයිට්‍රජන්", "ආගන්"],
            c: 2, h: "වායුගෝලීය සංයුතිය ගැන සිතන්න.",
            exps: ["ඔක්සිජන් වාතයේ 21% ක් පමණ අඩංගු වේ.", "හයිඩ්‍රජන් වාතයේ ඇත්තේ ඉතා අල්ප වශයෙනි.", "වාතයෙන් 78% ක්ම නයිට්‍රජන් වායුව අඩංගු බැවින් මෙය නිවැරදි පිළිතුරයි.", "ආගන් යනු වාතයේ ඇති උදාසීන වායුවකි (0.9% පමණ)."]
        }],
        "physical": [{
            q: "පද්ධතියක එන්තැල්පි වෙනස (ΔH) ධන අගයක් ගන්නේ නම් එය?",
            o: ["තාපදායක ප්‍රතික්‍රියාවකි", "තාප අවශෝෂක ප්‍රතික්‍රියාවකි", "සමතාපී ප්‍රතික්‍රියාවකි", "කිසිවක් නොවේ"],
            c: 1, h: "තාපය පිටකිරීම සහ ලබාගැනීම අතර වෙනස සලකන්න.",
            exps: ["තාපදායක ප්‍රතික්‍රියාවක ΔH අගය සෘණ වේ.", "තාපය අවශෝෂණය කරන විට පද්ධතියේ ශක්තිය වැඩි වන බැවින් ΔH ධන වේ.", "සමතාපී ප්‍රතික්‍රියාවක උෂ්ණත්වය වෙනස් නොවේ.", "නිවැරදි පිළිතුර B වේ."]
        }],
        "organic": [{
            q: "පහත ඒවායින් ඇල්කයින වල පොදු සූත්‍රය කුමක්ද?",
            o: ["CnH2n+2", "CnH2n", "CnH2n-2", "CnHn"],
            c: 2, h: "ත්‍රිත්ව බන්ධන සහිත හයිඩ්‍රොකාබන වල සූත්‍රය.",
            exps: ["මෙය ඇල්කේන වල පොදු සූත්‍රයයි.", "මෙය ඇල්කීන වල පොදු සූත්‍රයයි.", "ත්‍රිත්ව බන්ධනයක් සෑදීමට හයිඩ්‍රජන් පරමාණු 4ක් ඉවත් වන බැවින් CnH2n-2 නිවැරදිය.", "මෙය පොදු සූත්‍රයක් ලෙස භාවිත නොවේ."]
        }]
    };

    let currentIdx = 0;
    let rScore = 0, wScore = 0;
    let activeList = [];

    function goToStep(s) {
        document.querySelectorAll('.step').forEach(el => el.classList.remove('active'));
        document.getElementById(s === 'quizStep' ? 'quizStep' : 'step' + s).classList.add('active');
    }

    function showPlanner() {
        let days = document.getElementById('daysInput').value;
        if(!days || days < 1) return alert("කරුණාකර දින ගණන ඇතුළත් කරන්න.");
        let daily = Math.ceil(15330 / days);
        document.getElementById('plannerResult').innerHTML = `විභාගය ජය ගැනීමට නම් ඔබ<br><span style="font-size: 1.8em; color:var(--success); font-weight:bold;">දිනකට MCQ ${daily} බැගින්</span><br>කළ යුතුය.`;
        goToStep(4);
    }

    function startQuiz() {
        let branch = document.getElementById('branchSelect').value;
        activeList = questionsDB[branch];
        currentIdx = 0; rScore = 0; wScore = 0;
        updateScoreBoard();
        loadQuestion();
        goToStep('quizStep');
    }

    function loadQuestion() {
        let q = activeList[currentIdx];
        document.getElementById('qDisplay').innerText = q.q;
        document.getElementById('qInfo').innerText = `${currentIdx + 1} / ${activeList.length}`;
        document.getElementById('pFill').style.width = `${((currentIdx + 1)/activeList.length)*100}%`;
        document.getElementById('hintBox').innerHTML = `💡 ${q.h}`;
        document.getElementById('hintBox').style.display = 'none';
        document.getElementById('doneBtn').style.display = 'none';

        let container = document.getElementById('optionsDisplay');
        container.innerHTML = "";
        let lbls = ['A.', 'B.', 'C.', 'D.'];

        q.o.forEach((opt, i) => {
            let div = document.createElement('div');
            div.className = 'mcq-opt';
            div.id = 'opt-' + i;
            div.innerHTML = `<b>${lbls[i]}</b> ${opt} <div id="fb-${i}"></div>`;
            div.onclick = () => handleCheck(i);
            container.appendChild(div);
        });
    }

    function handleCheck(selected) {
        let q = activeList[currentIdx];
        document.querySelectorAll('.mcq-opt').forEach(el => el.style.pointerEvents = 'none');

        q.o.forEach((_, i) => {
            let el = document.getElementById('opt-' + i);
            let fb = document.getElementById('fb-' + i);
            
            if(i === q.c) { // Correct Answer
                el.classList.add('correct-final');
                fb.innerHTML = `<div class="fb-tag" style="color:var(--success)">✓ Right answer</div><div class="exp-text">${q.exps[i]}</div>`;
            } else if(i === selected) { // User's Wrong Choice
                el.classList.add('wrong-final');
                fb.innerHTML = `<div class="fb-tag" style="color:var(--error)">✕ Not quite</div><div class="exp-text">${q.exps[i]}</div>`;
            } else { // Rationale for other options
                fb.innerHTML = `<div class="exp-text" style="margin-top:8px; border-top:1px solid #333; padding-top:5px;">${q.exps[i]}</div>`;
            }
        });

        if(selected === q.c) rScore++; else wScore++;
        updateScoreBoard();
        document.getElementById('doneBtn').style.display = 'block';
    }

    function updateScoreBoard() {
        document.getElementById('rScore').innerText = rScore;
        document.getElementById('wScore').innerText = wScore;
    }

    function toggleHint() {
        let h = document.getElementById('hintBox');
        h.style.display = (h.style.display === 'block') ? 'none' : 'block';
    }

    function nextQuestion() {
        currentIdx++;
        if(currentIdx < activeList.length) loadQuestion();
        else { alert("අද දින ඉලක්කය සාර්ථකයි!"); goToStep(1); }
    }
</script>

</body>
</html>
