<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ColorBook Store | Cadernos de Colorir</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
scroll-behavior:smooth;
}

body{
background:#ebebeb;
overflow-x:hidden;
color:#333;
}

/* TOPO */

.topo{
background:#fff159;
padding:10px 5%;
display:flex;
justify-content:space-between;
align-items:center;
font-size:14px;
flex-wrap:wrap;
}

header{
background:#fff159;
padding:18px 5%;
display:flex;
justify-content:space-between;
align-items:center;
gap:20px;
flex-wrap:wrap;
position:sticky;
top:0;
z-index:999;
box-shadow:0 2px 10px rgba(0,0,0,0.08);
}

.logo{
font-size:34px;
font-weight:700;
color:#333;
}

.logo span{
color:#ff7a00;
}

.search-area{
flex:1;
display:flex;
flex-direction:column;
gap:8px;
min-width:320px;
position:relative;
}

.search{
display:flex;
}

.search input{
width:100%;
padding:16px;
border:none;
border-radius:8px 0 0 8px;
font-size:15px;
outline:none;
}

.search button{
padding:16px 25px;
border:none;
background:#3483fa;
color:white;
font-weight:600;
border-radius:0 8px 8px 0;
cursor:pointer;
}

.sugestoes{
background:white;
border-radius:10px;
padding:10px;
box-shadow:0 5px 15px rgba(0,0,0,0.08);
display:flex;
flex-wrap:wrap;
gap:10px;
}

.sugestoes span{
background:#f5f5f5;
padding:8px 12px;
border-radius:30px;
font-size:13px;
cursor:pointer;
transition:0.3s;
}

.sugestoes span:hover{
background:#3483fa;
color:white;
}

.menu{
display:flex;
gap:20px;
flex-wrap:wrap;
}

.menu a{
text-decoration:none;
font-weight:600;
color:#333;
transition:0.3s;
}

.menu a:hover{
color:#3483fa;
}

.banner{
height:90vh;
background:
linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,0.4)),
url('https://images.unsplash.com/photo-1503454537195-1dcabb73ffb9?q=80&w=1400&auto=format&fit=crop');
background-size:cover;
background-position:center;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
color:white;
}

.banner h1{
font-size:65px;
margin-bottom:20px;
animation:fade 1s ease;
}

.banner p{
font-size:24px;
margin-bottom:30px;
animation:fade 1.4s ease;
}

@keyframes fade{
from{
opacity:0;
transform:translateY(40px);
}
to{
opacity:1;
transform:translateY(0);
}
}

.btn{
background:#3483fa;
padding:16px 35px;
border:none;
border-radius:10px;
color:white;
font-weight:600;
cursor:pointer;
text-decoration:none;
display:inline-block;
transition:0.3s;
}

.btn:hover{
transform:scale(1.05);
background:#2968c8;
}

section{
padding:70px 5%;
}

.titulo{
font-size:38px;
margin-bottom:40px;
color:#333;
text-align:center;
}

.produtos{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
gap:25px;
}

.card{
background:white;
border-radius:15px;
overflow:hidden;
box-shadow:0 2px 10px rgba(0,0,0,0.08);
transition:0.3s;
}

.card:hover{
transform:translateY(-8px);
}

.card img{
width:100%;
height:260px;
object-fit:cover;
}

.card-content{
padding:22px;
}

.avaliacao{
color:#ffb400;
margin:10px 0;
font-size:15px;
}

.card-content h3{
margin-bottom:10px;
font-size:24px;
}

.card-content p{
line-height:1.7;
font-size:15px;
color:#555;
}

.preco{
font-size:32px;
font-weight:700;
color:#00a650;
margin:15px 0;
}

.pix{
color:#00a650;
font-size:14px;
font-weight:600;
margin-bottom:10px;
}

.entrega{
font-size:14px;
color:#3483fa;
font-weight:600;
margin-bottom:20px;
}

.pagamento{
background:white;
padding:40px;
border-radius:20px;
max-width:900px;
margin:auto;
box-shadow:0 2px 10px rgba(0,0,0,0.08);
}

input,
select{
width:100%;
padding:16px;
border-radius:10px;
border:1px solid #ddd;
margin-bottom:15px;
font-size:15px;
}

.grid2{
display:grid;
grid-template-columns:1fr 1fr;
gap:15px;
}

.seguro{
background:#e3f7ea;
padding:15px;
border-radius:10px;
margin-bottom:20px;
color:#00a650;
font-weight:600;
}

.galeria{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:20px;
}

.galeria img{
width:100%;
height:320px;
object-fit:cover;
border-radius:15px;
transition:0.3s;
}

.galeria img:hover{
transform:scale(1.03);
}

.login-box{
background:white;
padding:40px;
border-radius:20px;
max-width:500px;
margin:auto;
box-shadow:0 2px 10px rgba(0,0,0,0.08);
}

footer{
background:#fff159;
padding:50px 5%;
text-align:center;
margin-top:50px;
}

.whatsapp{
position:fixed;
right:20px;
bottom:20px;
background:#25D366;
padding:18px 22px;
border-radius:50px;
color:white;
text-decoration:none;
font-weight:700;
box-shadow:0 5px 20px rgba(0,0,0,0.3);
z-index:999;
animation:pulse 1.5s infinite;
}

.carrinho{
position:fixed;
left:20px;
bottom:20px;
background:#3483fa;
color:white;
padding:15px 20px;
border-radius:50px;
font-weight:700;
z-index:999;
box-shadow:0 5px 20px rgba(0,0,0,0.2);
}

@keyframes pulse{
0%{
transform:scale(1);
}
50%{
transform:scale(1.06);
}
100%{
transform:scale(1);
}
}

@media(max-width:900px){

.banner h1{
font-size:42px;
}

.grid2{
grid-template-columns:1fr;
}

header{
flex-direction:column;
align-items:stretch;
}

}

</style>
</head>

<body>

<div class="topo">

<div>
📞 Atendimento: (92) 98646-0651
</div>

<div>
⚡ Produto liberado automaticamente após pagamento
</div>

</div>

<header>

<div class="logo">
Color<span>Book</span>
</div>

<div class="search-area">

<div class="search">

<input type="text" id="pesquisa" placeholder="Pesquisar desenhos, kits infantis, colorir kids...">

<button onclick="pesquisar()">
Buscar
</button>

</div>

<div class="sugestoes">

<span onclick="buscarSugestao('Animais')">Animais</span>

<span onclick="buscarSugestao('Princesas')">Princesas</span>

<span onclick="buscarSugestao('Dinossauros')">Dinossauros</span>

<span onclick="buscarSugestao('Escolinha')">Escolinha</span>

<span onclick="buscarSugestao('Educativo')">Educativo</span>

<span onclick="buscarSugestao('Premium')">Premium</span>

</div>

</div>

<div class="menu">

<a href="#">Início</a>
<a href="#produtos">Produtos</a>
<a href="#pagamento">Pagamento</a>
<a href="#login">Login</a>
<a href="#cadastro">Cadastro</a>

</div>

</header>

<section class="banner">

<div>

<h1>
Cadernos de Colorir Educativos
</h1>

<p>
Aprendizado, diversão e criatividade para crianças.
</p>

<a href="#produtos" class="btn">
Comprar Agora
</a>

</div>

</section>

<section id="produtos">

<h2 class="titulo">
Produtos Populares
</h2>

<div class="produtos">

<div class="card">

<img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?q=80&w=1200&auto=format&fit=crop">

<div class="card-content">

<h3>
Kit Colorir Kids
</h3>

<div class="avaliacao">
⭐⭐⭐⭐⭐ 4.9 | +2.300 vendas
</div>

<p>
Pacote infantil com desenhos educativos, animais, alfabetização e atividades divertidas para imprimir.
</p>

<div class="preco">
R$ 19,90
</div>

<div class="pix">
💚 10% OFF no Pix
</div>

<div class="entrega">
⚡ Produto digital liberado imediatamente
</div>

<a href="#pagamento" class="btn">
Comprar Agora
</a>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1513258496099-48168024aec0?q=80&w=1200&auto=format&fit=crop">

<div class="card-content">

<h3>
Mundo Kids Premium
</h3>

<div class="avaliacao">
⭐⭐⭐⭐⭐ 5.0 | Mais vendido
</div>

<p>
Mais de 200 páginas premium com desenhos educativos, coordenação motora e criatividade infantil.
</p>

<div class="preco">
R$ 39,90
</div>

<div class="pix">
💚 Parcelamento disponível
</div>

<div class="entrega">
⚡ Download automático após pagamento
</div>

<a href="#pagamento" class="btn">
Comprar Agora
</a>

</div>

</div>

<div class="card">

<img src="https://images.unsplash.com/photo-1516627145497-ae6968895b74?q=80&w=1200&auto=format&fit=crop">

<div class="card-content">

<h3>
Mega Kit Educativo
</h3>

<div class="avaliacao">
⭐⭐⭐⭐⭐ 4.8 | Oferta especial
</div>

<p>
Atividades educativas, desenhos criativos e jogos infantis para aprender brincando.
</p>

<div class="preco">
R$ 24,90
</div>

<div class="pix">
💚 Pagamento seguro
</div>

<div class="entrega">
⚡ Liberação instantânea
</div>

<a href="#pagamento" class="btn">
Comprar Agora
</a>

</div>

</div>

</div>

</section>

<section id="pagamento">

<h2 class="titulo">
Finalizar Compra
</h2>

<div class="pagamento">

<div class="seguro">
🔒 Pagamento Seguro e Criptografado
</div>

<input type="text" id="nome" placeholder="Nome completo">

<input type="email" id="email" placeholder="Seu e-mail">

<input type="text" id="zap" placeholder="WhatsApp">

<select>

<option>
Pix Instantâneo
</option>

<option>
Cartão de Crédito
</option>

<option>
Cartão de Débito
</option>

<option>
Parcelamento
</option>

<option>
Boleto Bancário
</option>

</select>

<input type="text" placeholder="Número do cartão">

<div class="grid2">

<input type="text" placeholder="Validade">

<input type="text" placeholder="CVV">

</div>

<button class="btn" style="width:100%;" onclick="finalizarCompra()">
Pagar Agora
</button>

</div>

</section>

<section>

<h2 class="titulo">
Crianças Colorindo
</h2>

<div class="galeria">

<img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?q=80&w=1200&auto=format&fit=crop">

<img src="https://images.unsplash.com/photo-1513258496099-48168024aec0?q=80&w=1200&auto=format&fit=crop">

<img src="https://images.unsplash.com/photo-1516627145497-ae6968895b74?q=80&w=1200&auto=format&fit=crop">

</div>

</section>

<section id="login">

<h2 class="titulo">
Entrar na Conta
</h2>

<div class="login-box">

<input type="email" placeholder="Seu e-mail">

<input type="password" placeholder="Sua senha">

<button class="btn" style="width:100%;" onclick="login()">
Entrar
</button>

</div>

</section>

<section id="cadastro">

<h2 class="titulo">
Criar Conta
</h2>

<div class="login-box">

<input type="text" placeholder="Seu nome">

<input type="email" placeholder="Seu e-mail">

<input type="text" placeholder="WhatsApp">

<input type="password" placeholder="Crie sua senha">

<button class="btn" style="width:100%;" onclick="cadastro()">
Criar Conta
</button>

</div>

</section>

<footer>

<h2>
ColorBook Store
</h2>

<br>

<p>
© 2026 - Todos os direitos reservados.
</p>

<br>

<p>
📞 WhatsApp: (92) 98646-0651
</p>

</footer>

<div class="carrinho">
🛒 Carrinho: 3 Produtos
</div>

<a class="whatsapp"
href="https://wa.me/5592986460651"
target="_blank">

💬 WhatsApp

</a>

<script>

function finalizarCompra(){

let nome = document.getElementById("nome").value;

if(nome == ""){

alert("Preencha seu nome.");

return;

}

alert("Pagamento aprovado! Produto liberado com sucesso.");

window.open("https://wa.me/5592986460651","_blank");

}

function login(){

alert("Login realizado com sucesso!");

}

function cadastro(){

alert("Conta criada com sucesso!");

}

function pesquisar(){

let pesquisa = document.getElementById("pesquisa").value;

if(pesquisa == ""){

alert("Digite algo para pesquisar.");

}else{

alert("Resultados encontrados para: " + pesquisa);

}

}

function buscarSugestao(texto){

document.getElementById("pesquisa").value = texto;

}

</script>

</body>
</html>
