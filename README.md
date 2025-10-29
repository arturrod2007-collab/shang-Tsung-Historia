<!doctype html> Ermac
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Ermac — Ficha do Agente de Shao Kahn</title>
  <style>
    :root{--bg:#0b0f14;--card:#0f1720;--accent:#a22;--muted:#97a0ab;--glass:rgba(255,255,255,0.04)}
    *{box-sizing:border-box;font-family:Inter,Segoe UI,Roboto,Arial, sans-serif}
    body{margin:0;background:linear-gradient(180deg,#05060a 0%, #0b0f14 60%);color:#e6eef6;min-height:100vh}
    .container{max-width:980px;margin:36px auto;padding:24px}
    header{display:flex;align-items:center;gap:16px}
    .logo{width:68px;height:68px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#4b0f0f);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:22px;box-shadow:0 6px 24px rgba(0,0,0,0.6)}
    h1{margin:0;font-size:24px}
    p.lead{color:var(--muted);margin-top:6px}

    main{display:grid;grid-template-columns:1fr 340px;gap:20px;margin-top:22px}

    .card{background:var(--card);border-radius:14px;padding:18px;box-shadow:0 8px 30px rgba(2,6,12,0.6);border:1px solid rgba(255,255,255,0.02)}

    .lore h2{margin-top:0}
    .lore p{line-height:1.5;color:#dfe9f6}

    .stats{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:12px}
    .stat{background:var(--glass);padding:12px;border-radius:10px}
    .stat strong{display:block;font-size:18px}
    .stat small{color:var(--muted)}

    .power-bar{height:18px;background:rgba(255,255,255,0.06);border-radius:9px;overflow:hidden;margin-top:10px}
    .power-level{height:100%;width:80%;background:linear-gradient(90deg,var(--accent),#f04f4f);transition:width .5s ease}

    .right .portrait{height:220px;border-radius:10px;background:linear-gradient(180deg,#1a1f26,#0f1114);display:flex;align-items:center;justify-content:center;font-size:18px;color:var(--muted);border:1px solid rgba(255,255,255,0.02)}
    .right .info{margin-top:14px}
    .tag{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(255,255,255,0.03);font-size:13px}

    .souls{margin-top:12px;display:flex;align-items:center;gap:8px}
    .souls button{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px 10px;border-radius:8px;color:inherit;cursor:pointer}

    footer{margin-top:26px;text-align:center;color:var(--muted);font-size:13px}

    @media(max-width:880px){main{grid-template-columns:1fr;}.right{order:-1}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">EK</div>
      <div>
        <h1>Ermac — Agente de Shao Kahn</h1>
        <p class="lead">Ficha interativa — descrição, atributos e mecânicas de poder telecinético.</p>
      </div>
    </header>

    <main>
      <section class="card lore">
        <h2>Contexto / Lore</h2>
        <p>Como punição à resistência contra o domínio de Shao Kahn sobre o reino de Edenia, as almas incontroláveis de guerreiros mortos em kombate foram arrancadas e vinculadas — formando entidades como Ermac. Servindo a Shao Kahn, Ermac é seu agente mais importante. As essências de tantas almas concedem-lhe um imenso poder telecinético, uma vantagem capaz de destruir a resistência ao domínio do Plano Terreno por Shao Kahn.</p>

        <h3>Descrição resumida</h3>
        <p>Ermac é a colmeia de almas: uma consciência forjada por centenas de essências, cada uma contribuindo memória, técnica e raiva. Essa soma lhe dá força sobre-humana e, sobretudo, um controle telecinético que pode mover, esmagar e partir objetos — e até manipular adversários.</p>

        <div class="stats">
          <div class="stat">
            <strong>Telecinese</strong>
            <small>Nível / Fonte: Essências vinculadas</small>
            <div class="power-bar" aria-hidden>
              <div id="powerLevel" class="power-level" style="width:88%"></div>
            </div>
            <small id="powerPercent">88% do potencial disponível</small>
          </div>

          <div class="stat">
            <strong>Função</strong>
            <small>Agente de controle e supressão</small>
            <div style="margin-top:8px">Ações: subjugação, captura, demolir defesas.</div>
          </div>

          <div class="stat">
            <strong>Origem</strong>
            <small>Edenia — Punição por resistência</small>
          </div>

          <div class="stat">
            <strong>Vulnerabilidades</strong>
            <small>Rituais de purificação; magias de dispersão de alma; armas encantadas.</small>
          </div>
        </div>

        <h3 style="margin-top:14px">Mecânica proposta para site</h3>
        <ol>
          <li>Ficha estática com lore, atributos e animações de poder.</li>
          <li>Contadores interativos ("Almas vinculadas") que afetam a barra de poder telecinético.</li>
          <li>Simulação simples: aumentar/reduzir almas e observar efeitos (força, alcance).</li>
          <li>Seção "Escolha do jogador" para testar resistências ou rituais.</li>
        </ol>
      </section>

      <aside class="card right">
        <div class="portrait">[Ilustração de Ermac — Insira imagem]</div>
        <div class="info">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <div>
              <div class="tag">Agente: Shao Kahn</div>
              <div style="margin-top:8px;font-size:13px;color:var(--muted)">Classe: Entidade composta</div>
            </div>
            <div style="text-align:right">
              <div style="font-weight:700;font-size:20px">Poder</div>
              <div style="color:var(--muted)">Telecinético</div>
            </div>
          </div>

          <div class="souls" aria-live="polite">
            <div>
              <div style="font-size:13px;color:var(--muted)">Almas vinculadas</div>
              <div id="soulsCount" style="font-weight:700;font-size:22px">128</div>
            </div>
            <div style="margin-left:auto;display:flex;gap:8px">
              <button id="btnAdd">+ 1</button>
              <button id="btnSub">- 1</button>
            </div>
          </div>

          <div style="margin-top:12px">
            <button id="ritualBtn" style="width:100%;padding:10px;border-radius:10px;border:0;background:linear-gradient(90deg,#3b0d0d,#7e1111);cursor:pointer">Executar Ritual de Dispersão (simular)</button>
          </div>
        </div>
      </aside>
    </main>

    <footer class="card">Criado automaticamente — página de apresentação/ficha. Edite imagens e textos conforme necessário.</footer>
  </div>

  <script>
    // Lógica simples para demonstrar como a "programação" do site pode reagir ao número de almas
    const soulsEl = document.getElementById('soulsCount');
    const powerEl = document.getElementById('powerLevel');
    const powerPercent = document.getElementById('powerPercent');
    let souls = 128;

    function updateUI(){
      soulsEl.textContent = souls;
      // Escala do poder: 0-300 almas -> 0% a 100% (cap arbitrário)
      const cap = 300;
      const pct = Math.min(100, Math.round((souls / cap) * 100));
      powerEl.style.width = pct + '%';
      powerPercent.textContent = pct + '% do potencial disponível';
    }

    document.getElementById('btnAdd').addEventListener('click',()=>{souls++;updateUI();});
    document.getElementById('btnSub').addEventListener('click',()=>{if(souls>0) souls--;updateUI();});

    document.getElementById('ritualBtn').addEventListener('click',()=>{
      // Simular ritual de dispersão: reduz 40% das almas por "sucesso"
      const lost = Math.max(1, Math.floor(souls * 0.4));
      souls = Math.max(0, souls - lost);
      updateUI();
      alert('Ritual executado: ' + lost + ' almas dispersas.');
    });

    updateUI();
  </script>
</body>
</html>
