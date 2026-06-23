<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal-Setting for ESL Lesson Design - Casa Thomas Jefferson</title>
    <style>
        *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
        :root {
            --bg: #ffffff;
            --bg2: #f5f5f4;
            --bg3: #e7e5e4;
            --text: #1c1917;
            --text2: #57534e;
            --text3: #a8a29e;
            --border: #e7e5e4;
            --border2: #d6d3d1;
            --radius-sm: 6px;
            --radius-md: 10px;
            --radius-lg: 14px;
            --blue: #185FA5;
            --blue-l: #E6F1FB;
            --blue-m: #378ADD;
            --teal: #0F6E56;
            --teal-l: #E1F5EE;
            --amber: #BA7517;
            --amber-l: #FAEEDA;
            --coral: #993C1D;
            --coral-l: #FAECE7;
            --green: #3B6D11;
            --green-l: #EAF3DE;
            --purple: #534AB7;
            --purple-l: #EEEDFE;
            --navy: #0C447C;
        }
        @media (prefers-color-scheme: dark) {
            :root {
                --bg: #1c1917; --bg2: #292524; --bg3: #3c3836;
                --text: #fafaf9; --text2: #a8a29e; --text3: #78716c;
                --border: #3c3836; --border2: #57534e;
            }
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background: var(--bg2);
            color: var(--text);
            min-height: 100vh;
            padding: 0;
        }
        .shell {
            max-width: 760px;
            margin: 0 auto;
            background: var(--bg);
            min-height: 100vh;
            padding: 0 0 4rem;
            box-shadow: 0 0 0 0.5px var(--border);
        }
        .topbar {
            background: var(--blue);
            color: #fff;
            padding: 1rem 1.5rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 1rem;
        }
        .topbar-title { font-size: 15px; font-weight: 600; letter-spacing: -0.01em; }
        .topbar-sub { font-size: 12px; opacity: 0.75; margin-top: 2px; }
        .ctj-badge {
            font-size: 11px; font-weight: 600; letter-spacing: 0.06em;
            background: rgba(255,255,255,0.18); color: #fff;
            padding: 4px 10px; border-radius: 20px; white-space: nowrap;
        }
        .phase-nav-wrap { padding: 1rem 1.5rem 0; }
        .phase-nav { display: flex; gap: 6px; margin-bottom: 0.5rem; }
        .phase-dot {
            flex: 1; height: 5px; border-radius: 3px;
            background: var(--border2); transition: background 0.3s;
        }
        .phase-dot.done { background: var(--teal); }
        .phase-dot.active { background: var(--blue-m); }
        .phase-labels { display: flex; justify-content: space-between; }
        .phase-label {
            font-size: 10px; color: var(--text3); flex: 1; text-align: center; cursor: default;
        }
        .phase-label.active { color: var(--blue-m); font-weight: 500; }
        .phase-label.done { color: var(--teal); }
        .content { padding: 1.5rem; }
        .phase-eyebrow {
            font-size: 11px; font-weight: 500; letter-spacing: 0.08em;
            text-transform: uppercase; color: var(--text3); margin-bottom: 4px;
        }
        .phase-title { font-size: 22px; font-weight: 600; margin-bottom: 6px; letter-spacing: -0.02em; }
        .phase-desc { font-size: 15px; color: var(--text2); line-height: 1.65; margin-bottom: 1.5rem; }
        .concept-card {
            background: var(--bg);
            border: 0.5px solid var(--border2);
            border-radius: var(--radius-lg);
            padding: 1.5rem;
            display: flex; flex-direction: column; gap: 1.25rem;
        }
        .card-top { display: flex; align-items: center; justify-content: space-between; }
        .pill {
            font-size: 11px; font-weight: 600; letter-spacing: 0.06em;
            text-transform: uppercase; padding: 4px 12px; border-radius: 20px;
        }
        .card-num { font-size: 12px; color: var(--text3); }
        .card-rule {
            font-size: 17px; font-weight: 600; line-height: 1.45;
            border-left: 3px solid var(--blue-m); padding-left: 12px;
            letter-spacing: -0.01em;
        }
        .card-tip { font-size: 14px; color: var(--text2); line-height: 1.7; }
        .ba-wrap { display: flex; flex-direction: column; gap: 6px; }
        .ba-block { border-radius: var(--radius-md); overflow: hidden; }
        .ba-label {
            font-size: 10px; font-weight: 600; text-transform: uppercase;
            letter-spacing: 0.07em; padding: 5px 12px;
        }
        .ba-text { font-size: 13px; font-style: italic; line-height: 1.6; padding: 9px 12px; }
        .ba-why { font-size: 12px; padding: 5px 12px 9px; border-top: 0.5px solid rgba(0,0,0,0.08); }
        .bad.ba-label { background: #FAECE7; color: #993C1D; }
        .bad.ba-text { background: #FAECE7; color: #712B13; }
        .bad.ba-why { background: #FAECE7; color: #993C1D; }
        .good.ba-label { background: #EAF3DE; color: #3B6D11; }
        .good.ba-text { background: #EAF3DE; color: #27500A; }
        .good.ba-why { background: #EAF3DE; color: #3B6D11; }
        .arrow-row { display: flex; align-items: center; gap: 8px; }
        .arrow-line { flex: 1; height: 0.5px; background: var(--border2); }
        .arrow-txt { font-size: 11px; color: var(--text3); white-space: nowrap; }
        .prog-wrap { height: 4px; background: var(--border2); border-radius: 2px; margin-top: 10px; }
        .prog-fill { height: 4px; background: var(--blue-m); border-radius: 2px; transition: width 0.3s; }
        .card-nav { display: flex; justify-content: space-between; align-items: center; margin-top: 1rem; }
        .card-counter { font-size: 13px; color: var(--text2); }
        .btn {
            display: inline-flex; align-items: center; gap: 6px;
            padding: 0.5rem 1.1rem;
            border-radius: var(--radius-md);
            font-size: 14px; font-weight: 500;
            cursor: pointer;
            border: 0.5px solid var(--border2);
            background: transparent; color: var(--text);
            transition: background 0.12s, color 0.12s;
            font-family: inherit;
        }
        .btn:hover { background: var(--bg2); }
        .btn:disabled { opacity: 0.4; cursor: default; }
        .btn-p { background: var(--blue); color: #fff; border-color: var(--blue); }
        .btn-p:hover { background: #0C447C; color: #fff; }
        .btn-sm { padding: 0.35rem 0.8rem; font-size: 13px; }
        .score-band {
            display: flex; align-items: center; justify-content: space-between;
            background: var(--bg2); border-radius: var(--radius-md);
            padding: 0.75rem 1rem; margin-bottom: 1.5rem; font-size: 14px;
        }
        .score-num { font-size: 20px; font-weight: 600; color: var(--blue); }
        .obj-card {
            background: var(--bg); border: 0.5px solid var(--border2);
            border-radius: var(--radius-lg); padding: 1.25rem 1.5rem; margin-bottom: 1rem;
        }
        .obj-meta { font-size: 12px; color: var(--text3); margin-bottom: 0.5rem; }
        .obj-text { font-size: 15px; line-height: 1.65; margin-bottom: 1rem; font-style: italic; }
        .rbtn-row { display: flex; gap: 12px; flex-wrap: wrap; }
        .rbtn {
            padding: 0.55rem 1.25rem; border-radius: 20px;
            font-size: 14px; font-weight: 500; border: 1.5px solid;
            cursor: pointer; background: transparent; transition: all 0.12s;
            font-family: inherit;
        }
        .rbtn.g { border-color: var(--green); color: var(--green); }
        .rbtn.g:hover, .rbtn.g.sel { background: var(--green-l); }
        .rbtn.m { border-color: var(--amber); color: var(--amber); }
        .rbtn.m:hover, .rbtn.m.sel { background: var(--amber-l); }
        .fb {
            margin-top: 1rem; padding: 1rem 1.25rem;
            border-radius: var(--radius-md); font-size: 14px; line-height: 1.6;
            border-left: 3px solid;
        }
        .fb-ok { background: var(--green-l); border-color: var(--green); color: #27500A; }
        .fb-no { background: var(--coral-l); border-color: var(--coral); color: #712B13; }
        .p3-progress { display: flex; align-items: center; gap: 10px; margin-bottom: 1.5rem; flex-wrap: wrap; }
        .p3-dots { display: flex; gap: 5px; flex-wrap: wrap; }
        .p3-dot {
            width: 28px; height: 28px; border-radius: 50%; border: 2px solid;
            display: flex; align-items: center; justify-content: center;
            font-size: 11px; font-weight: 600; transition: all 0.2s;
        }
        .p3-dot.pending { border-color: var(--border2); color: var(--text3); background: transparent; }
        .p3-dot.active { border-color: var(--blue); color: var(--blue); background: var(--blue-l); }
        .p3-dot.done { border-color: var(--teal); color: var(--teal); background: var(--teal-l); }
        .obj-box { background: var(--bg2); border-radius: var(--radius-md); padding: 1rem 1.25rem; margin-bottom: 1rem; }
        .obj-box-label { font-size: 11px; font-weight: 500; text-transform: uppercase; letter-spacing: 0.06em; color: var(--text3); margin-bottom: 6px; }
        .obj-box-badge { display: inline-flex; align-items: center; gap: 5px; font-size: 11px; font-weight: 600; padding: 3px 9px; border-radius: 20px; margin-bottom: 6px; }
        .badge-m { background: var(--amber-l); color: var(--amber); }
        .obj-box-text { font-size: 15px; font-style: italic; line-height: 1.6; }
        .chat-win { border: 0.5px solid var(--border2); border-radius: var(--radius-lg); overflow: hidden; display: flex; flex-direction: column; height: 420px; }
        .chat-hd { padding: 0.75rem 1rem; background: var(--blue); color: #fff; font-size: 14px; font-weight: 500; display: flex; align-items: center; gap: 8px; }
        .bdot { width: 8px; height: 8px; border-radius: 50%; background: #9fe1cb; }
        .chat-msgs { flex: 1; overflow-y: auto; padding: 1rem; display: flex; flex-direction: column; gap: 10px; background: var(--bg2); }
        .msg { max-width: 85%; font-size: 14px; line-height: 1.6; padding: 0.6rem 0.9rem; border-radius: 12px; white-space: pre-wrap; }
        .msg.bot { background: var(--bg); border: 0.5px solid var(--border2); align-self: flex-start; }
        .msg.user { background: var(--blue); color: #fff; align-self: flex-end; }
        
        /* Structured Feedback styling inside chat boxes */
        .feedback-block { margin-top: 5px; font-size: 13.5px; }
        .feedback-good { color: #27500A; background: #EAF3DE; border-left: 3px solid #3B6D11; padding: 6px 10px; border-radius: 4px; margin-bottom: 6px; }
        .feedback-missing { color: #712B13; background: #FAECE7; border-left: 3px solid #993C1D; padding: 6px 10px; border-radius: 4px; }

        .chat-ir { display: flex; gap: 8px; padding: 0.75rem; background: var(--bg); border-top: 0.5px solid var(--border2); }
        .chat-in { flex: 1; padding: 0.5rem 0.75rem; font-size: 14px; border: 0.5px solid var(--border2); border-radius: var(--radius-md); background: var(--bg2); color: var(--text); resize: none; font-family: inherit; }
        .chat-in:focus { outline: none; border-color: var(--blue-m); }
        .typ { font-size: 12px; color: var(--text3); padding: 0 1rem 0.5rem; background: var(--bg2); display: none; }
        .approved-bar { background: var(--green-l); padding: 0.75rem 1rem; font-size: 14px; color: #27500A; border-top: 0.5px solid #b2d89a; display: flex; align-items: center; justify-content: space-between; gap: 10px; flex-wrap: wrap; }
        .peer-card { background: var(--bg); border: 0.5px solid var(--border2); border-radius: var(--radius-lg); padding: 1.25rem 1.5rem; margin-bottom: 1rem; }
        .peer-hd { display: flex; align-items: center; gap: 10px; margin-bottom: 0.75rem; }
        .av { width: 36px; height: 36px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 13px; font-weight: 600; flex-shrink: 0; }
        .peer-obj { font-size: 14px; font-style: italic; line-height: 1.65; padding: 0.75rem; background: var(--bg2); border-radius: var(--radius-md); margin-bottom: 1rem; }
        .mv-row { display: flex; gap: 8px; margin-bottom: 0.75rem; flex-wrap: wrap; }
        .mvbtn { flex: 1; min-width: 100px; padding: 0.45rem 0.5rem; border-radius: var(--radius-md); font-size: 12px; font-weight: 500; border: 1.5px solid; cursor: pointer; background: transparent; text-align: center; transition: all 0.12s; font-family: inherit; }
        .mvbtn.q { border-color: var(--purple); color: var(--purple); }
        .mvbtn.q.sel, .mvbtn.q:hover { background: var(--purple-l); }
        .mvbtn.c { border-color: var(--blue); color: var(--blue); }
        .mvbtn.c.sel, .mvbtn.c:hover { background: var(--blue-l); }
        .mvbtn.s { border-color: var(--teal); color: var(--teal); }
        .mvbtn.s.sel, .mvbtn.s:hover { background: var(--teal-l); }
        .peer-ta { width: 100%; padding: 0.6rem 0.75rem; font-size: 14px; border: 0.5px solid var(--border2); border-radius: var(--radius-md); background: var(--bg2); color: var(--text); resize: vertical; min-height: 80px; font-family: inherit; margin-bottom: 0.75rem; }
        .peer-ta:focus { outline: none; border-color: var(--blue-m); }
        .sent-badge { display: inline-flex; align-items: center; gap: 5px; font-size: 12px; color: var(--green); background: var(--green-l); padding: 4px 10px; border-radius: 20px; }
        .stat-row { display: flex; gap: 12px; justify-content: center; margin: 1.5rem 0; flex-wrap: wrap; }
        .stat { background: var(--bg2); border-radius: var(--radius-md); padding: 0.75rem 12px; text-align: center; min-width: 110px; }
        .stat-v { font-size: 24px; font-weight: 600; color: var(--blue); }
        .stat-l { font-size: 12px; color: var(--text2); margin-top: 2px; }
        .divider { height: 0.5px; background: var(--border2); margin: 1.5rem 0; }
        .api-setup { background: var(--blue-l); border: 1px solid var(--blue-m); border-radius: var(--radius-lg); padding: 1.5rem; margin-bottom: 1.5rem; }
        .api-setup h3 { font-size: 16px; font-weight: 600; color: var(--navy); margin-bottom: 0.5rem; }
        .api-setup p { font-size: 13px; color: var(--navy); line-height: 1.6; margin-bottom: 1rem; }
        .api-input { width: 100%; padding: 0.5rem 0.75rem; font-size: 13px; border: 0.5px solid var(--blue-m); border-radius: var(--radius-md); background: var(--bg); color: var(--text); font-family: monospace; margin-bottom: 0.75rem; }
        .api-input:focus { outline: none; border-color: var(--blue); }
        .api-saved { color: var(--teal); font-size: 13px; font-weight: 500; display: none; }
        .move-legend { display: flex; gap: 8px; margin-bottom: 1.25rem; flex-wrap: wrap; }
        .move-legend-item { flex: 1; min-width: 130px; padding: 0.75rem; border-radius: var(--radius-md); font-size: 13px; }
        .move-legend-item strong { display: block; margin-bottom: 2px; }
    </style>
</head>
<body>
    <div class="shell">
        <div class="topbar">
            <div>
                <div class="topbar-title">Goal-Setting for ESL Lesson Design</div>
                <div class="topbar-sub">Professional Development Module • 5 Phases</div>
            </div>
            <div class="ctj-badge">CTJ</div>
        </div>
        <div class="phase-nav-wrap">
            <div class="phase-nav" id="pnav"></div>
            <div class="phase-labels">
                <span class="phase-label" id="pl1">Concepts</span>
                <span class="phase-label" id="pl2">Classify</span>
                <span class="phase-label" id="pl3">Rewrite</span>
                <span class="phase-label" id="pl4">Apply</span>
                <span class="phase-label" id="pl5">Exchange</span>
            </div>
        </div>
        <div class="content" id="root"></div>
    </div>

    <script>
        /* --- API KEY MANAGEMENT --- */
        function getKey(){ return sessionStorage.getItem('ctj_gemini_key') || ""; }
        function setKey(k){ sessionStorage.setItem('ctj_gemini_key', k.trim()); }

        /* --- CONFIG DATA --- */
        const CARDS=[
            {pill: 'Observable', pillBg: '#E6F1FB', pillC:'#185FA5', rule:'Use a verb that describes something you can see or hear.', tip:'If you can\'t watch a student doing it, you can\'t assess whether they learned it. Swap invisible words like "understand" or "know" for visible actions like "describe," "write," or "ask."', bad:'Students will understand the present perfect.', badWhy:'"Understand" is invisible; you can\'t watch it happen.', good:'Students will be able to describe three past experiences using the present perfect in a short speaking activity.', goodWhy: 'You can listen and assess whether they did this.'},
            {pill: 'Student-centered', pillBg: '#E1F5EE', pillC:'#0F6E56', rule: 'Write about what students do, not what you do.', tip: 'Check who is the subject of the sentence. If it\'s "I" or "the teacher," rewrite. A lesson objective describes a student behavior, not a teaching action.', bad:'I will explain the grammar rules for conditionals using examples.', badWhy:'The teacher is the subject. Students are invisible.', good:'Students will be able to use first conditional sentences to discuss real plans for the week.', goodWhy: 'Now the student is the actor. You can assess whether they succeeded.'},
            {pill:'Specific', pillBg: '#EEEDFE', pillC: '#534AB7', rule: 'Name the skill, the sub-skill, and the context.', tip: 'Vague objectives can\'t guide what you teach, what materials you choose, or how you assess. Push yourself to answer: What exactly will students do? With what language? In what situation?', bad:'Students will improve their speaking skills.', badWhy: 'Which aspect of speaking? In what situation? What counts as improvement?', good:'Students will be able to describe symptoms of an illness to a pharmacist using target medical vocabulary.', goodWhy: 'Skill, sub-skill, context, and language all named.'}
        ];

        // Adjusted structure to support a two-option state map: "Effective" (g) or "Missing something" (m)
        const OBJECTIVES=[
            {text:'By the end of the lesson, students will be able to talk about food.', level:'m', explanation:'This objective lacks parameters. "Talk about food" is unmeasurable and vague. It needs specific target forms and a real-world task context.'},
            {text:'Students will be able to distinguish between formal and informal register when making requests in a professional email context.', level:'g', explanation:'Excellent. This objective cleanly maps out student ownership, explicit context (professional email), and a clear language filter (register shifts).'},
            {text:'Students will learn about the difference between the Present Simple and Present Continuous.', level:'m', explanation:'"Learn about" reflects a classroom process or lecture approach rather than a tangible, observable student milestone.'},
            {text:'Students will be able to identify the main idea and two supporting details from an authentic podcast excerpt at B2 level.', level:'g', explanation:'Great structure. Highly specific, measurable via criteria (main idea + 2 details), and features an unambiguous observable condition.'}
        ];

        const PEERS=[
            {name:'Luísa A.', level:'Senior teacher, 8 years', ini:'LA', bg:'#E1F5EE', c:'#0F6E56', obj:'By the end of class, students will be able to construct a 90-second spoken narrative about a past professional challenge using narrative tenses and at least two cohesive adverbs.'},
            {name:'Thiago B.', level:'Trainee teacher, 2nd semester', ini:'TB', bg:'#FAEEDA', c:'#BA7517', obj:'Students will learn the difference between too, also, and as well and when to use them.'}
        ];

        /* --- STATE --- */
        let S = {
            ph: 1, ci: 0,
            p2a: {}, p2s: 0,
            p3weak: [], p3idx: 0, p3chats: {}, p3approved: {}, p3finished: false,
            c4: [], pm: {}, pt: {}, ps: {}, done: []
        };

        /* --- AI PROMPTS WITH HTML RESPONSE FORMAT RULES --- */
        const SYS_P3 = `You are Coach Alex, a helpful ELT development mentor at Casa Thomas Jefferson (CTJ).
The user is attempting to rewrite a weak lesson objective. Assess their proposal strictly against CTJ standards.
Your response MUST use the following raw HTML format structure to cleanly parse strengths and weaknesses:

🎉 A brief friendly opening comment here.

<div class="feedback-block">
  <div class="feedback-good"><strong>🟢 What is in a good place:</strong> State here what criteria they met (e.g., student-centered, has an active verb, explicit timeframe). If none, state "Needs foundation."</div>
  <div class="feedback-missing"><strong>🔴 What is missing:</strong> State here exactly what parts are still missing or require expansion (e.g., lacks real-world communication context, missing explicit linguistic forms, needs countability). If completely perfect, state "None! Ready to go."</div>
</div>

Closing friendly advice or guidance here.

CRITICAL RULE: If their rewrite successfully fulfills all standards (it is student-centered, observable, specific, language-focused, and situated), you MUST include the token text '##APPROVED##' at the absolute bottom of your response so the software can progress. Keep total text short.`;

        const SYS_P4 = `You are Coach Alex, an ELT professional development coach at Casa Thomas Jefferson (CTJ). Help this teacher write two fresh, highly communicative lesson objectives for an upcoming class. Ensure they meet all foundational criteria: student-centered, clear context, clear structural form, and realistic timeframe. Give precise feedback and guide them step-by-step. Keep responses under 130 words in conversational flowing prose.`;

        /* --- GEMINI BOT ENGINE NETWORK CALL --- */
        async function callBot(history, sys) {
            const key = getKey();
            if(!key) {
                showApiPrompt();
                return 'Please configure your Gemini API key above to collaborate with Coach Alex.';
            }

            // Map standard chat array format into Google Gemini API request body structure
            const contents = history.map(m => {
                return {
                    role: m.role === 'assistant' ? 'model' : 'user',
                    parts: [{ text: m.content }]
                };
            });

            try {
                const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=${key}`;
                const response = await fetch(url, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        contents: contents,
                        systemInstruction: { parts: [{ text: sys }] },
                        generationConfig: { maxOutputTokens: 500, temperature: 0.3 }
                    })
                });

                if(!response.ok) {
                    const err = await response.json();
                    return `API Error: ${err.error?.message || response.statusText}`;
                }

                const data = await response.json();
                return data.candidates[0].content.parts[0].text;
            } catch (err) {
                console.error(err);
                return `Connection Failure: ${err.message}. Check network configurations and API token validity.`;
            }
        }

        /* --- INTERFACE RENDERER --- */
        function render() {
            renderNav();
            const root = document.getElementById('root');
            
            if(S.ph === 1) root.innerHTML = rP1();
            else if(S.ph === 2) root.innerHTML = rP2();
            else if(S.ph === 3) root.innerHTML = rP3();
            else if(S.ph === 4) root.innerHTML = rP4();
            else if(S.ph === 5) root.innerHTML = rP5();
            else if(S.ph === 6) root.innerHTML = rP6();

            if(S.ph === 3 || S.ph === 4) {
                if(!getKey()) showApiPrompt();
            }
        }

        function renderNav() {
            const pnav = document.getElementById('pnav');
            let navHtml = '';
            for(let i=1; i<=5; i++) {
                let cls = 'phase-dot';
                if(S.ph > i || S.done.includes(i)) cls += ' done';
                else if(S.ph === i) cls += ' active';
                navHtml += `<div class="${cls}"></div>`;
            }
            pnav.innerHTML = navHtml;

            for(let i=1; i<=5; i++) {
                const lbl = document.getElementById('pl' + i);
                lbl.className = 'phase-label';
                if(S.ph > i) lbl.classList.add('done');
                if(S.ph === i) lbl.classList.add('active');
            }
        }

        function showApiPrompt() {
            if(document.getElementById('api-box')) return;
            const box = document.createElement('div');
            box.className = 'api-setup';
            box.id = 'api-box';
            box.innerHTML = `
                <h3>Gemini API Key Setup</h3>
                <p>Phases 3 and 4 connect directly with Coach Alex via Google's Gemini API. Input your API key below to launch interaction safely via your browser session context.</p>
                <input class="api-input" type="password" id="api-key-input" placeholder="AIzaSy..." value="${getKey()}">
                <div style="display:flex;align-items:center;gap:10px">
                    <button class="btn btn-p btn-sm" onclick="saveKey()">Save key</button>
                    <span class="api-saved" id="api-saved-msg">✓ Key verified</span>
                </div>
            `;
            document.querySelector('.content').prepend(box);
        }

        function saveKey(){
            const val = document.getElementById('api-key-input')?.value?.trim();
            if(!val) return;
            setKey(val);
            const msg = document.getElementById('api-saved-msg');
            if(msg) msg.style.display = 'inline';
            setTimeout(() => { render(); }, 800);
        }

        /* --- PHASE RENDERERS --- */
        function rP1() {
            const c = CARDS[S.ci];
            const pct = Math.round(((S.ci + 1)/CARDS.length)*100);
            return `
                <div class="phase-eyebrow">Phase 1 of 5</div>
                <h1 class="phase-title">Core Concepts</h1>
                <p class="phase-desc">Analyze foundational target filters. Examine the rule execution models below.</p>
                <div class="concept-card">
                    <div class="card-top">
                        <span class="pill" style="background:${c.pillBg};color:${c.pillC}">${c.pill}</span>
                        <span class="card-num">Card ${S.ci+1} of ${CARDS.length}</span>
                    </div>
                    <div class="card-rule">${c.rule}</div>
                    <div class="card-tip">${c.tip}</div>
                    <div class="ba-wrap">
                        <div class="ba-block bad">
                            <div class="ba-label">Weak</div>
                            <div class="ba-text">"${c.bad}"</div>
                            <div class="ba-why">Problem: ${c.badWhy}</div>
                        </div>
                        <div class="arrow-row"><div class="arrow-line"></div><div class="arrow-txt">revised to</div><div class="arrow-line"></div></div>
                        <div class="ba-block good">
                            <div class="ba-label">Strong</div>
                            <div class="ba-text">"${c.good}"</div>
                            <div class="ba-why">Why it works: ${c.goodWhy}</div>
                        </div>
                    </div>
                    <div class="prog-wrap"><div class="prog-fill" style="width:${pct}%"></div></div>
                    <div class="card-nav">
                        <button class="btn" onclick="p1b()" ${S.ci===0?'disabled':''}>Previous</button>
                        <span class="card-counter">${S.ci+1} / ${CARDS.length}</span>
                        ${S.ci === CARDS.length-1 ? `<button class="btn btn-p" onclick="fin(1)">Go to Phase 2 →</button>` : `<button class="btn btn-p" onclick="p1n()">Next Card</button>`}
                    </div>
                </div>
            `;
        }

        function rP2() {
            let h = `
                <div class="phase-eyebrow">Phase 2 of 5</div>
                <h1 class="phase-title">Classify Objectives</h1>
                <p class="phase-desc">Evaluate the sample objectives below. Determine whether they are effective or missing core pedagogical variables.</p>
                <div class="score-band">
                    <span>Performance Score:</span>
                    <span class="score-num">${S.p2s} / ${OBJECTIVES.length}</span>
                </div>
            `;
            
            OBJECTIVES.forEach((o, i) => {
                const a = S.p2a[i];
                const ok = a && (o.level === a);
                h += `
                    <div class="obj-card">
                        <div class="obj-meta">Objective ${i+1}</div>
                        <div class="obj-text">"${o.text}"</div>
                        <div class="rbtn-row">
                            <button class="rbtn g ${a==='g'?'sel':''}" onclick="rate(${i},'g')" ${a?'disabled':''}>✓ Effective</button>
                            <button class="rbtn m ${a==='m'?'sel':''}" onclick="rate(${i},'m')" ${a?'disabled':''}>⚠ Missing something</button>
                        </div>
                        ${a ? `<div class="fb ${ok?'fb-ok':'fb-no'}"><strong>${ok?'✓ Correct.':'✗ Incorrect choice.'}</strong> ${o.explanation}</div>` : ''}
                    </div>
                `;
            });

            const all = Object.keys(S.p2a).length === OBJECTIVES.length;
            if(all) {
                h += `
                    <div style="text-align:center; padding:1.5rem 0">
                        <button class="btn btn-p" onclick="initPhase3()">Continue to Phase 3 →</button>
                    </div>
                `;
            }
            return h;
        }

        function initPhase3() {
            S.p3weak = [];
            OBJECTIVES.forEach((o, i) => {
                if(o.level !== 'g') {
                    S.p3weak.push({ index: i, obj: o });
                }
            });
            S.p3idx = 0;
            S.p3approved = {};
            S.p3finished = false;
            initChat(0);
            fin(2);
        }

        function initChat(idx) {
            if(!S.p3weak[idx]) return;
            const item = S.p3weak[idx];
            S.p3chats[idx] = [{
                role: 'assistant',
                content: `Let's rebuild this objective together:\n\n"${item.obj.text}"\n\nProvide your updated draft below starting with "Students will be able to...". I will break down your version using explicit color-coded parameter metrics.`
            }];
        }

        function rP3dots() {
            const dots = S.p3weak.map((_, i) => {
                let cls = 'pending';
                if(S.p3approved[i]) cls = 'done';
                else if(i === S.p3idx && !S.p3finished) cls = 'active';
                return `<div class="p3-dot ${cls}">${i+1}</div>`;
            }).join('');
            const doneCount = Object.keys(S.p3approved).length;
            return `<div class="p3-progress"><div class="p3-dots">${dots}</div><span style="font-size:13px;color:var(--text2)">${doneCount} of ${S.p3weak.length} complete</span></div>`;
        }

        function rP3() {
            if(S.p3finished) {
                return `
                    <div class="phase-eyebrow">Phase 3 of 5</div>
                    <h1 class="phase-title">Rewrite Weak Objectives</h1>
                    ${rP3dots()}
                    <div style="background:var(--green-l);border:0.5px solid var(--green);border-radius:var(--radius-lg);padding:1.5rem;text-align:center">
                        <div style="font-size:28px;margin-bottom:0.5rem">✓</div>
                        <div style="font-size:17px;font-weight:600;color:#27500A;margin-bottom:0.5rem">Redesign Sequence Met!</div>
                        <p style="font-size:14px;color:var(--green);margin-bottom:1.25rem">All tracked target objectives have been successfully adjusted up to CTJ procedural standards.</p>
                        <button class="btn btn-p" onclick="fin(3)">Continue to Phase 4 →</button>
                    </div>
                `;
            }

            const idx = S.p3idx;
            const item = S.p3weak[idx];
            if(!item) return '';
            const msgs = S.p3chats[idx] || [];
            const isApproved = S.p3approved[idx];

            return `
                <div class="phase-eyebrow">Phase 3 of 5</div>
                <h1 class="phase-title">Rewrite Weak Objectives</h1>
                <p class="phase-desc">Submit revisions to Coach Alex. The coach will render structural feedback broken down into clear visual components.</p>
                ${rP3dots()}
                <div class="obj-box">
                    <div class="obj-box-label">Target Weak Objective</div>
                    <div class="obj-box-badge badge-m">Needs Improvement</div>
                    <div class="obj-box-text">"${item.obj.text}"</div>
                </div>
                <div class="chat-win">
                    <div class="chat-hd"><div class="bdot"></div>Coach Alex</div>
                    <div class="chat-msgs" id="p3chat">
                        ${msgs.map(m => `<div class="msg ${m.role==='user'?'user':'bot'}">${m.content.replace('##APPROVED##', '')}</div>`).join('')}
                    </div>
                    <div class="typ" id="p3typ">Coach Alex analyzing criteria structures...</div>
                    
                    ${isApproved ? `
                        <div class="approved-bar">
                            <span>✨ Objective certified by Coach Alex!</span>
                            <button class="btn btn-p btn-sm" onclick="advanceP3()">Next Objective →</button>
                        </div>
                    ` : `
                        <div class="chat-ir">
                            <textarea class="chat-in" id="p3in" placeholder="Type your alternative layout proposal here..." rows="2" onkeydown="if(event.key==='Enter'&&!event.shiftKey){event.preventDefault();sendP3();}"></textarea>
                            <button class="btn btn-p btn-sm" onclick="sendP3()">Send</button>
                        </div>
                    `}
                </div>
            `;
        }

        async function sendP3() {
            const inp = document.getElementById('p3in');
            const txt = inp?.value?.trim(); if(!txt) return;
            inp.value = '';

            const idx = S.p3idx;
            if(!S.p3chats[idx]) S.p3chats[idx] = [];
            S.p3chats[idx].push({role:'user', content:txt});
            render(); sb('p3chat');

            document.getElementById('p3typ').style.display = 'block';
            const item = S.p3weak[idx];
            const sys = SYS_P3 + `\n\nORIGINAL FLATTENED TARGET BASELINE: "${item.obj.text}"\nPre-calculated flaw parameters: ${item.obj.explanation}`;
            
            const rep = await callBot(S.p3chats[idx], sys);
            document.getElementById('p3typ').style.display = 'none';
            
            S.p3chats[idx].push({role:'assistant', content:rep});

            if(rep.includes('##APPROVED##')) {
                S.p3approved[idx] = true;
            }
            render(); sb('p3chat');
        }

        function advanceP3() {
            if(S.p3idx < S.p3weak.length - 1) {
                S.p3idx++;
                initChat(S.p3idx);
            } else {
                S.p3finished = true;
            }
            render();
            window.scrollTo({top:0, behavior:'smooth'});
        }

        function rP4() {
            return `
                <div class="phase-eyebrow">Phase 4 of 5</div>
                <h1 class="phase-title">Apply to Your Class</h1>
                <p class="phase-desc">Construct targets for your own upcoming module design blocks.</p>
                <div class="chat-win" style="height: 420px;">
                    <div class="chat-hd"><div class="bdot"></div>Coach Alex</div>
                    <div class="chat-msgs" id="p4chat">
                        <div class="msg bot">Welcome to Phase 4. Share details regarding your target class layer: provide your course track title, student demographics/level profiles, and core topic. Let's frame out two final operational goals together.</div>
                        ${S.c4.map(m => `<div class="msg ${m.role==='user'?'user':'bot'}">${m.content}</div>`).join('')}
                    </div>
                    <div class="typ" id="p4typ">Analyzing targets...</div>
                    <div class="chat-ir">
                        <textarea class="chat-in" id="p4in" placeholder="Provide target metrics or drafts here..." rows="2" onkeydown="if(event.key==='Enter'&&!event.shiftKey){event.preventDefault();sendP4();}"></textarea>
                        <button class="btn btn-p btn-sm" onclick="sendP4()">Send</button>
                    </div>
                </div>
                <div style="margin-top:1rem; text-align:right">
                    <button class="btn btn-sm btn-p" onclick="fin(4)">Move to Phase 5 →</button>
                </div>
            `;
        }

        async function sendP4() {
            const inp = document.getElementById('p4in');
            const txt = inp?.value?.trim(); if(!txt) return;
            inp.value = '';

            S.c4.push({role:'user', content:txt});
            render(); sb('p4chat');

            document.getElementById('p4typ').style.display = 'block';
            const rep = await callBot(S.c4, SYS_P4);
            document.getElementById('p4typ').style.display = 'none';

            S.c4.push({role:'assistant', content:rep});
            render(); sb('p4chat');
        }

        function rP5() {
            let h = `
                <div class="phase-eyebrow">Phase 5 of 5</div>
                <h1 class="phase-title">Exchange Peer Reviews</h1>
                <p class="phase-desc">Evaluate goal profiles submitted by other staff units. Provide peer review notes.</p>
                <div class="move-legend">
                    <div class="move-legend-item" style="background:#EEEDFE;color:#534AB7"><strong>Ask a question</strong>Clarify contextual logic maps</div>
                    <div class="move-legend-item" style="background:#E6F1FB;color:#185FA5"><strong>Make a comment</strong>Highlight strong architecture elements</div>
                    <div class="move-legend-item" style="background:#E1F5EE;color:#0F6E56"><strong>Offer a suggestion</strong>Provide structural optimizations</div>
                </div>
            `;

            PEERS.forEach((p, i) => {
                const mv = S.pm[i];
                const sent = S.ps[i];
                h += `
                    <div class="peer-card">
                        <div class="peer-hd">
                            <div class="av" style="background:${p.bg};color:${p.c}">${p.ini}</div>
                            <div>
                                <div style="font-size:14px;font-weight:500">${p.name}</div>
                                <div style="font-size:12px;color:var(--text2)">${p.level}</div>
                            </div>
                        </div>
                        <div class="peer-obj">"${p.obj}"</div>
                        ${!sent ? `
                            <div style="font-size:11px; font-weight:500; color:var(--text3); margin-bottom:6px; text-transform:uppercase; letter-spacing:0.06em">Select Feedback Matrix Move</div>
                            <div class="mv-row">
                                <button class="mvbtn q ${mv==='q'?'sel':''}" onclick="setM(${i},'q')">Ask Question</button>
                                <button class="mvbtn c ${mv==='c'?'sel':''}" onclick="setM(${i},'c')">Comment</button>
                                <button class="mvbtn s ${mv==='s'?'sel':''}" onclick="setM(${i},'s')">Suggestion</button>
                            </div>
                            ${mv ? `
                                <textarea class="peer-ta" id="pt${i}" placeholder="Enter constructive calibration summary response..."></textarea>
                                <button class="btn btn-sm btn-p" onclick="speer(${i})">Publish Review</button>
                            ` : ''}
                        ` : `
                            <div class="sent-badge">✓ Review Safely Synchronized: "${S.pt[i]}"</div>
                        `}
                    </div>
                `;
            });

            const allSent = PEERS.every((_, i) => S.ps[i]);
            if(allSent) {
                h += `
                    <div style="text-align:center; padding:1rem 0">
                        <button class="btn btn-p" onclick="fin(5)">Complete Calibration Engine 🎉</button>
                    </div>
                `;
            }
            return h;
        }

        function rP6() {
            return `
                <div style="text-align:center;padding:2rem 0">
                    <div style="width:68px;height:68px;border-radius:50%;background:var(--teal-l);border:2px solid var(--teal);display:flex;align-items:center;justify-content:center;margin:0 auto 1.25rem;font-size:30px">✓</div>
                    <h2 style="font-size:22px;font-weight:600;margin-bottom:0.5rem;letter-spacing:-0.02em">Calibration Track Matrix Complete</h2>
                    <p style="font-size:15px;color:var(--text2);line-height:1.6;max-width:480px;margin:0 auto 0.5rem">You've successfully completed your goal optimization parameters.</p>
                    <div class="divider"></div>
                    <div class="stat-row">
                        <div class="stat"><div class="stat-v">${CARDS.length}</div><div class="stat-l">Focal items logs</div></div>
                        <div class="stat"><div class="stat-v">${S.p2s}/${OBJECTIVES.length}</div><div class="stat-l">Classification accuracy</div></div>
                        <div class="stat"><div class="stat-v">100%</div><div class="stat-l">Status score</div></div>
                    </div>
                    <button class="btn" onclick="location.reload()">Restart Module</button>
                </div>
            `;
        }

        /* --- CONTROLLER HELPERS --- */
        function sb(id){ const el=document.getElementById(id); if(el) el.scrollTop=el.scrollHeight; }
        function p1b(){ if(S.ci>0){S.ci--; render();} }
        function p1n(){ if(S.ci<CARDS.length-1){S.ci++; render();} }
        
        function rate(i, v) {
            if(S.p2a[i]) return;
            const o = OBJECTIVES[i];
            const ok = (o.level === v);
            S.p2a[i] = v; 
            if(ok) S.p2s++;
            render();
            setTimeout(() => { 
                const el = document.querySelectorAll('.obj-card')[i]; 
                if(el) el.scrollIntoView({behavior:'smooth', block:'nearest'}); 
            }, 100);
        }

        function setM(i, m){ S.pm[i] = m; render(); }
        
        function speer(i) {
            const ta = document.getElementById('pt'+i); 
            const txt = ta?.value?.trim(); if(!txt) return;
            S.pt[i] = txt; S.ps[i] = true; 
            render();
        }

        function fin(n) {
            if(!S.done.includes(n)) S.done.push(n);
            S.ph = n + 1;
            window.scrollTo({top:0, behavior:'smooth'});
            render();
        }

        render();
    </script>
</body>
</html>
