<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EnzyMail - Comunidade Científica sobre Enzimas</title>
  <style>
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background-color: #f4f4f4;
      margin: 0;
      padding: 0;
      color: #333;
    }
    .header {
      background: linear-gradient(135deg, #1abc9c, #16a085);
      color: white;
      padding: 25px 20px;
      text-align: center;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    .logo {
      font-size: 2.5em;
      margin: 0;
      font-weight: 700;
      letter-spacing: 1px;
    }
    .tagline {
      margin: 5px 0 0;
      font-size: 1.1em;
      opacity: 0.9;
    }
    .tab-container {
      display: flex;
      background-color: #34495e;
      justify-content: center;
    }
    .tab {
      padding: 15px 25px;
      color: white;
      cursor: pointer;
      transition: all 0.3s;
      text-align: center;
    }
    .tab:hover {
      background-color: #3d566e;
      transform: translateY(-2px);
    }
    .tab.active {
      background-color: #1abc9c;
      font-weight: bold;
    }
    .content {
      max-width: 1000px;
      margin: 30px auto;
      padding: 0 20px;
    }
    .tab-content {
      display: none;
      animation: fadeIn 0.5s;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    .tab-content.active {
      display: block;
    }
    .info {
      background: white;
      padding: 25px;
      margin-bottom: 25px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    }
    .post {
      background: #e8f0fe;
      padding: 20px;
      margin-bottom: 15px;
      border-radius: 8px;
      transition: transform 0.2s;
    }
    .post:hover {
      transform: translateX(5px);
    }
    .post h3 {
      margin: 0 0 10px;
      cursor: pointer;
      color: #2c3e50;
    }
    .form {
      margin: 30px auto;
      padding: 25px;
      background: #ffffff;
      border-radius: 10px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    textarea, input[type="text"], input[type="file"] {
      width: 100%;
      padding: 12px;
      margin-bottom: 15px;
      border-radius: 5px;
      border: 1px solid #ddd;
      font-family: inherit;
    }
    button {
      padding: 12px 25px;
      background-color: #16a085;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s;
      font-weight: bold;
    }
    button:hover {
      background-color: #1abc9c;
      transform: translateY(-2px);
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .section-title {
      color: #16a085;
      margin-top: 0;
      border-bottom: 2px solid #eee;
      padding-bottom: 10px;
    }
    .article-content, .comments {
      display: none;
      margin-top: 15px;
    }
    .comment-box textarea {
      height: 80px;
    }
    .like-btn {
      margin-right: 10px;
      cursor: pointer;
      color: #16a085;
      font-weight: bold;
    }
    .like-count {
      font-weight: bold;
      color: #7f8c8d;
    }
    .post img {
      max-width: 100%;
      margin-top: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .enzyme-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 25px;
      margin-top: 25px;
    }
    .enzyme-card {
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }
    .enzyme-card:hover {
      transform: translateY(-5px);
    }
    .enzyme-card h3 {
      color: #16a085;
      margin-top: 0;
    }
    .benefits-list {
      margin-left: 20px;
    }
    .benefits-list li {
      margin-bottom: 10px;
      line-height: 1.5;
    }
    .enzyme-of-the-day {
      background: #e8f4f1;
      border-left: 4px solid #16a085;
      padding: 15px;
      margin: 20px 0;
    }
  </style>
</head>
<body>
  <div class="header">
    <h1 class="logo">EnzyMail</h1>
    <p class="tagline">Comunidade científica sobre enzimas e saúde</p>
  </div>

  <div class="tab-container">
    <div class="tab active" onclick="openTab('home')">🏠 Início</div>
    <div class="tab" onclick="openTab('types')">🧪 Tipos de Enzimas</div>
    <div class="tab" onclick="openTab('nutrition')">🍏 Nutrição Enzimática</div>
    <div class="tab" onclick="openTab('wellness')">💪 Saúde Integral</div>
    <div class="tab" onclick="openTab('forum')">💬 Comunidade</div>
  </div>

  <div class="content">
    <!-- Página Inicial -->
    <div id="home" class="tab-content active">
      <div class="info">
        <h2 class="section-title">Bem-vindo ao EnzyMail!</h2>
        <p>O EnzyMail é a principal comunidade online dedicada ao estudo e compartilhamento de conhecimento sobre enzimas e seu impacto na saúde humana. Conectamos entusiastas, profissionais de saúde e pesquisadores em um ambiente colaborativo.</p>
        
        <div class="enzyme-of-the-day">
          <h3>🧪 Enzima em Destaque: Catalase</h3>
          <p><strong>Catalase</strong> é uma enzima antioxidante crucial que protege as células contra danos oxidativos, convertendo peróxido de hidrogênio em água e oxigênio. Presente em vegetais como brócolis e espinafre, sua atividade pode ser otimizada através de uma alimentação rica em nutrientes.</p>
        </div>

        <h3>Por que participar do EnzyMail?</h3>
        <ul class="benefits-list">
          <li>🔹 Acesso a pesquisas atualizadas sobre enzimologia</li>
          <li>🔹 Troca de conhecimentos com especialistas da área</li>
          <li>🔹 Discussões sobre aplicações terapêuticas de enzimas</li>
          <li>🔹 Dicas práticas para otimizar sua saúde enzimática</li>
          <li>🔹 Suporte para dúvidas sobre suplementação enzimática</li>
        </ul>
        
        <div class="enzyme-grid">
          <div class="enzyme-card">
            <h3>Enzimas Digestivas</h3>
            <p>Essenciais para a quebra e absorção de nutrientes, incluindo amilase (carboidratos), protease (proteínas) e lipase (gorduras). Problemas digestivos frequentemente estão relacionados à deficiência dessas enzimas.</p>
          </div>
          <div class="enzyme-card">
            <h3>Enzimas Sistêmicas</h3>
            <p>Atuam em todo o organismo, regulando processos como inflamação, circulação e imunidade. Exemplos incluem serrapeptase e nattokinase, usadas em protocolos de saúde integrativa.</p>
          </div>
          <div class="enzyme-card">
            <h3>Enzimas Alimentares</h3>
            <p>Presentes em alimentos crus e fermentados, como bromelina (abacaxi) e papaína (mamão). Essas enzimas auxiliam na digestão e possuem propriedades anti-inflamatórias.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Tipos de Enzimas -->
    <div id="types" class="tab-content">
      <div class="info">
        <h2 class="section-title">Classificação das Enzimas</h2>
        
        <h3>1. Enzimas Digestivas</h3>
        <ul class="benefits-list">
          <li><strong>Amilase Salivar:</strong> Inicia a digestão de carboidratos na boca. Atividade reduzida em dietas com excesso de alimentos processados.</li>
          <li><strong>Pepsina:</strong> Produzida no estômago, atua em pH ácido para digerir proteínas. Sua produção diminui com o envelhecimento.</li>
          <li><strong>Lipase Pancreática:</strong> Essencial para digestão de gorduras. Deficiências podem levar a má absorção de vitaminas lipossolúveis.</li>
        </ul>
        
        <h3>2. Enzimas Metabólicas</h3>
        <ul class="benefits-list">
          <li><strong>Superóxido Dismutase (SOD):</strong> Poderoso antioxidante que protege contra radicais livres. Níveis podem ser aumentados com consumo de vegetais crucíferos.</li>
          <li><strong>ATP Sintase:</strong> Responsável pela produção de energia celular. Otimizada por exercícios regulares e nutrição adequada.</li>
          <li><strong>DNA Polimerase:</strong> Essencial para reparo e replicação do DNA. Requer zinco e magnésio para funcionamento ideal.</li>
        </ul>
      </div>
      
      <div class="info">
        <h2 class="section-title">Enzimas na Medicina</h2>
        <p>As aplicações terapêuticas das enzimas estão em expansão:</p>
        <ul class="benefits-list">
          <li><strong>Terapia de Reposição:</strong> Para condições como insuficiência pancreática (enzimas pancreáticas) ou intolerância à lactose (lactase).</li>
          <li><strong>Anti-inflamatórias:</strong> Enzimas proteolíticas como bromelina são usadas para reduzir edema e inflamação.</li>
          <li><strong>Cardiovasculares:</strong> Nattokinase e lumbrokinase auxiliam na saúde circulatória.</li>
          <li><strong>Oncologia:</strong> Pesquisas investigam o uso de enzimas como L-asparaginase em tratamentos contra o câncer.</li>
        </ul>
      </div>
    </div>

    <!-- Nutrição Enzimática -->
    <div id="nutrition" class="tab-content">
      <div class="info">
        <h2 class="section-title">Dieta Rica em Enzimas</h2>
        
        <h3>Alimentos Crus</h3>
        <p>Fontes naturais de enzimas digestivas (destruídas acima de 47°C):</p>
        <ul class="benefits-list">
          <li><strong>Abacaxi:</strong> Contém bromelina, que auxilia na digestão de proteínas e tem efeito anti-inflamatório.</li>
          <li><strong>Mamão:</strong> Fonte de papaína, especialmente eficaz para digerir carnes e proteínas complexas.</li>
          <li><strong>Mel cru:</strong> Contém diastases, invertases e outras enzimas benéficas.</li>
        </ul>
        
        <h3>Alimentos Fermentados</h3>
        <p>Processo que aumenta exponencialmente o conteúdo enzimático:</p>
        <ul class="benefits-list">
          <li><strong>Kefir:</strong> Rico em enzimas e probióticos que melhoram a saúde intestinal.</li>
          <li><strong>Missô:</strong> Pasta de soja fermentada contendo enzimas que auxiliam na digestão.</li>
          <li><strong>Chucrute:</strong> Repolho fermentado que fornece enzimas e bactérias benéficas.</li>
        </ul>
      </div>
      
      <div class="info">
        <h2 class="section-title">Suplementação Enzimática</h2>
        <p>Quando a dieta não é suficiente, suplementos podem ajudar:</p>
        <ul class="benefits-list">
          <li><strong>Enzimas Digestivas:</strong> Para quem sofre de indigestão, inchaço ou má absorção.</li>
          <li><strong>Enzimas Sistêmicas:</strong> Usadas entre refeições para efeitos anti-inflamatórios.</li>
          <li><strong>Combinações Específicas:</strong> Como DPP-IV para sensibilidade ao glúten/caseína.</li>
        </ul>
        <p class="enzyme-of-the-day">💡 Dica EnzyMail: Consulte um profissional antes de iniciar qualquer suplementação enzimática.</p>
      </div>
    </div>

    <!-- Saúde Integral -->
    <div id="wellness" class="tab-content">
      <div class="info">
        <h2 class="section-title">Enzimas e Longevidade</h2>
        
        <p>Estudos mostram que a atividade enzimática diminui com a idade, contribuindo para o envelhecimento. Estratégias para manter a função enzimática:</p>
        <ul class="benefits-list">
          <li><strong>Dieta Alcalinizante:</strong> pH adequado é crucial para atividade enzimática.</li>
          <li><strong>Jejum Intermitente:</strong> Reduz a sobrecarga do sistema enzimático digestivo.</li>
          <li><strong>Exercício Moderado:</strong> Estimula a produção de enzimas antioxidantes.</li>
          <li><strong>Gerenciamento do Estresse:</strong> Cortisol elevado inibe enzimas digestivas.</li>
        </ul>
      </div>
      
      <div class="info">
        <h2 class="section-title">Enzimas na Prática Clínica</h2>
        <p>Aplicações terapêuticas documentadas:</p>
        <ul class="benefits-list">
          <li><strong>Lactase:</strong> Tratamento para intolerância à lactose.</li>
          <li><strong>Serrapeptase:</strong> Redução de inflamação e muco em condições respiratórias.</li>
          <li><strong>Nattokinase:</strong> Melhora da circulação e saúde cardiovascular.</li>
          <li><strong>Proteases:</strong> Auxílio na digestão e modulação imunológica.</li>
        </ul>
      </div>
    </div>

    <!-- Comunidade -->
    <div id="forum" class="tab-content">
      <div class="info">
        <h2 class="section-title">📚 Artigos da Comunidade</h2>
        <div class="post">
          <h3 onclick="toggleContent(this)">Experiência com suplementação de enzimas digestivas</h3>
          <div class="article-content">
            <p>Relato de caso: Melhora de 80% nos sintomas de distensão abdominal após 3 meses de uso de enzimas pancreáticas. Protocolo incluiu mudanças dietéticas concomitantes.</p>
            <div class="comments">
              <h4>Comentários</h4>
              <div class="comment-list"></div>
              <div class="comment-box">
                <input type="text" placeholder="Seu nome...">
                <textarea placeholder="Contribua com sua experiência..."></textarea>
                <button onclick="addComment(this)">Enviar</button>
              </div>
            </div>
          </div>
        </div>
        
        <div class="post">
          <h3 onclick="toggleContent(this)">Pesquisa: Efeitos da bromelina na artrite</h3>
          <div class="article-content">
            <p>Estudo recente demonstra redução de 40% nos marcadores inflamatórios com uso de bromelina em comparação com placebo. Discussão sobre mecanismos de ação.</p>
            <div class="comments">
              <h4>Comentários</h4>
              <div class="comment-list"></div>
              <div class="comment-box">
                <input type="text" placeholder="Seu nome...">
                <textarea placeholder="Contribua com sua experiência..."></textarea>
                <button onclick="addComment(this)">Enviar</button>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="form">
        <h2>📝 Compartilhe seu conhecimento</h2>
        <input type="text" id="usuario" placeholder="Nome (opcional)">
        <input type="text" id="titulo" placeholder="Título do seu post">
        <textarea id="conteudo" rows="5" placeholder="Descreva sua experiência, pesquisa ou dúvida sobre enzimas..."></textarea>
        <input type="file" id="imagem" accept="image/*">
        <button onclick="publicar()">Publicar na Comunidade</button>
      </div>

      <div class="info" id="posts">
        <h2>🗣️ Discussões Recentes</h2>
      </div>
    </div>
  </div>

  <script>
    const postsData = JSON.parse(localStorage.getItem('postsData')) || [];
    const likedPosts = JSON.parse(localStorage.getItem('likedPosts')) || {};

    function saveData() {
      localStorage.setItem('postsData', JSON.stringify(postsData));
      localStorage.setItem('likedPosts', JSON.stringify(likedPosts));
    }

    function renderPosts() {
      const posts = document.getElementById('posts');
      posts.innerHTML = '<h2>🗣️ Discussões Recentes</h2>';
      
      if (postsData.length === 0) {
        posts.innerHTML += '<p>Nenhuma discussão ainda. Seja o primeiro a postar!</p>';
        return;
      }

      postsData.forEach((post, index) => {
        const postDiv = document.createElement('div');
        postDiv.className = 'post';

        const h3 = document.createElement('h3');
        h3.textContent = post.titulo;
        if (post.usuario) {
          h3.textContent = `${post.usuario}: ${post.titulo}`;
        }

        const p = document.createElement('p');
        p.textContent = post.conteudo;

        const like = document.createElement('span');
        like.className = 'like-btn';
        like.textContent = likedPosts[index] ? '👎 Retirar curtida' : '👍 Curtir';
        const count = document.createElement('span');
        count.className = 'like-count';
        count.textContent = ` (${post.likes || 0})`;
        like.onclick = () => {
          if (!likedPosts[index]) {
            post.likes = (post.likes || 0) + 1;
            likedPosts[index] = true;
          } else {
            post.likes = (post.likes || 0) - 1;
            delete likedPosts[index];
          }
          saveData();
          renderPosts();
        };

        const commentList = document.createElement('div');
        commentList.className = 'comment-list';
        (post.comentarios || []).forEach(c => {
          const p = document.createElement('p');
          p.textContent = `${c.usuario}: ${c.texto}`;
          commentList.appendChild(p);
        });

        const commentBox = document.createElement('div');
        commentBox.className = 'comment-box';
        const nomeInput = document.createElement('input');
        nomeInput.placeholder = 'Seu nome...';
        const textarea = document.createElement('textarea');
        textarea.placeholder = 'Escreva seu comentário...';
        const button = document.createElement('button');
        button.textContent = 'Comentar';
        button.onclick = function () {
          const txt = textarea.value.trim();
          const nome = nomeInput.value.trim();
          if (txt !== '') {
            if (!post.comentarios) post.comentarios = [];
            const comentario = { usuario: nome || 'Anônimo', texto: txt };
            post.comentarios.push(comentario);
            const p = document.createElement('p');
            p.textContent = `${comentario.usuario}: ${comentario.texto}`;
            commentList.appendChild(p);
            textarea.value = '';
            nomeInput.value = '';
            saveData();
          } else {
            alert('Por favor, escreva seu comentário.');
          }
        };
        commentBox.appendChild(nomeInput);
        commentBox.appendChild(textarea);
        commentBox.appendChild(button);

        postDiv.appendChild(h3);
        postDiv.appendChild(p);
        if (post.imagem) {
          const img = document.createElement('img');
          img.src = post.imagem;
          postDiv.appendChild(img);
        }
        postDiv.appendChild(document.createElement('br'));
        postDiv.appendChild(like);
        postDiv.appendChild(count);
        postDiv.appendChild(document.createElement('hr'));
        postDiv.appendChild(commentList);
        postDiv.appendChild(commentBox);

        posts.appendChild(postDiv);
      });
    }

    function publicar() {
      const usuario = document.getElementById('usuario').value;
      const titulo = document.getElementById('titulo').value;
      const conteudo = document.getElementById('conteudo').value;
      const imagemInput = document.getElementById('imagem');

      if (titulo.trim() === '' || conteudo.trim() === '') {
        alert('Por favor, adicione um título e conteúdo para seu post.');
        return;
      }

      let imagem = '';
      if (imagemInput.files && imagemInput.files[0]) {
        const reader = new FileReader();
        reader.onload = function(e) {
          imagem = e.target.result;
          postsData.unshift({ 
            usuario: usuario.trim() || null, 
            titulo, 
            conteudo, 
            imagem, 
            likes: 0, 
            comentarios: [] 
          });
          saveData();
          renderPosts();
          resetForm();
        };
        reader.readAsDataURL(imagemInput.files[0]);
      } else {
        postsData.unshift({ 
          usuario: usuario.trim() || null, 
          titulo, 
          conteudo, 
          imagem: '', 
          likes: 0, 
          comentarios: [] 
        });
        saveData();
        renderPosts();
        resetForm();
      }
    }

    function resetForm() {
      document.getElementById('usuario').value = '';
      document.getElementById('titulo').value = '';
      document.getElementById('conteudo').value = '';
      document.getElementById('imagem').value = '';
    }

    function toggleContent(titleElement) {
      const content = titleElement.nextElementSibling;
      content.style.display = content.style.display === 'block' ? 'none' : 'block';
    }

    function addComment(button) {
      const nomeInput = button.parentElement.querySelector('input');
      const textarea = button.parentElement.querySelector('textarea');
      const nome = nomeInput.value.trim();
      const comment = textarea.value.trim();
      if (comment === '') {
        alert('Por favor, escreva seu comentário.');
        return;
      }

      const commentList = button.parentElement.previousElementSibling;
      const p = document.createElement('p');
      p.textContent = `${nome || 'Anônimo'}: ${comment}`;
      commentList.appendChild(p);
      nomeInput.value = '';
      textarea.value = '';
    }

    function openTab(tabName) {
      // Esconde todos os conteúdos de abas
      const tabContents = document.getElementsByClassName('tab-content');
      for (let i = 0; i < tabContents.length; i++) {
        tabContents[i].classList.remove('active');
      }
      
      // Remove a classe 'active' de todas as abas
      const tabs = document.getElementsByClassName('tab');
      for (let i = 0; i < tabs.length; i++) {
        tabs[i].classList.remove('active');
      }
      
      // Mostra a aba atual e marca como ativa
      document.getElementById(tabName).classList.add('active');
      event.currentTarget.classList.add('active');
      
      // Renderiza os posts se for a aba do fórum
      if (tabName === 'forum') {
        renderPosts();
      }
    }

    // Renderiza os posts ao carregar a página se estiver na aba do fórum
    if (window.location.hash === '#forum') {
      document.querySelector('.tab.active').classList.remove('active');
      document.querySelector('.tab-content.active').classList.remove('active');
      document.querySelector('[onclick="openTab(\'forum\')"]').classList.add('active');
      document.getElementById('forum').classList.add('active');
    }
    renderPosts();
  </script>
</body>
</html>
