<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="HandheldFriendly" content="true">
    <meta name="MobileOptimized" content="width">
    <meta name="theme-color" content="#128C7E">
    <meta name="format-detection" content="telephone=no">
    <title>Formulário de Candidatura Unnichat</title>
    <style>
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
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, 
                         Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
            line-height: 1.5;
            color: var(--text-color);
            background-color: var(--light-gray);
            padding: 0;
            margin: 0;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            text-rendering: optimizeLegibility;
        }
        
        .container {
            width: 100%;
            max-width: 100%;
            min-height: 100vh;
            padding: 0;
            margin: 0 auto;
            background: var(--white);
            overflow-x: hidden;
        }
        
        .content-wrapper {
            padding: 12px;
            max-width: 900px;
            margin: 0 auto;
        }
        
        .logo {
            max-height: 60px;
            width: auto;
            height: auto;
            margin: 12px auto;
            display: block;
        }
        
        header {
            text-align: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid var(--medium-gray);
        }
        
        h1 {
            color: var(--secondary-color);
            margin: 10px 0;
            font-size: clamp(1.4rem, 5vw, 1.8rem);
            font-weight: 600;
            line-height: 1.3;
        }
        
        h2 {
            color: var(--secondary-color);
            margin: 20px 0 12px;
            padding-bottom: 5px;
            border-bottom: 2px solid var(--medium-gray);
            font-size: clamp(1.2rem, 4vw, 1.5rem);
            font-weight: 600;
        }
        
        h3 {
            margin: 15px 0 8px;
            color: var(--secondary-color);
            font-size: clamp(1.1rem, 3.5vw, 1.3rem);
        }
        
        .intro-text {
            margin-bottom: 15px;
            font-size: clamp(0.9rem, 3vw, 1rem);
            line-height: 1.5;
            color: var(--dark-gray);
        }
        
        .part {
            margin-bottom: 20px;
            padding: 15px;
            background-color: var(--light-gray);
            border-radius: 8px;
        }
        
        .question {
            margin-bottom: 15px;
        }
        
        .question label {
            display: block;
            font-weight: 500;
            margin-bottom: 6px;
            font-size: clamp(0.9rem, 3vw, 1rem);
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
            padding: 12px;
            border: 1px solid var(--medium-gray);
            border-radius: 6px;
            font-size: clamp(0.9rem, 3vw, 1rem);
            background-color: var(--white);
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
            transition: border-color 0.3s ease;
        }
        
        .question textarea {
            min-height: 100px;
            resize: vertical;
        }
        
        .question input:focus,
        .question textarea:focus {
            outline: none;
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 2px rgba(18, 140, 126, 0.2);
        }
        
        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 12px;
        }
        
        .form-group {
            flex: 1 1 100%;
            min-width: 0;
        }
        
        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 25px;
        }
        
        button {
            flex: 1 1 100%;
            padding: 14px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: clamp(0.95rem, 3vw, 1.05rem);
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            -webkit-tap-highlight-color: transparent;
        }
        
        .btn-email {
            background-color: var(--secondary-color);
            color: var(--white);
        }
        
        .btn-whatsapp {
            background-color: var(--primary-color);
            color: var(--white);
        }
        
        button:active, button:focus {
            opacity: 0.9;
            transform: translateY(1px);
        }
        
        .emoji {
            font-size: 1.1em;
            margin-right: 5px;
        }
        
        .candidate-info {
            background-color: #f0f8ff;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        
        .screen-image {
            width: 100%;
            max-width: 100%;
            margin: 10px auto;
            display: block;
            border-radius: 8px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }
        
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
            padding: 25px;
            border-radius: 10px;
            width: 100%;
            max-width: 400px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .modal-content p {
            margin-bottom: 20px;
            font-size: clamp(1rem, 3vw, 1.1rem);
            line-height: 1.5;
        }
        
        .modal-close {
            background-color: var(--secondary-color);
            color: var(--white);
            border: none;
            padding: 10px 20px;
            border-radius: 6px;
            font-weight: 500;
            cursor: pointer;
            font-size: clamp(0.95rem, 3vw, 1.05rem);
        }
        
        @media (max-width: 360px) {
            .content-wrapper {
                padding: 10px;
            }
            
            .part {
                padding: 12px;
            }
            
            .question input,
            .question textarea {
                padding: 10px;
            }
        }
        
        @media (min-width: 600px) {
            .content-wrapper {
                padding: 20px;
            }
            
            .form-group {
                flex: 1 1 calc(50% - 12px);
            }
            
            button {
                flex: 1 1 calc(50% - 12px);
            }
        }
        
        @supports (-webkit-touch-callout: none) {
            input, textarea {
                font-size: 16px !important;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="content-wrapper">
            <!-- Logotipo da empresa -->
            <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.14.04.png" alt="Unnichat Logo" class="logo">
            
            <header>
                <h1><span class="emoji">📝</span> Formulário de Candidatura</h1>
                <p class="intro-text">Preencha o formulário abaixo para conhecermos melhor seu perfil e suas habilidades. Todos os campos são obrigatórios, exceto quando indicado.</p>
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
                            <input type="tel" id="candidatePhone" name="candidatePhone" pattern="[0-9]{2}-[0-9]{5}-[0-9]{4}" required placeholder="Formato: 00-00000-0000">
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group question">
                            <label for="candidateEmail" class="required-field">E-mail:</label>
                            <input type="email" id="candidateEmail" name="candidateEmail" required placeholder="Digite seu e-mail">
                        </div>
                        
                        <div class="form-group question">
                            <label for="jobTitle" class="required-field">Nome da vaga pretendida:</label>
                            <input type="text" id="jobTitle" name="jobTitle" maxlength="30" required placeholder="Digite o nome da vaga (máx. 30 caracteres)">
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-group question">
                            <label for="jobCode">Código da Vaga (opcional):</label>
                            <input type="text" id="jobCode" name="jobCode" placeholder="Digite o código da vaga, se houver">
                        </div>
                    </div>
                </div>

                <div class="part">
                    <h2>PARTE 1 - Comportamental</h2>
                    <p>Considere o seguinte cenário: Você presta suporte para uma ferramenta de automação de WhatsApp.</p>
                    
                    <div class="question">
                        <label for="p1a" class="required-field">a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?</label>
                        <textarea id="p1a" name="p1a" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p1b" class="required-field">b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?</label>
                        <textarea id="p1b" name="p1b" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p1c" class="required-field">c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?</label>
                        <textarea id="p1c" name="p1c" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p1d" class="required-field">d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?</label>
                        <textarea id="p1d" name="p1d" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p1e1" class="required-field">1. Monte um Roteiro de atendimento para Dúvida operacional da ferramenta</label>
                        <textarea id="p1e1" name="p1e1" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p1e2" class="required-field">2. Monte um Roteiro de atendimento para Suporte técnico</label>
                        <textarea id="p1e2" name="p1e2" required></textarea>
                    </div>
                </div>
                
                <div class="part">
                    <h2>PARTE 2 - Conhecimento do Produto</h2>
                    <p>Observe essa tela:</p>
                    
                    <!-- Imagem da tela centralizada -->
                    <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.10.17.png" alt="Tela do Unnichat" class="screen-image">
                    
                    <div class="question">
                        <label for="p2a" class="required-field">a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?</label>
                        <textarea id="p2a" name="p2a" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p2b" class="required-field">b. Onde o cliente aperta para efetuar disparos em massa para os clientes?</label>
                        <textarea id="p2b" name="p2b" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p2c" class="required-field">c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?</label>
                        <textarea id="p2c" name="p2c" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p2d" class="required-field">d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?</label>
                        <textarea id="p2d" name="p2d" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p2e" class="required-field">e. Onde você iria para entender mais sobre o Unnichat?</label>
                        <textarea id="p2e" name="p2e" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p2f" class="required-field">f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?</label>
                        <textarea id="p2f" name="p2f" required></textarea>
                    </div>
                </div>
                
                <div class="part">
                    <h2>PARTE 3 - Conhecimentos Específicos</h2>
                    <p>Agora, teremos perguntas nichadas. Se você não souber a resposta, não se preocupe, não é uma etapa eliminatória (mas você pode tentar responder também).</p>
                    
                    <div class="question">
                        <label for="p3a" class="required-field">a. O que é API Oficial do WhatsApp?</label>
                        <textarea id="p3a" name="p3a" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p3b" class="required-field">b. Qual o custo médio de envio da API?</label>
                        <textarea id="p3b" name="p3b" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p3c" class="required-field">c. Qualquer pessoa pode ter uma conta API Oficial?</label>
                        <textarea id="p3c" name="p3c" required></textarea>
                    </div>
                    
                    <div class="question">
                        <label for="p3d" class="required-field">d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.</label>
                        <textarea id="p3d" name="p3d" required></textarea>
                    </div>
                </div>
                
                <div class="buttons">
                    <button type="button" class="btn-email" id="sendEmail">
                        <span class="emoji">📧</span> Enviar por E-mail
                    </button>
                    <button type="button" class="btn-whatsapp" id="sendWhatsApp">
                        <span class="emoji">💬</span> Enviar por WhatsApp
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal de confirmação -->
    <div id="confirmationModal" class="modal">
        <div class="modal-content">
            <p>Suas respostas foram enviadas com sucesso!</p>
            <p>Aguarde o nosso retorno o mais breve possível, Unnichat SendFlow, agradece, obrigado!</p>
            <button class="modal-close" onclick="closeModal()">OK</button>
        </div>
    </div>

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
        
        // Função para limpar o formulário
        function clearForm() {
            document.getElementById('candidateForm').reset();
        }
        
        // Função para formatar data e hora
        function getFormattedDateTime() {
            const now = new Date();
            const date = now.toLocaleDateString('pt-BR');
            const time = now.toLocaleTimeString('pt-BR');
            return `${date} às ${time}`;
        }
        
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
        
        document.getElementById('sendEmail').addEventListener('click', function() {
            // Validar formulário
            const form = document.getElementById('candidateForm');
            const requiredFields = form.querySelectorAll('[required]');
            let isValid = true;
            
            requiredFields.forEach(field => {
                if (!field.value.trim()) {
                    isValid = false;
                    field.style.borderColor = 'red';
                } else {
                    field.style.borderColor = '';
                }
            });
            
            // Validar formato do telefone
            const phoneField = document.getElementById('candidatePhone');
            const phoneRegex = /^\d{2}-\d{5}-\d{4}$/;
            if (!phoneRegex.test(phoneField.value)) {
                isValid = false;
                phoneField.style.borderColor = 'red';
                alert('Por favor, insira um telefone no formato 00-00000-0000');
            }
            
            // Validar e-mail
            const emailField = document.getElementById('candidateEmail');
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(emailField.value)) {
                isValid = false;
                emailField.style.borderColor = 'red';
                alert('Por favor, insira um e-mail válido');
            }
            
            if (!isValid) {
                alert('Por favor, preencha todos os campos obrigatórios corretamente antes de enviar.');
                return;
            }
            
            // Criar PDF
            const doc = new jsPDF();
            
            // Configurações de margem
            const marginLeft = 15;
            const marginRight = 15;
            const maxWidth = 180; // Largura máxima do texto (210 - margens)
            
            let yPosition = 30;
            
            // Adicionar cabeçalho com logo
            try {
                const logoImg = new Image();
                logoImg.src = 'https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.14.04.png';
                doc.addImage(logoImg, 'PNG', marginLeft, 10, 40, 20);
            } catch (e) {
                console.log('Erro ao carregar logo:', e);
            }
            
            doc.setFontSize(18);
            doc.setTextColor(18, 140, 126);
            doc.text('Formulário de Candidatura Unnichat', 105, yPosition, { align: 'center' });
            yPosition += 15;
            
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
            
            const candidateName = document.getElementById('candidateName').value;
            doc.text('Nome: ' + candidateName, marginLeft, yPosition);
            yPosition += 7;
            
            const candidatePhone = document.getElementById('candidatePhone').value;
            doc.text('Telefone: ' + candidatePhone, marginLeft, yPosition);
            yPosition += 7;
            
            const candidateEmail = document.getElementById('candidateEmail').value;
            doc.text('E-mail: ' + candidateEmail, marginLeft, yPosition);
            yPosition += 7;
            
            const jobTitle = document.getElementById('jobTitle').value;
            doc.text('Vaga Pretendida: ' + jobTitle, marginLeft, yPosition);
            yPosition += 7;
            
            const jobCode = document.getElementById('jobCode').value;
            if (jobCode) {
                doc.text('Código da Vaga: ' + jobCode, marginLeft, yPosition);
                yPosition += 7;
            }
            
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
            
            // Adicionar respostas
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            yPosition = addTextWithBreaks('PARTE 1 - COMPORTAMENTAL', marginLeft, yPosition, maxWidth, 10);
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            // Parte 1
            const p1a = document.getElementById('p1a').value;
            yPosition = addTextWithBreaks('a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p1a, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p1b = document.getElementById('p1b').value;
            yPosition = addTextWithBreaks('b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p1b, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p1c = document.getElementById('p1c').value;
            yPosition = addTextWithBreaks('c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p1c, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p1d = document.getElementById('p1d').value;
            yPosition = addTextWithBreaks('d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p1d, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p1e1 = document.getElementById('p1e1').value;
            yPosition = addTextWithBreaks('1. Monte um Roteiro de atendimento para Dúvida operacional da ferramenta', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p1e1, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p1e2 = document.getElementById('p1e2').value;
            yPosition = addTextWithBreaks('2. Monte um Roteiro de atendimento para Suporte técnico', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p1e2, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 10;
            
            // Parte 2
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            yPosition = addTextWithBreaks('PARTE 2 - CONHECIMENTO DO PRODUTO', marginLeft, yPosition, maxWidth, 10);
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            const p2a = document.getElementById('p2a').value;
            yPosition = addTextWithBreaks('a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p2a, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p2b = document.getElementById('p2b').value;
            yPosition = addTextWithBreaks('b. Onde o cliente aperta para efetuar disparos em massa para os clientes?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p2b, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p2c = document.getElementById('p2c').value;
            yPosition = addTextWithBreaks('c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p2c, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p2d = document.getElementById('p2d').value;
            yPosition = addTextWithBreaks('d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p2d, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p2e = document.getElementById('p2e').value;
            yPosition = addTextWithBreaks('e. Onde você iria para entender mais sobre o Unnichat?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p2e, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p2f = document.getElementById('p2f').value;
            yPosition = addTextWithBreaks('f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p2f, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 10;
            
            // Parte 3
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            yPosition = addTextWithBreaks('PARTE 3 - CONHECIMENTOS ESPECÍFICOS', marginLeft, yPosition, maxWidth, 10);
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            const p3a = document.getElementById('p3a').value;
            yPosition = addTextWithBreaks('a. O que é API Oficial do WhatsApp?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p3a, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p3b = document.getElementById('p3b').value;
            yPosition = addTextWithBreaks('b. Qual o custo médio de envio da API?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p3b, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p3c = document.getElementById('p3c').value;
            yPosition = addTextWithBreaks('c. Qualquer pessoa pode ter uma conta API Oficial?', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p3c, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            yPosition += 5;
            
            const p3d = document.getElementById('p3d').value;
            yPosition = addTextWithBreaks('d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.', marginLeft, yPosition, maxWidth, 7);
            doc.setTextColor(0, 0, 255);
            yPosition = addTextWithBreaks(p3d, marginLeft + 5, yPosition, maxWidth - 5, 7);
            doc.setTextColor(0, 0, 0);
            
            // Adicionar rodapé com data e hora
            doc.setFontSize(10);
            doc.setTextColor(100, 100, 100);
            doc.text('Enviado em: ' + getFormattedDateTime(), marginLeft, 290, { align: 'left' });
            
            // Salvar PDF em nova aba
            const pdfBlob = doc.output('blob');
            const pdfUrl = URL.createObjectURL(pdfBlob);
            window.open(pdfUrl, '_blank');
            
            // Criar corpo do e-mail
            let emailBody = `Formulário de Candidatura Unnichat\n\n`;
            emailBody += `Enviado em: ${getFormattedDateTime()}\n\n`;
            emailBody += `Candidato: ${candidateName}\n`;
            emailBody += `Telefone: ${candidatePhone}\n`;
            emailBody += `E-mail: ${candidateEmail}\n`;
            emailBody += `Vaga Pretendida: ${jobTitle}\n`;
            if (jobCode) emailBody += `Código da Vaga: ${jobCode}\n\n`;
            
            emailBody += `\nPARTE 1 - COMPORTAMENTAL\n\n`;
            emailBody += `a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?\n${p1a}\n\n`;
            emailBody += `b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?\n${p1b}\n\n`;
            emailBody += `c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?\n${p1c}\n\n`;
            emailBody += `d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?\n${p1d}\n\n`;
            emailBody += `1. Monte um Roteiro de atendimento para Dúvida operacional da ferramenta\n${p1e1}\n\n`;
            emailBody += `2. Monte um Roteiro de atendimento para Suporte técnico\n${p1e2}\n\n`;
            
            emailBody += `\nPARTE 2 - CONHECIMENTO DO PRODUTO\n\n`;
            emailBody += `a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?\n${p2a}\n\n`;
            emailBody += `b. Onde o cliente aperta para efetuar disparos em massa para os clientes?\n${p2b}\n\n`;
            emailBody += `c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?\n${p2c}\n\n`;
            emailBody += `d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?\n${p2d}\n\n`;
            emailBody += `e. Onde você iria para entender mais sobre o Unnichat?\n${p2e}\n\n`;
            emailBody += `f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?\n${p2f}\n\n`;
            
            emailBody += `\nPARTE 3 - CONHECIMENTOS ESPECÍFICOS\n\n`;
            emailBody += `a. O que é API Oficial do WhatsApp?\n${p3a}\n\n`;
            emailBody += `b. Qual o custo médio de envio da API?\n${p3b}\n\n`;
            emailBody += `c. Qualquer pessoa pode ter uma conta API Oficial?\n${p3c}\n\n`;
            emailBody += `d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.\n${p3d}\n\n`;
            
            emailBody += `\n\nUnnichat SendFlow agradece seu contato!`;
            
            // Abrir cliente de e-mail
            window.location.href = `mailto:shi@sendflow.com.br?cc=luiz@sendflow.pro&subject=Candidatura para ${jobTitle} - ${candidateName}&body=${encodeURIComponent(emailBody)}`;
            
            // Mostrar modal de confirmação
            showModal();
            
            // Limpar formulário após 1 segundo (para garantir que o envio foi concluído)
            setTimeout(clearForm, 1000);
        });
        
        document.getElementById('sendWhatsApp').addEventListener('click', function() {
            // Validar formulário
            const form = document.getElementById('candidateForm');
            const requiredFields = form.querySelectorAll('[required]');
            let isValid = true;
            
            requiredFields.forEach(field => {
                if (!field.value.trim()) {
                    isValid = false;
                    field.style.borderColor = 'red';
                } else {
                    field.style.borderColor = '';
                }
            });
            
            // Validar formato do telefone
            const phoneField = document.getElementById('candidatePhone');
            const phoneRegex = /^\d{2}-\d{5}-\d{4}$/;
            if (!phoneRegex.test(phoneField.value)) {
                isValid = false;
                phoneField.style.borderColor = 'red';
                alert('Por favor, insira um telefone no formato 00-00000-0000');
            }
            
            if (!isValid) {
                alert('Por favor, preencha todos os campos obrigatórios corretamente antes de enviar.');
                return;
            }
            
            // Obter valores dos campos
            const candidateName = document.getElementById('candidateName').value;
            const candidatePhone = document.getElementById('candidatePhone').value;
            const candidateEmail = document.getElementById('candidateEmail').value;
            const jobTitle = document.getElementById('jobTitle').value;
            const jobCode = document.getElementById('jobCode').value;
            
            const p1a = document.getElementById('p1a').value;
            const p1b = document.getElementById('p1b').value;
            const p1c = document.getElementById('p1c').value;
            const p1d = document.getElementById('p1d').value;
            const p1e1 = document.getElementById('p1e1').value;
            const p1e2 = document.getElementById('p1e2').value;
            
            const p2a = document.getElementById('p2a').value;
            const p2b = document.getElementById('p2b').value;
            const p2c = document.getElementById('p2c').value;
            const p2d = document.getElementById('p2d').value;
            const p2e = document.getElementById('p2e').value;
            const p2f = document.getElementById('p2f').value;
            
            const p3a = document.getElementById('p3a').value;
            const p3b = document.getElementById('p3b').value;
            const p3c = document.getElementById('p3c').value;
            const p3d = document.getElementById('p3d').value;
            
            // Criar mensagem para WhatsApp com formatação melhorada
            let whatsappMessage = `*FORMULÁRIO DE CANDIDATURA UNNICHAT*\n\n`;
            whatsappMessage += `*Enviado em:* ${getFormattedDateTime()}\n\n`;
            whatsappMessage += `*INFORMAÇÕES DO CANDIDATO*\n`;
            whatsappMessage += `• *Nome:* ${candidateName}\n`;
            whatsappMessage += `• *Telefone:* ${candidatePhone}\n`;
            whatsappMessage += `• *E-mail:* ${candidateEmail}\n`;
            whatsappMessage += `• *Vaga Pretendida:* ${jobTitle}\n`;
            if (jobCode) whatsappMessage += `• *Código da Vaga:* ${jobCode}\n`;
            whatsappMessage += `\n`;
            
            whatsappMessage += `*PARTE 1 - COMPORTAMENTAL*\n\n`;
            whatsappMessage += `*a. Um cliente trouxe uma dúvida que você não tem certeza absoluta da resposta. Qual sua conduta?*\n${p1a}\n\n`;
            whatsappMessage += `*b. Cliente pede que você execute uma ação para ele no sistema. O que faz?*\n${p1b}\n\n`;
            whatsappMessage += `*c. Surgiu um problema que aparenta ser um bug e você não sabe contornar. O que faz?*\n${p1c}\n\n`;
            whatsappMessage += `*d. Cliente acabou de assinar a ferramenta. Qual sua conduta inicial?*\n${p1d}\n\n`;
            whatsappMessage += `*1. Roteiro para Dúvida operacional:*\n${p1e1}\n\n`;
            whatsappMessage += `*2. Roteiro para Suporte técnico:*\n${p1e2}\n\n`;
            
            whatsappMessage += `*PARTE 2 - CONHECIMENTO DO PRODUTO*\n\n`;
            whatsappMessage += `*a. Onde conectar uma nova conta de API OFICIAL?*\n${p2a}\n\n`;
            whatsappMessage += `*b. Onde efetuar disparos em massa?*\n${p2b}\n\n`;
            whatsappMessage += `*c. Onde adicionar acessos de equipe?*\n${p2c}\n\n`;
            whatsappMessage += `*d. É possível segmentar e organizar os leads?*\n${p2d}\n\n`;
            whatsappMessage += `*e. Onde entender mais sobre o Unnichat?*\n${p2e}\n\n`;
            whatsappMessage += `*f. Quais funcionalidades você identifica?*\n${p2f}\n\n`;
            
            whatsappMessage += `*PARTE 3 - CONHECIMENTOS ESPECÍFICOS*\n\n`;
            whatsappMessage += `*a. O que é API Oficial do WhatsApp?*\n${p3a}\n\n`;
            whatsappMessage += `*b. Custo médio de envio da API?*\n${p3b}\n\n`;
            whatsappMessage += `*c. Qualquer pessoa pode ter conta API?*\n${p3c}\n\n`;
            whatsappMessage += `*d. Sua experiência com API Oficial:*\n${p3d}\n\n`;
            
            whatsappMessage += `\n*Unnichat SendFlow agradece seu contato!*`;
            
            // Codificar mensagem para URL
            const encodedMessage = encodeURIComponent(whatsappMessage);
            
            // Abrir WhatsApp com a mensagem
            window.open(`https://wa.me/5511996504486?text=${encodedMessage}`, '_blank');
            
            // Mostrar modal de confirmação
            showModal();
            
            // Limpar formulário após 1 segundo (para garantir que o envio foi concluído)
            setTimeout(clearForm, 1000);
        });
    </script>
</body>
</html>
