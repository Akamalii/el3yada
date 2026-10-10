<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<style>:root{color-scheme:light;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}body{margin:0}[hidden]{display:none!important}</style>
<title>الحساب يوم الحساب 🎮</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;500;700&family=Readex+Pro:wght@500;700&display=swap">
<style>
/* Layout: a phone-first tool. Sticky title bar, one scrolling column, four bottom tabs.
   Each tab wears one controller shape (triangle, circle, cross, square) as its marker. */
:root{
  --bg:#EDF0F6;
  --surface:#FFFFFF;
  --surface2:#F3F5FA;
  --fg:#151A2E;
  --muted:#5A6482;
  --line:#D9DEEA;
  --accent:#3446D8;
  --accent-fg:#FFFFFF;
  --tri:#0B8F63;
  --cir:#D63A47;
  --crs:#2F66DB;
  --sqr:#B83A94;
  --warn:#B45309;
  --display:"Readex Pro","IBM Plex Sans Arabic",Tahoma,system-ui,sans-serif;
  --body:"IBM Plex Sans Arabic",Tahoma,system-ui,sans-serif;
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#0E1222;
    --surface:#171C33;
    --surface2:#1F2542;
    --fg:#EDEFF8;
    --muted:#9AA3C6;
    --line:#2B3257;
    --accent:#8190FF;
    --accent-fg:#0E1222;
    --tri:#34D399;
    --cir:#FF6B78;
    --crs:#6FA0FF;
    --sqr:#F178CF;
    --warn:#F5B454;
    color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#0E1222;
  --surface:#171C33;
  --surface2:#1F2542;
  --fg:#EDEFF8;
  --muted:#9AA3C6;
  --line:#2B3257;
  --accent:#8190FF;
  --accent-fg:#0E1222;
  --tri:#34D399;
  --cir:#FF6B78;
  --crs:#6FA0FF;
  --sqr:#F178CF;
  --warn:#F5B454;
  color-scheme:dark;
}

*{box-sizing:border-box}
body{
  background:var(--bg);
  color:var(--fg);
  font:400 15px/1.6 var(--body);
  direction:rtl;
  padding-inline:16px;
  padding-block:0 110px;
}
.wrap{max-width:560px;margin-inline:auto}
button,input,textarea{font:inherit;color:inherit}
button{cursor:pointer}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}

/* title bar */
.top{
  position:sticky;top:env(safe-area-inset-top,0px);z-index:5;
  display:flex;align-items:baseline;justify-content:space-between;gap:12px;
  background:var(--bg);padding-block:14px 10px;
}
.top h1{margin:0;font:700 21px/1.2 var(--display)}
.top .date{color:var(--muted);font-size:13px}

/* section heads */
.sec-head{display:flex;align-items:center;gap:10px;margin-block:6px 4px}
.sec-head h2{margin:0;font:700 19px/1.3 var(--display);text-wrap:balance;flex:1;min-width:0}
.sec-head .ico{color:var(--c)}
.lead{color:var(--muted);margin:0 0 14px;max-width:62ch}
.stack{display:flex;flex-direction:column;gap:12px}

.card{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:16px}
.card h3{margin:0 0 10px;font:700 15px/1.4 var(--display)}
.hint{color:var(--muted);font-size:13px;margin:8px 0 0}

/* controls */
.btn{
  border:1px solid var(--line);background:var(--surface);color:var(--fg);
  border-radius:10px;padding:9px 14px;font-weight:500;min-height:40px;
}
.btn.primary{background:var(--accent);border-color:var(--accent);color:var(--accent-fg);font-weight:700}
.btn.armed{background:var(--cir);border-color:var(--cir);color:#fff}
.btn.small{min-height:34px;padding:5px 11px;font-size:13px}
.btn.block{width:100%}
.mini{
  border:1px solid var(--line);background:var(--surface2);border-radius:8px;
  min-height:36px;min-width:36px;padding:4px 10px;font-size:13px;font-weight:500;
}
.ico{width:22px;height:22px;fill:none;stroke:currentColor;stroke-width:2.4;stroke-linecap:round;stroke-linejoin:round;flex:none}
.icon-btn{border:0;background:transparent;color:var(--muted);width:40px;height:40px;border-radius:10px;display:grid;place-items:center}
.icon-btn:hover{background:var(--surface2);color:var(--cir)}
.icon-btn .ico{width:18px;height:18px}

input[type=text],input[type=time]{
  background:var(--surface2);border:1px solid var(--line);border-radius:10px;
  padding:8px 12px;min-height:40px;width:100%;min-width:0;
}
input[type=time]{direction:ltr;text-align:center;font-variant-numeric:tabular-nums}
input.num{direction:ltr;text-align:center;font-variant-numeric:tabular-nums}

.seg{display:grid;grid-auto-flow:column;grid-auto-columns:1fr;gap:4px;background:var(--surface2);border:1px solid var(--line);border-radius:12px;padding:4px}
.seg button{border:0;background:transparent;border-radius:9px;min-height:38px;padding:4px 8px;font-weight:500;color:var(--muted)}
.seg button[aria-pressed=true]{background:var(--surface);color:var(--fg);font-weight:700;box-shadow:0 1px 3px rgba(20,26,50,.18)}

.tf{display:flex;align-items:center;gap:8px}
.tf label{flex:none;width:52px;color:var(--muted);font-size:13px}
.tf .grow{flex:1;min-width:0}
.fields{display:flex;flex-direction:column;gap:10px}
.price{display:flex;align-items:center;gap:8px;margin-top:12px}
.price .unit{flex:none;color:var(--muted);font-size:13px}

/* friends list */
.list{list-style:none;margin:0;padding:0;display:flex;flex-direction:column}
.row{display:flex;align-items:center;gap:8px;padding-block:6px;border-bottom:1px solid var(--line)}
.row:last-child{border-bottom:0}
.row .nm{flex:1;min-width:0;overflow-wrap:anywhere;font-weight:500}
.add{display:flex;gap:8px}
.note{display:flex;gap:10px;align-items:center;justify-content:space-between;background:var(--surface2);border:1px dashed var(--line);border-radius:12px;padding:10px 12px;font-size:13px;color:var(--muted)}
.empty{color:var(--muted);text-align:center;padding:18px 8px;margin:0}

/* time tab */
.who{
  width:100%;display:flex;align-items:center;gap:12px;text-align:start;
  background:transparent;border:0;padding:8px 0;min-height:44px;
}
.who .box{
  width:24px;height:24px;border-radius:7px;border:2px solid var(--line);display:grid;place-items:center;flex:none;
  color:transparent;background:var(--surface2);
}
.who.on .box{background:var(--accent);border-color:var(--accent);color:var(--accent-fg)}
.who .box svg{width:14px;height:14px;fill:none;stroke:currentColor;stroke-width:3.2;stroke-linecap:round;stroke-linejoin:round}
.who .nm{flex:1;min-width:0;font-weight:500;overflow-wrap:anywhere}
.person{border-bottom:1px solid var(--line);padding-block:2px}
.person:last-child{border-bottom:0}
.person .when{padding:2px 0 12px 0;padding-inline-start:36px}

/* matches tab */
.chips{display:flex;flex-wrap:wrap;gap:8px}
.chip{border:1px solid var(--line);background:var(--surface2);border-radius:999px;padding:6px 14px;min-height:38px;font-weight:500}
.chip[aria-pressed=true]{background:var(--crs);border-color:var(--crs);color:#fff}
.cnt{display:flex;align-items:center;gap:6px}
.cnt output{min-width:34px;text-align:center;font:700 18px/1 var(--display);font-variant-numeric:tabular-nums}
.sq{width:40px;height:40px;border-radius:10px;border:1px solid var(--line);background:var(--surface2);font-size:20px;line-height:1;display:grid;place-items:center}

/* summary */
.total{background:var(--accent);color:var(--accent-fg);border-radius:16px;padding:18px 18px 16px;border:0}
.total .lbl{font-size:13px;opacity:.85}
.total .big{font:700 40px/1.15 var(--display);font-variant-numeric:tabular-nums;display:flex;align-items:baseline;gap:8px}
.total .big small{font:500 15px var(--body)}
.total .sub{font-size:13px;opacity:.9;margin-top:4px}
.share{display:flex;align-items:center;gap:12px;padding-block:10px;border-bottom:1px solid var(--line)}
.share:last-child{border-bottom:0}
.share .who2{flex:1;min-width:0}
.share .who2 b{display:block;font-weight:700;overflow-wrap:anywhere}
.share .who2 span{color:var(--muted);font-size:13px}
.share .who2 em{display:block;font-style:normal;color:var(--warn);font-size:12px}
.share .amt{font:700 22px/1 var(--display);font-variant-numeric:tabular-nums;white-space:nowrap}
.share .amt small{font:500 12px var(--body);color:var(--muted);margin-inline-start:4px}
.resets{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:8px}
.mono{font-variant-numeric:tabular-nums}
textarea.out{width:100%;min-height:130px;background:var(--surface2);border:1px solid var(--line);border-radius:10px;padding:10px;direction:rtl;margin-top:10px}

/* bottom tabs */
.tabs{
  position:fixed;inset-inline:0;bottom:0;z-index:10;background:var(--surface);border-top:1px solid var(--line);
  padding-bottom:env(safe-area-inset-bottom,0px);
}
.tabs .in{max-width:560px;margin-inline:auto;display:grid;grid-template-columns:repeat(4,1fr);gap:4px;padding:6px 8px}
.tab{
  border:0;background:transparent;border-radius:12px;color:var(--muted);
  display:flex;flex-direction:column;align-items:center;gap:2px;padding:7px 2px 6px;font-size:12px;font-weight:500;min-width:0;
}
.tab[aria-selected=true]{color:var(--c);background:color-mix(in srgb,var(--c) 14%,transparent);font-weight:700}
.t-friends{--c:var(--tri)}
.t-time{--c:var(--cir)}
.t-matches{--c:var(--crs)}
.t-summary{--c:var(--sqr)}
.sec-friends{--c:var(--tri)}
.sec-time{--c:var(--cir)}
.sec-matches{--c:var(--crs)}
.sec-summary{--c:var(--sqr)}

.toast{
  position:fixed;inset-inline:0;bottom:calc(84px + env(safe-area-inset-bottom,0px));margin-inline:auto;width:max-content;max-width:90%;
  background:var(--fg);color:var(--bg);padding:8px 16px;border-radius:999px;font-size:13px;z-index:20;
}
@media (prefers-reduced-motion: no-preference){
  .btn,.chip,.tab,.who .box{transition:background-color .15s,color .15s,border-color .15s}
}
</style>
</head>
<body>
<div class="wrap">
  <header class="top"><h1>حسبة القعدة</h1><span class="date" id="date"></span></header>
  <main id="view"></main>
</div>

<nav class="tabs" aria-label="التابات">
  <div class="in" role="tablist">
    <button class="tab t-friends" role="tab" data-act="tab" data-tab="friends">
      <svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 4 L21 19 H3 Z"/></svg>الأصحاب
    </button>
    <button class="tab t-time" role="tab" data-act="tab" data-tab="time">
      <svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><circle cx="12" cy="12" r="8"/></svg>الوقت
    </button>
    <button class="tab t-matches" role="tab" data-act="tab" data-tab="matches">
      <svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><path d="M5 5 L19 19 M19 5 L5 19"/></svg>الماتشات
    </button>
    <button class="tab t-summary" role="tab" data-act="tab" data-tab="summary">
      <svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><rect x="5" y="5" width="14" height="14" rx="1"/></svg>الملخص
    </button>
  </div>
</nav>
<div class="toast" id="toast" hidden></div>

<script>
/*LOGIC-START*/
function num(s){
  if(s==null) return NaN;
  s=String(s).replace(/[٠-٩]/g,function(d){return '٠١٢٣٤٥٦٧٨٩'.indexOf(d)}).replace('٫','.').replace(',','.');
  return parseFloat(s);
}
function toMin(s){
  if(!s) return null;
  var m=/^(\d{1,2}):(\d{2})/.exec(s);
  if(!m) return null;
  return (+m[1])*60+(+m[2]);
}
function fmtDur(m){
  m=Math.round(m);
  var h=Math.floor(m/60), r=m%60;
  if(h===0) return r+' د';
  if(r===0) return h+' س';
  return h+' س '+r+' د';
}
/* Split the bill by real time: every stretch of time is divided among the people present in it. */
function computeTime(st,nowM){
  var t=st.time;
  var base=toMin(t.start);
  if(base==null) return {err:'اكتب بداية الجلسة في تاب الوقت.',go:'time'};
  var off=function(m){return ((m-base)%1440+1440)%1440};
  var endOff=t.end? off(toMin(t.end)) : off(nowM);
  if(endOff<=0) return {err:'نهاية الجلسة لازم تيجي بعد البداية.',go:'time'};
  var people=st.friends.filter(function(f){return f.present});
  if(!people.length) return {err:'اختار الأصحاب الحاضرين في تاب الوقت.',go:'time'};
  var iv=people.map(function(f){
    var a=f.in? off(toMin(f.in)) : 0;
    var b=f.out? off(toMin(f.out)) : endOff;
    var warn='';
    if(b>endOff){b=endOff;warn='خروجه بعد نهاية الجلسة'}
    if(a>=b){return {f:f,a:0,b:0,warn:'وقت دخوله وخروجه مش مظبوط'}}
    return {f:f,a:a,b:b,warn:warn};
  });
  var pts={0:1};pts[endOff]=1;
  iv.forEach(function(x){pts[x.a]=1;pts[x.b]=1});
  var arr=Object.keys(pts).map(Number).filter(function(p){return p>=0&&p<=endOff}).sort(function(x,y){return x-y});
  var segs=[],covered=0;
  for(var i=0;i<arr.length-1;i++){
    var a=arr[i],b=arr[i+1];
    var n=iv.filter(function(x){return x.b>x.a&&x.a<=a&&x.b>=b}).length;
    if(n){segs.push({a:a,b:b,n:n});covered+=b-a}
  }
  if(!covered) return {err:'مفيش وقت متسجل لأي حد.',go:'time'};
  var perMin,total;
  if(t.mode==='rate'){
    var r=num(t.rate);
    if(!(r>0)) return {err:'اكتب سعر الساعة في تاب الوقت.',go:'time'};
    perMin=r/60;total=perMin*covered;
  }else{
    var T=num(t.total);
    if(!(T>0)) return {err:'اكتب إجمالي الفاتورة في تاب الوقت.',go:'time'};
    perMin=T/covered;total=T;
  }
  var share={},mins={};
  iv.forEach(function(x){share[x.f.id]=0;mins[x.f.id]=0});
  segs.forEach(function(s){
    var cost=perMin*(s.b-s.a)/s.n;
    iv.forEach(function(x){
      if(x.b>x.a&&x.a<=s.a&&x.b>=s.b){share[x.f.id]+=cost;mins[x.f.id]+=s.b-s.a}
    });
  });
  var rows=iv.map(function(x){
    return {id:x.f.id,name:x.f.name,share:share[x.f.id],detail:fmtDur(mins[x.f.id]),warn:x.warn};
  });
  return {rows:rows,total:total,sub:fmtDur(covered)+' · '+people.length+' أصحاب'};
}
/* Split the bill by how many matches each person played. */
function computeMatches(st){
  var total=num(st.matches.total);
  if(!(total>0)) return {err:'اكتب إجمالي الفاتورة في تاب الماتشات.',go:'matches'};
  var players=st.friends.filter(function(f){return f.matches>0});
  var sum=players.reduce(function(a,f){return a+f.matches},0);
  if(!sum) return {err:'سجّل ماتشات في تاب الماتشات الأول.',go:'matches'};
  var rows=players.map(function(f){
    return {id:f.id,name:f.name,share:total*f.matches/sum,detail:f.matches+' ماتش',warn:''};
  });
  return {rows:rows,total:total,sub:sum+' ماتش · سعر الماتش '+(Math.round(total/sum*100)/100)};
}
function roundRows(rows,total,step){
  var out=rows.map(function(r){
    var s=r.share;
    if(step>0) s=Math.ceil(s/step-1e-9)*step;
    return {id:r.id,name:r.name,share:s,detail:r.detail,warn:r.warn};
  });
  var collected=out.reduce(function(a,r){return a+r.share},0);
  return {rows:out,collected:collected,diff:collected-total};
}
/*LOGIC-END*/

(function(){
document.documentElement.lang='ar';
document.documentElement.dir='rtl';

var KEY='hesba-qa3da-v2';
function uid(){return Math.random().toString(36).slice(2,9)}
function person(name){return {id:uid(),name:name,present:false,in:'',out:'',matches:0}}
function defaults(){
  return {
    friends:['بودي','نوفا','بوبو','معجزة','جارحي','روماني','كيرو','بشار','ريشة','سعديشن','باسم','صيعو','سانتوس','محمد محمود','جعفر','عمرو صبري','عبزو رمضان','وحيد','حمزة','نور','عمر خالد'].map(person),
    time:{start:'',end:'',mode:'rate',rate:'',total:''},
    matches:{total:''},
    summary:{method:'time',round:'1'},
    tab:'friends',
    noteDismissed:true
  };
}
var state=load();
function load(){
  try{
    var s=localStorage.getItem(KEY);
    if(s){
      var o=JSON.parse(s),d=defaults();
      return {
        friends:Array.isArray(o.friends)?o.friends:d.friends,
        time:Object.assign(d.time,o.time||{}),
        matches:Object.assign(d.matches,o.matches||{}),
        summary:Object.assign(d.summary,o.summary||{}),
        tab:o.tab||d.tab,
        noteDismissed:!!o.noteDismissed
      };
    }
  }catch(e){}
  return defaults();
}
function save(){try{localStorage.setItem(KEY,JSON.stringify(state))}catch(e){}}

var pick=new Set();
var armed=null,armTimer=null;
var lastText='',showCopyBox=false;

function esc(s){return String(s).replace(/[&<>"']/g,function(c){return {'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]})}
var nf=new Intl.NumberFormat('en-US',{maximumFractionDigits:2});
function money(n){return nf.format(Math.round(n*100)/100)}
function nowMin(){var d=new Date();return d.getHours()*60+d.getMinutes()}
function nowStr(){var d=new Date();return String(d.getHours()).padStart(2,'0')+':'+String(d.getMinutes()).padStart(2,'0')}
function byId(id){return state.friends.find(function(f){return f.id===id})}

var SH={
  tri:'<svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 4 L21 19 H3 Z"/></svg>',
  cir:'<svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><circle cx="12" cy="12" r="8"/></svg>',
  crs:'<svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><path d="M5 5 L19 19 M19 5 L5 19"/></svg>',
  sqr:'<svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><rect x="5" y="5" width="14" height="14" rx="1"/></svg>'
};
var CHECK='<svg viewBox="0 0 24 24" aria-hidden="true"><path d="M5 12.5 L10 17.5 L19 7"/></svg>';
var DEL='<svg class="ico" viewBox="0 0 24 24" aria-hidden="true"><path d="M6 6 L18 18 M18 6 L6 18"/></svg>';

function head(cls,shape,title,right){
  return '<div class="sec-head '+cls+'">'+SH[shape]+'<h2>'+title+'</h2>'+(right||'')+'</div>';
}
function resetBtn(key,label){
  var on=armed===key;
  return '<button class="btn small'+(on?' armed':'')+'" data-act="reset" data-key="'+key+'">'+(on?'اضغط تاني للتأكيد':label)+'</button>';
}

/* ---------- views ---------- */
function viewFriends(){
  var note=state.noteDismissed?'':
    '<div class="note"><span>الأسماء دي تجريبية. امسحها أو ضيف أصحابك الحقيقيين.</span>'+
    '<button class="btn small" data-act="dismissNote">تمام</button></div>';
  var list=state.friends.length?
    '<ul class="list">'+state.friends.map(function(f){
      return '<li class="row"><span class="nm">'+esc(f.name)+'</span>'+
        '<button class="icon-btn" data-act="delFriend" data-id="'+f.id+'" aria-label="حذف '+esc(f.name)+'">'+DEL+'</button></li>';
    }).join('')+'</ul>':
    '<p class="empty">مفيش أصحاب لسه. ضيف أول اسم من فوق.</p>';
  return head('sec-friends','tri','الأصحاب')+
    '<p class="lead">كل اللي ممكن يجي القعدة. القايمة بتفضل محفوظة حتى لو صفّرت الحساب.</p>'+
    '<div class="stack">'+note+
    '<div class="card"><div class="add"><input type="text" id="newName" placeholder="اسم صاحبك" autocomplete="off" aria-label="اسم صاحبك">'+
    '<button class="btn primary" data-act="addFriend">إضافة</button></div></div>'+
    '<div class="card"><h3>القايمة ('+state.friends.length+')</h3>'+list+'</div>'+
    (state.friends.length?'<div>'+resetBtn('friends','مسح القايمة كلها')+'</div>':'')+
    '</div>';
}

function tfield(label,scope,f,val,id,withNow,hintId){
  return '<div class="tf"><label for="'+hintId+'">'+label+'</label>'+
    '<div class="grow"><input type="time" id="'+hintId+'" data-in="'+scope+'" data-f="'+f+'"'+(id?' data-id="'+id+'"':'')+' value="'+esc(val)+'"></div>'+
    '<button class="mini" data-act="now" data-scope="'+scope+'" data-f="'+f+'"'+(id?' data-id="'+id+'"':'')+'>الآن</button>'+
    (val?'<button class="mini" data-act="clr" data-scope="'+scope+'" data-f="'+f+'"'+(id?' data-id="'+id+'"':'')+' aria-label="مسح">×</button>':'')+
    '</div>';
}

function viewTime(){
  var t=state.time;
  var sess='<div class="card"><h3>الجلسة</h3><div class="fields">'+
    tfield('بداية','sess','start',t.start,null,true,'t-start')+
    tfield('نهاية','sess','end',t.end,null,true,'t-end')+
    '</div><p class="hint">سيب النهاية فاضية لو لسه قاعدين، وهتتحسب لحد دلوقتي.</p>'+
    '<div class="seg" style="margin-top:14px" role="group" aria-label="طريقة التسعير">'+
    '<button data-act="priceMode" data-mode="rate" aria-pressed="'+(t.mode==='rate')+'">سعر الساعة</button>'+
    '<button data-act="priceMode" data-mode="total" aria-pressed="'+(t.mode==='total')+'">إجمالي الفاتورة</button></div>'+
    '<div class="price"><input type="text" class="num" inputmode="decimal" id="t-price" data-in="sess" data-f="'+(t.mode==='rate'?'rate':'total')+'" '+
    'value="'+esc(t.mode==='rate'?t.rate:t.total)+'" placeholder="'+(t.mode==='rate'?'سعر الساعة':'الإجمالي')+'" aria-label="'+(t.mode==='rate'?'سعر الساعة':'إجمالي الفاتورة')+'">'+
    '<span class="unit">جنيه</span></div></div>';
  var people=state.friends.length?state.friends.map(function(f){
    var when=f.present?'<div class="when fields">'+
      tfield('دخل','friend','in',f.in,f.id,true,'in-'+f.id)+
      tfield('خرج','friend','out',f.out,f.id,true,'out-'+f.id)+
      '<p class="hint" style="margin:0">دخل فاضي = من أول الجلسة. خرج فاضي = لسه قاعد.</p></div>':'';
    return '<div class="person"><button class="who'+(f.present?' on':'')+'" data-act="togglePresent" data-id="'+f.id+'" aria-pressed="'+f.present+'">'+
      '<span class="box">'+CHECK+'</span><span class="nm">'+esc(f.name)+'</span></button>'+when+'</div>';
  }).join(''):'<p class="empty">ضيف أصحابك الأول من تاب الأصحاب.</p>';
  return head('sec-time','cir','الوقت',resetBtn('time','تصفير'))+
    '<p class="lead">كل واحد يدفع على قد الوقت اللي قعده. وقت ما يكونوا اتنين مع بعض، سعره بيتقسم عليهم.</p>'+
    '<div class="stack">'+sess+'<div class="card"><h3>مين كان موجود؟</h3>'+people+'</div>'+
    '<p class="hint" style="margin:0">التصفير بيمسح الأوقات والإجمالي، ويسيب الأصحاب وسعر الساعة.</p></div>';
}

function viewMatches(){
  var chips=state.friends.map(function(f){
    return '<button class="chip" data-act="pick" data-id="'+f.id+'" aria-pressed="'+pick.has(f.id)+'">'+esc(f.name)+'</button>';
  }).join('');
  var counters=state.friends.length?'<ul class="list">'+state.friends.map(function(f){
    return '<li class="row"><span class="nm">'+esc(f.name)+'</span><div class="cnt">'+
      '<button class="sq" data-act="dec" data-id="'+f.id+'" aria-label="نقص ماتش لـ '+esc(f.name)+'">−</button>'+
      '<output>'+f.matches+'</output>'+
      '<button class="sq" data-act="inc" data-id="'+f.id+'" aria-label="زوّد ماتش لـ '+esc(f.name)+'">+</button></div></li>';
  }).join('')+'</ul>':'<p class="empty">ضيف أصحابك الأول من تاب الأصحاب.</p>';
  var n=pick.size;
  return head('sec-matches','crs','الماتشات',resetBtn('matches','تصفير'))+
    '<p class="lead">الفاتورة بتتقسم على قد عدد الماتشات اللي لعبها كل واحد.</p>'+
    '<div class="stack">'+
    '<div class="card"><h3>إجمالي الفاتورة</h3><div class="price" style="margin-top:0"><input type="text" class="num" inputmode="decimal" id="m-total" data-in="mTotal" value="'+esc(state.matches.total)+'" placeholder="الإجمالي" aria-label="إجمالي الفاتورة"><span class="unit">جنيه</span></div></div>'+
    '<div class="card"><h3>ماتش جديد</h3><div class="chips">'+(chips||'<p class="empty">مفيش أصحاب.</p>')+'</div>'+
    '<p class="hint">اختار اللي لعبوا الماتش وسجّله، وكل واحد ياخد ماتش.</p>'+
    '<div style="margin-top:10px"><button class="btn primary block" data-act="logMatch"'+(n?'':' disabled style="opacity:.5"')+'>'+(n?'سجّل الماتش ('+n+' لاعبين)':'اختار اللاعبين الأول')+'</button></div></div>'+
    '<div class="card"><h3>عدد الماتشات لكل واحد</h3>'+counters+'</div>'+
    '<p class="hint" style="margin:0">التصفير بيمسح الماتشات والإجمالي، ويسيب الأصحاب.</p></div>';
}

function viewSummary(){
  var s=state.summary;
  var res=s.method==='time'?computeTime(state,nowMin()):computeMatches(state);
  var seg='<div class="seg" role="group" aria-label="طريقة الحساب">'+
    '<button data-act="method" data-m="time" aria-pressed="'+(s.method==='time')+'">بالوقت</button>'+
    '<button data-act="method" data-m="matches" aria-pressed="'+(s.method==='matches')+'">بالماتشات</button></div>';
  var body;
  lastText='';
  if(res.err){
    body='<div class="card"><p class="empty">'+esc(res.err)+'</p><div style="text-align:center">'+
      '<button class="btn primary" data-act="tab" data-tab="'+res.go+'">'+(res.go==='time'?'افتح تاب الوقت':'افتح تاب الماتشات')+'</button></div></div>';
  }else{
    var step=Number(s.round)||0;
    var r=roundRows(res.rows,res.total,step);
    var diffLine=(step>0&&Math.abs(r.diff)>0.004)?
      '<div class="sub">بعد التقريب هتتجمع '+money(r.collected)+' جنيه ('+(r.diff>0?'زيادة ':'نقص ')+money(Math.abs(r.diff))+')</div>':'';
    var rows=r.rows.map(function(x){
      return '<div class="share"><div class="who2"><b>'+esc(x.name)+'</b><span>'+esc(x.detail)+'</span>'+(x.warn?'<em>'+esc(x.warn)+'</em>':'')+'</div>'+
        '<div class="amt">'+money(x.share)+'<small>جنيه</small></div></div>';
    }).join('');
    body='<div class="total"><div class="lbl">إجمالي الحساب</div><div class="big">'+money(res.total)+'<small>جنيه</small></div>'+
      '<div class="sub">'+esc(res.sub)+'</div>'+diffLine+'</div>'+
      '<div class="card"><h3>حساب كل واحد</h3>'+rows+'</div>'+
      '<div class="card"><h3>التقريب</h3><div class="seg" role="group" aria-label="التقريب">'+
      ['0:بدون','1:لأقرب 1 جنيه','5:لأقرب 5 جنيه'].map(function(o){var p=o.split(':');
        return '<button data-act="round" data-v="'+p[0]+'" aria-pressed="'+(String(s.round)===p[0])+'">'+p[1]+'</button>'}).join('')+'</div>'+
      '<p class="hint">التقريب بيكون لفوق علشان الفلوس المتجمعة متقلش عن الفاتورة.</p></div>'+
      '<div><button class="btn block" data-act="copy">نسخ الحساب للواتساب</button>'+
      (showCopyBox?'<textarea class="out" id="copyBox" readonly aria-label="نص الحساب"></textarea>':'')+'</div>';
    lastText='حسبة القعدة ('+(s.method==='time'?'بالوقت':'بالماتشات')+')\nالإجمالي: '+money(res.total)+' جنيه\n'+
      r.rows.map(function(x){return x.name+': '+money(x.share)+' جنيه ('+x.detail+')'}).join('\n');
  }
  var resets='<div class="card"><h3>تصفير</h3><div class="resets">'+
    resetBtn('time','تصفير الوقت')+resetBtn('matches','تصفير الماتشات')+resetBtn('all','تصفير الكل')+
    '</div><p class="hint">الأصحاب وسعر الساعة بيفضلوا زي ما هم، فتبدأ قعدة جديدة بدون ما تمسح حاجة.</p></div>';
  return head('sec-summary','sqr','الملخص')+'<div class="stack" style="margin-top:8px">'+seg+body+resets+'</div>';
}

var VIEWS={friends:viewFriends,time:viewTime,matches:viewMatches,summary:viewSummary};
var view=document.getElementById('view');
function render(){
  if(!VIEWS[state.tab]) state.tab='friends';
  view.innerHTML=VIEWS[state.tab]();
  document.querySelectorAll('.tab').forEach(function(b){
    b.setAttribute('aria-selected',String(b.dataset.tab===state.tab));
  });
  if(showCopyBox){var cb=document.getElementById('copyBox');if(cb){cb.value=lastText;cb.focus();cb.select()}}
}

var toastEl=document.getElementById('toast'),toastTimer=null;
function toast(msg){
  toastEl.textContent=msg;toastEl.hidden=false;
  clearTimeout(toastTimer);toastTimer=setTimeout(function(){toastEl.hidden=true},1800);
}

/* ---------- resets ---------- */
function resetTime(){
  state.friends.forEach(function(f){f.present=false;f.in='';f.out=''});
  state.time.start='';state.time.end='';state.time.total='';
}
function resetMatches(){
  state.friends.forEach(function(f){f.matches=0});
  state.matches.total='';pick.clear();
}

/* ---------- events ---------- */
function setField(scope,id,f,val){
  if(scope==='sess') state.time[f]=val;
  else{var p=byId(id);if(p) p[f]=val}
}
function addFriend(){
  var inp=document.getElementById('newName');
  var name=inp.value.trim();
  if(!name){inp.focus();return}
  state.friends.push(person(name));
  save();render();
  var n=document.getElementById('newName');if(n) n.focus();
}

document.addEventListener('click',function(e){
  var el=e.target.closest('[data-act]');
  if(!el) return;
  var act=el.dataset.act,id=el.dataset.id;
  if(act!=='reset'&&armed){armed=null;clearTimeout(armTimer)}
  switch(act){
    case 'tab': state.tab=el.dataset.tab;showCopyBox=false;save();render();window.scrollTo(0,0);return;
    case 'addFriend': addFriend();return;
    case 'delFriend': state.friends=state.friends.filter(function(f){return f.id!==id});pick.delete(id);break;
    case 'dismissNote': state.noteDismissed=true;break;
    case 'togglePresent': var p=byId(id);if(p) p.present=!p.present;break;
    case 'now': setField(el.dataset.scope,id,el.dataset.f,nowStr());break;
    case 'clr': setField(el.dataset.scope,id,el.dataset.f,'');break;
    case 'priceMode': state.time.mode=el.dataset.mode;break;
    case 'pick': if(pick.has(id)) pick.delete(id); else pick.add(id);break;
    case 'logMatch':
      if(!pick.size) return;
      state.friends.forEach(function(f){if(pick.has(f.id)) f.matches+=1});
      toast('اتسجل ماتش لـ '+pick.size+' لاعبين');pick.clear();break;
    case 'inc': var a=byId(id);if(a) a.matches+=1;break;
    case 'dec': var b=byId(id);if(b&&b.matches>0) b.matches-=1;break;
    case 'method': state.summary.method=el.dataset.m;showCopyBox=false;break;
    case 'round': state.summary.round=el.dataset.v;showCopyBox=false;break;
    case 'copy':
      if(!lastText) return;
      var done=function(){toast('اتنسخ');};
      var fail=function(){showCopyBox=true;render();};
      try{
        if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(lastText).then(done,fail)}
        else fail();
      }catch(err){fail()}
      return;
    case 'reset':
      var key=el.dataset.key;
      if(armed!==key){
        armed=key;clearTimeout(armTimer);
        armTimer=setTimeout(function(){armed=null;render()},3500);
        render();return;
      }
      armed=null;clearTimeout(armTimer);
      if(key==='time'){resetTime();toast('اتصفّر الوقت')}
      else if(key==='matches'){resetMatches();toast('اتصفّرت الماتشات')}
      else if(key==='all'){resetTime();resetMatches();toast('اتصفّر كل شيء')}
      else if(key==='friends'){state.friends=[];pick.clear();toast('اتمسحت القايمة')}
      break;
    default: return;
  }
  save();render();
});

document.addEventListener('input',function(e){
  var el=e.target.closest('[data-in]');
  if(!el) return;
  var kind=el.dataset.in;
  if(kind==='mTotal') state.matches.total=el.value;
  else setField(kind,el.dataset.id,el.dataset.f,el.value);
  save();
});
document.addEventListener('keydown',function(e){
  if(e.target.id==='newName'&&e.key==='Enter'){e.preventDefault();addFriend()}
});

try{
  document.getElementById('date').textContent=new Date().toLocaleDateString('ar-EG-u-nu-latn',{weekday:'long',day:'numeric',month:'long'});
}catch(e){}
render();
})();
</script>
</body>
</html>
