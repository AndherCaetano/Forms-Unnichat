<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="HandheldFriendly" content="true">
    <meta name="MobileOptimized" content="width">
    <meta name="theme-color" content="#128C7E">
    <meta name="format-detection" content="telephone=no">
    <title>Formulário Unnichat SendFlow</title>
    
    <style>
        /* ===== VARIÁVEIS E RESET ===== */
        :root {
            --primary-color: #25D366;
            --secondary-color: #128C7E;
            --text-color: #333333;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #757575;
            --white: #ffffff;
            --error-color: #ff4444;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            -webkit-text-size-adjust: 100%;
            -ms-text-size-adjust: 100%;
            -webkit-tap-highlight-color: transparent;
        }
        
        /* ===== ESTILOS GERAIS ===== */
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, 
                         Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
            line-height: 1.5;
            color: var(--text-color);
            background-color: var(--light-gray);
            padding: 20px;
            margin: 0;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            text-rendering: optimizeLegibility;
        }
        
        .container {
            width: 100%;
            max-width: 100%;
            min-height: 100vh;
            margin: 0 auto;
            background: var(--white);
            overflow-x: hidden;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        
        .content-wrapper {
            padding: 20px;
            max-width: 900px;
            margin: 0 auto;
        }
        
        /* ===== CABEÇALHO E TIPOGRAFIA ===== */
        .logo {
            max-height: 60px;
            width: auto;
            height: auto;
            margin: 0 auto 20px;
            display: block;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--medium-gray);
        }
        
        h1 {
            color: var(--secondary-color);
            margin: 15px 0;
            font-size: clamp(1.4rem, 5vw, 1.8rem);
            font-weight: 600;
            line-height: 1.3;
        }
        
        h2 {
            color: var(--secondary-color);
            margin: 25px 0 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid var(--medium-gray);
            font-size: clamp(1.2rem, 4vw, 1.5rem);
            font-weight: 600;
        }
        
        h3 {
            margin: 18px 0 10px;
            color: var(--secondary-color);
            font-size: clamp(1.1rem, 3.5vw, 1.3rem);
        }
        
        .intro-text {
            text-align: justify;
            margin-bottom: 18px;
            font-size: clamp(0.95rem, 3vw, 1.05rem);
            line-height: 1.6;
            color: var(--dark-gray);
            hyphens: auto;
            text-justify: inter-word;
        }
        
        /* ===== SEÇÕES E FORMULÁRIO ===== */
        .part {
            margin-bottom: 25px;
            padding: 20px;
            background-color: var(--light-gray);
            border-radius: 8px;
        }
        
        .question {
            margin-bottom: 18px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }
        
        .question label {
            display: block;
            font-weight: 500;
            margin-bottom: 8px;
            font-size: clamp(0.95rem, 3vw, 1.05rem);
            text-align: left;
            width: 100%;
        }
        
        .required-field::after {
            content: " *";
            color: var(--error-color);
        }
        
        .question input[type="text"],
        .question input[type="email"],
        .question input[type="tel"],
        .question textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--medium-gray);
            border-radius: 6px;
            font-size: clamp(0.95rem, 3vw, 1.05rem);
            background-color: var(--white);
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
            transition: all 0.3s ease;
        }
        
        .question textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        .question input:focus,
        .question textarea:focus {
            outline: none;
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 3px rgba(18, 140, 126, 0.15);
        }
        
        /* Contador de caracteres */
        .char-counter {
            font-size: 0.8rem;
            color: var(--dark-gray);
            text-align: right;
            margin-top: 5px;
        }
        
        .char-counter.warning {
            color: orange;
        }
        
        .char-counter.danger {
            color: var(--error-color);
            font-weight: bold;
        }
        
        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 15px;
        }
        
        .form-group {
            flex: 1 1 100%;
            min-width: 0;
        }
        
        /* ===== BOTÕES ===== */
        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }
        
        button {
            flex: 1 1 100%;
            padding: 15px 25px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: clamp(1rem, 3vw, 1.1rem);
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            -webkit-tap-highlight-color: transparent;
        }
        
        .btn-email {
            background-color: var(--secondary-color);
            color: var(--white);
        }
        
        button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        /* ===== ELEMENTOS ESPECIAIS ===== */
        .emoji {
            font-size: 1.1em;
            margin-right: 5px;
        }
        
        .candidate-info {
            background-color: #f0f8ff;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 25px;
        }
        
        .screen-image {
            width: 100%;
            max-width: 100%;
            margin: 15px auto;
            display: block;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        
        /* ===== MODAL ===== */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0,0,0,0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s ease;
            padding: 20px;
        }
        
        .modal.active {
            opacity: 1;
            pointer-events: all;
        }
        
        .modal-content {
            background-color: var(--white);
            padding: 30px;
            border-radius: 10px;
            width: 100%;
            max-width: 450px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.2);
        }
        
        .modal-content p {
            margin-bottom: 20px;
            font-size: clamp(1.05rem, 3vw, 1.15rem);
            line-height: 1.6;
        }
        
        .modal-close {
            background-color: var(--secondary-color);
            color: var(--white);
            border: none;
            padding: 12px 25px;
            border-radius: 6px;
            font-weight: 500;
            cursor: pointer;
            font-size: clamp(1rem, 3vw, 1.1rem);
            transition: all 0.3s ease;
        }
        
        .modal-close:hover {
            opacity: 0.9;
        }
        
        /* ===== FOOTER E BOTÃO LIMPAR ===== */
        .footer {
            margin-top: 30px;
            padding: 20px;
            text-align: center;
            font-size: 0.9rem;
            color: var(--dark-gray);
            border-top: 1px solid var(--medium-gray);
        }
        
        .footer-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-bottom: 15px;
        }
        
        .footer a {
            color: #0066cc;
            text-decoration: underline;
            font-weight: 500;
        }
        
        .footer a:hover {
            text-decoration: underline;
            color: #004499;
        }
        
        .btn-clear {
            background-color: transparent;
            color: var(--dark-gray);
            border: 1px solid var(--medium-gray);
            margin-top: 10px;
        }
        
        .btn-clear:hover {
            background-color: var(--light-gray);
            transform: none;
        }
        
        /* Botão de scroll */
        .scroll-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: var(--secondary-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            z-index: 99;
            transition: all 0.3s ease;
            border: none;
        }
        
        .scroll-top:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }
        
        .scroll-top i {
            font-size: 24px;
            transition: transform 0.3s ease;
        }
        
        /* ===== MEDIA QUERIES ===== */
        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            
            .content-wrapper {
                padding: 15px;
            }
            
            .part {
                padding: 15px;
            }
            
            .question input,
            .question textarea {
                padding: 10px 12px;
            }
            
            .footer-links {
                flex-direction: column;
                gap: 10px;
            }
            
            .scroll-top {
                bottom: 20px;
                right: 20px;
                width: 40px;
                height: 40px;
            }
        }
        
        @media (min-width: 600px) {
            .form-group {
                flex: 1 1 calc(50% - 15px);
            }
            
            button {
                flex: 1 1 calc(50% - 15px);
            }
        }
        
        @media (min-width: 768px) {
            .content-wrapper {
                padding: 30px;
            }
        }
        
        @media print {
            .footer, .btn-clear, .scroll-top {
                display: none;
            }
        }
        
        /* Correção para iOS */
        @supports (-webkit-touch-callout: none) {
            input, 
            textarea,
            select {
                font-size: 16px !important;
            }
        }
    </style>
    <!-- Ícones Font Awesome para a seta -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <div class="container">
        <div class="content-wrapper">
            <!-- Logotipo -->
            <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.14.04.png" alt="Unnichat Logo" class="logo">
            
            <header>
                <h1><span class="emoji">📝</span> Formulário Unnichat SendFlow</h1>
                
                <p class="intro-text">Olá, se você chegou até aqui é porque possui as atribuições necessárias para fazer parte da Equipe Unnichat! Então, parabéns! 🥳 Essa etapa é composta por algumas perguntas e um teste prático criado para avaliar suas habilidades e abordagens.</p>
                
                <p class="intro-text">O teste será avaliado com confidencialidade, e suas soluções não serão usadas para fins comerciais.</p>
                
                <p class="intro-text"><strong>ORIENTAÇÕES PARA RESPOSTA:</strong> Para esta etapa do teste, você terá 24 horas até a entrega final, a contar do horário em que a mensagem com o teste foi enviada para você.</p>
                
                <p class="intro-text">Preencha o formulário abaixo para conhecermos melhor seu perfil e suas habilidades. Todos os campos são obrigatórios, exceto quando indicado.</p><br>
               
                * Ao finalizar, clique no botão Enviar por E-mail e compartilhe o arquivo PDF para o email: <strong>shi@sendflow.com.br</strong>, com cópia para <strong>luiz@sendflow.pro</strong>
            </header>

            <form id="candidateForm">
                <!-- Seção de informações do candidato -->
                <div class="candidate-info">
                    <h2>Informações do Candidato</h2>
                    
                    <div class="form-row">
                        <div class="form-group question">
                            <label for="candidateName" class="required-field">Nome:</label>
                            <input type="text" id="candidateName" name="candidateName" maxlength="40" required placeholder="Digite seu nome completo (máx. 40 caracteres)">
                        </div>
                        
                        <div class="form-group question">
                            <label for="candidatePhone" class="required-field">Telefone:</label>
                            <input type="tel" id="candidatePhone" name="candidatePhone" pattern="[0-9]{2}-[0-9]{5}-[0-9]{4}" required placeholder="Digite direto 😁">
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group question">
                            <label for="candidateEmail" class="required-field">E-mail:</label>
                            <input type="email" id="candidateEmail" name="candidateEmail" required placeholder="Seu e-mail 😌">
                        </div>
                        
                        <div class="form-group question">
                            <label for="jobTitle" class="required-field">Nome da vaga pretendida: ✌🏽</label>
                            <input type="text" id="jobTitle" name="jobTitle" maxlength="50" required placeholder="Digite o nome da vaga (máx. 50 caracteres)">
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group question">
                            <label for="jobCode">Código da Vaga (opcional):</label>
                            <input type="text" id="jobCode" name="jobCode" placeholder="Digite o código da vaga, se houver 🤙🏾">
                        </div>
                    </div>
                </div>

                <!-- Parte 1 - Comportamental -->
                <div class="part">
                    <h2>PARTE 1 - Comportamental</h2>
                    <p class="intro-text">Considere o seguinte cenário: Você presta suporte para uma ferramenta de automação de WhatsApp.</p>
                    
                    <div class="question">
                        <label for="p1a" class="required-field">a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?</label>
                        <textarea id="p1a" name="p1a" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p1b" class="required-field">b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?</label>
                        <textarea id="p1b" name="p1b" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p1c" class="required-field">c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?</label>
                        <textarea id="p1c" name="p1c" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p1d" class="required-field">d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?</label>
                        <textarea id="p1d" name="p1d" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p1e1" class="required-field">1. Monte um Roteiro de atendimento para: Dúvida operacional da ferramenta.</label>
                        <textarea id="p1e1" name="p1e1" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p1e2" class="required-field">2. Monte um Roteiro de atendimento para: Suporte técnico.</label>
                        <textarea id="p1e2" name="p1e2" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                </div>
                
                <!-- Parte 2 - Conhecimento do Produto -->
                <div class="part">
                    <h2>PARTE 2 - Conhecimento do Produto</h2>
                    <p class="intro-text">Observe essa tela:</p>
                    
                    <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.10.17.png" alt="Tela do Unnichat" class="screen-image">
                    
                    <div class="question">
                        <label for="p2a" class="required-field">a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?</label>
                        <textarea id="p2a" name="p2a" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p2b" class="required-field">b. Onde o cliente aperta para efetuar disparos em massa para os clientes?</label>
                        <textarea id="p2b" name="p2b" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p2c" class="required-field">c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?</label>
                        <textarea id="p2c" name="p2c" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p2d" class="required-field">d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?</label>
                        <textarea id="p2d" name="p2d" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p2e" class="required-field">e. Onde você iria para entender mais sobre o Unnichat?</label>
                        <textarea id="p2e" name="p2e" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p2f" class="required-field">f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?</label>
                        <textarea id="p2f" name="p2f" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                </div>
                
                <!-- Parte 3 - Conhecimentos Específicos -->
                <div class="part">
                    <h2>PARTE 3 - Conhecimentos Específicos</h2>
                    <p class="intro-text">Agora, teremos perguntas nichadas. Se você não souber a resposta, não se preocupe, não é uma etapa eliminatória (mas você pode tentar responder também).</p>
                    
                    <div class="question">
                        <label for="p3a" class="required-field">a. O que é API Oficial do WhatsApp?</label>
                        <textarea id="p3a" name="p3a" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p3b" class="required-field">b. Qual o custo médio de envio da API?</label>
                        <textarea id="p3b" name="p3b" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p3c" class="required-field">c. Qualquer pessoa pode ter uma conta API Oficial?</label>
                        <textarea id="p3c" name="p3c" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                    
                    <div class="question">
                        <label for="p3d" class="required-field">d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.</label>
                        <textarea id="p3d" name="p3d" required maxlength="5000"></textarea>
                        <div class="char-counter" data-maxlength="5000">5000 caracteres restantes</div>
                    </div>
                </div>
                
                <!-- Botões de envio -->
                <div class="buttons">
                    <button type="button" class="btn-email" id="sendEmail">
                        <span class="emoji">📧</span> Enviar por E-mail
                    </button>
                </div>
            </form>

            <!-- Rodapé com links e botão Limpar -->
            <div class="footer">
                <div class="footer-links">
                    <br><br>
                    <a href="mailto:shi@sendflow.com.br?cc=luiz@sendflow.pro">Clique aqui para enviar por e-mail: shi@sendflow.com.br (com cópia para luiz@sendflow.pro)</a>
                </div>
                <br><br> <!-- Duas quebras de linha adicionadas -->
                <button type="button" class="btn-clear" onclick="clearForm()">Limpar Formulário</button>
                <p>Formulário gerado em: <span id="generatedDate"></span></p>
            </div>
        </div>
    </div>

    <!-- Botão de scroll -->
    <button class="scroll-top" id="scrollTop" title="Ir para o topo">
        <i class="fas fa-arrow-up"></i>
    </button>

    <!-- Modal de confirmação -->
    <div id="confirmationModal" class="modal">
        <div class="modal-content">
            <p>Suas respostas foram enviadas com sucesso!</p>
            <p>Aguarde o nosso retorno o mais breve possível, Unnichat SendFlow agradece, obrigado!</p>
            <button class="modal-close" onclick="closeModal()">OK</button>
        </div>
    </div>

    <!-- Modal de informação inicial -->
    <div id="infoModal" class="modal active">
        <div class="modal-content">
            <p><strong>Atenção!</strong></p>
            <p>Por favor, preencha primeiro todas as informações na seção "Informações do Candidato" antes de responder às demais perguntas.</p>
            <p>Os campos marcados com * são obrigatórios.</p>
            <button class="modal-close" onclick="closeInfoModal()">Entendi</button>
        </div>
    </div>

    <!-- Scripts -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
    <script>
        // Inicializar jsPDF
        const { jsPDF } = window.jspdf;
        
        // Funções para o modal
        function showModal() {
            document.getElementById('confirmationModal').classList.add('active');
        }
        
        function closeModal() {
            document.getElementById('confirmationModal').classList.remove('active');
        }
        
        function closeInfoModal() {
            document.getElementById('infoModal').classList.remove('active');
        }
        
        // Função para limpar o formulário
        function clearForm() {
            if (confirm('Tem certeza que deseja limpar todo o formulário? Todos os dados serão perdidos.')) {
                document.getElementById('candidateForm').reset();
                
                // Reset character counters
                document.querySelectorAll('.char-counter').forEach(counter => {
                    const maxLength = parseInt(counter.getAttribute('data-maxlength')) || 5000;
                    counter.textContent = `${maxLength} caracteres restantes`;
                    counter.classList.remove('warning', 'danger');
                });
                
                // Show confirmation
                alert('Formulário limpo com sucesso!');
            }
        }
        
        // Função para formatar data e hora
        function getFormattedDateTime() {
            const now = new Date();
            const date = now.toLocaleDateString('pt-BR');
            const time = now.toLocaleTimeString('pt-BR', { hour: '2-digit', minute: '2-digit' });
            return `${date} às ${time}`;
        }
        
        // Adicionar data de geração ao rodapé
        document.getElementById('generatedDate').textContent = getFormattedDateTime();
        
        // Máscara para telefone
        document.getElementById('candidatePhone').addEventListener('input', function(e) {
            let value = e.target.value.replace(/\D/g, '');
            if (value.length > 2) {
                value = value.substring(0, 2) + '-' + value.substring(2);
            }
            if (value.length > 8) {
                value = value.substring(0, 8) + '-' + value.substring(8, 12);
            }
            e.target.value = value;
        });
        
        // Contador de caracteres em tempo real
        document.querySelectorAll('textarea').forEach(textarea => {
            const counter = textarea.nextElementSibling;
            if (counter && counter.classList.contains('char-counter')) {
                const maxLength = parseInt(counter.getAttribute('data-maxlength')) || 5000;
                
                textarea.addEventListener('input', function() {
                    const remaining = maxLength - this.value.length;
                    counter.textContent = `${remaining} caracteres restantes`;
                    
                    // Altera a cor conforme a quantidade de caracteres
                    counter.classList.remove('warning', 'danger');
                    if (remaining < 100) {
                        counter.classList.add('danger');
                    } else if (remaining < 300) {
                        counter.classList.add('warning');
                    }
                });
            }
        });
        
        // Validação de formulário genérica
        function validateForm() {
            const form = document.getElementById('candidateForm');
            const requiredFields = form.querySelectorAll('[required]');
            let isValid = true;
            
            requiredFields.forEach(field => {
                if (!field.value.trim()) {
                    isValid = false;
                    field.style.borderColor = 'var(--error-color)';
                    field.scrollIntoView({ behavior: 'smooth', block: 'center' });
                } else {
                    field.style.borderColor = '';
                }
            });
            
            // Validar formato do telefone
            const phoneField = document.getElementById('candidatePhone');
            const phoneRegex = /^\d{2}-\d{5}-\d{4}$/;
            if (!phoneRegex.test(phoneField.value)) {
                isValid = false;
                phoneField.style.borderColor = 'var(--error-color)';
                phoneField.scrollIntoView({ behavior: 'smooth', block: 'center' });
                alert('Por favor, insira um telefone no formato 00-00000-0000');
            }
            
            // Validar e-mail
            const emailField = document.getElementById('candidateEmail');
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(emailField.value)) {
                isValid = false;
                emailField.style.borderColor = 'var(--error-color)';
                emailField.scrollIntoView({ behavior: 'smooth', block: 'center' });
                alert('Por favor, insira um e-mail válido');
            }
            
            if (!isValid) {
                alert('Por favor, preencha todos os campos obrigatórios corretamente antes de enviar.');
            }
            
            return isValid;
        }
        
        // Botão de scroll
        const scrollTopBtn = document.getElementById('scrollTop');
        
        window.addEventListener('scroll', function() {
            if (window.pageYOffset > 300) {
                scrollTopBtn.style.display = 'flex';
                scrollTopBtn.querySelector('i').className = 'fas fa-arrow-up';
                scrollTopBtn.setAttribute('title', 'Ir para o topo');
            } else {
                scrollTopBtn.querySelector('i').className = 'fas fa-arrow-down';
                scrollTopBtn.setAttribute('title', 'Descer ligeiramente');
            }
        });
        
        scrollTopBtn.addEventListener('click', function() {
            if (window.pageYOffset > 300) {
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            } else {
                window.scrollTo({
                    top: 350,
                    behavior: 'smooth'
                });
            }
        });
        
        // Função para criar o PDF
        function createPDF() {
            const doc = new jsPDF();
            
            // Configurações de margem
            const marginLeft = 15;
            const marginRight = 15;
            const maxWidth = 180; // Largura máxima do texto (210 - margens)
            
            let yPosition = 10; // Posição inicial mais alta

            // 1. Adicionar "Projeto B" no topo do PDF
            doc.setFontSize(12);
            doc.setTextColor(50, 50, 50); // Cor escura
            doc.setFont(undefined, 'italic'); // Define o estilo como itálico
            doc.text("Projeto B", marginLeft, yPosition); // Alinhado à esquerda
            doc.setFont(undefined, 'normal'); // Negrito
            yPosition += 8; // Espaçamento após o texto

            // 2. Adicionar a logo
            const logoUrl = 'https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-29-as-10.26.42.png';
            try {
                doc.addImage(logoUrl, 'PNG', marginLeft, yPosition, 40, 20);
                yPosition += 25;
            } catch (e) {
                console.log('Erro ao carregar logo:', e);
                doc.setFontSize(12);
                doc.text('Unnichat SendFlow', marginLeft, yPosition);
                doc.setFont(undefined, 'normal'); // Negrito
                yPosition += 15;
            }

            // 3. Adicionar título principal
            doc.setFontSize(18);
            doc.setTextColor(18, 140, 126);
            doc.text('Formulário de Questões Unnichat-SendFlow', 105, yPosition, { align: 'center' });
            yPosition += 10;
            
            doc.setFontSize(12);
            doc.setTextColor(0, 0, 0);
            doc.text('Data e hora do envio: ' + getFormattedDateTime(), 105, yPosition, { align: 'center' });
            yPosition += 20;
            
            // Adicionar informações do candidato
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            doc.text('INFORMAÇÕES DO CANDIDATO', marginLeft, yPosition);
            yPosition += 10;
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            const fields = [
                { id: 'candidateName', label: 'Nome: ' },
                { id: 'candidatePhone', label: 'Telefone: ' },
                { id: 'candidateEmail', label: 'E-mail: ' },
                { id: 'jobTitle', label: 'Vaga Pretendida: ' },
                { id: 'jobCode', label: 'Código da Vaga: ', optional: true }
            ];
            
            fields.forEach(field => {
                const value = document.getElementById(field.id).value;
                if (!field.optional || value) {
                    doc.text(field.label + value, marginLeft, yPosition);
                    yPosition += 7;
                }
            });
            
            yPosition += 10;
            
            // Função para adicionar texto com quebra de linha e verificação de página
            function addTextWithBreaks(text, x, y, maxWidth, lineHeight) {
                const lines = doc.splitTextToSize(text, maxWidth);
                for (let i = 0; i < lines.length; i++) {
                    if (y > 280) { // Verifica se está no final da página
                        doc.addPage();
                        y = 20;
                    }
                    doc.text(lines[i], x, y);
                    y += lineHeight;
                }
                return y;
            }
            
            // Adicionar respostas das partes 1, 2 e 3
            const parts = [
                { 
                    title: 'PARTE 1 - COMPORTAMENTAL',
                    questions: [
                        { id: 'p1a', text: 'a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?' },
                        { id: 'p1b', text: 'b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?' },
                        { id: 'p1c', text: 'c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?' },
                        { id: 'p1d', text: 'd. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?' },
                        { id: 'p1e1', text: '1. Monte um Roteiro de atendimento para: Dúvida operacional da ferramenta.' },
                        { id: 'p1e2', text: '2. Monte um Roteiro de atendimento para: Suporte técnico.' }
                    ]
                },
                {
                    title: 'PARTE 2 - CONHECIMENTO DO PRODUTO',
                    questions: [
                        { id: 'p2a', text: 'a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?' },
                        { id: 'p2b', text: 'b. Onde o cliente aperta para efetuar disparos em massa para os clientes?' },
                        { id: 'p2c', text: 'c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?' },
                        { id: 'p2d', text: 'd. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?' },
                        { id: 'p2e', text: 'e. Onde você iria para entender mais sobre o Unnichat?' },
                        { id: 'p2f', text: 'f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?' }
                    ]
                },
                {
                    title: 'PARTE 3 - CONHECIMENTOS ESPECÍFICOS',
                    questions: [
                        { id: 'p3a', text: 'a. O que é API Oficial do WhatsApp?' },
                        { id: 'p3b', text: 'b. Qual o custo médio de envio da API?' },
                        { id: 'p3c', text: 'c. Qualquer pessoa pode ter uma conta API Oficial?' },
                        { id: 'p3d', text: 'd. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.' }
                    ]
                }
            ];
            
            parts.forEach(part => {
                doc.setFontSize(14);
                doc.setTextColor(18, 140, 126);
                yPosition = addTextWithBreaks(part.title, marginLeft, yPosition, maxWidth, 10);
                
                doc.setFontSize(11);
                doc.setTextColor(0, 0, 0);
                
                part.questions.forEach(question => {
                    const answer = document.getElementById(question.id).value;
                    yPosition = addTextWithBreaks(question.text, marginLeft, yPosition, maxWidth, 7);
                    doc.setTextColor(0, 0, 255);
                    yPosition = addTextWithBreaks(answer, marginLeft + 5, yPosition, maxWidth - 5, 7);
                    doc.setTextColor(0, 0, 0);
                    yPosition += 5;
                });
                
                yPosition += 10;
            });
            
            // Adicionar rodapé com logo e data
            doc.setFontSize(10);
            doc.setTextColor(100, 100, 100);
            
            try {
                // Add footer logo
                doc.addImage(logoUrl, 'PNG', marginLeft, 275, 30, 15);
            } catch (e) {
                console.log('Erro ao carregar logo no rodapé:', e);
            }

            // Criar link de email com campos pré-preenchidos
            const candidateName = document.getElementById('candidateName').value;
            const jobTitle = document.getElementById('jobTitle').value;
            const emailLink = `mailto:shi@sendflow.com.br?cc=luiz@sendflow.pro&subject=Candidatura%20para%20${encodeURIComponent(jobTitle)}%20-%20${encodeURIComponent(candidateName)}&body=Por%20favor,%20anexe%20este%20PDF%20ao%20seu%20email.%0A%0AAtenciosamente,%0A${encodeURIComponent(candidateName)}`;

            // Adicionar instruções e link clicável (sublinhado)
            doc.setTextColor(0, 0, 255);
            doc.textWithLink('Clique aqui para enviar por email: shi@sendflow.com.br (cópia para luiz@sendflow.pro)', 
                           marginLeft, 285, 
                           { url: emailLink, maxWidth: maxWidth });
            doc.setTextColor(100, 100, 100);
            
            doc.text('* Importante: Anexe o arquivo PDF ao enviar o email', marginLeft, 290);
            doc.text('Criado em: ' + getFormattedDateTime(), marginLeft, 295, { align: 'left' });
            
            return doc;
        }
        
        // Função para criar corpo do e-mail
        function createEmailBody() {
            const candidateName = document.getElementById('candidateName').value;
            const candidatePhone = document.getElementById('candidatePhone').value;
            const candidateEmail = document.getElementById('candidateEmail').value;
            const jobTitle = document.getElementById('jobTitle').value;
            const jobCode = document.getElementById('jobCode').value;
            
            let emailBody = `FORMULÁRIO DE QUESTÕES UNNICHAT-SENDFLOW\n\n`;
            emailBody += `Enviado em: ${getFormattedDateTime()}\n\n`;
            emailBody += `INFORMAÇÕES DO CANDIDATO\n`;
            emailBody += `• Nome: ${candidateName}\n`;
            emailBody += `• Telefone: ${candidatePhone}\n`;
            emailBody += `• E-mail: ${candidateEmail}\n`;
            emailBody += `• Vaga Pretendida: ${jobTitle}\n`;
            if (jobCode) emailBody += `• Código da Vaga: ${jobCode}\n`;
            emailBody += `\n`;
            
            // Adicionar respostas das partes
            const parts = [
                { 
                    title: 'PARTE 1 - COMPORTAMENTAL',
                    questions: [
                        { id: 'p1a', text: 'a. Um cliente trouxe uma dúvida que você não tem certeza absoluta da resposta. Qual sua conduta?' },
                        { id: 'p1b', text: 'b. Cliente pede que você execute uma ação para ele no sistema. O que faz?' },
                        { id: 'p1c', text: 'c. Surgiu um problema que aparenta ser um bug e você não sabe contornar. O que faz?' },
                        { id: 'p1d', text: 'd. Cliente acabou de assinar a ferramenta. Qual sua conduta inicial?' },
                        { id: 'p1e1', text: '1. Roteiro para Dúvida operacional:' },
                        { id: 'p1e2', text: '2. Roteiro para Suporte técnico:' }
                    ]
                },
                {
                    title: 'PARTE 2 - CONHECIMENTO DO PRODUTO',
                    questions: [
                        { id: 'p2a', text: 'a. Onde conectar uma nova conta de API OFICIAL?' },
                        { id: 'p2b', text: 'b. Onde efetuar disparos em massa?' },
                        { id: 'p2c', text: 'c. Onde adicionar acessos de equipe?' },
                        { id: 'p2d', text: 'd. É possível segmentar e organizar os leads?' },
                        { id: 'p2e', text: 'e. Onde entender mais sobre o Unnichat?' },
                        { id: 'p2f', text: 'f. Quais funcionalidades você identifica?' }
                    ]
                },
                {
                    title: 'PARTE 3 - CONHECIMENTOS ESPECÍFICOS',
                    questions: [
                        { id: 'p3a', text: 'a. O que é API Oficial do WhatsApp?' },
                        { id: 'p3b', text: 'b. Custo médio de envio da API?' },
                        { id: 'p3c', text: 'c. Qualquer pessoa pode ter conta API?' },
                        { id: 'p3d', text: 'd. Sua experiência com API Oficial:' }
                    ]
                }
            ];
            
            parts.forEach(part => {
                emailBody += `${part.title}\n\n`;
                
                part.questions.forEach(question => {
                    const answer = document.getElementById(question.id).value;
                    emailBody += `${question.text}\n${answer}\n\n`;
                });
            });
            
            emailBody += `\nBoa tarde, segue formulário preenchido!`;
            
            return emailBody;
        }
        
        // Evento de envio por e-mail
        document.getElementById('sendEmail').addEventListener('click', function() {
            if (!validateForm()) return;
            
            // Criar PDF
            const doc = createPDF();
            const pdfBlob = doc.output('blob');
            const pdfUrl = URL.createObjectURL(pdfBlob);
            window.open(pdfUrl, '_blank');
            
            // Criar e abrir cliente de e-mail
            const candidateName = document.getElementById('candidateName').value;
            const jobTitle = document.getElementById('jobTitle').value;
            const emailBody = createEmailBody();
            
            window.location.href = `mailto:shi@sendflow.com.br?cc=luiz@sendflow.pro&subject=Candidatura%20para%20${encodeURIComponent(jobTitle)}%20-%20${encodeURIComponent(candidateName)}&body=${encodeURIComponent(emailBody)}%0A%0APor%20favor,%20anexe%20o%20PDF%20gerado.`;
            
            // Mostrar modal de confirmação
            showModal();
            
            // Limpar formulário após 1 segundo
            setTimeout(clearForm, 1000);
        });
    </script>
</body>
</html>
