<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Dinamo Live</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:#101116;color:white;font-family:Arial,sans-serif}
header{background:#c90026;padding:25px 18px;text-align:center}
header h1{margin:0;font-size:30px}
header p{margin:7px 0 0}
nav{display:flex;background:#202127;position:sticky;top:0}
nav button{flex:1;padding:16px 5px;background:none;color:white;border:0;font-size:15px}
nav button.active{background:#c90026}
main{padding:16px}
h2{font-size:21px}
.card{background:#22242c;border-radius:12px;padding:16px;margin:12px 0}
.match{text-align:center}
.teams{display:flex;justify-content:space-around;align-items:center;font-size:17px;font-weight:bold}
.score{font-size:27px;color:#ff344f}
.small{color:#aaa;font-size:13px}
button.action{background:#c90026;color:white;border:0;padding:11px 16px;border-radius:8px;margin-top:12px}
table{width:100%;border-collapse:collapse;font-size:13px}
td,th{padding:11px 5px;text-align:center;border-bottom:1px solid #383943}
th{color:#ff536b}
.hidden{display:none}
#details{line-height:1.8}
footer{text-align:center;color:#999;padding:25px}
</style>
</head>
<body>
<header>
<h1>🔴⚪ DINAMO LIVE</h1>
<p>Totul despre FC Dinamo București</p>
</header>

<nav>
<button class="active" onclick="show('matches',this)">Meciuri</button>
<button onclick="show('table',this)">Clasament</button>
<button onclick="show('details',this)">Detalii</button>
</nav>

<main>
<section id="matches">
<h2>⚽ Meciurile lui Dinamo</h2>
<div class="card match">
<p class="small">Exemplu demonstrativ – înlocuiește cu datele reale</p>
<div class="teams">
<span>DINAMO</span>
<span class="score">0 - 0</span>
<span>ADVERSAR</span>
</div>
<p class="small">Data și ora meciului</p>
<button class="action" onclick="showDetails()">Vezi statistici</button>
</div>
<p class="small">Rezultatele live vor necesita conectarea unei surse de date sportive.</p>
</section>

<section id="table" class="hidden">
<h2>🏆 Clasamentul SuperLigii</h2>
<p class="small">Tabel demonstrativ – va fi conectat la clasamentul actualizat.</p>
<div class="card">
<table>
<thead><tr><th>Loc</th><th>Echipă</th><th>M</th><th>V</th><th>E</th><th>Î</th><th>Pts</th></tr></thead>
<tbody id="standings">
<tr><td>-</td><td>🔴⚪ Dinamo</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
<tr><td>-</td><td>Adversar</td><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>
</tbody>
</table>
</div>
</section>

<section id="details" class="hidden">
<h2>📊 Detalii meci</h2>
<div class="card">
<h3>Dinamo - Adversar</h3>
<p>Scor: 0 - 0</p>
<p>⚽ Marcatori: date indisponibile</p>
<p>🟨 Cartonașe: date indisponibile</p>
<p>📈 Posesie: date indisponibile</p>
<p>🥅 Șuturi: date indisponibile</p>
<h3>Echipe de start</h3>
<p>Loturile vor apărea după conectarea sursei de date.</p>
</div>
</section>
</main>
<footer>Hai Dinamo București! ❤️🤍 DDB</footer>

<script>
function show(id,btn){
document.querySelectorAll('main section').forEach(s=>s.classList.add('hidden'));
document.getElementById(id).classList.remove('hidden');
document.querySelectorAll('nav button').forEach(b=>b.classList.remove('active'));
if(btn)btn.classList.add('active');
}
function showDetails(){
show('details',document.querySelectorAll('nav button')[2]);
}
</script>
</body>
</html>
