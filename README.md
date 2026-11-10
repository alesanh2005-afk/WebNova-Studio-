<DOCTYPE html>
<html lang="pt-PT">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>WebNova Studio – Criação de sites e lojas online</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@500;700;800&family=Manrope:wght@400;500;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#F6F5FF;--surface:#FFFFFF;--ink:#12123A;--muted:#54567A;--line:#DEDCF5;--accent:#5B3DF5;--on-accent:#FFFFFF;--nova:#FFC93C;color-scheme:light;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0E0F2B;--surface:#171942;--ink:#EFEFFF;--muted:#A6A8D0;--line:#2A2C60;--accent:#8E78FF;--on-accent:#0E0F2B;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#0E0F2B;--surface:#171942;--ink:#EFEFFF;--muted:#A6A8D0;--line:#2A2C60;--accent:#8E78FF;--on-accent:#0E0F2B;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px);scroll-behavior:smooth}
*,*::before,*::after{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:400 1.0625rem/1.65 Manrope,system-ui,sans-serif}
h1,h2,h3{font-family:Sora,Manrope,system-ui,sans-serif;line-height:1.1;margin:0;letter-spacing:-.025em}
a{color:inherit}
:focus-visible{outline:3px solid var(--nova);outline-offset:3px;border-radius:6px}
.wrap{max-width:1140px;margin:0 auto;padding:0 24px}
.btn{display:inline-block;background:var(--nova);color:#12123A;font-weight:700;text-decoration:none;padding:15px 28px;border-radius:12px;border:0;cursor:pointer;font:700 1rem Manrope,sans-serif}
.btn.alt{background:var(--accent);color:var(--on-accent)}
.btn.ghost{background:transparent;color:#fff;border:1.5px solid rgba(255,255,255,.35)}
/* hero (sempre escuro) */
.hero{background:#12123A;color:#fff;position:relative;overflow:hidden}
.star{position:absolute;right:-140px;top:-120px;width:620px;height:620px;opacity:.14;animation:spin 90s linear infinite;pointer-events:none}
@keyframes spin{to{transform:rotate(360deg)}}
header{display:flex;align-items:center;justify-content:space-between;padding:24px 0;position:relative}
.logo{display:flex;align-items:center;gap:11px;text-decoration:none;font:800 1.35rem Sora,sans-serif;letter-spacing:-.03em;color:inherit}
.logo svg{width:36px;height:36px}
.logo span{font-weight:500;opacity:.75}
nav{display:flex;gap:28px;align-items:center}
nav a{text-decoration:none;font-weight:500;color:#C9C9EE}
nav a:hover{color:#fff}
nav .btn{padding:10px 20px;color:#12123A}
.hgrid{display:grid;grid-template-columns:1.1fr 1fr;gap:56px;align-items:center;padding:48px 0 96px;position:relative}
.hero h1{font-size:clamp(2.5rem,5.6vw,4.4rem);font-weight:800}
.hero p{color:#C9C9EE;max-width:46ch;margin:22px 0 32px;font-size:1.15rem}
.cta{display:flex;gap:14px;flex-wrap:wrap}
.proof{display:flex;gap:32px;margin-top:40px;color:#C9C9EE;font-size:.95rem}
.proof b{display:block;font:700 1.6rem Sora,sans-serif;color:#fff}
.demo{min-width:0}
.stage{perspective:1200px;padding:34px 0 50px}
.scene{position:relative;transform-style:preserve-3d;transform:rotateX(var(--rx,10deg)) rotateY(var(--ry,-18deg));transition:transform .2s ease-out}
.scene .browser{position:relative;box-shadow:0 30px 60px rgba(0,0,0,.45)}
.tile{position:absolute;inset:10% -4% -8% 8%;background:#5B3DF5;border-radius:16px;transform:translateZ(-70px);opacity:.9}
.phone{position:absolute;right:0;bottom:-14%;width:24%;aspect-ratio:9/18;background:#fff;border:4px solid #12123A;border-radius:18px;transform:translateZ(80px);box-shadow:0 24px 40px rgba(0,0,0,.5);padding:10px;display:grid;gap:7px;align-content:start}
.phone i{display:block;height:7px;background:#DEDCF5;border-radius:4px}.phone i:first-child{background:#12123A;width:60%}.phone u{display:block;height:34px;background:#FFC93C;border-radius:8px}
.gem{position:absolute;left:-4%;top:-10%;width:20%;transform:translateZ(120px);filter:drop-shadow(0 14px 14px rgba(0,0,0,.45));animation:fl 4s ease-in-out infinite}
@keyframes fl{50%{transform:translateZ(120px) translateY(-10px)}}
.browser{margin:0 auto;width:var(--w,100%);max-width:100%;border-radius:12px;overflow:hidden;background:#F6F5FF;transition:width .1s}
.bar{display:flex;gap:6px;padding:10px 12px;background:#fff;border-bottom:1.5px solid #DEDCF5}
.bar b{width:9px;height:9px;border-radius:50%;background:#DEDCF5}
.page{padding:18px;display:grid;gap:12px;container-type:inline-size}
.page .h{height:16px;width:62%;background:#12123A;border-radius:4px}
.page .l{height:8px;background:#DEDCF5;border-radius:4px}
.page .l.s{width:70%}
.page .b{height:30px;width:90px;background:#5B3DF5;border-radius:8px}
.blocks{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.blocks span{height:60px;border-radius:8px;background:#5B3DF5}
.blocks span:nth-child(2){background:#FFC93C}
.blocks span:nth-child(3){background:#12123A}
@container (max-width:300px){.blocks{grid-template-columns:1fr}.blocks span{height:32px}}
.ctrl{display:flex;align-items:center;gap:14px;margin-top:16px;font-size:.92rem;color:#C9C9EE}
.ctrl input{flex:1;accent-color:#FFC93C}
.ctrl output{min-width:5ch;text-align:right;font-weight:700;color:#fff}
/* planos */
.plans{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;margin-top:40px;perspective:1000px}
.plan{background:var(--bg);border:1.5px solid var(--line);border-radius:18px;padding:30px;transition:transform .15s,box-shadow .15s;will-change:transform;display:flex;flex-direction:column}
.plan:hover{box-shadow:0 24px 40px rgba(18,18,58,.18)}
.plan.hot{background:#12123A;color:#fff;border-color:var(--accent)}
.plan h3{font-size:1.3rem}
.plan .p{font:800 2.1rem Sora,sans-serif;margin:14px 0 4px;letter-spacing:-.03em}
.plan .p small{font:500 .9rem Manrope,sans-serif;opacity:.7;margin-right:4px}
.plan ul{list-style:none;padding:0;margin:18px 0 28px;display:grid;gap:10px;color:var(--muted);flex:1}
.plan.hot ul{color:#C9C9EE}
.plan li::before{content:"✓";color:var(--accent);font-weight:800;margin-right:10px}
.plan.hot li::before{color:#FFC93C}
.plan .btn{text-align:center}
/* secções */
section{padding:88px 0}
h2{font-size:clamp(1.9rem,3.6vw,2.8rem);font-weight:700}
.lead{color:var(--muted);max-width:52ch;margin:16px 0 0}
.svc{display:grid;grid-template-columns:1fr 1.5fr;gap:56px}
.svc .grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
.card{background:var(--surface);border:1.5px solid var(--line);border-radius:16px;padding:26px}
.card svg{width:26px;height:26px;margin-bottom:14px;color:var(--accent)}
.card h3{font-size:1.2rem;margin-bottom:8px}
.card p{margin:0;color:var(--muted);font-size:.98rem}
.work{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;margin-top:40px}
.work a{text-decoration:none;display:block}
.shot{border:1.5px solid var(--line);border-radius:14px;overflow:hidden;background:var(--surface);margin-bottom:16px}
.shot .bar{background:var(--surface);border-color:var(--line)}
.shot .bar b{background:var(--line)}
.shot div.body{aspect-ratio:4/3;display:flex;align-items:flex-end;padding:20px;font:800 1.5rem Sora,sans-serif;letter-spacing:-.02em}
.work a:nth-child(1) .body{background:#FFC93C;color:#12123A}
.work a:nth-child(2) .body{background:#12123A;color:#B9F5DF}
.work a:nth-child(3) .body{background:#5B3DF5;color:#fff}
.work h3{font-size:1.15rem}
.work .t{color:var(--muted);font-size:.95rem}
.alt-bg{background:var(--surface);border-block:1.5px solid var(--line)}
.steps{display:grid;grid-template-columns:repeat(4,1fr);gap:22px;margin-top:40px;counter-reset:s;list-style:none;padding:0}
.steps li{counter-increment:s;padding-top:20px;border-top:3px solid var(--accent)}
.steps li::before{content:"Passo " counter(s);display:block;font-weight:700;color:var(--accent);font-size:.9rem;margin-bottom:6px}
.steps b{display:block;font:700 1.2rem Sora,sans-serif;margin-bottom:6px}
.steps span{color:var(--muted);font-size:.97rem}
.contact{background:#12123A;color:#fff}
.cgrid{display:grid;grid-template-columns:1fr 1fr;gap:56px}
.contact .lead{color:#C9C9EE}
form{display:grid;gap:14px}
label{font-weight:700;font-size:.95rem;display:grid;gap:6px}
input[type=text],input[type=email],textarea{font:inherit;color:#12123A;background:#fff;border:1.5px solid #DEDCF5;border-radius:10px;padding:12px 14px;width:100%}
textarea{min-height:110px;resize:vertical}
#ok{color:#B9F5DF;font-weight:700;min-height:1.4em;margin:0}
footer{background:#12123A;color:#A6A8D0;padding:0 0 40px;font-size:.95rem}
footer .wrap{border-top:1.5px solid rgba(255,255,255,.14);padding-top:28px;display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px}
@media (max-width:900px){
.plans{grid-template-columns:1fr}
.hgrid,.svc,.cgrid{grid-template-columns:1fr;gap:36px}
.work{grid-template-columns:1fr}
.steps{grid-template-columns:1fr 1fr}
nav a:not(.btn){display:none}
.star{width:420px;height:420px;right:-120px;top:-60px}
}
@media (max-width:560px){.svc .grid,.steps{grid-template-columns:1fr}.proof{gap:20px}}
@media (prefers-reduced-motion:reduce){.gem{animation:none}.scene,.plan{transition:none}html{scroll-behavior:auto}.star{animation:none}.browser{transition:none}}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute" aria-hidden="true"><symbol id="mk" viewBox="0 0 32 32"><rect width="32" height="32" rx="9" fill="#5B3DF5"/><path d="M16 4l2.6 9.4L28 16l-9.4 2.6L16 28l-2.6-9.4L4 16l9.4-2.6z" fill="#FFC93C"/></symbol></svg>

<div class="hero">
<svg class="star" viewBox="0 0 32 32" aria-hidden="true"><path d="M16 1l3.2 11.8L31 16l-11.8 3.2L16 31l-3.2-11.8L1 16l11.8-3.2z" fill="#FFC93C"/></svg>
<div class="wrap">
<header>
<a class="logo" href="#topo" aria-label="WebNova Studio"><svg aria-hidden="true"><use href="#mk"/></svg>WebNova<span>Studio</span></a>
<nav><a href="#servicos">Serviços</a><a href="#planos">Planos</a><a href="#processo">Como trabalhamos</a><a class="btn" href="#contacto">Pedir orçamento</a></nav>
</header>
<main id="topo" class="hgrid">
<div>
<h1>Criamos sites que trazem clientes ao seu negócio.</h1>
<p>A WebNova Studio desenha e programa sites e lojas online para pequenas e médias empresas. Rápidos, bonitos e fáceis de atualizar.</p>
<div class="cta"><a class="btn" href="#contacto">Pedir orçamento</a><a class="btn ghost" href="#planos">Ver planos</a></div>
<div class="proof"><div><b>60+</b>sites publicados</div><div><b>4 semanas</b>prazo médio</div><div><b>1 dia</b>para responder</div></div>
</div>
<div class="demo">
<div class="stage" id="st"><div class="scene" id="sc"><div class="tile"></div><div class="browser" id="b"><div class="bar"><b></b><b></b><b></b></div><div class="page"><div class="h"></div><div class="l"></div><div class="l s"></div><div class="b"></div><div class="blocks"><span></span><span></span><span></span></div></div></div><div class="phone"><i></i><i></i><u></u><i></i><i></i></div><svg class="gem" viewBox="0 0 32 32" aria-hidden="true"><path d="M16 1l3.2 11.8L31 16l-11.8 3.2L16 31l-3.2-11.8L1 16l11.8-3.2z" fill="#FFC93C"/></svg></div></div>
<div class="ctrl"><label for="r" style="display:inline;font-weight:500">Veja o site em ecrãs diferentes</label><input id="r" type="range" min="30" max="100" value="100"><output id="o" for="r">100%</output></div>
</div>
</main>
</div>
</div>

<section id="servicos"><div class="wrap svc">
<div><h2>Tudo o que precisa para estar online</h2><p class="lead">Do design à publicação, tratamos de tudo. No fim, o site é seu e pode atualizá-lo sozinho.</p></div>
<div class="grid">
<div class="card"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="3" y="4" width="18" height="14" rx="2"/><path d="M8 21h8M12 18v3"/></svg><h3>Sites institucionais</h3><p>Páginas claras, rápidas e que se adaptam a telemóvel, tablet e computador.</p></div>
<div class="card"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M6 6h15l-2 9H8zM6 6L5 3H2"/><circle cx="9" cy="20" r="1.5"/><circle cx="18" cy="20" r="1.5"/></svg><h3>Lojas online</h3><p>Catálogo, pagamentos e envios configurados para vender desde o primeiro dia.</p></div>
<div class="card"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M12 3a9 9 0 100 18c1.5 0 2-1 1.5-2s-.5-2 1-2H17a4 4 0 004-4c0-5-4-10-9-10z"/><circle cx="8" cy="11" r="1"/><circle cx="12" cy="7.5" r="1"/><circle cx="16" cy="11" r="1"/></svg><h3>Identidade visual</h3><p>Logótipo, cores e tipos de letra para o seu negócio ter uma imagem coerente.</p></div>
<div class="card"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="11" cy="11" r="7"/><path d="M21 21l-5-5"/></svg><h3>Google e manutenção</h3><p>Otimização para pesquisas, cópias de segurança e atualizações todos os meses.</p></div>
</div>
</div></section>

<section id="planos" class="alt-bg"><div class="wrap">
<h2>Escolha o ponto de partida</h2>
<p class="lead">Cada projeto tem um orçamento fechado, sem surpresas. Os planos servem de base e ajustamos ao que precisa.</p>
<div class="plans">
<div class="plan"><h3>Essencial</h3><div class="p"><small>desde</small>490 €</div><ul><li>Site de uma página</li><li>Design adaptado ao telemóvel</li><li>Formulário de contacto</li><li>Publicação com domínio</li></ul><a class="btn alt" href="#contacto">Pedir orçamento</a></div>
<div class="plan hot"><h3>Profissional</h3><div class="p"><small>desde</small>1 190 €</div><ul><li>Até 6 páginas</li><li>Animações e elementos 3D</li><li>Otimização para o Google</li><li>Blog ou notícias</li></ul><a class="btn" href="#contacto">Pedir orçamento</a></div>
<div class="plan"><h3>Loja online</h3><div class="p"><small>desde</small>1 990 €</div><ul><li>Catálogo de produtos</li><li>Pagamentos e envios</li><li>Gestão de encomendas</li><li>Formação para a sua equipa</li></ul><a class="btn alt" href="#contacto">Pedir orçamento</a></div>
</div>
</div></section>

<section id="processo"><div class="wrap">
<h2>Do primeiro contacto ao site no ar</h2>
<ol class="steps">
<li><b>Conversa</b><span>Percebemos o seu negócio, os seus clientes e o que o site deve fazer.</span></li>
<li><b>Proposta</b><span>Recebe um orçamento com preço e prazo fechados.</span></li>
<li><b>Design e código</b><span>Mostramos o desenho e construímos o site. Acompanha cada etapa.</span></li>
<li><b>Publicação</b><span>Pomos o site no ar e ensinamos a atualizá-lo.</span></li>
</ol>
</div></section>

<section id="contacto" class="contact"><div class="wrap cgrid">
<div><h2>Vamos falar do seu projeto?</h2><p class="lead">Conte-nos o que precisa. Respondemos em 1 dia útil com uma ideia de preço e prazo.</p></div>
<form id="f">
<label>Nome<input type="text" name="n" required autocomplete="name"></label>
<label>Email<input type="email" name="e" required autocomplete="email"></label>
<label>O que precisa?<textarea name="m"></textarea></label>
<button class="btn" type="submit">Enviar pedido</button>
<p id="ok" role="status"></p>
</form>
</div></section>

<footer><div class="wrap"><span>© 2026 WebNova Studio</span><span>ola@webnovastudio.example</span></div></footer>
<script>
var r=document.getElementById('r'),b=document.getElementById('b'),o=document.getElementById('o');
r.addEventListener('input',function(){b.style.setProperty('--w',r.value+'%');o.textContent=r.value+'%'});
var mm=matchMedia('(prefers-reduced-motion:reduce)').matches,sc=document.getElementById('sc'),st=document.getElementById('st');
if(!mm){st.addEventListener('pointermove',function(e){var k=st.getBoundingClientRect(),x=(e.clientX-k.left)/k.width-.5,y=(e.clientY-k.top)/k.height-.5;sc.style.setProperty('--ry',(x*30)+'deg');sc.style.setProperty('--rx',(10-y*24)+'deg')});
st.addEventListener('pointerleave',function(){sc.style.removeProperty('--ry');sc.style.removeProperty('--rx')});
document.querySelectorAll('.plan').forEach(function(p){p.addEventListener('pointermove',function(e){var k=p.getBoundingClientRect(),x=(e.clientX-k.left)/k.width-.5,y=(e.clientY-k.top)/k.height-.5;p.style.transform='rotateX('+(-y*10)+'deg) rotateY('+(x*10)+'deg)'});p.addEventListener('pointerleave',function(){p.style.transform=''})})}
document.getElementById('f').addEventListener('submit',function(e){e.preventDefault();document.getElementById('ok').textContent='Pedido enviado. Obrigado, falamos em breve.';this.reset()});
</script>
</body>
</html>
