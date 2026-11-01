# MyFitness
<!doctype html>
<html lang="de">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#111318">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Fitness Tracker">
<title>Fitness Tracker</title>
<style>
:root{
  color-scheme:dark;
  --bg:#111318;
  --panel:#1d222b;
  --input:#28313f;
  --text:#f8fafc;
  --muted:#bdc8d7;
  --line:#ffffff30;
  --blue:#2563eb;
  --green:#176347;
  --purple:#493274;
  --orange:#80501e;
  --red:#743040;
  --teal:#155d63;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;
  background:var(--bg);
  color:var(--text);
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Arial,sans-serif;
  font-size:15px;
}
header{
  background:#1b2028;
  padding:25px 17px 20px;
  border-bottom:1px solid #ffffff20;
}
header h1{font-size:27px;margin:0 0 7px}
header p{color:var(--muted);margin:0;font-size:13px}
main{
  max-width:850px;
  margin:auto;
  padding:14px 13px 40px;
}
.card{
  border-radius:17px;
  padding:18px;
  margin-bottom:15px;
  overflow:hidden;
}
h2{font-size:20px;margin:0 0 14px}
h3{font-size:17px;margin:12px 0}
p{line-height:1.5}
small,.muted{font-size:13px;color:#e2e8f0}
label{
  display:block;
  font-size:13px;
  font-weight:600;
  margin-bottom:9px;
}
input,select,textarea{
  display:block;
  width:100%;
  background:var(--input);
  color:white;
  border:1px solid #758197;
  border-radius:10px;
  padding:11px 12px;
  margin-top:5px;
  font:inherit;
  font-size:16px;
  min-width:0;
}
textarea{min-height:70px;resize:vertical}
input::placeholder,textarea::placeholder{color:#aebaca}
button{
  border:0;
  border-radius:10px;
  padding:11px 13px;
  background:#2b75ef;
  color:white;
  font-size:14px;
  font-weight:600;
  cursor:pointer;
}
button:disabled{opacity:.45}
button:active{transform:scale(.98)}
button.secondary{background:#e3eaf5;color:#1b293d}
button.danger{background:#ffe0e5;color:#991b36}
button.purple{background:#8a5cf0}
button.dark{background:#ffffff20;color:white}
button.small{padding:8px 10px;font-size:12px}
.row{display:flex;align-items:center;gap:8px;flex-wrap:wrap}
.between{justify-content:space-between}
.actions{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
.fields{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:9px;
}
.full{grid-column:1/-1}
.hidden{display:none!important}
.divider{height:1px;background:var(--line);margin:16px 0}
.notice{
  padding:12px;
  border-radius:11px;
  background:#ffffff1b;
  line-height:1.5;
  margin:10px 0;
}
#dashboard{background:#173d78}
#training{background:#19543b}
#history{background:#665414}
#exercises{background:#493274}
#bodyweight{background:#754018}
#progress{background:#175c61}
#backup{background:#58402f}
#settings{background:#30343d}
.statgrid{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:9px;
}
.stat{
  padding:13px;
  background:#ffffff20;
  border-radius:12px;
}
.stat small{display:block}
.stat strong{display:block;font-size:23px;margin:8px 0 2px}
.entry,.exercise-row,.weight-row{
  border-bottom:1px solid var(--line);
  padding:12px 0;
}
.entry:last-child,.exercise-row:last-child,.weight-row:last-child{
  border-bottom:0;
}
.entry strong,.exercise-row strong{display:block}
.entry small,.exercise-row small{display:block;margin-top:5px}
.session-exercise{
  border:1px solid #ffffff4d;
  border-radius:13px;
  padding:13px;
  margin:12px 0;
  background:#00000016;
}
.set-header,.set-row{
  display:grid;
  grid-template-columns:36px minmax(0,1fr) minmax(0,1fr) 38px;
  gap:7px;
  align-items:center;
  margin:8px 0;
}
.set-header{font-size:12px;color:#e2e8f0}
.set-row input{margin:0;padding:10px 7px;text-align:center}
.set-number{text-align:center;font-weight:700}
.set-row button{padding:10px 0}
.exercise-picker{
  display:grid;
  grid-template-columns:1fr;
  gap:8px;
}
.exercise-picker button{text-align:left;background:#ffffff22}
.exercise-picker button.selected{
  background:#2d7bf1;
  outline:2px solid #b9d6ff;
}
.history-card{
  background:#ffffff18;
  padding:13px;
  border-radius:12px;
  margin:10px 0;
}
.history-card h3{margin:0 0 7px}
.history-exercise{
  border-top:1px solid #ffffff30;
  padding-top:9px;
  margin-top:9px;
}
.history-exercise strong{display:block}
.history-exercise small{display:block;margin-top:5px}
.chip{
  display:inline-block;
  background:#ffffff22;
  border-radius:8px;
  padding:6px 9px;
  margin:3px 4px 3px 0;
  font-size:12px;
}
.chart{
  width:100%;
  height:220px;
  background:#ffffff14;
  border-radius:12px;
  margin-top:10px;
}
.chart svg{width:100%;height:100%}
.empty{padding:13px 0;color:#e2e8f0;font-size:13px}
.progress-summary{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:9px;
}
.progress-summary div{
  background:#ffffff1c;
  padding:12px;
  border-radius:11px;
}
.progress-summary strong{display:block;font-size:20px;margin-top:5px}
footer{
  color:#9aa7b8;
  text-align:center;
  font-size:12px;
  padding:0 20px 25px;
}
@media(max-width:370px){
  .card{padding:13px}
  .set-header,.set-row{
    grid-template-columns:28px minmax(0,1fr) minmax(0,1fr) 34px;
    gap:5px;
  }
}
</style>
</head>
<body>
<header>
  <h1>Fitness Tracker</h1>
  <p>Mein Training · Meine Fortschritte · Mein Körpergewicht</p>
</header>

<main>

<section class="card" id="dashboard">
  <h2>Meine Übersicht</h2>
  <div class="statgrid">
    <div class="stat">
      <small>Trainingseinheiten</small>
      <strong id="statSessions">0</strong>
    </div>
    <div class="stat">
      <small>Trainingsübungen</small>
      <strong id="statExercises">0</strong>
    </div>
    <div class="stat">
      <small>Letztes Körpergewicht</small>
      <strong id="statWeight">–</strong>
    </div>
    <div class="stat">
      <small>Trainings diese Woche</small>
      <strong id="statWeek">0</strong>
    </div>
  </div>
  <div id="lastTraining" class="notice"></div>
  <button id="startTraining">+ Training starten</button>
</section>

<section class="card" id="training">
  <div class="row between">
    <h2 id="trainingTitle">Training erfassen</h2>
    <button id="newTraining" class="secondary small">Neues Training</button>
  </div>

  <div class="fields">
    <label>Trainingsdatum
      <input id="trainingDate" type="date">
    </label>
    <label>Körpergewicht (kg)
      <input id="trainingBodyweight" type="number" min="1" step="0.1" placeholder="z. B. 85.4">
    </label>
    <label class="full">Notizen (optional)
      <textarea id="trainingNotes" placeholder="z. B. gute Tagesform, wenig Schlaf"></textarea>
    </label>
  </div>

  <div class="divider"></div>
  <h3>Übungen in dieser Einheit</h3>
  <div id="trainingExercises"></div>

  <div class="divider"></div>
  <h3>Übung hinzufügen</h3>
  <input id="exerciseSearch" type="search" placeholder="Übung suchen ...">
  <div id="exercisePicker" class="exercise-picker"></div>

  <div class="actions">
    <button id="saveTraining">Training speichern</button>
    <button id="cancelTraining" class="secondary">Eingabe zurücksetzen</button>
  </div>
  <p class="muted">Gewicht und Wiederholungen werden für jeden Satz separat gespeichert. Bei der nächsten Einheit werden die Werte der letzten Einheit vorgeschlagen.</p>
</section>

<section class="card" id="history">
  <h2>Meine Trainingshistorie</h2>
  <div id="historyList"></div>
</section>

<section class="card" id="exercises">
  <div class="row between">
    <h2>Meine Übungen</h2>
    <button id="newExercise" class="secondary">+ Neue Übung</button>
  </div>
  <p class="muted">Hier verwaltest du deine Übungen. Gelöschte Übungen bleiben in bereits gespeicherten Trainingseinheiten erhalten.</p>

  <form id="exerciseForm" class="hidden">
    <div class="fields">
      <label class="full">Übungsname
        <input id="exerciseName" required placeholder="z. B. Kniebeugen">
      </label>
      <label>Muskelgruppe
        <select id="exerciseGroup">
          <option>Beine</option>
          <option>Brust</option>
          <option>Rücken</option>
          <option>Schultern</option>
          <option>Arme</option>
          <option>Bauch</option>
          <option>Ganzkörper</option>
          <option>Andere</option>
        </select>
      </label>
      <label>Art der Übung
        <select id="exerciseType">
          <option value="weight">Gewicht in kg</option>
          <option value="bodyweight">Körpergewicht</option>
        </select>
      </label>
    </div>
    <div class="actions">
      <button type="submit">Übung speichern</button>
      <button type="button" id="cancelExercise" class="secondary">Abbrechen</button>
    </div>
  </form>
  <div id="exerciseList"></div>
</section>

<section class="card" id="bodyweight">
  <h2>Mein Körpergewicht</h2>
  <form id="weightForm">
    <div class="fields">
      <label>Datum
        <input id="weightDate" type="date" required>
      </label>
      <label>Gewicht (kg)
        <input id="weightValue" type="number" min="1" step="0.1" placeholder="85.4" required>
      </label>
    </div>
    <button type="submit">Körpergewicht speichern</button>
  </form>
  <h3>Gewichtsverlauf</h3>
  <div id="weightChart" class="chart"></div>
  <div id="weightList"></div>
</section>

<section class="card" id="progress">
  <h2>Meine Trainingsfortschritte</h2>
  <label>Übung auswählen
    <select id="progressExercise"></select>
  </label>
  <div id="progressSummary" class="progress-summary"></div>
  <div id="exerciseChart" class="chart"></div>
  <p class="muted">Das Diagramm zeigt das Trainingsgewicht des schwersten Satzes pro Einheit. Bei Körpergewichtsübungen wird die höchste Wiederholungszahl angezeigt.</p>
  <div id="progressHistory"></div>
</section>

<section class="card" id="backup">
  <h2>Datensicherung</h2>
  <p class="muted">Deine Daten werden lokal auf diesem Gerät gespeichert. Ein JSON-Backup schützt dich vor Datenverlust und ermöglicht den Import auf einem anderen Gerät.</p>
  <div class="actions">
    <button id="exportBackup" class="secondary">Backup herunterladen</button>
    <button id="importBackup" class="secondary">Backup importieren</button>
    <input id="backupFile" type="file" accept=".json,application/json" class="hidden">
  </div>
</section>

<section class="card" id="settings">
  <h2>Informationen</h2>
  <p class="muted">Diese App funktioniert ohne Anmeldung und ohne externe Datenbank. Sie speichert deine Trainingseinheiten, Übungen und Körpergewichte im lokalen Speicher deines Browsers.</p>
  <p class="muted">Lösche keine Website-Daten und entferne die Home-Bildschirm-App nicht ohne vorheriges Backup. Ein öffentliches GitHub-Repository enthält nur den App-Code, nicht deine lokal gespeicherten Trainingsdaten.</p>
</section>

</main>

<footer>Fitness Tracker · Persönliches Trainingstagebuch</footer>

<script>
"use strict";

/* Speicherkennungen */
const EXERCISE_KEY="fitness_tracker_exercises_v1";
const SESSION_KEY="fitness_tracker_sessions_v1";
const BODYWEIGHT_KEY="fitness_tracker_bodyweights_v1";

const $=id=>document.getElementById(id);
const number=v=>Number(v);
const fmt=v=>Number(v).toLocaleString("de-CH",{
  maximumFractionDigits:2
});

function uid(){
  if(typeof crypto!=="undefined"&&crypto.randomUUID){
    return crypto.randomUUID();
  }
  return Date.now().toString(36)+
    Math.random().toString(36).slice(2);
}

function today(){
  const d=new Date();
  return d.getFullYear()+"-"+
    String(d.getMonth()+1).padStart(2,"0")+"-"+
    String(d.getDate()).padStart(2,"0");
}

function dateLabel(value){
  if(!value)return "Unbekannt";
  const p=value.split("-").map(Number);
  return new Date(p[0],p[1]-1,p[2],12)
    .toLocaleDateString("de-CH",{
      day:"2-digit",month:"2-digit",year:"numeric"
    });
}

function load(key,fallback){
  try{
    const v=JSON.parse(localStorage.getItem(key));
    return v===null?fallback:v;
  }catch{
    return fallback;
  }
}

const defaultExercises=[
  {id:"squat",name:"Kniebeugen",group:"Beine",type:"weight"},
  {id:"deadlift",name:"Kreuzheben",group:"Rücken",type:"weight"},
  {id:"bench",name:"Bankdrücken",group:"Brust",type:"weight"},
  {id:"pullup-under",name:"Klimmzüge Untergriff",group:"Rücken",type:"bodyweight"},
  {id:"pullup-over",name:"Klimmzüge Obergriff",group:"Rücken",type:"bodyweight"},
  {id:"pushup",name:"Liegestütze",group:"Brust",type:"bodyweight"},
  {id:"lateral",name:"Seitheben",group:"Schultern",type:"weight"},
  {id:"hammer",name:"Hammer Curls",group:"Arme",type:"weight"},
  {id:"australian",name:"Australian Pull-ups",group:"Rücken",type:"bodyweight"}
];

let exercises=load(EXERCISE_KEY,null);
let sessions=load(SESSION_KEY,[]);
let bodyweights=load(BODYWEIGHT_KEY,[]);

if(!Array.isArray(exercises)){
  exercises=defaultExercises.map(x=>({...x}));
}
if(!Array.isArray(sessions))sessions=[];
if(!Array.isArray(bodyweights))bodyweights=[];

let draft=[];
let editingSession=null;
let editingExercise=null;

function persist(){
  try{
    localStorage.setItem(EXERCISE_KEY,JSON.stringify(exercises));
    localStorage.setItem(SESSION_KEY,JSON.stringify(sessions));
    localStorage.setItem(BODYWEIGHT_KEY,JSON.stringify(bodyweights));
    return true;
  }catch(err){
    alert("Speichern fehlgeschlagen: "+err.message);
    return false;
  }
}

function makeButton(text,callback,cls=""){
  const b=document.createElement("button");
  b.type="button";
  b.className=cls;
  b.textContent=text;
  b.onclick=callback;
  return b;
}

function textEl(tag,text,cls=""){
  const el=document.createElement(tag);
  el.textContent=text;
  if(cls)el.className=cls;
  return el;
}

function getExercise(id){
  return exercises.find(e=>e.id===id);
}

function getPrevious(exerciseId,excludeId=null){
  const sorted=sessions
    .filter(s=>s.id!==excludeId&&
      s.exercises.some(e=>e.exerciseId===exerciseId))
    .sort((a,b)=>b.date.localeCompare(a.date));

  for(const s of sorted){
    const e=s.exercises.find(
      x=>x.exerciseId===exerciseId
    );
    if(e)return {session:s,exercise:e};
  }
  return null;
}

function exerciseSnapshot(e){
  return {
    exerciseId:e.id,
    name:e.name,
    group:e.group,
    type:e.type,
    sets:[]
  };
}

function addDraftExercise(id){
  const ex=getExercise(id);
  if(!ex)return;

  if(draft.some(d=>d.exerciseId===id)){
    alert("Diese Übung ist bereits im Training.");
    return;
  }

  const item=exerciseSnapshot(ex);
  const previous=getPrevious(id,editingSession);

  if(previous){
    item.sets=previous.exercise.sets.map(s=>({
      id:uid(),
      kg:s.kg===null?"":String(s.kg),
      reps:String(s.reps)
    }));
  }else{
    item.sets=[
      {id:uid(),kg:ex.type==="bodyweight"?"0":"",reps:""}
    ];
  }

  draft.push(item);
  renderDraft();
  renderExercisePicker();
}

function renderExercisePicker(){
  const box=$("exercisePicker");
  box.replaceChildren();
  const query=$("exerciseSearch").value.trim().toLowerCase();

  const found=exercises
    .filter(e=>e.name.toLowerCase().includes(query))
    .sort((a,b)=>a.name.localeCompare(b.name,"de"));

  if(!found.length){
    box.append(textEl("p","Keine Übungen gefunden.","empty"));
  }

  for(const ex of found){
    const exists=draft.some(d=>d.exerciseId===ex.id);
    const b=makeButton(
      (exists?"✓ ":"+ ")+ex.name+" · "+ex.group,
      ()=>addDraftExercise(ex.id),
      exists?"selected":""
    );
    b.disabled=exists;
    box.append(b);
  }
}

function renderDraft(){
  const box=$("trainingExercises");
  box.replaceChildren();

  if(!draft.length){
    box.append(textEl(
      "p","Noch keine Übungen hinzugefügt.","empty"
    ));
  }

  draft.forEach((ex,index)=>{
    const card=document.createElement("div");
    card.className="session-exercise";

    const head=document.createElement("div");
    head.className="row between";
    head.append(
      textEl("strong",ex.name),
      makeButton("Entfernen",()=>{
        draft.splice(index,1);
        renderDraft();
        renderExercisePicker();
      },"danger small")
    );
    card.append(head);

    const previous=getPrevious(ex.exerciseId,editingSession);
    if(previous){
      const details=previous.exercise.sets
        .map(s=>`${fmt(s.kg||0)} kg × ${fmt(s.reps)}`)
        .join(" · ");
      card.append(textEl(
        "p",
        "Letztes Training ("+
          dateLabel(previous.session.date)+"): "+details,
        "muted"
      ));
    }else{
      card.append(textEl(
        "p","Noch keine vorherige Einheit.","muted"
      ));
    }

    const labels=document.createElement("div");
    labels.className="set-header";
    ["Satz","Gewicht (kg)","Wdh.",""].forEach(t=>{
      labels.append(textEl("span",t));
    });
    card.append(labels);

    ex.sets.forEach((s,i)=>{
      const row=document.createElement("div");
      row.className="set-row";
      row.append(textEl("span",String(i+1)+".","set-number"));

      const kg=document.createElement("input");
      kg.type="number";
      kg.min="0";
      kg.step="0.5";
      kg.placeholder=ex.type==="bodyweight"?"0":"kg";
      kg.value=s.kg;
      kg.setAttribute("aria-label","Gewicht Satz "+(i+1));
      kg.oninput=()=>s.kg=kg.value;

      const reps=document.createElement("input");
      reps.type="number";
      reps.min="1";
      reps.step="1";
      reps.placeholder="Wdh.";
      reps.value=s.reps;
      reps.setAttribute("aria-label","Wiederholungen Satz "+(i+1));
      reps.oninput=()=>s.reps=reps.value;

      row.append(kg,reps,makeButton("×",()=>{
        ex.sets.splice(i,1);
        renderDraft();
      },"danger small"));
      card.append(row);
    });

    const add=makeButton("+ Satz hinzufügen",()=>{
      const last=ex.sets[ex.sets.length-1];
      ex.sets.push({
        id:uid(),
        kg:last?last.kg:(ex.type==="bodyweight"?"0":""),
        reps:""
      });
      renderDraft();
    },"secondary small");

    card.append(add);
    box.append(card);
  });
}

function resetTraining(){
  editingSession=null;
  draft=[];
  $("trainingDate").value=today();
  $("trainingBodyweight").value="";
  $("trainingNotes").value="";
  $("trainingTitle").textContent="Training erfassen";
  $("saveTraining").textContent="Training speichern";
  $("exerciseSearch").value="";
  renderDraft();
  renderExercisePicker();
}

function editTraining(id){
  const s=sessions.find(x=>x.id===id);
  if(!s)return;

  editingSession=id;
  $("trainingDate").value=s.date;
  $("trainingBodyweight").value=s.bodyweight??"";
  $("trainingNotes").value=s.notes||"";
  $("trainingTitle").textContent="Training bearbeiten";
  $("saveTraining").textContent="Änderungen speichern";

  draft=s.exercises.map(e=>({
    ...e,
    sets:e.sets.map(x=>({
      id:uid(),
      kg:x.kg===null?"":String(x.kg),
      reps:String(x.reps)
    }))
  }));

  renderDraft();
  renderExercisePicker();
  $("training").scrollIntoView({behavior:"smooth"});
}

function saveTraining(){
  const date=$("trainingDate").value;
  if(!date){
    alert("Bitte Trainingsdatum eingeben.");
    return;
  }

  if(!draft.length){
    alert("Bitte mindestens eine Übung hinzufügen.");
    return;
  }

  const result=[];

  for(const ex of draft){
    if(!ex.sets.length){
      alert(ex.name+": Bitte mindestens einen Satz eingeben.");
      return;
    }

    const sets=[];

    for(const s of ex.sets){
      const kg=number(s.kg);
      const reps=number(s.reps);

      if(
        String(s.kg).trim()===""||
        String(s.reps).trim()===""||
        !Number.isFinite(kg)||
        !Number.isInteger(reps)||
        kg<0||reps<1
      ){
        alert(ex.name+": Bitte alle Sätze korrekt ausfüllen.");
        return;
      }
      sets.push({kg,reps});
    }

    result.push({
      exerciseId:ex.exerciseId,
      name:ex.name,
      group:ex.group,
      type:ex.type,
      sets
    });
  }

  const bwText=$("trainingBodyweight").value.trim();
  const bw=bwText===""?null:Number(bwText);

  if(bw!==null&&(!Number.isFinite(bw)||bw<=0)){
    alert("Bitte gültiges Körpergewicht eingeben.");
    return;
  }

  const id=editingSession||uid();

  const session={
    id,
    date,
    bodyweight:bw,
    notes:$("trainingNotes").value.trim(),
    exercises:result
  };

  const previousSessions=sessions;
  const previousWeights=bodyweights;

  if(editingSession){
    sessions=sessions.map(s=>s.id===id?session:s);
  }else{
    sessions.push(session);
  }

  // Körpergewicht aus der Trainingseinheit synchronisieren
  bodyweights=bodyweights.filter(w=>w.sessionId!==id);

  if(bw!==null){
    bodyweights.push({
      id:uid(),
      sessionId:id,
      date,
      weight:bw
    });
  }

  if(!persist()){
    sessions=previousSessions;
    bodyweights=previousWeights;
    return;
  }

  resetTraining();
  renderAll();
  alert("Training erfolgreich gespeichert.");
}

function deleteTraining(id){
  const s=sessions.find(x=>x.id===id);
  if(!s)return;

  if(!confirm(
    "Training vom "+dateLabel(s.date)+" wirklich löschen?"
  ))return;

  sessions=sessions.filter(x=>x.id!==id);
  bodyweights=bodyweights.filter(x=>x.sessionId!==id);

  if(editingSession===id)resetTraining();

  persist();
  renderAll();
}

function renderHistory(){
  const box=$("historyList");
  box.replaceChildren();

  const sorted=[...sessions].sort(
    (a,b)=>b.date.localeCompare(a.date)
  );

  if(!sorted.length){
    box.append(textEl(
      "p","Noch keine Trainingseinheiten gespeichert.","empty"
    ));
    return;
  }

  for(const s of sorted){
    const card=document.createElement("div");
    card.className="history-card";
    card.append(textEl("h3",dateLabel(s.date)));

    const meta=[
      s.exercises.length+" Übungen",
      s.bodyweight!==null&&s.bodyweight!==undefined
        ?"Körpergewicht "+fmt(s.bodyweight)+" kg":null
    ].filter(Boolean).join(" · ");

    card.append(textEl("small",meta));

    for(const ex of s.exercises){
      const section=document.createElement("div");
      section.className="history-exercise";
      section.append(textEl("strong",ex.name));
      section.append(textEl(
        "small",
        ex.sets.map((set,i)=>
          `${i+1}. Satz: ${fmt(set.kg)} kg × ${fmt(set.reps)} Wdh.`
        ).join(" · ")
      ));
      card.append(section);
    }

    if(s.notes){
      card.append(textEl("p","Notiz: "+s.notes,"muted"));
    }

    const actions=document.createElement("div");
    actions.className="actions";
    actions.append(
      makeButton("Bearbeiten",()=>editTraining(s.id),"secondary small"),
      makeButton("Löschen",()=>deleteTraining(s.id),"danger small")
    );

    card.append(actions);
    box.append(card);
  }
}

function openExerciseForm(ex=null){
  editingExercise=ex?ex.id:null;
  $("exerciseName").value=ex?.name||"";
  $("exerciseGroup").value=ex?.group||"Beine";
  $("exerciseType").value=ex?.type||"weight";
  $("exerciseForm").classList.remove("hidden");
  $("exerciseForm").scrollIntoView({
    behavior:"smooth",block:"nearest"
  });
}

function renderExercises(){
  const box=$("exerciseList");
  box.replaceChildren();

  const sorted=[...exercises].sort((a,b)=>
    a.name.localeCompare(b.name,"de")
  );

  for(const ex of sorted){
    const row=document.createElement("div");
    row.className="exercise-row";

    const name=textEl("strong",ex.name);
    const info=textEl(
      "small",
      ex.group+" · "+
      (ex.type==="bodyweight"?"Körpergewicht":"Gewicht in kg")
    );

    const actions=document.createElement("div");
    actions.className="actions";
    actions.append(
      makeButton("Bearbeiten",()=>openExerciseForm(ex),
        "secondary small"),
      makeButton("Löschen",()=>{
        if(!confirm(
          "Übung „"+ex.name+"“ löschen? Alte Trainings bleiben erhalten."
        ))return;
        exercises=exercises.filter(e=>e.id!==ex.id);
        persist();
        renderAll();
      },"danger small")
    );

    row.append(name,info,actions);
    box.append(row);
  }
}

function saveExercise(event){
  event.preventDefault();

  const name=$("exerciseName").value.trim();
  if(!name)return;

  const ex={
    id:editingExercise||uid(),
    name,
    group:$("exerciseGroup").value,
    type:$("exerciseType").value
  };

  if(editingExercise){
    exercises=exercises.map(x=>
      x.id===editingExercise?ex:x
    );
  }else{
    exercises.push(ex);
  }

  editingExercise=null;
  $("exerciseForm").classList.add("hidden");
  persist();
  renderAll();
}

function saveWeight(event){
  event.preventDefault();

  const date=$("weightDate").value;
  const weight=Number($("weightValue").value);

  if(!date||!Number.isFinite(weight)||weight<=0){
    alert("Bitte gültige Angaben eingeben.");
    return;
  }

  bodyweights.push({
    id:uid(),
    date,
    weight,
    sessionId:null
  });

  persist();
  $("weightValue").value="";
  renderAll();
}

function renderWeights(){
  const box=$("weightList");
  box.replaceChildren();

  const sorted=[...bodyweights].sort(
    (a,b)=>b.date.localeCompare(a.date)
  );

  if(!sorted.length){
    box.append(textEl(
      "p","Noch keine Körpergewichte gespeichert.","empty"
    ));
  }

  for(const w of sorted){
    const row=document.createElement("div");
    row.className="weight-row";

    const info=document.createElement("div");
    info.append(
      textEl("strong",fmt(w.weight)+" kg"),
      textEl("small",
        dateLabel(w.date)+
        (w.sessionId?" · Training":" · Separater Eintrag")
      )
    );

    const actions=document.createElement("div");
    actions.className="actions";

    actions.append(
      makeButton("Bearbeiten",()=>{
        const value=prompt(
          "Körpergewicht in kg",String(w.weight)
        );
        if(value===null)return;

        const parsed=Number(value.replace(",","."));
        if(!Number.isFinite(parsed)||parsed<=0){
          alert("Ungültiges Körpergewicht.");
          return;
        }

        w.weight=parsed;

        if(w.sessionId){
          const s=sessions.find(x=>x.id===w.sessionId);
          if(s)s.bodyweight=parsed;
        }

        persist();
        renderAll();
      },"secondary small"),
      makeButton("Löschen",()=>{
        if(!confirm("Gewichtseintrag löschen?"))return;

        bodyweights=bodyweights.filter(x=>x.id!==w.id);

        if(w.sessionId){
          const s=sessions.find(x=>x.id===w.sessionId);
          if(s)s.bodyweight=null;
        }

        persist();
        renderAll();
      },"danger small")
    );

    row.append(info,actions);
    box.append(row);
  }

  drawChart(
    "weightChart",
    [...bodyweights].sort((a,b)=>a.date.localeCompare(b.date))
      .map(w=>({label:dateLabel(w.date),value:w.weight})),
    "kg"
  );
}

function drawChart(elementId,points,unit){
  const box=$(elementId);
  box.replaceChildren();

  if(!points.length){
    box.append(textEl(
      "p","Noch keine Daten für ein Diagramm.","empty"
    ));
    return;
  }

  const values=points.map(p=>p.value);
  let min=Math.min(...values);
  let max=Math.max(...values);

  const padding=Math.max((max-min)*.2,unit==="kg"?1:2);
  min=Math.max(0,min-padding);
  max+=padding;

  const W=340,H=190;
  const L=42,R=12,T=20,B=35;
  const innerW=W-L-R;
  const innerH=H-T-B;

  const x=i=>L+(points.length===1
    ?innerW/2:i*innerW/(points.length-1));

  const y=v=>T+(max-v)/(max-min)*innerH;

  const ns="http://www.w3.org/2000/svg";
  const svg=document.createElementNS(ns,"svg");
  svg.setAttribute("viewBox",`0 0 ${W} ${H}`);
  svg.setAttribute("preserveAspectRatio","xMidYMid meet");

  function svgNode(tag,attrs,text){
    const node=document.createElementNS(ns,tag);
    for(const [k,v] of Object.entries(attrs)){
      node.setAttribute(k,String(v));
    }
    if(text!==undefined)node.textContent=text;
    svg.append(node);
    return node;
  }

  for(let i=0;i<4;i++){
    const value=min+(max-min)*i/3;
    const yy=y(value);

    svgNode("line",{
      x1:L,y1:yy,x2:W-R,y2:yy,
      stroke:"#ffffff35","stroke-width":1
    });

    svgNode("text",{
      x:L-6,y:yy+4,fill:"#e2e8f0",
      "font-size":10,"text-anchor":"end"
    },fmt(value));
  }

  if(points.length>1){
    svgNode("polyline",{
      points:points.map((p,i)=>
        `${x(i)},${y(p.value)}`
      ).join(" "),
      fill:"none",
      stroke:"#f9d67b",
      "stroke-width":3,
      "stroke-linecap":"round",
      "stroke-linejoin":"round"
    });
  }

  points.forEach((p,i)=>{
    svgNode("circle",{
      cx:x(i),cy:y(p.value),r:4,
      fill:"#ffffff",stroke:"#f9d67b",
      "stroke-width":2
    });

    if(
      i===0||
      i===points.length-1||
      (points.length<=5)
    ){
      svgNode("text",{
        x:x(i),y:H-10,fill:"#e2e8f0",
        "font-size":9,"text-anchor":"middle"
      },p.label.slice(0,5));
    }
  });

  const last=points[points.length-1];
  svgNode("text",{
    x:W-R,y:13,fill:"#ffffff",
    "font-size":12,"text-anchor":"end"
  },fmt(last.value)+" "+unit);

  box.append(svg);
}

function progressRecords(exerciseId){
  const records=[];

  for(const s of sessions){
    const ex=s.exercises.find(
      e=>e.exerciseId===exerciseId
    );
    if(!ex)continue;

    const maxKg=Math.max(...ex.sets.map(x=>x.kg));
    const maxReps=Math.max(...ex.sets.map(x=>x.reps));
    const first=ex.sets[0];

    records.push({
      date:s.date,
      maxKg,
      maxReps,
      firstKg:first.kg,
      firstReps:first.reps,
      sets:ex.sets
    });
  }

  return records.sort((a,b)=>a.date.localeCompare(b.date));
}

function renderProgress(){
  const select=$("progressExercise");
  const selected=select.value;
  select.replaceChildren();

  for(const ex of [...exercises].sort((a,b)=>
    a.name.localeCompare(b.name,"de")
  )){
    select.add(new Option(ex.name,ex.id));
  }

  if(exercises.some(x=>x.id===selected)){
    select.value=selected;
  }

  const ex=getExercise(select.value);
  const summary=$("progressSummary");
  const history=$("progressHistory");

  summary.replaceChildren();
  history.replaceChildren();

  if(!ex){
    drawChart("exerciseChart",[],"kg");
    return;
  }

  const records=progressRecords(ex.id);

  if(!records.length){
    summary.append(textEl(
      "p","Für diese Übung gibt es noch keine Trainingsdaten.","empty"
    ));
    drawChart("exerciseChart",[],"kg");
    return;
  }

  const latest=records[records.length-1];
  const bestKg=Math.max(...records.map(r=>r.maxKg));
  const bestReps=Math.max(...records.map(r=>r.maxReps));

  const metrics=[
    ["Trainiert",records.length+" ×"],
    ["Letzter 1. Satz",
      fmt(latest.firstKg)+" kg × "+fmt(latest.firstReps)],
    ["Höchstes Gewicht",fmt(bestKg)+" kg"],
    ["Meiste Wiederholungen",fmt(bestReps)]
  ];

  for(const [label,value] of metrics){
    const cell=document.createElement("div");
    cell.append(
      textEl("small",label),
      textEl("strong",value)
    );
    summary.append(cell);
  }

  const bodyweight=ex.type==="bodyweight";

  drawChart(
    "exerciseChart",
    records.map(r=>({
      label:dateLabel(r.date),
      value:bodyweight?r.maxReps:r.maxKg
    })),
    bodyweight?"Wdh.":"kg"
  );

  history.append(textEl("h3","Verlauf"));

  for(const r of [...records].reverse()){
    const row=document.createElement("div");
    row.className="entry";
    row.append(
      textEl("strong",dateLabel(r.date)),
      textEl("small",
        r.sets.map((s,i)=>
          `${i+1}. Satz ${fmt(s.kg)} kg × ${fmt(s.reps)}`
        ).join(" · ")
      )
    );
    history.append(row);
  }
}

function weekStart(){
  const d=new Date();
  const offset=(d.getDay()+6)%7;
  d.setDate(d.getDate()-offset);
  return d.getFullYear()+"-"+
    String(d.getMonth()+1).padStart(2,"0")+"-"+
    String(d.getDate()).padStart(2,"0");
}

function renderDashboard(){
  $("statSessions").textContent=sessions.length;
  $("statExercises").textContent=exercises.length;
  $("statWeek").textContent=sessions.filter(s=>
    s.date>=weekStart()&&s.date<=today()
  ).length;

  const weights=[...bodyweights].sort(
    (a,b)=>b.date.localeCompare(a.date)
  );

  $("statWeight").textContent=weights.length
    ?fmt(weights[0].weight)+" kg":"–";

  const latest=[...sessions].sort(
    (a,b)=>b.date.localeCompare(a.date)
  )[0];

  $("lastTraining").textContent=latest
    ?"Letztes Training: "+dateLabel(latest.date)+
      " · "+latest.exercises.length+" Übungen"
    :"Noch kein Training gespeichert.";
}

function renderAll(){
  renderDashboard();
  renderDraft();
  renderExercisePicker();
  renderHistory();
  renderExercises();
  renderWeights();
  renderProgress();
}

/* Training */
$("startTraining").onclick=()=>{
  resetTraining();
  $("training").scrollIntoView({behavior:"smooth"});
};

$("newTraining").onclick=()=>{
  if(draft.length&&!confirm(
    "Aktuelle ungespeicherte Eingabe verwerfen?"
  ))return;
  resetTraining();
};

$("cancelTraining").onclick=()=>{
  if(draft.length&&!confirm(
    "Ungespeicherte Trainingseingabe zurücksetzen?"
  ))return;
  resetTraining();
};

$("exerciseSearch").oninput=renderExercisePicker;
$("saveTraining").onclick=saveTraining;

/* Übungen */
$("newExercise").onclick=()=>openExerciseForm();

$("cancelExercise").onclick=()=>{
  editingExercise=null;
  $("exerciseForm").classList.add("hidden");
};

$("exerciseForm").onsubmit=saveExercise;

/* Körpergewicht */
$("weightForm").onsubmit=saveWeight;

/* Fortschritt */
$("progressExercise").onchange=renderProgress;

/* Backup */
$("exportBackup").onclick=()=>{
  const data={
    app:"Fitness Tracker",
    version:1,
    created:new Date().toISOString(),
    exercises,
    sessions,
    bodyweights
  };

  const blob=new Blob(
    [JSON.stringify(data,null,2)],
    {type:"application/json"}
  );

  const url=URL.createObjectURL(blob);
  const link=document.createElement("a");
  link.href=url;
  link.download="fitness-backup-"+today()+".json";
  document.body.append(link);
  link.click();
  link.remove();

  setTimeout(()=>URL.revokeObjectURL(url),1000);
};

$("importBackup").onclick=()=>{
  $("backupFile").click();
};

$("backupFile").onchange=async event=>{
  const file=event.target.files[0];
  if(!file)return;

  try{
    const data=JSON.parse(await file.text());

    if(
      data.app!=="Fitness Tracker"||
      !Array.isArray(data.exercises)||
      !Array.isArray(data.sessions)||
      !Array.isArray(data.bodyweights)
    ){
      throw Error("Keine gültige Fitness-Tracker-Sicherung.");
    }

    if(!confirm(
      "Backup importieren? Alle bisherigen Fitness-Daten werden ersetzt."
    ))return;

    const old={
      exercises,
      sessions,
      bodyweights
    };

    exercises=data.exercises;
    sessions=data.sessions;
    bodyweights=data.bodyweights;

    if(!persist()){
      exercises=old.exercises;
      sessions=old.sessions;
      bodyweights=old.bodyweights;
      return;
    }

    resetTraining();
    renderAll();
    alert("Backup erfolgreich importiert.");

  }catch(err){
    alert("Import fehlgeschlagen: "+err.message);
  }finally{
    event.target.value="";
  }
};

/* Start */
$("trainingDate").value=today();
$("weightDate").value=today();
renderAll();

</script>
</body>
</html>
