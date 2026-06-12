<div id="inicio">
  <div class="hero">
    <h1>🌳 Campo e Cidade 🏙️</h1>
    <p>Explore as diferenças, vantagens e curiosidades entre o campo e a cidade.</p>
    <button id="entrarBtn">ENTRAR</button>
  </div>
</div>

<div id="site">
  <div id="progresso"></div>

  <header>
    <h1>Campo x Cidade</h1>
    <nav>
      <a href="#sec1">Introdução</a>
      <a href="#sec2">Campo</a>
      <a href="#sec3">Cidade</a>
      <a href="#sec4">Comparação</a>
    </nav>
  </header>

  <section class="reveal" id="sec1">
    <h2>🌎 Introdução</h2>
    <p>
      O campo e a cidade são ambientes muito diferentes. Cada um possui
      características únicas que influenciam a forma como as pessoas vivem,
      trabalham e se relacionam.
    </p>
    <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=1200" alt="">
  </section>

  <section class="reveal campo" id="sec2">
    <h2>🌳 Vida no Campo</h2>

    <div class="card">
      <h3>Natureza</h3>
      <p>
        O campo possui grande contato com a natureza, rios, montanhas,
        florestas e áreas agrícolas.
      </p>
    </div>

    <div class="card">
      <h3>Tranquilidade</h3>
      <p>
        Menos trânsito, menos poluição sonora e um ritmo de vida mais calmo.
      </p>
    </div>

    <div class="card">
      <h3>Produção de Alimentos</h3>
      <p>
        Grande parte dos alimentos consumidos nas cidades é produzida no campo.
      </p>
    </div>

    <img src="https://images.unsplash.com/photo-1500382017468-9049fed747ef?w=1200" alt="">
  </section>

  <section class="reveal cidade" id="sec3">
    <h2>🏙️ Vida na Cidade</h2>

    <div class="cconst entrarBtn = document.getElementById("entrarBtn");
const inicio = document.getElementById("inicio");
const site = document.getElementById("site");

entrarBtn.addEventListener("click", () => {
  inicio.style.display = "none";
  site.style.display = "block";

  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
});

const reveals = document.querySelectorAll(".reveal");

function revelarElementos() {
  reveals.forEach(elemento => {
    const topo = elemento.getBoundingClientRect().top;
    const alturaTela = window.innerHeight * 0.8;

    if (topo < alturaTela) {
      elemento.classList.add("active");
    }
  });
}

window.addEventListener("scroll", revelarElementos);
revelarElementos();

/* Barra de progresso */

window.addEventListener("scroll", () => {
  const scrollTop = document.documentElement.scrollTop;
  const altura =
    document.documentElement.scrollHeight -
    document.documentElement.clientHeight;

  const porcentagem = (scrollTop / altura) * 100;

  document.getElementById("progresso").style.width =
    porcentagem + "%";
});ard">
      <h3>Tecnologia</h3>
      <p>
        As cidades concentram empresas, universidades e centros tecnológicos.
      </p>
    </div>

    <div class="card">
      <h3>Oportunidades</h3>
      <p>
        Existem mais empregos, serviços e opções de estudo.
      </p>
    </div>

    <div class="card">
      <h3>Infraestrutura</h3>
      <p>
        Hospitais, escolas, transporte público e comércio são mais acessíveis.
      </p>
    </div>

    <img src="https://images.unsplash.com/photo-1477959858617-67f85cf4f1df?w=1200" alt="">
  </section>

  <section class="reveal comparacao" id="sec4">
    <h2>⚖️ Comparação</h2>

    <div class="comparador">
      <div class="lado campo-box">
        <h3>Campo</h3>
        <ul>
          <li>✔ Mais natureza</li>
          <li>✔ Menos poluição</li>
          <li>✔ Vida tranquila</li>
          <li>✔ Produção agrícola</li>
        </ul>
      </div>

      <div class="lado cidade-box">
        <h3>Cidade</h3>
        <ul>
          <li>✔ Mais empregos</li>
          <li>✔ Mais tecnologia</li>
          <li>✔ Mais serviços</li>
          <li>✔ Mais lazer urbano</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="reveal curiosidades">
    <h2>📚 Curiosidades</h2>

    <div class="curiosidade">
      <h3>🌽 Agricultura</h3>
      <p>
        O campo é responsável pela produção da maior parte dos alimentos que
        chegam às cidades.
      </p>
    </div>

    <div class="curiosidade">
      <h3>🚇 Transporte</h3>
      <p>
        As cidades possuem sistemas de transporte mais desenvolvidos.
      </p>
    </div>

    <div class="curiosidade">
      <h3>🌱 Sustentabilidade</h3>
      <p>
        Campo e cidade dependem um do outro para manter o equilíbrio social e econômico.
      </p>
    </div>
  </section>

  <footer>
    <h3>Campo x Cidade</h3>
    <p>Projeto Educativo Interativo</p>
  </footer>
</div>
*{
  padding:0;
  box-sizing:border-box;
  font-family:Arial, sans-serif;
}

html{
  scroll-behavior:smooth;
}

body{
  background:#f5f5f5;
  overflow-x:hidden;
}

/* Tela inicial */

#inicio{
  height:100vh;
  background:linear-gradient(135deg,#2e7d32,#1976d2);
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  color:white;
}

.hero h1{
  font-size:5rem;
  margin-bottom:20px;
}

.hero p{
  font-size:1.3rem;
  margin-bottom:30px;
}

#entrarBtn{
  padding:15px 40px;
  border:none;
  border-radius:50px;
  font-size:1.2rem;
  cursor:pointer;
  background:white;
  color:#333;
  transition:.3s;
}

#entrarBtn:hover{
  transform:scale(1.1);
}

/* Site */

#site{
  display:none;
}

#progresso{
  position:fixed;
  top:0;
  left:0;
  width:0%;
  height:8px;
  background:#00e676;
  z-index:9999;
}

header{
  background:#222;
  color:white;
  padding:25px;
  text-align:center;
  position:sticky;
  top:0;
  z-index:1000;
}

nav{
  margin-top:15px;
}

nav a{
  color:white;
  text-decoration:none;
  margin:0 15px;
}

section{
  min-height:100vh;
  padding:80px 10%;
}

section h2{
  font-size:3rem;
  margin-bottom:20px;
}

section p{
  font-size:1.2rem;
  line-height:1.8;
}

img{
  width:100%;
  margin-top:30px;
  border-radius:15px;
}

.campo{
  background:#e8f5e9;
}

.cidade{
  background:#e3f2fd;
}

.comparacao{
  background:#fff8e1;
}

.card{
  background:white;
  padding:20px;
  margin:20px 0;
  border-radius:15px;
  box-shadow:0 5px 15px rgba(0,0,0,.1);
}

.comparador{
  display:flex;
  gap:30px;
  flex-wrap:wrap;
}

.lado{
  flex:1;
  min-width:280px;
  background:white;
  padding:30px;
  border-radius:15px;
}

.campo-box{
  border-left:8px solid green;
}

.cidade-box{
  border-left:8px solid blue;
}

.lado ul{
  margin-top:15px;
}

.lado li{
  margin:10px 0;
}

.curiosidade{
  background:white;
  margin:25px 0;
  padding:25px;
  border-radius:15px;
}

footer{
  background:#111;
  color:white;
  text-align:center;
  padding:50px;
}

/* Animações */

.reveal{
  opacity:0;
  transform:translateY(80px);
  transition:1s;
}

.reveal.active{
  opacity:1;
  transform:translateY(0);
}
  margin:0;
  const entrarBtn = document.getElementById("entrarBtn");
const inicio = document.getElementById("inicio");
const site = document.getElementById("site");

entrarBtn.addEventListener("click", () => {
  inicio.style.display = "none";
  site.style.display = "block";

  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
});

const reveals = document.querySelectorAll(".reveal");

function revelarElementos() {
  reveals.forEach(elemento => {
    const topo = elemento.getBoundingClientRect().top;
    const alturaTela = window.innerHeight * 0.8;

    if (topo < alturaTela) {
      elemento.classList.add("active");
    }
  });
}

window.addEventListener("scroll", revelarElementos);
revelarElementos();

/* Barra de progresso */

window.addEventListener("scroll", () => {
  const scrollTop = document.documentElement.scrollTop;
  const altura =
    document.documentElement.scrollHeight -
    document.documentElement.clientHeight;

  const porcentagem = (scrollTop / altura) * 100;

  document.getElementById("progresso").style.width =
    porcentagem + "%";
});
