<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ระบบติดตามสถานะคิวตรวจสุขภาพ</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Kanit:wght@500;600;700&family=Sarabun:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#16233A;
    --ink-soft:#4A5A72;
    --hint:#8593A6;
    --page-bg:#EEF2F6;
    --card-bg:#FFFFFF;
    --line:#DFE5EC;
    --teal:#0D8C82;
    --teal-dark:#076A62;

    --red:#DC2626;
    --red-bg:#FDEBEB;
    --red-strong:#B91C1C;

    --amber:#D97706;
    --amber-bg:#FDF3E1;
    --amber-strong:#9A5B04;

    --green:#16A34A;
    --green-bg:#E7F6EC;
    --green-strong:#0F7A38;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--page-bg);
    font-family:'Sarabun', sans-serif;
    color:var(--ink);
    min-height:100vh;
  }
  .wrap{
    max-width:1180px;
    margin:0 auto;
    padding:20px 20px 60px;
  }

  /* Header */
  header{
    display:flex;
    flex-wrap:wrap;
    align-items:flex-end;
    justify-content:space-between;
    gap:12px;
    margin-bottom:18px;
  }
  h1{
    font-family:'Kanit', sans-serif;
    font-weight:600;
    font-size:26px;
    margin:0 0 4px;
    color:var(--ink);
  }
  .sub{
    font-size:14px;
    color:var(--ink-soft);
    margin:0;
  }
  .clock{
    font-family:'Kanit', sans-serif;
    font-size:15px;
    color:var(--ink-soft);
    font-weight:500;
    white-space:nowrap;
  }

  /* Summary bar */
  .summary{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:22px;
  }
  .pill{
    flex:1 1 160px;
    display:flex;
    align-items:center;
    gap:10px;
    background:var(--card-bg);
    border:1px solid var(--line);
    border-radius:14px;
    padding:14px 16px;
  }
  .pill .dot{
    width:16px;height:16px;border-radius:50%;flex-shrink:0;
  }
  .pill.red .dot{background:var(--red);}
  .pill.amber .dot{background:var(--amber);}
  .pill.green .dot{background:var(--green);}
  .pill .label{
    font-size:13px;
    color:var(--ink-soft);
    line-height:1.2;
  }
  .pill .count{
    font-family:'Kanit', sans-serif;
    font-size:22px;
    font-weight:600;
    line-height:1.1;
    display:block;
  }

  /* Grid of cards */
  .grid{
    display:grid;
    grid-template-columns:repeat(auto-fill, minmax(240px, 1fr));
    gap:14px;
  }
  .card{
    position:relative;
    text-align:left;
    cursor:pointer;
    border:none;
    border-radius:16px;
    padding:18px 16px 16px;
    font-family:inherit;
    border-top:6px solid var(--line);
    background:var(--card-bg);
    transition:transform .12s ease, box-shadow .12s ease;
    box-shadow:0 1px 2px rgba(22,35,58,0.04);
  }
  .card:hover{
    transform:translateY(-2px);
    box-shadow:0 6px 16px rgba(22,35,58,0.10);
  }
  .card:active{ transform:translateY(0) scale(0.99); }
  .card:focus-visible{
    outline:3px solid var(--teal);
    outline-offset:2px;
  }
  .card.red{ background:var(--red-bg); border-top-color:var(--red); }
  .card.amber{ background:var(--amber-bg); border-top-color:var(--amber); }
  .card.green{ background:var(--green-bg); border-top-color:var(--green); }

  .card-top{
    display:flex;
    align-items:flex-start;
    justify-content:space-between;
    gap:8px;
    margin-bottom:10px;
  }
  .badge{
    font-family:'Kanit', sans-serif;
    font-weight:600;
    font-size:12px;
    color:var(--ink-soft);
    background:rgba(22,35,58,0.06);
    border-radius:8px;
    padding:3px 8px;
    flex-shrink:0;
  }
  .status-tag{
    font-family:'Kanit', sans-serif;
    font-size:13px;
    font-weight:600;
    padding:3px 10px;
    border-radius:20px;
    white-space:nowrap;
  }
  .status-tag.red{ background:var(--red); color:#fff; }
  .status-tag.amber{ background:var(--amber); color:#fff; }
  .status-tag.green{ background:var(--green); color:#fff; }

  .station-name{
    font-family:'Kanit', sans-serif;
    font-weight:600;
    font-size:17px;
    line-height:1.3;
    margin:0 0 12px;
    min-height:44px;
    color:var(--ink);
  }
  .card-meta{
    font-size:12.5px;
    color:var(--ink-soft);
    line-height:1.7;
    border-top:1px solid rgba(22,35,58,0.08);
    padding-top:8px;
  }
  .card-meta .row{ display:flex; gap:6px; }
  .card-meta .row span:first-child{ color:var(--hint); flex-shrink:0; }
  .card-meta .row span:last-child{
    font-weight:500;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
  }

  /* Modal */
  .overlay{
    display:none;
    position:fixed;
    inset:0;
    background:rgba(20,30,45,0.45);
    align-items:center;
    justify-content:center;
    padding:16px;
    z-index:100;
  }
  .overlay.open{ display:flex; }
  .modal{
    background:var(--card-bg);
    border-radius:18px;
    width:100%;
    max-width:400px;
    padding:22px 22px 20px;
    box-shadow:0 20px 50px rgba(0,0,0,0.25);
  }
  .modal h2{
    font-family:'Kanit', sans-serif;
    font-size:19px;
    font-weight:600;
    margin:0 0 2px;
  }
  .modal .modal-sub{
    font-size:13px;
    color:var(--ink-soft);
    margin:0 0 18px;
  }
  .status-choices{
    display:flex;
    gap:8px;
    margin-bottom:18px;
  }
  .status-btn{
    flex:1;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:6px;
    padding:14px 6px;
    border-radius:14px;
    border:2px solid var(--line);
    background:#fff;
    cursor:pointer;
    font-family:'Kanit', sans-serif;
    font-weight:500;
    font-size:12.5px;
    color:var(--ink-soft);
    transition:border-color .12s, background .12s;
  }
  .status-btn .swatch{
    width:26px;height:26px;border-radius:50%;
  }
  .status-btn[data-c="red"] .swatch{ background:var(--red); }
  .status-btn[data-c="amber"] .swatch{ background:var(--amber); }
  .status-btn[data-c="green"] .swatch{ background:var(--green); }
  .status-btn.selected{ border-color:currentColor; }
  .status-btn.selected[data-c="red"]{ border-color:var(--red); background:var(--red-bg); color:var(--red-strong); }
  .status-btn.selected[data-c="amber"]{ border-color:var(--amber); background:var(--amber-bg); color:var(--amber-strong); }
  .status-btn.selected[data-c="green"]{ border-color:var(--green); background:var(--green-bg); color:var(--green-strong); }

  .field-label{
    display:block;
    font-size:13px;
    font-weight:600;
    color:var(--ink);
    margin-bottom:8px;
  }
  .name-input{
    width:100%;
    font-family:'Sarabun', sans-serif;
    font-size:15px;
    padding:11px 12px;
    border-radius:10px;
    border:1.5px solid var(--line);
    outline:none;
    margin-bottom:10px;
  }
  .name-input:focus{ border-color:var(--teal); }
  .chip-row{
    display:flex;
    flex-wrap:wrap;
    gap:6px;
    margin-bottom:18px;
  }
  .chip{
    font-size:12.5px;
    font-family:'Sarabun', sans-serif;
    padding:6px 12px;
    border-radius:20px;
    border:1px solid var(--line);
    background:#F6F8FA;
    color:var(--ink-soft);
    cursor:pointer;
  }
  .chip.active{
    background:var(--teal);
    border-color:var(--teal);
    color:#fff;
  }
  .modal-actions{
    display:flex;
    gap:10px;
  }
  .btn{
    flex:1;
    font-family:'Kanit', sans-serif;
    font-weight:500;
    font-size:15px;
    padding:12px;
    border-radius:12px;
    border:none;
    cursor:pointer;
  }
  .btn.cancel{
    background:#F1F3F6;
    color:var(--ink-soft);
  }
  .btn.save{
    background:var(--teal);
    color:#fff;
  }
  .btn.save:disabled{
    background:#B9C3CC;
    cursor:not-allowed;
  }
  .btn.save:not(:disabled):active{ background:var(--teal-dark); }

  @media (max-width:520px){
    h1{ font-size:22px; }
    .grid{ grid-template-columns:repeat(auto-fill, minmax(160px,1fr)); }
    .station-name{ font-size:15.5px; min-height:auto; }
  }
</style>
</head>
<body>
<div class="wrap">
  <header>
    <div>
      <h1>ระบบติดตามสถานะคิวตรวจสุขภาพ</h1>
      <p class="sub">แตะที่จุดตรวจเพื่ออัปเดตสถานะ</p>
    </div>
    <div class="clock" id="clock"></div>
  </header>

  <div class="summary" id="summary"></div>

  <div class="grid" id="grid"></div>
</div>

<div class="overlay" id="overlay">
  <div class="modal">
    <h2 id="modalTitle">ชื่อจุดตรวจ</h2>
    <p class="modal-sub">เลือกสถานะปัจจุบันและระบุชื่อผู้แจ้ง</p>

    <div class="status-choices" id="statusChoices">
      <button class="status-btn" data-c="red" type="button"><span class="swatch"></span>คิวแน่น</button>
      <button class="status-btn" data-c="amber" type="button"><span class="swatch"></span>คนมาเรื่อยๆ</button>
      <button class="status-btn" data-c="green" type="button"><span class="swatch"></span>ว่าง</button>
    </div>

    <label class="field-label" for="nameInput">ชื่อผู้แจ้ง</label>
    <input class="name-input" id="nameInput" placeholder="พิมพ์ชื่อทีมงาน" autocomplete="off">
    <div class="chip-row" id="chipRow"></div>

    <div class="modal-actions">
      <button class="btn cancel" id="cancelBtn" type="button">ยกเลิก</button>
      <button class="btn save" id="saveBtn" type="button" disabled>บันทึก</button>
    </div>
  </div>
</div>

<script>
const STATIONS = [
  { id: 1, name: "จุดลงทะเบียน, เช็คสิทธิ์, ติดอุปกรณ์" },
  { id: 2, name: "ชั่งน้ำหนัก, วัดส่วนสูง" },
  { id: 3, name: "ห้องเจาะเลือด, วัดความดัน" },
  { id: 4, name: "จุดตรวจสายตาทั่วไป" },
  { id: 5, name: "รถ X-Ray" },
  { id: 6, name: "ห้องตรวจสายตาอาชีวอนามัย" },
  { id: 7, name: "จุดตรวจสมรรถภาพทางปอด" },
  { id: 8, name: "ห้องตรวจการได้ยิน 1" },
  { id: 9, name: "ห้องตรวจการได้ยิน 2" },
  { id: 10, name: "จุดตรวจคลื่นไฟฟ้าหัวใจ" },
  { id: 11, name: "ห้องพบแพทย์" }
];

const STATUS_LABEL = { red: "คิวแน่น", amber: "คนมาเรื่อยๆ", green: "ว่าง" };
const STATE_KEY = "checkpoint-state";
const NAMES_KEY = "reporter-names";
const POLL_MS = 5000;

let state = {};
let names = [];
let activeStationId = null;
let selectedStatus = null;

function pad(n){ return n.toString().padStart(2,"0"); }
function fmtTime(ts){
  if(!ts) return "ยังไม่เคยอัปเดต";
  const d = new Date(ts);
  return pad(d.getHours()) + ":" + pad(d.getMinutes()) + " น.";
}
function defaultState(){
  const s = {};
  STATIONS.forEach(st => { s[st.id] = { status: "green", reporter: "-", updatedAt: null }; });
  return s;
}

async function loadState(){
  try{
    const res = await window.storage.get(STATE_KEY, true);
    state = res ? JSON.parse(res.value) : defaultState();
  }catch(e){
    state = defaultState();
    try{ await window.storage.set(STATE_KEY, JSON.stringify(state), true); }catch(e2){}
  }
}
async function loadNames(){
  try{
    const res = await window.storage.get(NAMES_KEY, true);
    names = res ? JSON.parse(res.value) : [];
  }catch(e){ names = []; }
}
async function saveState(){
  try{ await window.storage.set(STATE_KEY, JSON.stringify(state), true); }
  catch(e){ console.error("save state failed", e); }
}
async function saveNames(){
  try{ await window.storage.set(NAMES_KEY, JSON.stringify(names), true); }
  catch(e){ console.error("save names failed", e); }
}

function renderSummary(){
  const counts = { red:0, amber:0, green:0 };
  Object.values(state).forEach(s => { counts[s.status] = (counts[s.status]||0) + 1; });
  const el = document.getElementById("summary");
  el.innerHTML = `
    <div class="pill red"><span class="dot"></span><span><span class="count">${counts.red}</span><span class="label">คิวแน่น</span></span></div>
    <div class="pill amber"><span class="dot"></span><span><span class="count">${counts.amber}</span><span class="label">คนมาเรื่อยๆ</span></span></div>
    <div class="pill green"><span class="dot"></span><span><span class="count">${counts.green}</span><span class="label">ว่าง</span></span></div>
  `;
}

function renderGrid(){
  const grid = document.getElementById("grid");
  grid.innerHTML = "";
  STATIONS.forEach(st => {
    const s = state[st.id] || { status:"green", reporter:"-", updatedAt:null };
    const card = document.createElement("button");
    card.type = "button";
    card.className = "card " + s.status;
    card.setAttribute("aria-label", st.name + " สถานะ " + STATUS_LABEL[s.status]);
    card.innerHTML = `
      <div class="card-top">
        <span class="badge">${String(st.id).padStart(2,"0")}</span>
        <span class="status-tag ${s.status}">${STATUS_LABEL[s.status]}</span>
      </div>
      <p class="station-name">${st.name}</p>
      <div class="card-meta">
        <div class="row"><span>ผู้แจ้ง</span><span>${s.reporter || "-"}</span></div>
        <div class="row"><span>อัปเดต</span><span>${fmtTime(s.updatedAt)}</span></div>
      </div>
    `;
    card.addEventListener("click", () => openModal(st.id));
    grid.appendChild(card);
  });
}

function renderAll(){ renderSummary(); renderGrid(); }

function openModal(stationId){
  activeStationId = stationId;
  const s = state[stationId] || { status:"green", reporter:"" };
  selectedStatus = s.status;
  document.getElementById("modalTitle").textContent =
    STATIONS.find(x => x.id === stationId).name;
  document.querySelectorAll(".status-btn").forEach(b => {
    b.classList.toggle("selected", b.dataset.c === selectedStatus);
  });
  document.getElementById("nameInput").value = "";
  renderChips();
  updateSaveState();
  document.getElementById("overlay").classList.add("open");
  setTimeout(() => document.getElementById("nameInput").focus(), 50);
}
function closeModal(){
  document.getElementById("overlay").classList.remove("open");
  activeStationId = null;
}

function renderChips(){
  const row = document.getElementById("chipRow");
  row.innerHTML = "";
  const recent = names.slice(0, 8);
  const currentVal = document.getElementById("nameInput").value.trim();
  recent.forEach(n => {
    const chip = document.createElement("button");
    chip.type = "button";
    chip.className = "chip" + (n === currentVal ? " active" : "");
    chip.textContent = n;
    chip.addEventListener("click", () => {
      document.getElementById("nameInput").value = n;
      renderChips();
      updateSaveState();
    });
    row.appendChild(chip);
  });
}

function updateSaveState(){
  const nameVal = document.getElementById("nameInput").value.trim();
  document.getElementById("saveBtn").disabled = !(selectedStatus && nameVal);
}

document.querySelectorAll(".status-btn").forEach(b => {
  b.addEventListener("click", () => {
    selectedStatus = b.dataset.c;
    document.querySelectorAll(".status-btn").forEach(x => x.classList.remove("selected"));
    b.classList.add("selected");
    updateSaveState();
  });
});
document.getElementById("nameInput").addEventListener("input", () => {
  renderChips();
  updateSaveState();
});
document.getElementById("cancelBtn").addEventListener("click", closeModal);
document.getElementById("overlay").addEventListener("click", (e) => {
  if(e.target.id === "overlay") closeModal();
});

document.getElementById("saveBtn").addEventListener("click", async () => {
  const nameVal = document.getElementById("nameInput").value.trim();
  if(!selectedStatus || !nameVal || activeStationId === null) return;

  state[activeStationId] = {
    status: selectedStatus,
    reporter: nameVal,
    updatedAt: Date.now()
  };

  names = [nameVal, ...names.filter(n => n !== nameVal)].slice(0, 30);

  renderAll();
  closeModal();

  await Promise.all([saveState(), saveNames()]);
});

function tickClock(){
  const d = new Date();
  document.getElementById("clock").textContent =
    pad(d.getHours()) + ":" + pad(d.getMinutes()) + ":" + pad(d.getSeconds()) + " น.";
}

async function pollUpdates(){
  await Promise.all([loadState(), loadNames()]);
  if(document.getElementById("overlay").classList.contains("open")) return;
  renderAll();
}

(async function init(){
  await Promise.all([loadState(), loadNames()]);
  renderAll();
  tickClock();
  setInterval(tickClock, 1000);
  setInterval(pollUpdates, POLL_MS);
})();
</script>
</body>
</html>
