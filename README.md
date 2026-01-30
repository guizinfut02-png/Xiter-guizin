<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>@GUIZIN_XITER • AUXÍLIO FREE FIRE</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;500;700&display=swap');

* {
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

body {
  margin: 0;
  background: radial-gradient(circle at top, #140000, #000);
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
}

.menu {
  width: 100%;
  max-width: 410px;
  background: rgba(20, 20, 20, 0.92);
  border-radius: 28px;
  padding: 24px;
  box-shadow: 
    0 0 30px rgba(255, 0, 0, 0.35),
    inset 0 0 10px rgba(255,255,255,0.05);
}

.title {
  text-align: center;
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 6px;
  letter-spacing: 0.5px;
}

.legend {
  text-align: center;
  font-size: 13px;
  margin-bottom: 14px;
}

.legend .white { color: #ffffff; }
.legend .red { color: #ff4d4d; font-weight: bold; }

.warning {
  text-align: center;
  font-size: 14px;
  font-weight: bold;
  margin-bottom: 14px;
  color: #ff4d4d;
}

.options-group {
  margin-top: 10px;
}

.option {
  background: linear-gradient(145deg, #1b1b1b, #141414);
  border-radius: 18px;
  padding: 14px;
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  gap: 12px;
  box-shadow: 
    inset 0 0 0 1px rgba(255,255,255,0.06),
    0 0 10px rgba(255,0,0,0.12);
  cursor: pointer;
  transition: 0.3s ease;
}

.option:hover {
  transform: scale(1.02);
}

.option.clicked {
  background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
  box-shadow:
    0 0 18px rgba(255,0,0,0.6),
    0 0 28px rgba(255,0,0,0.4);
}

.icon {
  font-size: 22px;
}

.text {
  font-size: 15px;
  font-weight: 500;
}

.inject-btn {
  display: block;
  width: 100%;
  text-align: center;
  margin-top: 16px;
  padding: 13px;
  border: none;
  border-radius: 20px;
  background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
  color: #fff;
  font-weight: bold;
  font-size: 15px;
  cursor: pointer;
  box-shadow:
    0 0 20px rgba(255,0,0,0.6);
  transition: 0.3s ease;
}

.inject-btn:hover {
  transform: scale(1.04);
}

.loading-box {
  margin-top: 16px;
  background: #0f0f0f;
  border-radius: 16px;
  padding: 12px;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,0.06);
  display: none;
}

.loading-title {
  font-size: 13px;
  font-weight: bold;
  margin-bottom: 6px;
  color: #ff4d4d;
  text-align: center;
}

.loading-text {
  font-size: 12px;
  text-align: center;
  min-height: 18px;
}

.progress-container {
  width: 100%;
  height: 10px;
  background: #2a2a2a;
  border-radius: 10px;
  overflow: hidden;
  margin-top: 10px;
}

.progress-bar {
  height: 100%;
  width: 0%;
  background: linear-gradient(90deg, #ff4d4d, #ff1a1a);
  transition: width 0.25s ease;
}

.game-choice {
  display: none;
  margin-top: 16px;
}

.game-btn {
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  border: none;
  border-radius: 18px;
  background: #1f1f1f;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  transition: 0.3s;
}

.game-btn:hover {
  background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
}

.footer {
  text-align: center;
  font-size: 12px;
  color: #aaa;
  margin-top: 18px;
}
</style>
</head>

<body>

<div class="menu">

  <div class="title">@GUIZIN_XITER • AUXÍLIO FREE FIRE</div>

  <div class="legend">
    <span class="white">leve auxílio para móbiles</span>
    •
    <span class="red">não é XIT</span>
  </div>

  <div class="warning" id="status">🚫 VENDA PROIBIDA 🚫</div>

  <div class="options-group">
    <div class="option"><div class="icon">🎯</div><div class="text">Ajustar mira</div></div>
    <div class="option"><div class="icon">💥</div><div class="text">Aumentar desempenho</div></div>
    <div class="option"><div class="icon">👾</div><div class="text">Sistema avançado de sensibilidade</div></div>
    <div class="option"><div class="icon">🧠</div><div class="text">Redução de recoil</div></div>
    <div class="option"><div class="icon">⚡</div><div class="text">Otimização de FPS</div></div>
    <div class="option"><div class="icon">🔧</div><div class="text">Correção de travamentos</div></div>
    <div class="option"><div class="icon">📡</div><div class="text">Estabilidade de conexão</div></div>
    <div class="option"><div class="icon">🛡️</div><div class="text">Proteção anti-lag</div></div>
    <div class="option"><div class="icon">🎮</div><div class="text">Melhoria de resposta de toque</div></div>
  </div>

  <button class="inject-btn" id="injectBtn">INJETAR</button>

  <div class="loading-box" id="loadingBox">
    <div class="loading-title">STATUS DA INJEÇÃO</div>
    <div class="loading-text" id="loadingText">Aguardando...</div>

    <div class="progress-container">
      <div class="progress-bar" id="progressBar"></div>
    </div>
  </div>

  <div class="game-choice" id="gameChoice">
    <div class="warning">Selecione o jogo:</div>
    <button class="game-btn" onclick="openGame('ff')">Abrir Free Fire</button>
    <button class="game-btn" onclick="openGame('ffmax')">Abrir Free Fire MAX</button>
  </div>

  <div class="footer">By:GuizinXiter</div>

</div>

<script>
  const options = document.querySelectorAll('.option');
  const injectBtn = document.getElementById('injectBtn');
  const status = document.getElementById('status');
  const loadingBox = document.getElementById('loadingBox');
  const loadingText = document.getElementById('loadingText');
  const progressBar = document.getElementById('progressBar');
  const gameChoice = document.getElementById('gameChoice');

  options.forEach(option => {
    option.addEventListener('click', () => {
      option.classList.toggle('clicked');
    });
  });

  const steps = [
    "Inicializando núcleo...",
    "Carregando módulos gráficos...",
    "Aplicando ajustes de mira...",
    "Otimizando desempenho...",
    "Ajustando sensibilidade...",
    "Aplicando anti-lag...",
    "Finalizando injeção...",
    "AUXÍLIO INJETADO ✔️"
  ];

  injectBtn.addEventListener('click', () => {
    const selected = document.querySelectorAll('.option.clicked').length;
    if (selected === 0) {
      alert('Selecione pelo menos uma opção antes de injetar!');
      return;
    }

    injectBtn.disabled = true;
    loadingBox.style.display = 'block';
    progressBar.style.width = '0%';
    gameChoice.style.display = 'none';

    let step = 0;
    let progress = 0;

    function nextStep() {
      if (step < steps.length) {
        loadingText.textContent = steps[step];
        progress += 100 / steps.length;
        progressBar.style.width = progress + "%";
        step++;
        setTimeout(nextStep, 700);
      } else {
        setTimeout(() => {
          status.textContent = "🚀 Pronto para iniciar!";
          gameChoice.style.display = 'block';
        }, 600);
      }
    }

    nextStep();
  });

  function openGame(type) {
    if (type === 'ff') {
      alert('🚀 Abrindo Free Fire...');
    } else if (type === 'ffmax') {
      alert('🚀 Abrindo Free Fire MAX...');
    }
  }
</script>

</body>
</html>
