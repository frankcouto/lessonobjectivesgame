<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Goal-Setting for ESL Lesson Design — Casa Thomas Jefferson</title>
<style>
  /* ── Reset & base ── */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg:        #ffffff;
    --bg2:       #f5f5f4;
    --bg3:       #e7e5e4;
    --text:      #1c1917;
    --text2:     #57534e;
    --text3:     #a8a29e;
    --border:    #e7e5e4;
    --border2:   #d6d3d1;
    --radius-sm: 6px;
    --radius-md: 10px;
    --radius-lg: 14px;
    --blue:      #185FA5;
    --blue-l:    #E6F1FB;
    --blue-m:    #378ADD;
    --teal:      #0F6E56;
    --teal-l:    #E1F5EE;
    --amber:     #BA7517;
    --amber-l:   #FAEEDA;
    --coral:     #993C1D;
    --coral-l:   #FAECE7;
    --green:     #3B6D11;
    --green-l:   #EAF3DE;
    --purple:    #534AB7;
    --purple-l:  #EEEDFE;
    --navy:      #0C447C;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg:    #1c1917; --bg2: #292524; --bg3: #3c3836;
      --text:  #fafaf9; --text2: #a8a29e; --text3: #78716c;
      --border:#3c3836; --border2: #57534e;
    }
  }
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    background: var(--bg2);
    color: var(--text);
    min-height: 100vh;
    padding: 0;
  }

  /* ── Shell ── */
  .shell {
    max-width: 760px;
    margin: 0 auto;
    background: var(--bg);
    min-height: 100vh;
    padding: 0 0 4rem;
    box-shadow: 0 0 0 0.5px var(--border);
  }

  /* ── Top bar ── */
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
  .topbar-sub   { font-size: 12px; opacity: 0.75; margin-top: 2px; }
  .ctj-badge {
    font-size: 11px; font-weight: 600; letter-spacing: 0.06em;
    background: rgba(255,255,255,0.18); color: #fff;
    padding: 4px 10px; border-radius: 20px; white-space: nowrap;
  }

  /* ── Phase nav ── */
  .phase-nav-wrap { padding: 1rem 1.5rem 0; }
  .phase-nav { display: flex; gap: 6px; margin-bottom: 0.5rem; }
  .phase-dot {
    flex: 1; height: 5px; border-radius: 3px;
    background: var(--border2); transition: background 0.3s;
  }
  .phase-dot.done   { background: var(--teal); }
  .phase-dot.active { background: var(--blue-m); }
  .phase-labels { display: flex; justify-content: space-between; }
  .phase-label {
    font-size: 10px; color: var(--text3); flex: 1; text-align: center;
    cursor: default;
  }
  .phase-label.active { color: var(--blue-m); font-weight: 500; }
  .phase-label.done   { color: var(--teal); }

  /* ── Main content ── */
  .content { padding: 1.5rem; }
  .phase-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 0.08em;
    text-transform: uppercase; color: var(--text3); margin-bottom: 4px;
  }
  .phase-title { font-size: 22px; font-weight: 600; margin-bottom: 6px; letter-spacing: -0.02em; }
  .phase-desc  { font-size: 15px; color: var(--text2); line-height: 1.65; margin-bottom: 1.5rem; }

  /* ── Concept card ── */
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
  .ba-text  { font-size: 13px; font-style: italic; line-height: 1.6; padding: 9px 12px; }
  .ba-why   { font-size: 12px; padding: 5px 12px 9px; border-top: 0.5px solid rgba(0,0,0,0.08); }
  .bad .ba-label { background: #FAECE7; color: #993C1D; }
  .bad .ba-text  { background: #FAECE7; color: #712B13; }
  .bad .ba-why   { background: #FAECE7; color: #993C1D; }
  .good .ba-label { background: #EAF3DE; color: #3B6D11; }
  .good .ba-text  { background: #EAF3DE; color: #27500A; }
  .good .ba-why   { background: #EAF3DE; color: #3B6D11; }
  .arrow-row { display: flex; align-items: center; gap: 8px; }
  .arrow-line { flex: 1; height: 0.5px; background: var(--border2); }
  .arrow-txt  { font-size: 11px; color: var(--text3); white-space: nowrap; }
  .prog-wrap  { height: 4px; background: var(--border2); border-radius: 2px; }
  .prog-fill  { height: 4px; background: var(--blue-m); border-radius: 2px; transition: width 0.3s; }
  .card-nav   { display: flex; justify-content: space-between; align-items: center; }
  .card-counter { font-size: 13px; color: var(--text2); }

  /* ── Buttons ── */
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
  .btn:hover     { background: var(--bg2); }
  .btn:disabled  { opacity: 0.4; cursor: default; }
  .btn-p         { background: var(--blue); color: #fff; border-color: var(--blue); }
  .btn-p:hover   { background: #0C447C; color: #fff; }
  .btn-sm        { padding: 0.35rem 0.8rem; font-size: 13px; }

  /* ── Phase 2 ── */
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
  .obj-meta  { font-size: 12px; color: var(--text3); margin-bottom: 0.5rem; }
  .obj-text  { font-size: 15px; line-height: 1.65; margin-bottom: 1rem; font-style: italic; }
  .rbtn-row  { display: flex; gap: 8px; flex-wrap: wrap; }
  .rbtn {
    padding: 0.45rem 1rem; border-radius: 20px;
    font-size: 13px; font-weight: 500; border: 1.5px solid;
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

  /* ── Phase 3 ── */
  .p3-progress { display: flex; align-items: center; gap: 10px; margin-bottom: 1.5rem; flex-wrap: wrap; }
  .p3-dots     { display: flex; gap: 5px; flex-wrap: wrap; }
  .p3-dot {
    width: 28px; height: 28px; border-radius: 50%; border: 2px solid;
    display: flex; align-items: center; justify-content: center;
    font-size: 11px; font-weight: 600; transition: all 0.2s;
  }
  .p3-dot.pending { border-color: var(--border2); color: var(--text3); background: transparent; }
  .p3-dot.active  { border-color: var(--blue); color: var(--blue); background: var(--blue-l); }
  .p3-dot.done    { border-color: var(--teal); color: var(--teal); background: var(--teal-l); }
  .obj-box { background: var(--bg2); border-radius: var(--radius-md); padding: 1rem 1.25rem; margin-bottom: 1rem; }
  .obj-box-label { font-size: 11px; font-weight: 500; text-transform: uppercase; letter-spacing: 0.06em; color: var(--text3); margin-bottom: 6px; }
  .obj-box-badge { display: inline-flex; align-items: center; gap: 5px; font-size: 11px; font-weight: 600; padding: 3px 9px; border-radius: 20px; margin-bottom: 6px; }
  .badge-m { background: var(--amber-l); color: var(--amber); }
  .obj-box-text { font-size: 15px; font-style: italic; line-height: 1.6; }
  .checkpoint-box {
    background: var(--bg); border: 1.5px solid var(--blue-m);
    border-radius: var(--radius-lg); padding: 1.5rem; text-align: center; margin-bottom: 1rem;
  }
  .checkpoint-btns { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; margin-top: 1.25rem; }

  /* ── Redesigned P3 Lab Layout ── */
  .p3-lab-container { display: flex; flex-direction: column; gap: 1.25rem; }
  .p3-panel { background: var(--bg); border: 0.5px solid var(--border2); border-radius: var(--radius-lg); padding: 1.5rem; }
  .diag-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-top: 1rem; }
  @media(max-width: 600px) { .diag-grid { grid-template-columns: 1fr; } }
  .diag-card { border-radius: var(--radius-md); padding: 1rem; border: 1px solid; }
  .diag-card.good { background: var(--green-l); border-color: #b2d89a; color: #27500A; }
  .diag-card.missing { background: var(--coral-l); border-color: #f1b3a1; color: #712B13; }
  .diag-card h4 { font-size: 13px; text-transform: uppercase; letter-spacing: 0.05em; margin-bottom: 0.5rem; font-weight: 700; }
  .diag-list { list-style: none; display: flex; flex-direction: column; gap: 6px; font-size: 13px; }
  .diag-list li { display: flex; gap: 6px; align-items: flex-start; line-height: 1.4; }

  /* ── Chat & Panels ── */
  .chat-win {
    border: 0.5px solid var(--border2); border-radius: var(--radius-lg);
    overflow: hidden; display: flex; flex-direction: column; height: 380px;
  }
  .chat-hd {
    padding: 0.75rem 1rem; background: var(--blue); color: #fff;
    font-size: 14px; font-weight: 500; display: flex; align-items: center; gap: 8px;
  }
  .bdot { width: 8px; height: 8px; border-radius: 50%; background: #9fe1cb; }
  .chat-msgs {
    flex: 1; overflow-y: auto; padding: 1rem;
    display: flex; flex-direction: column; gap: 10px; background: var(--bg2);
  }
  .msg {
    max-width: 85%; font-size: 14px; line-height: 1.6;
    padding: 0.6rem 0.9rem; border-radius: 12px; white-space: pre-wrap;
  }
  .msg.bot   { background: var(--bg); border: 0.5px solid var(--border2); align-self: flex-start; }
  .msg.user { background: var(--blue); color: #fff; align-self: flex-end; }
  .chat-ir  {
    display: flex; gap: 8px; padding: 0.75rem; background: var(--bg);
    border-top: 0.5px solid var(--border2);
  }
  .chat-in {
    flex: 1; padding: 0.5rem 0.75rem; font-size: 14px;
    border: 0.5px solid var(--border2); border-radius: var(--radius-md);
    background: var(--bg2); color: var(--text); resize: none; font-family: inherit;
  }
  .chat-in:focus { outline: none; border-color: var(--blue-m); }
  .typ { font-size: 12px; color: var(--text3); padding: 0 1rem 0.5rem; background: var(--bg2); display: none; }
  .approved-bar {
    background: var(--green-l); padding: 0.75rem 1rem; font-size: 14px; color: #27500A;
    border-top: 0.5px solid #b2d89a; display: flex; align-items: center;
    justify-content: space-between; gap: 10px; flex-wrap: wrap;
  }
  .ctx-box {
    background: var(--blue-l); border: 0.5px solid var(--blue-m);
    border-radius: var(--radius-md); padding: 0.75rem 1rem; margin-bottom: 1rem;
    font-size: 13px; color: var(--navy);
  }

  /* ── Phase 5 ── */
  .peer-card {
    background: var(--bg); border: 0.5px solid var(--border2);
    border-radius: var(--radius-lg); padding: 1.25rem 1.5rem; margin-bottom: 1rem;
  }
  .peer-hd { display: flex; align-items: center; gap: 10px; margin-bottom: 0.75rem; }
  .av {
    width: 36px; height: 36px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 13px; font-weight: 600; flex-shrink: 0;
  }
  .peer-obj {
    font-size: 14px; font-style: italic; line-height: 1.65;
    padding: 0.75rem; background: var(--bg2); border-radius: var(--radius-md); margin-bottom: 1rem;
  }
  .mv-row { display: flex; gap: 8px; margin-bottom: 0.75rem; flex-wrap: wrap; }
  .mvbtn {
    flex: 1; min-width: 100px; padding: 0.45rem 0.5rem;
    border-radius: var(--radius-md); font-size: 12px; font-weight: 500;
    border: 1.5px solid; cursor: pointer; background: transparent;
    text-align: center; transition: all 0.12s; font-family: inherit;
  }
  .mvbtn.q { border-color: var(--purple); color: var(--purple); }
  .mvbtn.q.sel, .mvbtn.q:hover { background: var(--purple-l); }
  .mvbtn.c { border-color: var(--blue); color: var(--blue); }
  .mvbtn.c.sel, .mvbtn.c:hover { background: var(--blue-l); }
  .mvbtn.s { border-color: var(--teal); color: var(--teal); }
  .mvbtn.s.sel, .mvbtn.s:hover { background: var(--teal-l); }
  .peer-ta {
    width: 100%; padding: 0.6rem 0.75rem; font-size: 14px;
    border: 0.5px solid var(--border2); border-radius: var(--radius-md);
    background: var(--bg2); color: var(--text);
    resize: vertical; min-height: 80px; font-family: inherit; margin-bottom: 0.75rem;
  }
  .peer-ta:focus { outline: none; border-color: var(--blue-m); }
  .sent-badge {
    display: inline-flex; align-items: center; gap: 5px; font-size: 12px;
    color: var(--green); background: var(--green-l); padding: 4px 10px; border-radius: 20px;
  }

  /* ── Completion ── */
  .stat-row { display: flex; gap: 12px; justify-content: center; margin: 1.5rem 0; flex-wrap: wrap; }
  .stat {
    background: var(--bg2); border-radius: var(--radius-md);
    padding: 0.75rem 1.25rem; text-align: center; min-width: 110px;
  }
  .stat-v { font-size: 24px; font-weight: 600; color: var(--blue); }
  .stat-l { font-size: 12px; color: var(--text2); margin-top: 2px; }
  .divider { height: 0.5px; background: var(--border2); margin: 1.5rem 0; }

  /* ── Move legend ── */
  .move-legend { display: flex; gap: 8px; margin-bottom: 1.25rem; flex-wrap: wrap; }
  .move-legend-item {
    flex: 1; min-width: 130px; padding: 0.75rem;
    border-radius: var(--radius-md); font-size: 13px;
  }
  .move-legend-item strong { display: block; margin-bottom: 2px; }
</style>
</head>
<body>
<div class="shell">

  <!-- Top bar -->
  <div class="topbar">
    <div>
      <div class="topbar-title">Goal-Setting for ESL Lesson Design</div>
      <div class="topbar-sub">Professional Development Module · 5 Phases</div>
    </div>
    <div class="ctj-badge">CTJ</div>
  </div>

  <!-- Phase nav -->
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

  <!-- Main content -->
  <div class="content" id="root"></div>
</div>

<script>
/* ══════════════════════════════════════════
   DATA
   ══════════════════════════════════════════ */
const CARDS=[
  {pill:'Observable',pillBg:'#E6F1FB',pillC:'#185FA5',
   rule:'Use a verb that describes something you can see or hear.',
   tip:'If you can\'t watch a student doing it, you can\'t assess whether they learned it. Swap invisible words like "understand" or "know" for visible actions like "describe," "write," or "ask."',
   bad:'"Students will understand the present perfect."',badWhy:'"Understand" is invisible — you can\'t watch it happen.',
   good:'"Students will be able to describe three past experiences using the present perfect in a short speaking activity."',goodWhy:'You can listen and assess whether they did this.'},
  {pill:'Student-centered',pillBg:'#E1F5EE',pillC:'#0F6E56',
   rule:'Write about what students do, not what you do.',
   tip:'Check who is the subject of the sentence. If it\'s "I" or "the teacher," rewrite. A lesson objective describes a student behavior — not a teaching action.',
   bad:'"I will explain the grammar rules for conditionals using examples."',badWhy:'The teacher is the subject. Students are invisible.',
   good:'"Students will be able to use first conditional sentences to discuss real plans for the week."',goodWhy:'Now the student is the actor. You can assess whether they succeeded.'},
  {pill:'Specific',pillBg:'#EEEDFE',pillC:'#534AB7',
   rule:'Name the skill, the sub-skill, and the context.',
   tip:'Vague objectives can\'t guide what you teach, what materials you choose, or how you assess. Push yourself to answer: What exactly will students do? With what language? In what situation?',
   bad:'"Students will improve their speaking skills."',badWhy:'Which aspect of speaking? In what situation? What counts as improvement?',
   good:'"Students will be able to describe symptoms of an illness to a pharmacist using target medical vocabulary."',goodWhy:'Skill, sub-skill, context, and language — all named.'},
  {pill:'Measurable',pillBg:'#FAEEDA',pillC:'#BA7517',
   rule:'Include something you can count or check.',
   tip:'Ask yourself: how will I know at the end of the lesson whether students achieved this? If your answer is "I\'ll have a feeling they got it," the objective isn\'t measurable. Add a quantity, a standard, or a visible product.',
   bad:'"Students will practice vocabulary about travel."',badWhy:'How much vocabulary? What counts as practice? There\'s no finish line.',
   good:'"Students will be able to use six target travel phrases to book a hotel in a role-play."',goodWhy:'Six phrases is countable. The role-play is the visible product you check.'},
  {pill:'Achievable',pillBg:'#FAECE7',pillC:'#993C1D',
   rule:'Aim just beyond what students can already do — not five steps ahead.',
   tip:'The sweet spot is something that requires effort but is reachable within this lesson, at this level, with the support you provide.',
   bad:'"Students will know how to use articles in English."',badWhy:'English articles take years to master. This can\'t happen in one lesson.',
   good:'"Students will be able to use the definite article correctly when referring to a previously mentioned noun in a short paragraph."',goodWhy:'One rule, one context, one lesson. Reachable.'},
  {pill:'Language-focused',pillBg:'#EAF3DE',pillC:'#3B6D11',
   rule:'Name both the language form and what students will communicate with it.',
   tip:'Knowing a grammar rule is not the same as using it to communicate. Every ESL objective should specify the form (e.g. modal verbs) and the communicative job it does (e.g. giving advice).',
   bad:'"Students will learn about modal verbs."',badWhy:'"Learning about" a form is passive. No communicative function is named.',
   good:'"Students will be able to use modal verbs of obligation to give workplace advice in a pair discussion."',goodWhy:'Form + function + context. Complete.'},
  {pill:'Contextualized',pillBg:'#E6F1FB',pillC:'#0C447C',
   rule:'Situate the language in a real-world scenario.',
   tip:'Language always happens somewhere, with someone, for a reason. Naming the situation makes the lesson relevant and helps students see why they\'re learning this.',
   bad:'"Students will be able to write a formal email."',badWhy:'To whom? About what? The context is missing.',
   good:'"Students will be able to write a 50-word email to a colleague requesting to postpone a meeting, using appropriate formal register."',goodWhy:'Recipient, purpose, register, length — all named.'},
  {pill:'Realistic',pillBg:'#EEEDFE',pillC:'#534AB7',
   rule:'Keep the scope inside one lesson.',
   tip:'A lesson objective describes what\'s achievable in 50–90 minutes. If it would take three classes, it\'s a unit goal. Narrow it down.',
   bad:'"Students will become fluent in giving presentations in English."',badWhy:'Fluency in presentations is a semester goal.',
   good:'"Students will be able to deliver a 60-second spoken product introduction using a provided structure."',goodWhy:'60 seconds, one structure. Doable in a single class.'},
  {pill:'Scaffolded',pillBg:'#E1F5EE',pillC:'#0F6E56',
   rule:'Build multiple objectives as a staircase — not a list.',
   tip:'Each objective should open the door to the next. If you can reorder the activities without losing anything, there\'s no scaffold.',
   bad:'"Students will practice reading and writing and speaking and listening."',badWhy:'Four skills, no sequence, no connection. A list, not a plan.',
   good:'"Obj 1: Students identify key details in an article. Obj 2: Students use those details to argue a position in a group discussion."',goodWhy:'Reading feeds into speaking. Remove step 1 and step 2 collapses.'},
  {pill:'Communicative',pillBg:'#E6F1FB',pillC:'#185FA5',
   rule:'The lesson should end with students saying something to someone.',
   tip:'Does the final activity require genuine exchange of meaning between people? If the last task is a silent gap-fill, the objective needs rethinking.',
   bad:'"Students will read the text and answer comprehension questions."',badWhy:'Individual, silent, one-directional. No communication.',
   good:'"Students will be able to discuss the main argument with a partner and agree on whether it\'s convincing, giving one reason each."',goodWhy:'Reading becomes a launchpad for real spoken exchange.'},
];

const OBJECTIVES=[
  {text:'By the end of the lesson, students will be able to talk about food.',level:'Missing something',explanation:'This fails multiple key criteria. "Talk about food" is unmeasurable and unspecific. Revision: "Students will be able to describe a traditional dish using sensory adjectives and present tense in response to a partner\'s question."'},
  {text:'Students will be able to distinguish between formal and informal register when making requests in a professional email context.',level:'Effective',explanation:'Strong. Specific, measurable, student-centered, language-focused (requests + register), contextualized (professional email), and observable. All criteria met.'},
  {text:'Students will learn about the difference between the Present Simple and Present Continuous tenses.',level:'Missing something',explanation:'"Will learn about" is passive with no communicative context. Revision: "Students will be able to use Present Simple vs. Continuous to describe their daily routine vs. what they are doing right now in a class survey."'},
  {text:'By the end of class, students will be able to leave a 60-second voicemail in English requesting a rescheduled meeting, using appropriate formal language and at least three modal verbs.',level:'Effective',explanation:'Excellent. Specific, measurable (60 seconds, three modals), student-centered, language-focused, contextualized, and observable.'},
  {text:'Students will practice speaking.',level:'Missing something',explanation:'"Practice speaking" is an activity type, not a learning outcome. Revision: "Students will be able to express and justify a personal opinion using discourse markers in a structured class debate."'},
  {text:'Students will be able to use three repair strategies (asking for clarification, paraphrasing, and buying time) to maintain a conversation when they encounter an unknown word.',level:'Effective',explanation:'Specific (three named strategies), measurable, student-centered, contextualized, and observable.'},
  {text:'By the end of the lesson, students will understand the passive voice.',level:'Missing something',explanation:'"Understand" is not observable and there is no communicative context. Revision: "Students will be able to describe a manufacturing process using passive voice in a short class presentation."'},
  {text:'Students will be able to read a CTJ placement test instruction and identify the key task requirements within two minutes.',level:'Effective',explanation:'Specific, measurable (two minutes), student-centered, language-focused, and observable. CTJ-relevant.'},
  {text:'Students will improve their writing skills.',level:'Missing something',explanation:'Far too broad. "Improve" cannot be measured in 50 minutes. Revision: "Students will be able to write a three-sentence professional bio in third person using cohesive devices for a LinkedIn profile."'},
  {text:'By the end of the class, students will be able to ask and respond to three types of clarification questions in a B2-level discussion, using appropriate intonation.',level:'Effective',explanation:'Specific, measurable, student-centered, contextualized, and observable. Targets strategic competence and pronunciation.'},
  {text:'The teacher will explain the grammar rules for conditionals using examples.',level:'Missing something',explanation:'This is a teacher objective, not a student objective. Revision: "Students will be able to use first and second conditional sentences to discuss hypothetical professional dilemmas in a role-play."'},
  {text:'Students will be able to identify the main idea and two supporting details from an authentic podcast excerpt at B2 level.',level:'Effective',explanation:'Specific, measurable, student-centered, contextualized (authentic podcast, B2 level), and observable.'},
  {text:'Students will know how to use articles in English.',level:'Missing something',explanation:'Articles are a multi-lesson topic — too broad. Revision: "Students will be able to correctly use definite and indefinite articles when introducing new vs. known information in a short oral presentation."'},
  {text:'By the end of the activity, students will be able to negotiate a price for a second-hand item using at least two counter-offer expressions and polite hedging language.',level:'Effective',explanation:'Real-world task, specific forms (counter-offers, hedging), measurable (two expressions). Fully achievable.'},
  {text:'Students will complete a reading comprehension exercise about environmental issues.',level:'Missing something',explanation:'Describes an activity, not a learning outcome. Revision: "Students will be able to infer the author\'s implied opinion from a B2-level article, citing at least two pieces of textual evidence."'},
  {text:'Students will be able to use discourse markers (however, in contrast, furthermore) to structure a spoken opinion of 90 seconds or more on a B2-level topic.',level:'Effective',explanation:'Specific (three named markers, 90-second minimum), measurable, student-centered, contextualized, and observable.'},
  {text:'Students will enjoy the lesson about English phrasal verbs.',level:'Missing something',explanation:'Enjoyment is an aspiration, not a learning objective. Revision: "Students will be able to use five work-related phrasal verbs in a role-play about a workplace problem."'},
  {text:'By the end of the lesson, students will be able to summarize a 3-minute news report in 2-3 spoken sentences, identifying who, what, and where.',level:'Effective',explanation:'Specific, measurable, student-centered, contextualized, and observable.'},
  {text:'Students will be introduced to vocabulary related to health and medicine.',level:'Missing something',explanation:'"Be introduced to" is a teacher action in passive disguise. Revision: "Students will be able to use eight target medical vocabulary items to explain symptoms to a pharmacist in a role-play."'},
  {text:'Students will be able to write a professional cover letter opening paragraph of 50–75 words, using appropriate register and at least one subordinating clause.',level:'Effective',explanation:'Specific, measurable (50–75 words, one clause), student-centered, language-focused, and contextualized (job application).'},
];

const PEERS=[
  {name:'Carla M.',level:'Senior teacher, 5 years',ini:'CM',bg:'#EEEDFE',c:'#534AB7',obj:'By the end of the lesson, students will be able to use at least three comparative structures to describe differences between two job candidates in a simulated HR meeting.'},
  {name:'Rafael S.',level:'Trainee teacher, 1st semester',ini:'RS',bg:'#E6F1FB',c:'#185FA5',obj:'Students will practice vocabulary about travel and tourism and talk about their favorite places.'},
  {name:'Luísa A.',level:'Senior teacher, 8 years',ini:'LA',bg:'#E1F5EE',c:'#0F6E56',obj:'By the end of class, students will be able to construct a 90-second spoken narrative about a past professional challenge using narrative tenses and at least two cohesive adverbs.'},
  {name:'Thiago B.',level:'Trainee teacher, 2nd semester',ini:'TB',bg:'#FAEEDA',c:'#BA7517',obj:'Students will learn the difference between too, also, and as well and when to use them.'},
];

/* ══════════════════════════════════════════
   DIAGNOSTICS PARSER ENGINE (USED IN P3 & P4)
   ══════════════════════════════════════════ */
function parseObjectiveQuality(text) {
  const clean = text.toLowerCase().trim();
  let goodElements = [];
  let missingElements = [];
  let score = 8;

  if (!clean) {
    return { score: 0, good: [], missing: ["Start writing to run structural diagnostics."] };
  }

  // 1. Student Centered
  if (clean.startsWith("students will be able to") || clean.startsWith("obj") || clean.startsWith("by the end of the lesson, students will be able to")) {
    goodElements.push("<strong>Student-Centered:</strong> Correctly frames the target outcome around learner actions.");
  } else {
    missingElements.push("<strong>Not Student-Centered:</strong> Frame your objective starting exactly with <em>'Students will be able to...'</em> to ensure the focus is on student action.");
    score--;
  }

  // 2. Observable Verbs
  const invisibleVerbs = ["understand", "know", "learn about", "comprehend", "appreciate", "study", "master"];
  let foundInvisible = invisibleVerbs.filter(v => clean.includes(v));
  if (foundInvisible.length > 0) {
    missingElements.push(`<strong>Non-Observable Verbs Found:</strong> You used "${foundInvisible.join(", ")}". Swap these out for active verbs you can see or hear.`);
    score -= 2;
  } else if (clean.length > 15) {
    goodElements.push("<strong>Observable Action:</strong> Avoids weak mental state placeholders like 'know' or 'understand'.");
  }

  // 3. Measurable Metric
  const metrics = ["at least", "sentences", "minutes", "words", "phrases", "examples", "criteria", "seconds", "points"];
  let hasMetric = metrics.some(m => clean.includes(m)) || /\b\d+\b/.test(clean); 
  if (hasMetric) {
    goodElements.push("<strong>Quantifiable Metric:</strong> Includes clear criteria, time constraints, or countable values.");
  } else {
    missingElements.push("<strong>Missing Quantifiable Metric:</strong> Add a target threshold so you can count success (e.g., <em>'use three target phrases'</em>).");
    score--;
  }

  // 4. Real-World Context
  const contextClues = ["in a", "during", "role-play", "discussion", "email", "presentation", "context", "scenario", "with a partner", "meeting"];
  if (contextClues.some(c => clean.includes(c))) {
    goodElements.push("<strong>Real-World Context:</strong> Grounded within a specific communication environment or scenario.");
  } else {
    missingElements.push("<strong>Lacks Real-World Context:</strong> Where does this communication happen? Ground the task in a scenario (e.g., <em>'in a role-play'</em>).");
    score--;
  }

  // 5. Language Focus
  const languageClues = ["using", "by employing", "via", "with the aid of", "phrases", "verbs", "vocabulary", "tense"];
  if (languageClues.some(c => clean.includes(c))) {
    goodElements.push("<strong>Language Focus:</strong> Expressly targets linguistic structures, markers, or vocabulary words.");
  } else {
    missingElements.push("<strong>Vague Language Target:</strong> Explicitly mention the target linguistic structure or tools being tested (e.g., <em>'using modal verbs'</em>).");
    score--;
  }

  if (score < 0) score = 0;
  return { score, good: goodElements, missing: missingElements };
}

/* ══════════════════════════════════════════
   STATE
   ══════════════════════════════════════════ */
let S={
  ph:1, ci:0,
  p2a:{}, p2s:0,
  p3weak:[], p3idx:0, p3attempts:{}, p3approved:{}, p3checkpoint:false,
  c4:[], pm:{}, pt:{}, ps:{}, done:[]
};

/* ══════════════════════════════════════════
   UI ENGINE & ROUTING
   ══════════════════════════════════════════ */
function renderNav() {
  const nav = document.getElementById('pnav');
  if (!nav) return;
  nav.innerHTML = '';
  for (let i = 1; i <= 5; i++) {
    const dot = document.createElement('div');
    dot.className = `phase-dot ${S.ph === i ? 'active' : (S.ph > i || S.done.includes(i)) ? 'done' : ''}`;
    nav.appendChild(dot);
    
    const lbl = document.getElementById(`pl${i}`);
    if (lbl) {
      lbl.className = `phase-label ${S.ph === i ? 'active' : (S.ph > i || S.done.includes(i)) ? 'done' : ''}`;
    }
  }
}

function go(p) {
  S.ph = p;
  renderNav();
  const root = document.getElementById('root');
  if (!root) return;
  root.innerHTML = '';

  if (p === 1) renderP1(root);
  else if (p === 2) renderP2(root);
  else if (p === 3) renderP3(root);
  else if (p === 4) renderP4(root);
  else if (p === 5) renderP5(root);
  else if (p === 6) renderComplete(root);
  
  window.scrollTo(0, 0);
}

/* ══════════════════════════════════════════
   PHASE 1: CONCEPTS (FLASHCARDS)
   ══════════════════════════════════════════ */
function renderP1(root) {
  const c = CARDS[S.ci];
  const pct = Math.round(((S.ci + 1) / CARDS.length) * 100);

  root.innerHTML = `
    <div class="phase-eyebrow">Phase 1 of 5 · Deep Dive</div>
    <h2 class="phase-title">The Anatomy of a Perfect Lesson Goal</h2>
    <p class="phase-desc">Explore these ten design variables used at Casa Thomas Jefferson to scale objectives from weak placeholders to precision learning instruments.</p>
    
    <div class="concept-card">
      <div class="card-top">
        <span class="pill" style="background:${c.pillBg}; color:${c.pillC}">${c.pill}</span>
        <span class="card-num">Variable ${S.ci + 1} of ${CARDS.length}</span>
      </div>
      <div class="card-rule">${c.rule}</div>
      <div class="card-tip">${c.tip}</div>
      
      <div class="ba-wrap">
        <div class="ba-block bad">
          <div class="ba-label">❌ Weak Architecture</div>
          <div class="ba-text">${c.bad}</div>
          <div class="ba-why"><strong>Why it fails:</strong> ${c.badWhy}</div>
        </div>
        <div class="arrow-row">
          <div class="arrow-line"></div>
          <span class="arrow-txt">CTJ Refinement Transformation</span>
          <div class="arrow-line"></div>
        </div>
        <div class="ba-block good">
          <div class="ba-label">✨ Precision Calibrated Goal</div>
          <div class="ba-text">${c.good}</div>
          <div class="ba-why"><strong>Why it thrives:</strong> ${c.goodWhy}</div>
        </div>
      </div>
      
      <div class="prog-wrap"><div class="prog-fill" style="width:${pct}%"></div></div>
      
      <div class="card-nav">
        <button class="btn" id="p1Back" ${S.ci === 0 ? 'disabled' : ''}>Back</button>
        <span class="card-counter">${S.ci + 1} / ${CARDS.length}</span>
        <button class="btn btn-p" id="p1Next">${S.ci === CARDS.length - 1 ? 'Advance to Phase 2 →' : 'Next Metric'}</button>
      </div>
    </div>
  `;

  document.getElementById('p1Back').onclick = () => { if (S.ci > 0) { S.ci--; go(1); } };
  document.getElementById('p1Next').onclick = () => {
    if (S.ci < CARDS.length - 1) {
      S.ci++;
      go(1);
    } else {
      if (!S.done.includes(1)) S.done.push(1);
      go(2);
    }
  };
}

/* ══════════════════════════════════════════
   PHASE 2: CLASSIFYING CRITERIA (TWO OPTIONS ONLY)
   ══════════════════════════════════════════ */
function renderP2(root) {
  root.innerHTML = `
    <div class="phase-eyebrow">Phase 2 of 5 · Quality Sorting Matrix</div>
    <h2 class="phase-title">Objective Evaluation Audit</h2>
    <p class="phase-desc">Audit the following real classroom examples. Classify them as either <strong>Effective</strong> or <strong>Missing something</strong>.</p>
    
    <div class="score-band">
      <span>Progress Evaluation Tracker:</span>
      <div><span class="score-num" id="p2Score">${S.p2s}</span> / ${OBJECTIVES.length} Verified</div>
    </div>
    
    <div id="objList"></div>
    
    <div style="margin-top:2rem; text-align:right;">
      <button class="btn btn-p" id="p2DoneBtn" ${S.p2s < OBJECTIVES.length ? 'disabled' : ''}>Advance to Phase 3 →</button>
    </div>
  `;

  const list = document.getElementById('objList');
  OBJECTIVES.forEach((o, idx) => {
    const div = document.createElement('div');
    div.className = 'obj-card';
    
    const saved = S.p2a[idx];
    let feedbackHtml = '';
    if (saved) {
      const isCorrect = saved === o.level;
      feedbackHtml = `
        <div class="fb ${isCorrect ? 'fb-ok' : 'fb-no'}">
          <strong>${isCorrect ? '✓ Correct Alignment' : '✗ Structural Mismatch'}</strong> — ${o.explanation}
        </div>
      `;
    }

    div.innerHTML = `
      <div class="obj-meta">Sample Objective Case #${idx + 1}</div>
      <div class="obj-text">"${o.text}"</div>
      <div class="rbtn-row">
        <button class="rbtn g ${saved === 'Effective' ? 'sel' : ''}" data-v="Effective">Effective</button>
        <button class="rbtn m ${saved === 'Missing something' ? 'sel' : ''}" data-v="Missing something">Missing something</button>
      </div>
      <div class="fb-anchor">${feedbackHtml}</div>
    `;

    const btns = div.querySelectorAll('.rbtn');
    btns.forEach(b => {
      if (saved) b.disabled = true;
      b.onclick = () => {
        const val = b.getAttribute('data-v');
        S.p2a[idx] = val;
        if (val === o.level) S.p2s++;
        
        btns.forEach(btn => btn.disabled = true);
        b.classList.add('sel');
        
        const isCorrect = val === o.level;
        div.querySelector('.fb-anchor').innerHTML = `
          <div class="fb ${isCorrect ? 'fb-ok' : 'fb-no'}">
            <strong>${isCorrect ? '✓ Correct Alignment' : '✗ Structural Mismatch'}</strong> — ${o.explanation}
          </div>
        `;
        
        document.getElementById('p2Score').innerText = S.p2s;
        if (Object.keys(S.p2a).length === OBJECTIVES.length) {
          document.getElementById('p2DoneBtn').disabled = false;
        }
      };
    });
    list.appendChild(div);
  });

  document.getElementById('p2DoneBtn').onclick = () => {
    if (!S.done.includes(2)) S.done.push(2);
    S.p3weak = OBJECTIVES.filter((o, idx) => S.p2a[idx] && S.p2a[idx] !== 'Effective');
    if (S.p3weak.length === 0) {
      S.p3weak = OBJECTIVES.filter(o => o.level !== 'Effective');
    }
    S.p3idx = 0;
    go(3);
  };
}

/* ══════════════════════════════════════════
   PHASE 3: REWRITE LAB (COLOR-CODED LOCAL DIAGNOSTICS)
   ══════════════════════════════════════════ */
function renderP3(root) {
  root.innerHTML = `
    <div class="phase-eyebrow">Phase 3 of 5 · Engineering Lab</div>
    <h2 class="phase-title">Structural Re-Engineering Workshop</h2>
    <p class="phase-desc">Overhaul weak objective frameworks into high-performance milestones. Pass <strong>at least two entries</strong> to clear this phase checkpoint.</p>
  `;

  // Progress Indicators
  const prog = document.createElement('div');
  prog.className = 'p3-progress';
  const dotsWrap = document.createElement('div');
  dotsWrap.className = 'p3-dots';
  S.p3weak.forEach((_, i) => {
    const dot = document.createElement('div');
    dot.className = `p3-dot ${S.p3idx === i ? 'active' : S.p3approved[i] ? 'done' : 'pending'}`;
    dot.innerText = i + 1;
    dot.style.cursor = 'pointer';
    dot.onclick = () => { S.p3idx = i; S.p3checkpoint = false; go(3); };
    dotsWrap.appendChild(dot);
  });
  prog.appendChild(dotsWrap);

  const countApproved = Object.keys(S.p3approved).length;
  const statusTxt = document.createElement('span');
  statusTxt.className = 'card-counter';
  statusTxt.innerHTML = `⚙️ Modules Restructured: <strong>${countApproved} / 2</strong> required`;
  prog.appendChild(statusTxt);
  root.appendChild(prog);

  if (S.p3checkpoint) {
    renderP3Checkpoint(root, countApproved);
    return;
  }

  const currentWeakObj = S.p3weak[S.p3idx];
  
  // Work Area Layout
  const container = document.createElement('div');
  container.className = 'p3-lab-container';
  
  // Original Target Box
  const objBox = document.createElement('div');
  objBox.className = 'obj-box';
  objBox.style.margin = '0';
  objBox.innerHTML = `
    <div class="obj-box-label">Original Baseline Goal Case #${S.p3idx + 1}</div>
    <div><span class="obj-box-badge badge-m">${currentWeakObj.level}</span></div>
    <div class="obj-box-text">"${currentWeakObj.text}"</div>
  `;
  container.appendChild(objBox);

  // Active Diagnostics Dashboard Panel
  const panel = document.createElement('div');
  panel.className = 'p3-panel';
  
  const currentAttempt = S.p3attempts[S.p3idx] || "";
  const isApproved = S.p3approved[S.p3idx];

  panel.innerHTML = `
    <div class="obj-box-label" style="margin-bottom:8px;">Your Redesigned Calibration Variant</div>
    <textarea class="chat-in" id="p3DraftArea" style="width:100%; min-height:80px; margin-bottom:1rem; font-size:15px;" 
      placeholder="Type your improved objective variant here... (e.g. 'Students will be able to use...')" 
      ${isApproved ? 'disabled' : ''}>${currentAttempt}</textarea>
    
    <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:1rem;">
      <div id="p3ScoreBadge" style="font-weight:700; font-size:14px;">Architectural Clearance: Evaluating...</div>
      <button class="btn btn-p btn-sm" id="p3VerifyBtn" ${isApproved ? 'disabled' : ''}>${isApproved ? 'Calibrated ✓' : 'Run Quality Diagnostic Audit'}</button>
    </div>
    
    <div id="p3DiagnosticsDashboard"></div>
  `;
  container.appendChild(panel);
  root.appendChild(container);

  // Bottom Navigation Row
  const navRow = document.createElement('div');
  navRow.className = 'card-nav';
  navRow.style.marginTop = '1.5rem';
  
  const prevBtn = document.createElement('button');
  prevBtn.className = 'btn';
  prevBtn.innerText = '← Previous Case';
  prevBtn.disabled = S.p3idx === 0;
  prevBtn.onclick = () => { S.p3idx--; go(3); };

  const nextBtn = document.createElement('button');
  nextBtn.className = 'btn btn-p';
  nextBtn.innerText = S.p3idx === S.p3weak.length - 1 ? 'Go to Verification Checkpoint' : 'Next Case →';
  nextBtn.onclick = () => {
    if (S.p3idx < S.p3weak.length - 1) {
      S.p3idx++;
      go(3);
    } else {
      S.p3checkpoint = true;
      go(3);
    }
  };
  navRow.appendChild(prevBtn);
  navRow.appendChild(nextBtn);
  root.appendChild(navRow);

  // Diagnostic Updater Function
  const txtArea = document.getElementById('p3DraftArea');
  const dash = document.getElementById('p3DiagnosticsDashboard');
  const sBadge = document.getElementById('p3ScoreBadge');
  const verifyBtn = document.getElementById('p3VerifyBtn');

  const updateDashboard = (showFeedback = false) => {
    const analysis = parseObjectiveQuality(txtArea.value);
    
    let statusColor = analysis.score >= 7 ? "var(--green)" : analysis.score >= 5 ? "var(--amber)" : "var(--coral)";
    sBadge.innerHTML = `Architectural Rating: <span style="color:${statusColor}">${analysis.score} / 8</span>`;
    
    if (!showFeedback && !isApproved) {
      dash.innerHTML = `<p style="color:var(--text3); font-style:italic; font-size:13px;">Modify text components and click run audit to parse quality variables...</p>`;
      return;
    }

    if (analysis.score >= 7 && showFeedback && !isApproved) {
      S.p3approved[S.p3idx] = true;
      S.p3attempts[S.p3idx] = txtArea.value;
      setTimeout(() => go(3), 1200);
    }

    let goodListHtml = analysis.good.map(g => `<li><span style="color:var(--green)">✔</span> <span>${g}</span></li>`).join('');
    if (!goodListHtml) goodListHtml = `<li style="color:var(--text3); font-style:italic;">No target anchors validated yet.</li>`;

    let missingListHtml = analysis.missing.map(m => `<li><span style="color:var(--coral)">✦</span> <span>${m}</span></li>`).join('');
    if (!missingListHtml) missingListHtml = `<li style="color:var(--green); font-weight:600;">✨ All primary lesson parameters met!</li>`;

    dash.innerHTML = `
      <div class="diag-grid">
        <div class="diag-card good">
          <h4>🟩 In a Good Place</h4>
          <ul class="diag-list">${goodListHtml}</ul>
        </div>
        <div class="diag-card missing">
          <h4>🟧 Needs Improvement / Missing</h4>
          <ul class="diag-list">${missingListHtml}</ul>
        </div>
      </div>
      ${S.p3approved[S.p3idx] ? `
        <div class="fb fb-ok" style="margin-top:1rem;">
          <strong>✨ Architectural Target Validated!</strong> This blueprint meets all target educational metrics and has been locked.
        </div>
      ` : ''}
    `;
  };

  // Trigger base view configuration on screen render
  updateDashboard(isApproved);

  txtArea.oninput = () => {
    S.p3attempts[S.p3idx] = txtArea.value;
  };

  verifyBtn.onclick = () => {
    updateDashboard(true);
  };
}

function renderP3Checkpoint(root, approvedCount) {
  const box = document.createElement('div');
  box.className = 'checkpoint-box';
  
  if (approvedCount >= 2) {
    box.innerHTML = `
      <h3 style="color:var(--teal); font-size:20px; margin-bottom:0.5rem;">✨ Structural Checkpoint Cleared</h3>
      <p style="font-size:14px; color:var(--text2);">You have successfully optimized ${approvedCount} objectives. Your pedagogical foundations are stable.</p>
      <div class="checkpoint-btns">
        <button class="btn" id="cpBack">Return to Lab</button>
        <button class="btn btn-p" id="cpNext">Advance to Phase 4 Blueprinting →</button>
      </div>
    `;
  } else {
    box.innerHTML = `
      <h3 style="color:var(--coral); font-size:20px; margin-bottom:0.5rem;">⚠️ System Standards Alert</h3>
      <p style="font-size:14px; color:var(--text2);">You have verified <strong>${approvedCount} / 2</strong> objectives. Please optimize at least two samples to verify full procedural readiness.</p>
      <div class="checkpoint-btns">
        <button class="btn btn-p" id="cpBack">Return to Workshop</button>
      </div>
    `;
  }
  root.appendChild(box);

  document.getElementById('cpBack').onclick = () => { S.p3checkpoint = false; go(3); };
  const next = document.getElementById('cpNext');
  if (next) {
    next.onclick = () => {
      if (!S.done.includes(3)) S.done.push(3);
      go(4);
    };
  }
}

/* ══════════════════════════════════════════
   PHASE 4: LOCAL TUTOR COMPILER
   ══════════════════════════════════════════ */
function renderP4(root) {
  root.innerHTML = `
    <div class="phase-eyebrow">Phase 4 of 5 · Blueprint Production</div>
    <h2 class="phase-title">Local Lesson Blueprint Architecture</h2>
    <p class="phase-desc">Apply your training. Draft your lesson framework below. The integrated local writing tutor will parse your structural layout in real time.</p>
    
    <div style="display: flex; gap: 20px; flex-wrap: wrap; margin-top: 1.5rem;">
      <!-- Left Input Panel -->
      <div style="flex: 1; min-width: 300px; display: flex; flex-direction: column; gap: 1rem;">
        <div class="ctx-box" style="margin:0;">
          <strong>Target Operational Profile Workspace:</strong> State your target level and lesson topic (e.g., <em>B2 Level - Job Interviews</em>).
        </div>
        <textarea class="chat-in" id="p4Context" rows="2" placeholder="Course Name, Level, and Target Topic..."></textarea>
        
        <div class="obj-box-label" style="margin-top:0.5rem;">Draft Lesson Objective:</div>
        <textarea class="chat-in" id="p4ObjectiveInput" style="min-height: 120px;" placeholder="Students will be able to..."></textarea>
      </div>
      
      <!-- Right Live Feedback Diagnostics Terminal -->
      <div style="flex: 1; min-width: 300px; background: var(--bg2); border: 0.5px solid var(--border2); border-radius: var(--radius-lg); padding: 1.25rem;">
        <div style="font-size:12px; font-weight:600; text-transform:uppercase; color:var(--text3); margin-bottom:0.5rem; letter-spacing:0.05em;">
          🩺 Live Tutor Diagnostics
        </div>
        <div id="tutorFeedbackPanel" style="font-size: 14px;">
          <p style="color:var(--text3); font-style: italic;">Awaiting structural input layout string...</p>
        </div>
      </div>
    </div>

    <div class="card-nav" style="margin-top: 2rem; border-top: 0.5px solid var(--border2); padding-top: 1rem;">
      <div></div>
      <button class="btn btn-p" id="p4ExportBtn">Commit Layout & Advance to Phase 5 →</button>
    </div>
  `;

  const inputArea = document.getElementById('p4ObjectiveInput');
  const contextArea = document.getElementById('p4Context');
  const feedbackPanel = document.getElementById('tutorFeedbackPanel');

  const runDiagnostics = () => {
    const analysis = parseObjectiveQuality(inputArea.value);
    
    let goodListHtml = analysis.good.map(g => `<li><span style="color:var(--green)">✔</span> ${g}</li>`).join('');
    let missingListHtml = analysis.missing.map(m => `<li><span style="color:var(--coral)">✦</span> ${m}</li>`).join('');
    
    feedbackPanel.innerHTML = `
      <div style="margin-bottom:8px; font-weight:bold; font-size:15px;">Structural Score: ${analysis.score}/8</div>
      <div style="display:flex; flex-direction:column; gap:8px; margin-top:10px;">
        <div style="color:var(--green); font-size:13px;"><strong>Good Elements:</strong><ul style="padding-left:15px; margin-top:4px;">${goodListHtml || '<li>None</li>'}</ul></div>
        <div style="color:var(--amber); font-size:13px;"><strong>Missing Elements:</strong><ul style="padding-left:15px; margin-top:4px;">${missingListHtml || '<li>Perfect Calibration achieved!</li>'}</ul></div>
      </div>
    `;
  };

  inputArea.oninput = runDiagnostics;

  document.getElementById('p4ExportBtn').onclick = () => {
    if (!inputArea.value.trim()) {
      alert("Please compile your primary lesson objectives before finalizing pipeline vectors.");
      return;
    }
    
    S.c4 = [
      { role: 'user', content: `Context Strategy Profile: ${contextArea.value}` },
      { role: 'user', content: `Compiled Lesson Outcome: ${inputArea.value}` },
      { role: 'assistant', content: `Local evaluation optimization run complete.` }
    ];

    if (!S.done.includes(4)) S.done.push(4);
    go(5);
  };
}

/* ══════════════════════════════════════════
   PHASE 5: PEER REVIEW EXCHANGE
   ══════════════════════════════════════════ */
function renderP5(root) {
  root.innerHTML = `
    <div class="phase-eyebrow">Phase 5 of 5 · Peer Audit</div>
    <h2 class="phase-title">Peer Review Exchange Terminal</h2>
    <p class="phase-desc">Evaluate objective submissions from colleagues in the CTJ ecosystem. Diagnose their structural adjustments or log peer feedback notes.</p>
    
    <div class="move-legend">
      <div class="move-legend-item" style="background:var(--purple-l); color:var(--purple);">
        <strong>❓ Clarification Question</strong> Ask for context, level info, or structural mechanics parameters.
      </div>
      <div class="move-legend-item" style="background:var(--blue-l); color:var(--blue);">
        <strong>💡 Critical Celebration</strong> Detail why the objective works or highlight its specific, measurable components.
      </div>
      <div class="move-legend-item" style="background:var(--teal-l); color:var(--teal);">
        <strong>⚡ Restructuring Hint</strong> Propose an active action verb swap or contextual framework extension.
      </div>
    </div>
  `;

  PEERS.forEach((p, idx) => {
    const card = document.createElement('div');
    card.className = 'peer-card';
    
    const isSent = S.ps[idx];
    let actionAreaHtml = '';

    if (isSent) {
      let moveLabel = S.pm[idx] === 'q' ? 'Clarification Question' : S.pm[idx] === 'c' ? 'Critical Celebration' : 'Restructuring Hint';
      actionAreaHtml = `
        <div style="margin-top:1rem; border-top:0.5px solid var(--border2); padding-top:0.75rem;">
          <div style="margin-bottom:0.5rem;"><span class="sent-badge">✓ Feedback Transmitted</span></div>
          <div style="font-size:12px; color:var(--text2); margin-bottom:2px;"><strong>Move Profile Vector:</strong> ${moveLabel}</div>
          <div style="font-size:13px; font-style:italic; background:var(--bg2); padding:0.5rem; border-radius:4px;">"${S.pt[idx]}"</div>
        </div>
      `;
    } else {
      actionAreaHtml = `
        <div class="mv-row">
          <button class="mvbtn q ${S.pm[idx] === 'q' ? 'sel' : ''}" data-m="q">❓ Clarification</button>
          <button class="mvbtn p5-c-btn ${S.pm[idx] === 'c' ? 'sel' : ''}" data-m="c" style="border-color:var(--blue); color:var(--blue);">💡 Celebrate</button>
          <button class="mvbtn s ${S.pm[idx] === 's' ? 'sel' : ''}" data-m="s">⚡ Hint Suggestion</button>
        </div>
        <textarea class="peer-ta" id="ta-${idx}" placeholder="Formulate professional development commentary node here..."></textarea>
        <button class="btn btn-p btn-sm" id="send-${idx}" disabled>Transmit Peer Review Feedback</button>
      `;
    }

    card.innerHTML = `
      <div class="peer-hd">
        <div class="av" style="background:${p.bg}; color:${p.c}">${p.ini}</div>
        <div>
          <div style="font-size:14px; font-weight:600;">${p.name}</div>
          <div style="font-size:12px; color:var(--text3);">${p.level}</div>
        </div>
      </div>
      <div class="peer-obj">"${p.obj}"</div>
      <div class="action-anchor">${actionAreaHtml}</div>
    `;

    root.appendChild(card);

    if (!isSent) {
      const pTa = card.querySelector(`#ta-${idx}`);
      const pBtn = card.querySelector(`#send-${idx}`);
      const mBtns = card.querySelectorAll('.mvbtn');

      if (S.pt[idx]) pTa.value = S.pt[idx];
      if (S.pm[idx] && S.pt[idx]) pBtn.disabled = false;

      mBtns.forEach(b => {
        b.onclick = () => {
          mBtns.forEach(btn => btn.classList.remove('sel'));
          b.classList.add('sel');
          S.pm[idx] = b.getAttribute('data-m');
          if (pTa.value.trim()) pBtn.disabled = false;
        };
      });

      pTa.oninput = () => {
        S.pt[idx] = pTa.value;
        pBtn.disabled = !(S.pm[idx] && pTa.value.trim());
      };

      pBtn.onclick = () => {
        S.ps[idx] = true;
        if (!S.done.includes(5)) S.done.push(5);
        go(5);
      };
    }
  });

  const footerRow = document.createElement('div');
  footerRow.className = 'card-nav';
  footerRow.style.marginTop = '2rem';
  
  const compBtn = document.createElement('button');
  compBtn.className = 'btn btn-p';
  compBtn.innerText = 'Compile Module Evaluation Grid →';
  compBtn.disabled = Object.keys(S.ps).length < 2; 
  
  footerRow.appendChild(document.createElement('div'));
  footerRow.appendChild(compBtn);
  root.appendChild(footerRow);

  compBtn.onclick = () => { go(6); };
}

/* ══════════════════════════════════════════
   COMPLETION SUMMARY
   ══════════════════════════════════════════ */
function renderComplete(root) {
  root.innerHTML = `
    <div style="text-align:center; padding:2rem 0;">
      <span style="font-size:48px;">🏆</span>
      <h2 class="phase-title" style="font-size:28px; margin-top:1rem;">Module Clearance Confirmed</h2>
      <p class="phase-desc" style="max-width:580px; margin:0 auto 1.5rem;">Congratulations! You have completed the Casa Thomas Jefferson Goal-Setting professional development program.</p>
    </div>
    
    <div class="divider"></div>
    
    <h3 style="font-size:16px; font-weight:600; margin-bottom:1rem;">Your Program Performance Telemetry Matrix</h3>
    <div class="stat-row">
      <div class="stat"><div class="stat-v">${S.p2s} / 20</div><div class="stat-l">Audit Matches Verified</div></div>
      <div class="stat"><div class="stat-v">${Object.keys(S.p3approved).length}</div><div class="stat-l">Lab Goals Rewritten</div></div>
      <div class="stat"><div class="stat-v">${Object.keys(S.ps).length}</div><div class="stat-l">Peer Appraisals Logged</div></div>
    </div>
    
    <div class="divider"></div>
    
    <h3 style="font-size:16px; font-weight:600; margin-bottom:0.75rem;">Your Live Lesson Architecture Plan</h3>
    <div class="concept-card" style="background:var(--bg2); border:none; padding:1.25rem;">
      <div id="p4LogDump" style="font-size:14px; white-space:pre-wrap; line-height:1.6; max-height:250px; overflow-y:auto; color:var(--text2);"></div>
    </div>
    
    <div style="margin-top:2.5rem; text-align:center;">
      <button class="btn" id="restartGameBtn" style="border-color:var(--blue-m); color:var(--blue-m);">Reset Telemetry Data & Re-run Module</button>
    </div>
  `;

  const dump = document.getElementById('p4LogDump');
  if (S.c4 && S.c4.length > 0) {
    dump.textContent = S.c4.map(m => `${m.role === 'user' ? '► Data Input' : '⚡ Local System Analysis'}:\n${m.content}\n`).join('\n');
  } else {
    dump.textContent = "No Blueprint logs captured in session telemetry buffers.";
  }

  document.getElementById('restartGameBtn').onclick = () => {
    if (confirm("Are you sure you want to flush all custom text buffers and session progress metrics?")) {
      S = {
        ph:1, ci:0, p2a:{}, p2s:0,
        p3weak:[], p3idx:0, p3attempts:{}, p3approved:{}, done:[]
      };
      go(1);
    }
  };
}

/* Initialize app on load */
window.addEventListener('DOMContentLoaded', () => {
  go(1);
});
</script>
</body>
</html>
