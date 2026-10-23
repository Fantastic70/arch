<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="robots" content="noindex,nofollow">
<title>ALARAB ARCHITECTURE | دليل التشطيبات</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@400;600&display=swap">
<style>
:root{--bg:#eef1ee;--ink:#12302b;--mut:#5b6e69;--sf:#fff;--ln:#cfd8d4;--ac:#9a7b3f;--wr:#b3261e;--wb:#fdecea;--ok:#1f6b45;--okb:#e6f4ec;--nt:#7a5a00;--ntb:#fff4d6}
@media(prefers-color-scheme:dark){:root{--bg:#0f1c19;--ink:#e8efec;--mut:#9db0aa;--sf:#172824;--ln:#2c423c;--ac:#d1ae6a;--wr:#ffb4ab;--wb:#3a1a17;--ok:#8fd6ae;--okb:#143324;--nt:#f1d37a;--ntb:#3a3012}}
*{box-sizing:border-box}
html,body{margin:0}
body{background:var(--bg);color:var(--ink);font:400 16px/1.8 "IBM Plex Sans Arabic",Tahoma,sans-serif;padding:env(safe-area-inset-top,0) 0 env(safe-area-inset-bottom,0)}
h1,h2,h3{font-weight:600;line-height:1.4;margin:0}
button{font:inherit;color:inherit;cursor:pointer}
:focus-visible{outline:3px solid var(--ac);outline-offset:2px}
#gate{min-height:100vh;display:grid;place-items:center;padding:24px}
#gate form{width:min(380px,100%);display:grid;gap:14px}
#gate h1{font-size:30px}
#gate p{margin:0;color:var(--mut)}
input{font:inherit;padding:12px 14px;border:1px solid var(--ln);border-radius:6px;background:var(--sf);color:var(--ink);width:100%}
.btn{background:var(--ink);color:var(--bg);border:0;padding:12px 18px;border-radius:6px;font-weight:600}
#err{color:var(--wr);min-height:1.6em}
#app{display:none}
header{background:var(--ink);color:#eef1ee;padding:22px 20px}
header h1{font-size:24px}
header p{margin:4px 0 0;color:#b9c8c3;font-size:14px}
.wrap{max-width:980px;margin:0 auto;padding:0 16px}
.bar{display:flex;gap:8px;flex-wrap:wrap;padding:16px 0 4px}
.tab,.chip{border:1px solid var(--ln);background:var(--sf);padding:8px 14px;border-radius:999px}
.tab[aria-pressed=true],.chip[aria-pressed=true]{background:var(--ink);color:var(--bg);border-color:var(--ink)}
#warns{position:sticky;top:0;z-index:5;background:var(--bg);padding:10px 0;display:grid;gap:8px}
.w{padding:10px 14px;border-radius:6px;border-inline-start:5px solid;font-size:15px}
.w.bad{background:var(--wb);border-color:var(--wr);color:var(--wr)}
.w.note{background:var(--ntb);border-color:var(--nt);color:var(--nt)}
.w.good{background:var(--okb);border-color:var(--ok);color:var(--ok)}
section.cat{padding:22px 0;border-top:1px solid var(--ln)}
section.cat h2{font-size:20px;margin-bottom:4px}
.sub{color:var(--mut);font-size:14px;margin:0 0 10px}
.opts{display:flex;gap:8px;flex-wrap:wrap}
.det{margin-top:14px;background:var(--sf);padding:16px 18px;border-radius:8px;display:grid;gap:10px}
.det h3{font-size:17px}
.det h4{margin:0;font-size:14px;color:var(--ac)}
.det ul,.det ol{margin:0;padding-inline-start:20px}
.meta{display:flex;gap:16px;flex-wrap:wrap;color:var(--mut);font-size:14px}
.ph{padding:22px 0;border-top:1px solid var(--ln)}
.ph ol{padding-inline-start:20px;margin:8px 0 0}
footer{padding:28px 16px;text-align:center;color:var(--mut);font-size:13px}
.tools{display:flex;gap:8px;padding:14px 0 30px}
.tools .btn.alt{background:transparent;color:var(--ink);border:1px solid var(--ink)}

.chip.bad{opacity:.55;border-style:dashed}
.best{display:flex;gap:10px;align-items:center;flex-wrap:wrap;padding:8px 0;font-size:14px;color:var(--mut)}
.best .btn{padding:8px 14px}
table{width:100%;border-collapse:collapse;font-size:14px}th,td{padding:6px 8px;border-bottom:1px solid var(--ln);text-align:start}td input{width:90px;padding:4px 6px}
.tot{font-weight:600;margin:8px 0 0}.dims{display:flex;gap:16px;flex-wrap:wrap;margin:8px 0}.dims input{width:100px}
@media print{#warns{position:static}.bar,.tools,.opts{display:none}header{background:none;color:#000}}
</style>
</head>
<body>
<div id="gate">
<form id="f" autocomplete="off">
<h1>ALARAB ARCHITECTURE</h1>
<p>دليل التشطيبات الداخلية والخارجية. أدخل كلمة السر للدخول.</p>
<label for="pw" style="font-weight:600">كلمة السر</label>
<input id="pw" type="password" autocomplete="current-password">
<div id="err" role="alert"></div>
<button class="btn" type="submit">دخول</button>
</form>
</div>

<div id="app">
<header><div class="wrap"><h1>ALARAB ARCHITECTURE</h1><p>دليل التشطيبات: اختر المواد وشاهد التوافق والخطوات والمواد المطلوبة</p></div></header>
<main class="wrap">
<div class="bar" id="pbar"></div>
<div class="bar" id="zone" role="group" aria-label="النوع"></div>
<div class="bar" id="space" role="group" aria-label="المكان"></div>
<div id="warns" aria-live="polite"></div>
<div id="best" class="best"></div>
<div id="cats"></div>
<section class="ph" id="calc"></section>
<section class="ph"><h2>مراحل التشطيب بالترتيب الصحيح</h2><ol id="phases"></ol></section>
<section class="ph"><h2>ملاحظات التنفيذ والكود في مصر</h2><ul>
<li>الكهرباء: التزم بالكود المصري للتركيبات الكهربائية، مع تأريض وقواطع تسريب وفصل دوائر الحمام والمطبخ.</li>
<li>الحريق: في المباني العالية راجع اشتراطات الحماية المدنية لمواد الواجهات والأسقف.</li>
<li>السباكة: اختبر الضغط 24 ساعة قبل التغطية، وركّب العزل المائي قبل بلاط الحمامات.</li>
<li>التراخيص: أي تعديل إنشائي أو واجهات يحتاج ترخيصًا من الحي والجهات المختصة.</li>
<li>تحقق من الكود الأحدث والاشتراطات المحلية مع مهندس مختص قبل التنفيذ.</li></ul></section>
<section class="ph"><h2>قائمة فحص الاستلام</h2><ul>
<li>مستوى الأرضيات وغياب الأصوات الجوفاء في البلاط.</li>
<li>رأسية الحوائط وخلو الدهان من الشروخ.</li>
<li>تشغيل كل المفاتيح والبرايز والإضاءة واختبار القواطع.</li>
<li>عدم وجود تسريب في الحمامات والمطابخ، وميل الصرف.</li>
<li>فتح وغلق الأبواب والنوافذ وضبط الأقفال.</li>
<li>تشغيل التكييف والتأكد من التصريف.</li>
<li>مطابقة الأصناف المركّبة للمتفق عليه، وحفظ ضمانات المواد.</li>
<li>تنظيف نهائي وتسليم المفاتيح والرسومات التنفيذية.</li></ul></section>
<div class="tools"><button class="btn alt" onclick="csv()">تحميل جدول الكميات (CSV)</button><button class="btn" onclick="print()">طباعة الاختيارات</button><button class="btn alt" onclick="resetAll()">مسح الاختيارات</button></div>
</main>
<footer>المشاريع وقائمة الأسعار مشتركة بين فريق الشركة عند ربط قاعدة البيانات. الأسعار والكميات تقديرية وتختلف حسب المورد والمشروع. راجع المهندس المسؤول قبل التنفيذ.</footer>
</div>

<script>
const HASH="a0ba35c0b7f86928de83869b456a838eb51a81bd286771ad88bd3bdf29f51108";
async function sha(s){const b=await crypto.subtle.digest("SHA-256",new TextEncoder().encode(s));return[...new Uint8Array(b)].map(x=>x.toString(16).padStart(2,"0")).join("")}
f.addEventListener("submit",async e=>{e.preventDefault();let ok=false;try{ok=(await sha(pw.value.trim()))===HASH}catch(_){err.textContent="يجب فتح الموقع عبر رابط https";return}
if(ok){try{sessionStorage.setItem("al","1")}catch(_){}gate.style.display="none";app.style.display="block";init()}else{err.textContent="كلمة السر غير صحيحة";pw.select()}});
try{if(sessionStorage.getItem("al")==="1"){gate.style.display="none";app.style.display="block";addEventListener("DOMContentLoaded",init);if(document.readyState!=="loading")init()}}catch(_){}

/* c: التكلفة 1-3 | w: مناسب للأماكن الرطبة | st: الستايل | hv: ثقيل */
const M={
floor:{t:"الأرضيات",x:"i",items:[
{id:"por",n:"بورسلين",c:2,w:1,st:"m,c,r",d:"متين وقليل الامتصاص ويناسب كل الغرف.",s:"فحص مستوى الأرضية والمونة|رش وتبليل السطح|فرش مونة لاصق مع مشط سن|تركيب مع فواصل 2 مم|تنظيف بعد 24 ساعة وحشو الفواصل بالجراوت",m:"بلاط بورسلين|لاصق أو مونة|فواصل بلاستيك|جراوت|سقاطة"},
{id:"cer",n:"سيراميك",c:1,w:1,st:"m,r",d:"اقتصادي ومتنوع الألوان، أقل صلابة من البورسلين.",s:"تسوية الأرضية|تبليل السيراميك|تركيب بمونة أسمنتية|ضبط الميل في الأماكن الرطبة|حشو الفواصل",m:"سيراميك|أسمنت ورمل|جراوت|فواصل"},
{id:"mar",n:"رخام طبيعي",c:3,w:1,st:"c,m",slip:1,d:"فخم ويحتاج تلميع وعناية دورية، ينزلق عند البلل.",s:"تجهيز مونة مستوية|فرش الرخام بالمونة والحقن|تقفيل الفواصل|جلخ وتلميع|معالجة بمادة حماية (Sealer)",m:"رخام|مونة|مادة حماية|مواد تلميع"},
{id:"gra",n:"جرانيت",c:2,w:1,st:"m,c",d:"شديد التحمل للخدش والرطوبة ويناسب المداخل والمطابخ.",s:"تسوية الأرضية|فرش الجرانيت بمونة|ضبط المناسيب|تنظيف الفواصل|تلميع",m:"جرانيت|مونة|مادة حماية"},
{id:"lam",n:"باركيه لامينيت",c:2,w:0,st:"r,m",d:"دافئ ومريح، يتأثر بالمياه وعدم المسطح.",s:"التأكد من جفاف الأرضية|فرش طبقة عازلة (فوم)|تركيب الألواح بالتعشيق|ترك فراغ 10 مم عند الحوائط|تركيب وزرات",m:"ألواح لامينيت|فوم عازل|وزرة|بلاستيك عازل رطوبة"},
{id:"spc",n:"فينيل SPC",c:2,w:1,st:"m",d:"عازل للمياه ورفيع الارتفاع، مناسب للتجديد.",s:"تنظيف وتسوية الأرضية|فرش الألواح بالتعشيق|ترك فراغ تمدد|تركيب الوزرة",m:"ألواح SPC|وزرة|مادة تسوية"},
{id:"epx",n:"إيبوكسي",c:2,w:1,st:"m",d:"سطح مصمت بدون فواصل، مناسب للمطابخ والمحلات.",s:"جلخ الخرسانة وتنظيفها|طبقة برايمر|طبقة إيبوكسي أساسية|طبقة نهائية|معالجة 24 إلى 72 ساعة",m:"برايمر|إيبوكسي|ملونات|ورنيش نهائي"}]},
wall:{t:"الحوائط",x:"i",items:[
{id:"pnt",n:"دهان بلاستيك",c:1,w:0,st:"m,c,r",d:"الأكثر شيوعًا ويناسب كل الغرف الجافة.",s:"معجون وصنفرة|طبقة سيلر|وجهان دهان|تلميع خفيف أو تشطيب مطفي",m:"معجون|سيلر|دهان بلاستيك|صنفرة"},
{id:"wp",n:"ورق حائط",c:2,w:0,st:"c,r",d:"سريع التنفيذ وتشكيلات غير محدودة، لا يناسب الرطوبة.",s:"تسوية السطح وسيلر|قياس وقص الشرائح|لصق بالغراء المخصص|إزالة الفقاعات",m:"ورق حائط|غراء|سيلر"},
{id:"wt",n:"سيراميك أو بورسلين حوائط",c:2,w:1,hv:1,st:"m,r",d:"مناسب للحمامات والمطابخ.",s:"طرطشة وتخشين الحائط|تركيب مونة أو لاصق|ضبط الفواصل والأفقي|جراوت",m:"بلاط|لاصق|فواصل|جراوت"},
{id:"wd",n:"ألواح WPC أو خشب",c:2,w:0,st:"r,m",d:"دافئ وأنيق، لا يناسب الأماكن الرطبة.",s:"تثبيت شدادات خشبية أو معدنية|تثبيت الألواح بالمشابك|معالجة الأركان",m:"ألواح WPC|شدادات|مسامير ومشابك"},
{id:"stn",n:"حجر أو ستون",c:3,w:1,hv:1,st:"c,r",d:"مظهر فاخر وثقيل، يحتاج تثبيتًا قويًا.",s:"عمل شبكة تثبيت|تركيب بمونة لاصقة قوية|تنظيف الفواصل|عزل بمادة حماية",m:"حجر|لاصق حجر|مادة حماية"},
{id:"plt",n:"استوكو ديكوري",c:3,w:0,st:"c,m",d:"ملمس رخامي لامع، تنفيذ بواسطة عمالة متخصصة.",s:"تجهيز سطح مستوٍ|طبقتان أساسيتان|طبقات التشطيب|تلميع بالشمع",m:"مواد استوكو|شمع|أدوات تلميع"}]},
ceil:{t:"الأسقف",x:"i",items:[
{id:"gyp",n:"جيبس بورد عادي",c:1,w:0,st:"m,c,r",d:"يسمح بالإضاءة المخفية، لا يناسب الرطوبة.",s:"عمل هيكل معدني معلّق|تثبيت الألواح|معالجة الفواصل بالشريط|معجون ودهان",m:"ألواح جيبس|هيكل معدني|مسامير|شريط وفواصل"},
{id:"gyw",n:"جيبس بورد مقاوم للرطوبة (أخضر)",c:2,w:1,st:"m,c",d:"مناسب للحمامات والمطابخ.",s:"هيكل معدني مجلفن|تثبيت الألواح الخضراء|معجون مقاوم|دهان مقاوم للرطوبة",m:"ألواح مقاومة للرطوبة|هيكل مجلفن|دهان"},
{id:"pvc",n:"PVC",c:1,w:1,st:"m",d:"اقتصادي ومقاوم للمياه، مظهره بسيط.",s:"تثبيت الفريمات|تركيب الألواح بالتعشيق|تقفيل الزوايا",m:"ألواح PVC|فريمات|زوايا"},
{id:"str",n:"سقف شد (Stretch)",c:3,w:1,st:"m",d:"سطح لامع أو مطفي، سريع التركيب.",s:"تثبيت البروفايل على الحائط|تسخين وتمديد الغشاء|تقفيل وفتح فتحات الإضاءة",m:"غشاء شد|بروفايل|مسدس تسخين"},
{id:"plt2",n:"محارة ودهان مباشر",c:1,w:1,st:"r,m",d:"بسيط وموفر.",s:"تأسيس المحارة|معجون|دهان",m:"محارة|معجون|دهان"}]},
face:{t:"الواجهة",x:"o",items:[
{id:"fp",n:"دهان خارجي ضد العوامل",c:1,w:1,st:"m,r",d:"اقتصادي وتجديده سهل.",s:"تنظيف ومعالجة الشروخ|سيلر خارجي|وجهان دهان",m:"سيلر خارجي|دهان خارجي|معجون خارجي"},
{id:"hs",n:"حجر هاشمي",c:3,w:1,hv:1,st:"c,r",d:"ثقيل وطبيعي، شائع في الواجهات.",s:"تجهيز الحائط بالسيخ|تركيب بالمونة|تقفيل وتنظيف|معالجة بمادة حماية",m:"حجر هاشمي|مونة|مادة حماية"},
{id:"acp",n:"ألوميتال (ACP)",c:3,w:1,st:"m",fire:1,d:"خفيف وحديث، اختر نوعًا مقاومًا للحريق في المباني العالية.",s:"عمل شبكة هيكل معدني|تثبيت الألواح|حشو الفواصل بسيليكون خارجي",m:"ألواح ACP|هيكل ألومنيوم|سيليكون"},
{id:"hpl",n:"HPL",c:3,w:1,st:"m,r",d:"مقاوم للأشعة ويعطي مظهر الخشب.",s:"تثبيت شبكة|تثبيت الألواح ببراغي مخفية",m:"ألواح HPL|هيكل|براغي"},
{id:"grc",n:"GRC",c:2,w:1,st:"c",d:"عناصر كلاسيكية خفيفة الوزن وقابلة للتشكيل.",s:"تثبيت الشبكة|تركيب العناصر|دهان",m:"عناصر GRC|مونة|دهان"}]},
grd:{t:"الأرضيات الخارجية",x:"o",items:[
{id:"int",n:"إنترلوك",c:1,w:1,st:"r,m",d:"يسمح بنفاذ المياه ويسهل صيانته.",s:"حفر وردم|طبقة رمل|رص القطع|دك وتثبيت|رمل ناعم بين الفواصل",m:"قطع إنترلوك|رمل|طبقة أساس"},
{id:"pco",n:"بورسلين خارجي 2 سم",c:3,w:1,st:"m,c",d:"مظهر أنيق، خاص بالأماكن الخارجية فقط.",s:"خرسانة مستوية|مونة لاصق خاص|تركيب بفواصل|جراوت",m:"بورسلين 2 سم|لاصق|فواصل"},
{id:"nst",n:"حجر طبيعي",c:3,w:1,st:"r,c",d:"متين ويناسب المداخل.",s:"تجهيز خرسانة|تركيب بمونة|ضبط الميل|حماية",m:"حجر|مونة|مادة حماية"}]},
roof:{t:"السطح والعزل",x:"o",items:[
{id:"bit",n:"رولات بيتومين",c:1,w:1,st:"m",d:"شائع ومتين.",s:"تنظيف|برايمر|لحام الرولات بالتراكب|حماية بطبقة نهائية",m:"برايمر|رولات بيتومين|غاز"},
{id:"pu",n:"بولي يوريثان سائل",c:2,w:1,st:"m",d:"سطح واحد متصل بلا فواصل.",s:"تجهيز وتنظيف|برايمر|طبقتان من البولي يوريثان",m:"برايمر|بولي يوريثان"},
{id:"xps",n:"عزل حراري XPS مع عزل مائي",c:3,w:1,st:"m",d:"يقلل الحرارة ويحمي السطح.",s:"عزل مائي|ألواح XPS|طبقة فصل|بلاطة حماية",m:"ألواح XPS|رولات|طبقة فصل"}]},
door:{t:"الأبواب",x:"i",r:["liv","bed","kid","kit","bth","off","ent"],items:[
{id:"dwd",n:"خشب طبيعي (زان)",c:3,w:0,st:"c,r",d:"متين وفاخر ولا يناسب الحمامات.",s:"أخذ المقاسات بعد التشطيب|تثبيت الحلق بالفوم|تعليق الضلفة|تركيب الكالون والمفصلات|ضبط الضلفة",m:"باب وحلق|مفصلات|كالون|فوم تثبيت"},
{id:"dmd",n:"MDF مغلف",c:2,w:0,st:"m,c",d:"اقتصادي بأشكال كثيرة ويتأثر بالمياه.",s:"أخذ المقاسات|تثبيت الحلق|تركيب الضلفة|تركيب الكالون",m:"باب MDF|حلق|مفصلات|كالون"},
{id:"dpv",n:"PVC أو WPC",c:1,w:1,st:"m",d:"يتحمل الرطوبة ويناسب الحمامات والمطابخ.",s:"أخذ المقاسات|تثبيت الحلق|تركيب الضلفة|تركيب الكالون",m:"باب PVC|حلق|كالون"},
{id:"dst",n:"باب مصفح",c:3,w:1,st:"m,c",d:"للمدخل الرئيسي فقط.",s:"تركيب الحلق الحديد بالخرسانة|تعليق الضلفة|ضبط الأقفال والعين السحرية",m:"باب مصفح|أقفال|عين سحرية"},
{id:"dal",n:"ألوميتال وزجاج",c:2,w:1,st:"m",d:"مناسب للبلكونات والمطابخ المفتوحة.",s:"أخذ المقاسات|تثبيت الإطار|تركيب الزجاج|تركيب الإكسسوارات",m:"قطاعات ألومنيوم|زجاج|إكسسوار"}]},
win:{t:"النوافذ",x:"b",r:["liv","bed","kid","kit","bth","off","ent","fac"],items:[
{id:"wal",n:"ألومنيوم عادي",c:1,w:1,st:"m",d:"اقتصادي ومتوفر.",s:"فتحة بمقاس دقيق|تثبيت الحلق|تركيب الضلف والزجاج|عزل بالسيليكون",m:"قطاعات ألومنيوم|زجاج|سيليكون"},
{id:"wtb",n:"ألومنيوم قطع حراري",c:3,w:1,st:"m",d:"عزل حراري وصوتي عالٍ.",s:"قياس دقيق|تثبيت الحلق|تركيب الزجاج المزدوج|عزل بالفوم والسيليكون",m:"قطاعات قطع حراري|زجاج مزدوج|فوم وسيليكون"},
{id:"wpv",n:"uPVC",c:2,w:1,st:"m,r",d:"عازل وقليل الصيانة.",s:"قياس|تثبيت الحلق|تركيب الضلف|عزل",m:"قطاعات uPVC|زجاج|سيليكون"},
{id:"wwd",n:"خشب",c:3,w:0,st:"c,r",d:"دافئ ويحتاج صيانة دورية.",s:"قياس|تثبيت الحلق|تركيب الضلف|دهان حماية",m:"خشب|زجاج|ورنيش"}]},
elec:{t:"الكهرباء",x:"i",r:["liv","bed","kid","kit","bth","off","ent"],items:[
{id:"e1",n:"تأسيس قياسي",c:1,w:1,st:"m",d:"مواسير وأسلاك نحاس بمقاسات قياسية.",s:"رسم النقاط على الحائط|حفر وتركيب المواسير|سحب الأسلاك|تركيب علب التوصيل|اختبار العزل",m:"مواسير|أسلاك نحاس|علب|مفاتيح وبرايز"},
{id:"e2",n:"تأسيس متكامل بقواطع حماية",c:2,w:1,st:"m",d:"مناطق مستقلة وقواطع تسريب وتأريض.",s:"تقسيم الدوائر|تأسيس المواسير والأسلاك|تركيب لوحة التوزيع والقواطع|تأريض|اختبار",m:"أسلاك مقاسات مناسبة|لوحة توزيع|قواطع|تأريض"},
{id:"e3",n:"منزل ذكي (Smart)",c:3,w:1,st:"m",d:"تحكم بالإضاءة والستائر والتكييف.",s:"تصميم المخطط|تأسيس كابلات التحكم|تركيب الوحدات|برمجة|تجربة",m:"وحدات تحكم|كابلات|مفاتيح ذكية|هب"}]},
plum:{t:"السباكة",x:"i",r:["kit","bth"],items:[
{id:"p1",n:"PPR",c:1,w:1,st:"m",d:"شائع ويتحمل الحرارة.",s:"رسم نقاط المياه|تقطيع ولحام المواسير|تثبيت|اختبار ضغط 24 ساعة|طرطشة وتغطية",m:"مواسير PPR|وصلات|مثبتات|محابس"},
{id:"p2",n:"PEX",c:2,w:1,st:"m",d:"مرن وبلا وصلات داخل الحائط.",s:"رسم النقاط|تمديد وتوصيل|تثبيت|اختبار ضغط",m:"مواسير PEX|مشعب|وصلات"},
{id:"p3",n:"نحاس",c:3,w:1,st:"c",d:"أعلى تحملًا وأعلى سعرًا.",s:"رسم|تقطيع ولحام|تثبيت|اختبار ضغط",m:"مواسير نحاس|وصلات|قصدير لحام"}]},
light:{t:"الإضاءة",x:"i",r:["liv","bed","kid","kit","bth","off","ent"],items:[
{id:"l1",n:"سبوت LED",c:1,w:1,st:"m",d:"إضاءة عامة موزعة.",s:"تحديد الأماكن|قص فتحات السقف|توصيل ودرايفر|تركيب القطع",m:"سبوت LED|درايفر|كابلات"},
{id:"l2",n:"شريط LED مخفي",c:2,w:0,st:"m,c",d:"إضاءة غير مباشرة في الجيبس.",s:"تجهيز مجرى بالجيبس|تثبيت الشريط والألومنيوم|توصيل الدرايفر|تجربة",m:"شريط LED|بروفايل|درايفر"},
{id:"l3",n:"نجفة",c:3,w:1,st:"c",d:"للصالات الكبيرة.",s:"تحديد المنتصف|تثبيت خطاف قوي بالخرسانة|التوصيل|التعليق",m:"نجفة|خطاف|كابلات"},
{id:"l4",n:"تراك لايت",c:2,w:1,st:"m",d:"إضاءة موجهة للمعارض والمكاتب.",s:"تثبيت المسار|تركيب الرؤوس|التوصيل",m:"مسار تراك|رؤوس|محول"}]},
san:{t:"الأطقم الصحية",x:"i",r:["bth"],items:[
{id:"s1",n:"طقم اقتصادي (أرضي)",c:1,w:1,st:"m,r",d:"مرحاض أرضي وحوض.",s:"تثبيت المرحاض|تركيب الحوض|توصيل الخلاط والمحابس|اختبار التسريب",m:"مرحاض|حوض|خلاط|محابس"},
{id:"s2",n:"طقم متوسط (مدمج)",c:2,w:1,st:"m,c",d:"مرحاض بخزان مدمج.",s:"تثبيت|توصيل|اختبار",m:"طقم|خلاطات|محابس"},
{id:"s3",n:"طقم معلّق",c:3,w:1,st:"m",d:"مظهر حديث وتنظيف أسهل.",s:"تثبيت الهيكل الحديدي قبل البلاط|تغطية بالجبس والبلاط|تركيب الأطقم|اختبار",m:"هيكل مدفون|مرحاض معلق|حوض|خلاطات"}]},
skirt:{t:"الوزرات",x:"i",r:["liv","bed","kid","kit","bth","off","ent"],items:[
{id:"sk1",n:"بورسلين أو سيراميك",c:1,w:1,st:"m,r",d:"متينة وتناسب كل الأماكن.",s:"قص الوزرة بالمقاس|تثبيت بلاصق أو مونة|حشو الفواصل",m:"وزرة بورسلين|لاصق|جراوت"},
{id:"sk2",n:"MDF مدهون",c:1,w:0,st:"m,c",d:"اقتصادية وسهلة التركيب، لا تناسب الرطوبة.",s:"تثبيت بالغراء والمسامير|معالجة الفواصل بالسيليكون|دهان",m:"وزرة MDF|غراء|سيليكون|دهان"},
{id:"sk3",n:"ألومنيوم",c:2,w:1,st:"m",d:"مظهر حديث وعمر طويل.",s:"تثبيت المشابك|تركيب الوزرة|تقفيل الزوايا",m:"بروفايل ألومنيوم|مشابك|زوايا"}]},
cab:{t:"خزائن المطبخ",x:"i",r:["kit"],items:[
{id:"cb1",n:"ألوميتال",c:2,w:1,st:"m",d:"مقاوم للمياه وسهل التنظيف.",s:"أخذ المقاسات بعد البلاط|تصنيع الوحدات|تركيب السفلي والعلوي|تركيب الكونتر والحوض|ضبط الضلف",m:"ألواح ومفصلات|مجاري|يدات|كونتر"},
{id:"cb2",n:"MDF مقاوم للرطوبة",c:2,w:1,st:"m,c",d:"اختيار شائع بألوان كثيرة.",s:"أخذ المقاسات|التصنيع والتغليف|التركيب|ضبط الضلف",m:"MDF مقاوم|مفصلات|مجاري|يدات"},
{id:"cb3",n:"أكريليك لامع",c:3,w:1,st:"m",d:"مظهر لامع وعصري.",s:"أخذ المقاسات|التصنيع|التركيب|ضبط",m:"أكريليك|مفصلات|مجاري"},
{id:"cb4",n:"خشب طبيعي",c:3,w:0,st:"c,r",d:"فاخر لكنه يتأثر بالرطوبة والحرارة.",s:"أخذ المقاسات|التصنيع|دهان حماية|التركيب",m:"خشب|مفصلات|ورنيش"}]},
ac:{t:"التكييف",x:"i",r:["liv","bed","kid","off"],items:[
{id:"ac1",n:"سبليت",c:1,w:1,st:"m",d:"الأكثر انتشارًا وسهل الصيانة.",s:"تحديد أماكن الوحدات والتصريف|تمديد مواسير النحاس والصرف|تركيب الوحدتين|تفريغ وشحن|اختبار",m:"وحدة سبليت|مواسير نحاس معزولة|كابلات|حامل|مواسير صرف"},
{id:"ac2",n:"دكت",c:3,w:1,st:"m",d:"توزيع مخفي ويحتاج سقفًا معلقًا.",s:"تصميم الدكت|تركيب المجاري في السقف|تركيب الوحدات|تجربة",m:"وحدة دكت|مجاري|فتحات توزيع"},
{id:"ac3",n:"كاسيت",c:3,w:1,st:"m",d:"للصالات الكبيرة، يتطلب سقفًا معلقًا.",s:"تحديد المكان|قص السقف|تثبيت الوحدة|مواسير وصرف|شحن واختبار",m:"وحدة كاسيت|مواسير|كابلات"}]},
curt:{t:"الستائر",x:"i",r:["liv","bed","kid","off"],items:[
{id:"cu1",n:"قماش",c:1,w:0,st:"c,r",d:"أنواع وألوان كثيرة.",s:"قياس العرض والارتفاع|تركيب الشيش|التعليق|الضبط",m:"قماش|شيش|مسامير"},
{id:"cu2",n:"رولر أو زيبرا",c:2,w:1,st:"m",d:"عملي ويتحكم في الإضاءة.",s:"قياس|تثبيت الحوامل|تركيب القماش|ضبط",m:"ستارة رولر|حوامل|مسامير"},
{id:"cu3",n:"بلاك أوت",c:3,w:0,st:"m,c",d:"يمنع الضوء بالكامل ويناسب غرف النوم.",s:"قياس|تركيب الشيش|التعليق|ضبط",m:"قماش بلاك أوت|شيش|مسامير"}]},
stair:{t:"السلالم",x:"i",r:["ent"],items:[
{id:"st1",n:"رخام",c:3,w:1,slip:1,st:"c,m",d:"فخم ويحتاج معالجة ضد الانزلاق.",s:"قياس الدرج|قص القطع|تركيب بمونة قوية|تلميع|تركيب شريط مانع انزلاق",m:"رخام|مونة|شريط مانع انزلاق|درابزين"},
{id:"st2",n:"جرانيت",c:2,w:1,st:"m,c",d:"متين وأقل انزلاقًا.",s:"قياس|قص|تركيب|تنظيف",m:"جرانيت|مونة|درابزين"},
{id:"st3",n:"خشب",c:3,w:0,st:"r,c",d:"دافئ ويناسب الفيلات.",s:"قياس|تصنيع|تثبيت|دهان",m:"خشب|مسامير|ورنيش|درابزين"}]},
gate:{t:"السور والبوابة",x:"o",r:["fac"],items:[
{id:"gt1",n:"بوابة حديد",c:1,w:1,st:"c,m",d:"اقتصادية وتقبل الأشكال المشغولة.",s:"تثبيت الأعمدة|تركيب البوابة|دهان مقاوم للصدأ|ضبط القفل",m:"حديد|مفصلات|دهان صدأ|قفل"},
{id:"gt2",n:"بوابة ألومنيوم",c:2,w:1,st:"m",d:"لا تصدأ وخفيفة.",s:"تثبيت الأعمدة|تركيب البوابة|ضبط",m:"ألومنيوم|مفصلات|قفل"},
{id:"gt3",n:"بوابة أوتوماتيك",c:3,w:1,st:"m",d:"تحكم عن بعد، تحتاج كهرباء وسلامة.",s:"تأسيس كهرباء|تركيب البوابة والموتور|برمجة|اختبار السلامة",m:"بوابة|موتور|ريموت|كابلات"}]},
extl:{t:"الإضاءة الخارجية",x:"o",r:["fac","ter"],items:[
{id:"x1",n:"أعمدة حدائق LED",c:2,w:1,st:"r,m",d:"إضاءة الممرات والحدائق.",s:"تحديد المواقع|تأسيس الكابلات المدفونة|تركيب الأعمدة|اختبار",m:"أعمدة LED|كابلات مدفونة|علب مقاومة"},
{id:"x2",n:"كشافات حائط IP65",c:1,w:1,st:"m",d:"مقاومة للمياه والغبار.",s:"تحديد|تأسيس|تركيب|اختبار",m:"كشافات IP65|كابلات"},
{id:"x3",n:"إضاءة أرضية",c:2,w:1,st:"m,c",d:"إضاءة الواجهات والممرات من الأرض.",s:"تحديد|تأسيس|تركيب|اختبار",m:"كشافات أرضية|كابلات|علب"}]},
rail:{t:"الدرابزين والحدادة",x:"i",r:["ent"],items:[
{id:"rl1",n:"حديد مشغول",c:1,w:1,st:"c,r",d:"اقتصادي وأشكال كثيرة.",s:"قياس السلم|تصنيع الأجزاء|تثبيت بالحوامل|دهان مقاوم للصدأ",m:"حديد|لحام|دهان صدأ|مسامير"},
{id:"rl2",n:"ستانلس ستيل",c:2,w:1,st:"m",d:"لا يصدأ وعمره طويل.",s:"قياس|تصنيع|تثبيت|تلميع",m:"ستانلس|لحام|حوامل"},
{id:"rl3",n:"زجاج سيكوريت",c:3,w:1,st:"m,c",d:"مظهر خفيف وعصري.",s:"قياس دقيق|تصنيع الزجاج|تثبيت بالمشابك|تقفيل",m:"زجاج سيكوريت|مشابك ستانلس|مسامير"}]},
acou:{t:"العزل الصوتي",x:"i",r:["liv","bed","off"],items:[
{id:"au1",n:"صوف صخري داخل الجدران",c:2,w:0,st:"m",d:"يقلل نقل الصوت بين الغرف.",s:"تجهيز الهيكل|حشو الصوف الصخري|تغطية بألواح الجيبس|معجون",m:"صوف صخري|هيكل|ألواح جيبس"},
{id:"au2",n:"جيبس مزدوج مع عازل",c:2,w:0,st:"m",d:"طبقتان من الجيبس بينهما عازل.",s:"تثبيت الهيكل|طبقة جيبس أولى|عازل|طبقة ثانية|معالجة الفواصل",m:"ألواح جيبس|عازل|هيكل"},
{id:"au3",n:"فوم تحت الأرضية",c:1,w:0,st:"m,r",d:"يقلل صوت الخطوات.",s:"تنظيف الأرضية|فرش الفوم|تركيب الأرضية فوقه",m:"فوم عازل|شريط لاصق"}]},
fire:{t:"الحريق والإنذار",x:"i",r:["liv","bed","kid","kit","off","ent"],items:[
{id:"fr1",n:"كاشف دخان مستقل",c:1,w:1,st:"m",d:"أبسط وسيلة إنذار مبكر.",s:"تحديد أماكن السقف|تثبيت القاعدة|تركيب البطارية|اختبار",m:"كاشف دخان|بطارية|مسامير"},
{id:"fr2",n:"نظام إنذار متصل",c:2,w:1,st:"m",d:"لوحة تحكم وكواشف وسارينة.",s:"تأسيس الكابلات|تركيب الكواشف|توصيل اللوحة|برمجة واختبار",m:"لوحة إنذار|كواشف|سارينة|كابلات"},
{id:"fr3",n:"رشاشات مياه",c:3,w:1,st:"m",d:"للمباني الكبيرة حسب اشتراطات الحماية المدنية.",s:"تصميم الشبكة|تمديد المواسير|تركيب الرشاشات|اختبار ضغط",m:"مواسير|رشاشات|محابس|مضخة"}]},
heat:{t:"سخان المياه",x:"i",r:["bth","kit"],items:[
{id:"ht1",n:"كهرباء",c:1,w:1,st:"m",d:"الأسهل في التركيب.",s:"تحديد الموضع|تركيب الحامل|توصيل المياه والكهرباء|اختبار",m:"سخان|مواسير|قاطع مخصص"},
{id:"ht2",n:"غاز",c:2,w:1,st:"m",d:"سريع وأوفر في التشغيل، يحتاج تهوية.",s:"تحديد موضع آمن|تمديد الغاز والشفط|تركيب|اختبار تسريب",m:"سخان غاز|مواسير غاز|ماسورة شفط"},
{id:"ht3",n:"طاقة شمسية",c:3,w:1,st:"m",d:"توفير على المدى الطويل.",s:"تحديد مكان اللوح على السطح|تركيب|مواسير|اختبار",m:"لوح شمسي|خزان|مواسير معزولة"}]},
sec:{t:"الأمن والتيار الخفيف",x:"b",r:["ent","fac"],items:[
{id:"sc1",n:"كاميرات مراقبة",c:2,w:1,st:"m",d:"تغطية المداخل والواجهة.",s:"تحديد الزوايا|تمديد الكابلات|تركيب الكاميرات والمسجل|ضبط",m:"كاميرات|مسجل|كابلات|مصدر طاقة"},
{id:"sc2",n:"إنتركم فيديو",c:2,w:1,st:"m",d:"التحدث مع الزائر قبل فتح الباب.",s:"تأسيس الكابلات|تركيب الوحدتين|ربط القفل|اختبار",m:"وحدة خارجية وداخلية|كابلات|قفل كهربائي"},
{id:"sc3",n:"نظام أمني متكامل",c:3,w:1,st:"m",d:"كاميرات وإنذار سرقة وتحكم.",s:"تصميم النظام|تأسيس|تركيب|برمجة|تدريب",m:"لوحة|حساسات|كاميرات|سارينة"}]},
land:{t:"تنسيق الحدائق",x:"o",r:["ter"],items:[
{id:"ld1",n:"نجيل طبيعي",c:1,w:1,st:"r",d:"يحتاج ري وعناية.",s:"تسوية التربة|فرش التربة الزراعية|زراعة النجيل|ري",m:"تربة|نجيل|سماد"},
{id:"ld2",n:"نجيل صناعي",c:2,w:1,st:"m",d:"بلا صيانة تقريبًا.",s:"تسوية وفرش رمل|فرش النجيل|تثبيت الحواف",m:"نجيل صناعي|رمل|لاصق|مسامير"},
{id:"ld3",n:"ري بالتنقيط وأحواض",c:2,w:1,st:"r,m",d:"توفير مياه وتنسيق نباتات.",s:"تصميم الأحواض|تمديد شبكة الري|الزراعة|ضبط المؤقت",m:"مواسير ري|نقاطات|مؤقت|تربة|نباتات"}]}
};
const SP={i:[
["liv","غرفة معيشة",0,{floor:["por","gra","mar"],wall:["pnt","wp","plt"],ceil:["gyp"],door:["dmd","dwd"],win:["wtb","wpv"],elec:["e2","e3"],light:["l1","l2","l3"]}],
["bed","غرفة نوم",0,{floor:["lam","spc","por"],wall:["pnt","wp","wd"],ceil:["gyp","plt2"],door:["dmd","dwd"],win:["wtb","wpv"],elec:["e2"],light:["l2","l1"]}],
["kid","غرفة أطفال",0,{floor:["spc","lam"],wall:["pnt","wp"],ceil:["gyp"],door:["dmd"],win:["wpv","wtb"],elec:["e2"],light:["l1"]}],
["kit","مطبخ",1,{floor:["por","gra","epx"],wall:["wt"],ceil:["gyw","pvc"],door:["dpv","dal"],win:["wal","wpv"],elec:["e2"],plum:["p1","p2"],light:["l1"]}],
["bth","حمام",1,{floor:["por","cer"],wall:["wt"],ceil:["gyw","pvc","str"],door:["dpv"],win:["wal","wpv"],elec:["e2"],plum:["p1","p2"],light:["l1"],san:["s2","s3","s1"]}],
["off","مكتب",0,{floor:["lam","por","spc"],wall:["pnt","wd"],ceil:["gyp"],door:["dmd","dwd"],win:["wtb","wpv"],elec:["e2"],light:["l4","l1"]}],
["ent","مدخل وصالة",0,{floor:["mar","gra","por"],wall:["stn","plt","pnt"],ceil:["gyp"],door:["dst"],win:["wal","wtb"],elec:["e2"],light:["l1","l3"]}]],
o:[["fac","الواجهة",0,{face:["hs","acp","hpl","grc","fp"],win:["wtb","wpv"]}],["ter","تراس وحوش",0,{grd:["pco","int","nst"]}],["rof","السطح",0,{roof:["xps","pu","bit"]}]]};
const PR={por:[480,"م²"],cer:[310,"م²"],mar:[1100,"م²"],gra:[1700,"م²"],lam:[400,"م²"],spc:[600,"م²"],epx:[500,"م²"],pnt:[90,"م²"],wp:[350,"م²"],wt:[410,"م²"],wd:[1200,"م²"],stn:[1500,"م²"],plt:[700,"م²"],gyp:[450,"م²"],gyw:[600,"م²"],pvc:[300,"م²"],str:[900,"م²"],plt2:[180,"م²"],fp:[200,"م²"],hs:[1100,"م²"],acp:[1800,"م²"],hpl:[2500,"م²"],grc:[1500,"م²"],int:[350,"م²"],pco:[900,"م²"],nst:[1400,"م²"],bit:[250,"م²"],pu:[350,"م²"],xps:[600,"م²"],dwd:[6500,"قطعة"],dmd:[3500,"قطعة"],dpv:[1800,"قطعة"],dst:[9000,"قطعة"],dal:[3000,"قطعة"],wal:[2800,"م²"],wtb:[5500,"م²"],wpv:[3800,"م²"],wwd:[6000,"م²"],e1:[350,"نقطة"],e2:[500,"نقطة"],e3:[1200,"نقطة"],p1:[450,"نقطة"],p2:[600,"نقطة"],p3:[1200,"نقطة"],l1:[120,"قطعة"],l2:[160,"متر"],l3:[3500,"قطعة"],l4:[900,"قطعة"],s1:[5500,"طقم"],s2:[9000,"طقم"],s3:[15000,"طقم"],sk1:[90,"متر"],sk2:[70,"متر"],sk3:[130,"متر"],cb1:[5500,"متر"],cb2:[6500,"متر"],cb3:[9500,"متر"],cb4:[12000,"متر"],ac1:[22000,"قطعة"],ac2:[30000,"قطعة"],ac3:[38000,"قطعة"],cu1:[450,"م²"],cu2:[650,"م²"],cu3:[850,"م²"],st1:[1500,"متر"],st2:[1200,"متر"],st3:[1800,"متر"],gt1:[14000,"قطعة"],gt2:[18000,"قطعة"],gt3:[38000,"قطعة"],x1:[1800,"قطعة"],x2:[900,"قطعة"],x3:[700,"قطعة"],rl1:[1800,"متر"],rl2:[2800,"متر"],rl3:[4200,"متر"],au1:[250,"م²"],au2:[350,"م²"],au3:[120,"م²"],fr1:[600,"قطعة"],fr2:[1500,"قطعة"],fr3:[1800,"قطعة"],ht1:[5500,"قطعة"],ht2:[9000,"قطعة"],ht3:[25000,"قطعة"],sc1:[2500,"قطعة"],sc2:[4500,"قطعة"],sc3:[15000,"قطعة"],ld1:[120,"م²"],ld2:[350,"م²"],ld3:[200,"م²"]};
const REC2={liv:{skirt:["sk1","sk2"],ac:["ac1"],curt:["cu1","cu2"]},bed:{skirt:["sk2","sk1"],ac:["ac1"],curt:["cu3","cu1"]},kid:{skirt:["sk2"],ac:["ac1"],curt:["cu2"]},kit:{skirt:["sk1"],cab:["cb1","cb2"]},bth:{skirt:["sk1"]},off:{skirt:["sk2","sk1"],ac:["ac1"],curt:["cu2"]},ent:{skirt:["sk1"],stair:["st2","st1"]},fac:{gate:["gt1","gt2"],extl:["x2","x1"]},ter:{extl:["x1","x3"]}};
Object.entries(REC2).forEach(([id,r])=>Object.assign([...SP.i,...SP.o].find(x=>x[0]===id)[3],r));
const REC3={liv:{fire:["fr1"],acou:["au2"]},bed:{fire:["fr1"],acou:["au3","au2"]},kid:{fire:["fr1"]},kit:{fire:["fr1"],heat:["ht1","ht2"]},bth:{heat:["ht1","ht3"]},off:{fire:["fr1"],acou:["au2"]},ent:{fire:["fr1"],rail:["rl1","rl2"],sec:["sc2","sc1"]},fac:{sec:["sc1","sc3"]},ter:{land:["ld1","ld3"]}};
Object.entries(REC3).forEach(([id,r])=>Object.assign([...SP.i,...SP.o].find(x=>x[0]===id)[3],r));
const DA={liv:25,bed:16,kid:12,kit:10,bth:5,off:12,ent:8,fac:120,ter:30,rof:80};
let DIM={},QO={},PX={};
const r1=n=>Math.round(n*10)/10,fm=n=>Math.round(n).toLocaleString("en-US");
function zoneOf(sp){return SP.i.some(x=>x[0]===sp)?"i":"o"}
function applies(k,sp){const m=M[k];return(m.x===zoneOf(sp)||m.x==="b")&&(!m.r||m.r.includes(sp))}
function inZ(k){return applies(k,space)}
function dim(sp){return DIM[sp]||(DIM[sp]={a:DA[sp],h:3})}
function Q(sp,k,id){const d=dim(sp),A=d.a,u=PR[id][1];
if(k==="cab")return 6;if(k==="rail")return 6;if(id==="sc1")return 4;if(k==="stair")return 8;if(k==="extl")return 6;if(k==="curt")return r1(Math.max(2,A*.2));
if(k==="win")return r1(Math.max(1.2,A*(zoneOf(sp)==="o"?.15:.12)));
if(zoneOf(sp)==="o"&&u==="م²")return A;
if(k==="wall")return r1(4*Math.sqrt(A)*d.h*.85);
if(k==="floor")return r1(A*1.1);
if(u==="م²")return A;
if(u==="نقطة")return k==="plum"?(sp==="bth"?6:4):Math.max(3,Math.round(A*.9));
if(u==="متر")return r1(4*Math.sqrt(A));
if(id==="l1")return Math.max(3,Math.round(A*.7));
return 1}
function rowsFor(sp){return Object.keys(M).filter(k=>applies(k,sp)&&pick[sp+k]).map(k=>{const id=pick[sp+k],it=M[k].items.find(i=>i.id===id),q=QO[sp+k]??Q(sp,k,id),p=PX[id]??PR[id][0];return{k,it,q,p,u:PR[id][1],t:q*p}})}
function calc(){
const d=dim(space),rows=rowsFor(space),sub=rows.reduce((a,r)=>a+r.t,0),ext=zoneOf(space)==="o";
let all=0;[...SP.i,...SP.o].forEach(x=>rowsFor(x[0]).forEach(r=>all+=r.t));
document.getElementById("calc").innerHTML="<h2>الكميات والتكلفة التقديرية</h2><p class='sub'>أسعار الأرضيات والبلاط والرخام والباركيه مبنية على أسعار مواد منشورة في السوق المصري خلال 2026 مع بدل تركيب تقديري، وباقي الأسعار تقديرية. تختلف حسب المورد والمنطقة، فعدّل أي سعر أو كمية. كمية الأرضيات تشمل 10% هالك.</p><div class='dims'><label>"+(ext?"المساحة":"مساحة الغرفة")+" (م²) <input type='number' min='1' step='any' value='"+d.a+"' id='da'></label>"+(ext?"":"<label>الارتفاع (م) <input type='number' min='2' step='any' value='"+d.h+"' id='dh'></label>")+"</div><div style='overflow-x:auto'><table><thead><tr><th>البند</th><th>الكمية</th><th>الوحدة</th><th>سعر الوحدة</th><th>الإجمالي</th></tr></thead><tbody>"+(rows.length?rows.map(r=>"<tr><td>"+M[r.k].t+": "+r.it.n+"</td><td><input type='number' min='0' step='any' value='"+r.q+"' data-q='"+space+r.k+"'></td><td>"+r.u+"</td><td><input type='number' min='0' step='any' value='"+r.p+"' data-p='"+r.it.id+"'></td><td>"+fm(r.t)+"</td></tr>").join(""):"<tr><td colspan='5'>اختر بنودًا لتظهر الحسابات</td></tr>")+"</tbody></table></div><p class='tot'>إجمالي هذا المكان: "+fm(sub)+" ج.م</p><p class='tot'>إجمالي كل الأماكن المختارة: "+fm(all)+" ج.م</p>";
const clr=()=>Object.keys(QO).forEach(k=>{if(k.startsWith(space))delete QO[k]});
document.getElementById("da").onchange=e=>{d.a=Math.max(1,+e.target.value||d.a);clr();save();calc()};
const dh=document.getElementById("dh");if(dh)dh.onchange=e=>{d.h=Math.max(2,+e.target.value||d.h);clr();save();calc()};
document.querySelectorAll("[data-q]").forEach(i=>i.onchange=()=>{QO[i.dataset.q]=Math.max(0,+i.value||0);save();calc()});
document.querySelectorAll("[data-p]").forEach(i=>i.onchange=()=>{PX[i.dataset.p]=Math.max(0,+i.value||0);save();calc()})}
const PH=["تسليم الموقع والقياسات والرسومات التنفيذية","أعمال الهدم والتكسير","الأعمال الكهربائية والسباكة (الحفر والمواسير)","اختبار الضغط وتشغيل المواسير","المحارة","العزل المائي في الحمامات والمطابخ","الأسقف المعلّقة","اللياسة الأساسية والمعجون","تركيب الأرضيات والحوائط","الدهانات (الوجه الأول)","تركيب الأبواب والنوافذ والأطقم","الدهان النهائي وتركيب الإضاءة","التنظيف والاستلام"];
const CN=["","اقتصادي","متوسط","مرتفع"];
let zone="i",space="liv",pick={};
const DB_URL="";/* رابط Firebase Realtime Database الخاص بالشركة، راجع ملف SETUP.md */
let PROJ={},cur=null,tmr=null,dirty=false,stat="",started=false;
async function api(p,m,b){const r=await fetch(DB_URL.replace(/\/$/,"")+p+".json",{method:m||"GET",body:b!==undefined?JSON.stringify(b):undefined});if(!r.ok)throw new Error("db");return r.json()}
function status(m){stat=m;const e=document.getElementById("st");if(e)e.textContent=m}
function useP(id){cur=id;const p=PROJ[id]||{};pick=p.pick||{};QO=p.QO||{};DIM=p.DIM||{}}
function newId(){return"p"+Date.now().toString(36)+Math.random().toString(36).slice(2,5)}
async function loadAll(){let d=null;try{d=DB_URL?await api("/alarab"):JSON.parse(localStorage.getItem("al_all")||"null");status(DB_URL?"متصل بقاعدة الشركة":"وضع محلي: البيانات على هذا الجهاز فقط")}catch(_){status("تعذر الاتصال بقاعدة الشركة")}
d=d||{};PROJ=d.projects||{};PX=d.prices||{};if(!Object.keys(PROJ).length){PROJ[newId()]={name:"مشروع 1",t:Date.now()}}
let id=null;try{id=localStorage.getItem("al_cur")}catch(_){}if(!PROJ[id])id=Object.keys(PROJ)[0];useP(id)}
function save(){dirty=true;clearTimeout(tmr);tmr=setTimeout(flush,500)}
async function flush(){clearTimeout(tmr);const p=PROJ[cur];if(!p)return;p.pick=pick;p.QO=QO;p.DIM=DIM;p.t=Date.now();
try{if(DB_URL){await api("/alarab/projects/"+cur,"PUT",p);await api("/alarab/prices","PUT",PX);status("متصل بقاعدة الشركة، تم الحفظ")}else{localStorage.setItem("al_all",JSON.stringify({projects:PROJ,prices:PX}));status("وضع محلي: تم الحفظ على هذا الجهاز فقط")}
try{localStorage.setItem("al_cur",cur)}catch(_){}dirty=false}catch(_){status("تعذر الحفظ على قاعدة الشركة، تحقق من الاتصال")}}
async function poll(){if(!DB_URL||document.hidden||dirty)return;if(document.activeElement&&document.activeElement.tagName==="INPUT")return;
try{const d=await api("/alarab")||{};PROJ=d.projects||PROJ;PX=d.prices||{};if(!PROJ[cur])cur=Object.keys(PROJ)[0];useP(cur);renderBar();render()}catch(_){}}
function renderBar(){document.getElementById("pbar").innerHTML="<label>المشروع <select id='ps'>"+Object.entries(PROJ).map(([id,p])=>"<option value='"+id+"'"+(id===cur?" selected":"")+">"+(p.name||"بدون اسم")+"</option>").join("")+"</select></label><button class='chip' id='pn'>مشروع جديد</button><button class='chip' id='pr'>إعادة تسمية</button><button class='chip' id='pd'>حذف المشروع</button><span class='sub' id='st'>"+stat+"</span>";
document.getElementById("ps").onchange=async e=>{await flush();useP(e.target.value);try{localStorage.setItem("al_cur",cur)}catch(_){}render()};
document.getElementById("pn").onclick=async()=>{const n=prompt("اسم المشروع الجديد");if(!n)return;await flush();const id=newId();PROJ[id]={name:n.trim(),t:Date.now()};useP(id);await flush();renderBar();render()};
document.getElementById("pr").onclick=async()=>{const n=prompt("الاسم الجديد",PROJ[cur].name);if(!n)return;PROJ[cur].name=n.trim();await flush();renderBar()};
document.getElementById("pd").onclick=async()=>{if(Object.keys(PROJ).length<2){alert("لا يمكن حذف آخر مشروع");return}if(!confirm("حذف المشروع نهائيًا لكل الفريق؟"))return;const old=cur;delete PROJ[old];try{if(DB_URL)await api("/alarab/projects/"+old,"DELETE")}catch(_){}useP(Object.keys(PROJ)[0]);await flush();renderBar();render()}}
async function init(){if(started)return;started=true;await loadAll();phases.innerHTML=PH.map(x=>"<li>"+x+"</li>").join("");renderBar();render();if(DB_URL)setInterval(poll,20000);document.addEventListener("visibilitychange",()=>{if(!document.hidden)poll()})}
function wet(){return (SP[zone].find(s=>s[0]===space)||[])[2]===1}
function g(k){const m=M[k];return m&&m.items.find(i=>i.id===pick[space+k])}
function R(k){const r=SP[zone].find(x=>x[0]===space);return(r&&r[3]&&r[3][k])||[]}
function bad(i){return zone==="i"&&wet()&&!i.w}
function nm(k,id){return M[k].items.find(i=>i.id===id).n}
function applyBest(){Object.keys(M).filter(inZ).forEach(k=>{const r=R(k);if(r.length)pick[space+k]=r[0]});save();render()}
function render(){
zone_();
const sp=SP[zone].find(x=>x[0]===space);
document.getElementById("best").innerHTML="<span>الأفضل لـ "+sp[1]+" معلّم بنجمة ★</span><button class='btn' id='ab'>طبّق الاختيار الأفضل</button>";
document.getElementById("ab").onclick=applyBest;
cats.innerHTML="";
Object.entries(M).filter(([k])=>inZ(k)).forEach(([k,m])=>{
const cur=g(k);
const s=document.createElement("section");s.className="cat";
s.innerHTML="<h2>"+m.t+"</h2><p class='sub'>"+(R(k).length?"الأفضل لهذا المكان: "+R(k).map(x=>nm(k,x)).join("، "):"اختر نوعًا واحدًا")+"</p><div class='opts' role='radiogroup' aria-label='"+m.t+"'>"+m.items.map(i=>"<button class='chip"+(bad(i)?" bad":"")+"' role='radio' aria-pressed='"+(cur&&cur.id===i.id)+"' data-k='"+k+"' data-i='"+i.id+"'>"+(R(k).includes(i.id)?"★ ":"")+i.n+(bad(i)?" (غير مناسب)":"")+"</button>").join("")+"</div>"+(cur?det(cur):"");
cats.appendChild(s)});
cats.querySelectorAll(".chip").forEach(b=>b.onclick=()=>{pick[space+b.dataset.k]=b.dataset.i;save();render()});
calc();warn()}
function det(i){return "<div class='det'><h3>"+i.n+"</h3><div class='meta'><span>التكلفة: "+CN[i.c]+"</span><span>"+(i.w?"يتحمل الرطوبة":"لا يناسب الرطوبة")+"</span></div><p style='margin:0'>"+i.d+"</p><h4>خطوات التنفيذ</h4><ol>"+i.s.split("|").map(x=>"<li>"+x+"</li>").join("")+"</ol><h4>المواد المطلوبة</h4><ul>"+i.m.split("|").map(x=>"<li>"+x+"</li>").join("")+"</ul></div>"}
function zone_(){
zone_el();}
function zone_el(){
document.getElementById("zone").innerHTML=[["i","تشطيب داخلي"],["o","تشطيب خارجي"]].map(z=>"<button class='tab' aria-pressed='"+(zone===z[0])+"' data-z='"+z[0]+"'>"+z[1]+"</button>").join("");
document.getElementById("space").innerHTML=SP[zone].map(s=>"<button class='chip' aria-pressed='"+(space===s[0])+"' data-s='"+s[0]+"'>"+s[1]+"</button>").join("");
document.querySelectorAll("[data-z]").forEach(b=>b.onclick=()=>{zone=b.dataset.z;space=SP[zone][0][0];render()});
document.querySelectorAll("[data-s]").forEach(b=>b.onclick=()=>{space=b.dataset.s;render()})}
function warn(){
const o=[],w=wet(),F=g("floor"),W=g("wall"),C=g("ceil"),Fa=g("face"),R=g("roof");
if(zone==="i"){
[[F,"الأرضية"],[W,"الحائط"],[C,"السقف"],[g("door"),"الباب"],[g("win"),"النافذة"],[g("cab"),"خزائن المطبخ"],[g("skirt"),"الوزرة"]].forEach(([x,n])=>{if(x&&w&&!x.w)o.push(["bad","تحذير: "+n+" ("+x.n+") لا يتحمل الرطوبة في "+SP.i.find(s=>s[0]===space)[1]+". اختر بديلًا مقاومًا للمياه."])});
if(F&&F.slip&&w)o.push(["note","الرخام الطبيعي زلق عند البلل، ويفضّل استخدام ملمس خشن (Honed) أو بلاط آخر."]);
if(F&&W){const a=F.st.split(","),b=W.st.split(",");if(!a.some(x=>b.includes(x)))o.push(["note","الأرضية والحائط من ستايلين مختلفين، راجع تناسق الألوان والمظهر."])}
if(W&&W.hv&&C&&C.id==="gyp"&&!w)o.push(["note","الحوائط الثقيلة تتطلب حائطًا مبنيًا أو تثبيتًا جيدًا، ولا تُركّب على ألواح جيبس عادية."]);
if(F&&F.id==="lam"&&W&&W.id==="wt")o.push(["note","باركيه لامينيت مع حوائط بلاط: افصل بينهما بوزرة ومعالجة الزوايا بسيليكون."]);
if(F&&C&&F.c===3&&C.c===1)o.push(["note","أرضية مرتفعة التكلفة مع سقف اقتصادي، راجع التوازن العام للتشطيب."]);
const L=g("light"),S=g("san"),D=g("door"),E=g("elec");
if(L&&L.id==="l3"&&C&&C.id==="gyp")o.push(["note","النجفة الثقيلة تحتاج تثبيتًا في الخرسانة، لا تعلّق على الجيبس بورد فقط."]);
if(L&&L.id==="l1"&&C&&C.id==="str")o.push(["note","السقف الشد: استخدم سبوت LED منخفض الحرارة فقط."]);
if(L&&L.id==="l2"&&C&&C.id==="pvc")o.push(["note","الإضاءة المخفية لا تناسب سقف PVC، استخدم جيبس بورد."]);
if(S&&S.id==="s3")o.push(["note","الطقم المعلّق يحتاج هيكلًا حديديًا مدفونًا وحائطًا مبنيًا، قرّره قبل المحارة."]);
if(D&&D.id==="dst"&&space!=="ent")o.push(["note","الباب المصفح مخصص للمدخل الرئيسي."]);
if(E&&E.id==="e3")o.push(["note","المنزل الذكي يحتاج مخططًا للكابلات قبل المحارة."]);
const AC=g("ac"),ST=g("stair"),H=g("heat");
if(H&&H.id==="ht2"&&space==="bth")o.push(["bad","تحذير: سخان الغاز داخل الحمام غير آمن. ضعه خارجه أو في مكان مهوّى مع ماسورة شفط للخارج."]);
if(AC&&AC.id!=="ac1"&&C&&C.id!=="gyp"&&C.id!=="gyw")o.push(["note","الدكت والكاسيت يحتاجان سقفًا معلقًا من الجيبس بورد."]);
if(ST&&ST.slip)o.push(["note","درج الرخام زلق: أضف شريط مانع انزلاق أو حافة خشنة."]);
}else{
const Gt=g("gate");if(Gt&&Gt.id==="gt3")o.push(["note","البوابة الأوتوماتيك تحتاج تأسيس كهرباء وتأريضًا ومستشعرات أمان."]);
if(Fa&&Fa.fire)o.push(["note","ألوميتال: استخدم نوعًا مقاومًا للحريق (FR) في المباني العالية، وراجع اشتراطات الحماية المدنية."]);
if(Fa&&Fa.hv)o.push(["note","واجهة ثقيلة: تأكد من تحمل الهيكل الخرساني وطريقة التثبيت."]);
if(R&&R.id==="bit"&&space==="rof")o.push(["note","الرولات تتأثر بالأشعة، أضف طبقة حماية أو بلاط فوقها."])}
if(!o.length){const n=zone==="i"?[g("floor"),g("wall"),g("ceil")]:[g("face"),g("grd"),g("roof")];o.push(n.every(Boolean)?["good","الاختيارات متوافقة. لا توجد تحذيرات."]:["note","اختر كل البنود لتظهر نتيجة التوافق الكاملة."])}
document.getElementById("warns").innerHTML=o.map(x=>"<div class='w "+x[0]+"'>"+x[1]+"</div>").join("")}
function csv(){const L=[["المكان","البند","الصنف","الكمية","الوحدة","سعر الوحدة","الإجمالي"]];[...SP.i,...SP.o].forEach(x=>rowsFor(x[0]).forEach(r=>L.push([x[1],M[r.k].t,r.it.n,r.q,r.u,r.p,Math.round(r.t)])));const t="\ufeff"+L.map(r=>r.map(c=>'"'+String(c).replace(/"/g,'""')+'"').join(",")).join("\n");const a=document.createElement("a");a.href=URL.createObjectURL(new Blob([t],{type:"text/csv;charset=utf-8"}));a.download="boq-"+(PROJ[cur].name||"alarab")+".csv";a.click()}
function resetAll(){pick={};QO={};save();render()}
</script>
</body>
</html>
