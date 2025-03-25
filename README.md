<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teste Unnichat - Formulário de Respostas</title>
    <style>
        :root {
            --primary-color: #25D366;
            --secondary-color: #128C7E;
            --text-color: #333;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #757575;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--light-gray);
            padding: 20px;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
        }
        
        .header-image {
            width: 100%;
            max-height: 150px;
            object-fit: contain;
            margin-bottom: 20px;
            border-radius: 8px;
        }
        
        .screen-image {
            width: 100%;
            max-width: 800px;
            margin: 15px auto;
            display: block;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--medium-gray);
        }
        
        h1 {
            color: var(--secondary-color);
            margin-bottom: 10px;
        }
        
        h2 {
            color: var(--secondary-color);
            margin: 25px 0 15px;
            padding-bottom: 5px;
            border-bottom: 2px solid var(--medium-gray);
        }
        
        h3 {
            margin: 20px 0 10px;
            color: var(--secondary-color);
        }
        
        .intro-text {
            margin-bottom: 20px;
            font-size: 16px;
        }
        
        .part {
            margin-bottom: 30px;
            padding: 20px;
            background-color: var(--light-gray);
            border-radius: 8px;
        }
        
        .question {
            margin-bottom: 20px;
        }
        
        .question label {
            display: block;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        .question textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid var(--medium-gray);
            border-radius: 5px;
            min-height: 100px;
            resize: vertical;
            font-size: 15px;
        }
        
        .question textarea:focus {
            outline: none;
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 2px rgba(18, 140, 126, 0.2);
        }
        
        .buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        button {
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            font-size: 16px;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 200px;
        }
        
        .btn-email {
            background-color: var(--secondary-color);
            color: white;
        }
        
        .btn-whatsapp {
            background-color: var(--primary-color);
            color: white;
        }
        
        button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }
        
        .emoji {
            font-size: 1.2em;
            margin-right: 5px;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            
            .part {
                padding: 15px;
            }
            
            button {
                width: 100%;
            }
        }
        
        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            
            .container {
                padding: 15px;
            }
            
            h1 {
                font-size: 24px;
            }
            
            h2 {
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Cabeçalho com imagem do painel -->
        <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.14.04.png" alt="Painel Unnichat" class="header-image">
        
        <header>
            <h1><span class="emoji">🥳</span> Teste Unnichat - Formulário de Respostas</h1>
            <p class="intro-text">Olá, se você chegou até aqui é porque possui as atribuições necessárias para fazer parte da Equipe Unnichat! Então, parabéns!</p>
            <p class="intro-text">Essa etapa é composta por algumas perguntas e um teste prático criado para avaliar suas habilidades e abordagens.</p>
            <p class="intro-text">O teste será avaliado com confidencialidade, e suas soluções não serão usadas para fins comerciais.</p>
        </header>

        <form id="unnichatForm">
            <div class="part">
                <h2>PARTE 1</h2>
                <p>Considere o seguinte cenário: Você presta suporte para uma ferramenta de automação de WhatsApp.</p>
                
                <div class="question">
                    <label for="p1a">a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?</label>
                    <textarea id="p1a" name="p1a" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p1b">b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?</label>
                    <textarea id="p1b" name="p1b" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p1c">c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?</label>
                    <textarea id="p1c" name="p1c" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p1d">d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?</label>
                    <textarea id="p1d" name="p1d" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p1e1">e1. Monte um Roteiro de atendimento para Dúvida operacional da ferramenta</label>
                    <textarea id="p1e1" name="p1e1" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p1e2">e2. Monte um Roteiro de atendimento para Suporte técnico</label>
                    <textarea id="p1e2" name="p1e2" required></textarea>
                </div>
            </div>
            
            <div class="part">
                <h2>PARTE 2</h2>
                <p>Observe essa tela:</p>
                
                <!-- Imagem da tela centralizada -->
                <img src="https://gabriellemoreira.com.br/wp-content/uploads/2025/03/Captura-de-Tela-2025-03-24-as-23.10.17.png" alt="Tela do Unnichat" class="screen-image">
                
                <div class="question">
                    <label for="p2a">a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?</label>
                    <textarea id="p2a" name="p2a" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p2b">b. Onde o cliente aperta para efetuar disparos em massa para os clientes?</label>
                    <textarea id="p2b" name="p2b" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p2c">c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?</label>
                    <textarea id="p2c" name="p2c" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p2d">d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?</label>
                    <textarea id="p2d" name="p2d" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p2e">e. Onde você iria para entender mais sobre o Unnichat?</label>
                    <textarea id="p2e" name="p2e" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p2f">f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?</label>
                    <textarea id="p2f" name="p2f" required></textarea>
                </div>
            </div>
            
            <div class="part">
                <h2>PARTE 3 - Conhecimentos Específicos</h2>
                <p>Agora, teremos perguntas nichadas. Se você não souber a resposta, não se preocupe, não é uma etapa eliminatória (mas você pode tentar responder também).</p>
                
                <div class="question">
                    <label for="p3a">a. O que é API Oficial do WhatsApp?</label>
                    <textarea id="p3a" name="p3a" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p3b">b. Qual o custo médio de envio da API?</label>
                    <textarea id="p3b" name="p3b" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p3c">c. Qualquer pessoa pode ter uma conta API Oficial?</label>
                    <textarea id="p3c" name="p3c" required></textarea>
                </div>
                
                <div class="question">
                    <label for="p3d">d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.</label>
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

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
    <script>
        // Inicializar jsPDF
        const { jsPDF } = window.jspdf;
        
        document.getElementById('sendEmail').addEventListener('click', function() {
            // Validar formulário
            const form = document.getElementById('unnichatForm');
            const allTextareas = form.querySelectorAll('textarea');
            let isValid = true;
            
            allTextareas.forEach(textarea => {
                if (!textarea.value.trim()) {
                    isValid = false;
                    textarea.style.borderColor = 'red';
                } else {
                    textarea.style.borderColor = '';
                }
            });
            
            if (!isValid) {
                alert('Por favor, responda todas as perguntas antes de enviar.');
                return;
            }
            
            // Criar PDF
            const doc = new jsPDF();
            let yPosition = 20;
            
            // Adicionar cabeçalho
            doc.setFontSize(18);
            doc.setTextColor(18, 140, 126);
            doc.text('Respostas do Teste Unnichat', 105, yPosition, { align: 'center' });
            yPosition += 15;
            
            doc.setFontSize(12);
            doc.setTextColor(0, 0, 0);
            doc.text('Data: ' + new Date().toLocaleDateString(), 105, yPosition, { align: 'center' });
            yPosition += 20;
            
            // Adicionar respostas
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            doc.text('PARTE 1', 14, yPosition);
            yPosition += 10;
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            // Parte 1
            const p1a = document.getElementById('p1a').value;
            doc.text('a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p1a, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p1a, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p1b = document.getElementById('p1b').value;
            doc.text('b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p1b, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p1b, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p1c = document.getElementById('p1c').value;
            doc.text('c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p1c, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p1c, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p1d = document.getElementById('p1d').value;
            doc.text('d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p1d, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p1d, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p1e1 = document.getElementById('p1e1').value;
            doc.text('e1. Monte um Roteiro de atendimento para Dúvida operacional da ferramenta', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p1e1, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p1e1, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p1e2 = document.getElementById('p1e2').value;
            doc.text('e2. Monte um Roteiro de atendimento para Suporte técnico', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p1e2, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p1e2, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            // Adicionar nova página se necessário
            if (yPosition > 250) {
                doc.addPage();
                yPosition = 20;
            }
            
            // Parte 2
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            doc.text('PARTE 2', 14, yPosition);
            yPosition += 10;
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            const p2a = document.getElementById('p2a').value;
            doc.text('a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p2a, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p2a, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p2b = document.getElementById('p2b').value;
            doc.text('b. Onde o cliente aperta para efetuar disparos em massa para os clientes?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p2b, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p2b, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p2c = document.getElementById('p2c').value;
            doc.text('c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p2c, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p2c, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p2d = document.getElementById('p2d').value;
            doc.text('d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p2d, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p2d, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p2e = document.getElementById('p2e').value;
            doc.text('e. Onde você iria para entender mais sobre o Unnichat?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p2e, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p2e, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p2f = document.getElementById('p2f').value;
            doc.text('f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p2f, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p2f, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            // Adicionar nova página se necessário
            if (yPosition > 250) {
                doc.addPage();
                yPosition = 20;
            }
            
            // Parte 3
            doc.setFontSize(14);
            doc.setTextColor(18, 140, 126);
            doc.text('PARTE 3 - Conhecimentos Específicos', 14, yPosition);
            yPosition += 10;
            
            doc.setFontSize(11);
            doc.setTextColor(0, 0, 0);
            
            const p3a = document.getElementById('p3a').value;
            doc.text('a. O que é API Oficial do WhatsApp?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p3a, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p3a, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p3b = document.getElementById('p3b').value;
            doc.text('b. Qual o custo médio de envio da API?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p3b, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p3b, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p3c = document.getElementById('p3c').value;
            doc.text('c. Qualquer pessoa pode ter uma conta API Oficial?', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p3c, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p3c, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            const p3d = document.getElementById('p3d').value;
            doc.text('d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.', 14, yPosition);
            yPosition += 7;
            doc.setTextColor(0, 0, 255);
            doc.text(p3d, 20, yPosition, { maxWidth: 170 });
            yPosition += doc.getTextDimensions(p3d, { maxWidth: 170 }).h + 10;
            doc.setTextColor(0, 0, 0);
            
            // Salvar PDF
            const pdfBlob = doc.output('blob');
            const pdfUrl = URL.createObjectURL(pdfBlob);
            
            // Criar corpo do e-mail
            let emailBody = "Olá,\n\nSegue em anexo as respostas do teste Unnichat.\n\n";
            emailBody += "Atenciosamente,\n[Seu Nome]";
            
            // Abrir cliente de e-mail
            window.location.href = `mailto:shi@sendflow.com.br?cc=luiz@sendflow.pro&subject=Respostas do Teste Unnichat&body=${encodeURIComponent(emailBody)}&attachment=${encodeURIComponent(pdfUrl)}`;
        });
        
        document.getElementById('sendWhatsApp').addEventListener('click', function() {
            // Validar formulário
            const form = document.getElementById('unnichatForm');
            const allTextareas = form.querySelectorAll('textarea');
            let isValid = true;
            
            allTextareas.forEach(textarea => {
                if (!textarea.value.trim()) {
                    isValid = false;
                    textarea.style.borderColor = 'red';
                } else {
                    textarea.style.borderColor = '';
                }
            });
            
            if (!isValid) {
                alert('Por favor, responda todas as perguntas antes de enviar.');
                return;
            }
            
            // Criar mensagem para WhatsApp
            let whatsappMessage = "*RESPOSTAS DO TESTE UNNICHAT*\n\n";
            whatsappMessage += "*Data:* " + new Date().toLocaleDateString() + "\n\n";
            
            // Parte 1
            whatsappMessage += "*PARTE 1*\n\n";
            whatsappMessage += "*a. Um cliente trouxe a você uma dúvida a qual você não tem certeza absoluta da resposta. Qual é a sua conduta nesse caso?*\n";
            whatsappMessage += document.getElementById('p1a').value + "\n\n";
            
            whatsappMessage += "*b. O cliente pede que você execute uma ação para ele no sistema. O que você faz?*\n";
            whatsappMessage += document.getElementById('p1b').value + "\n\n";
            
            whatsappMessage += "*c. Surgiu um problema na ferramenta que aparenta ser um bug de sistema e você ainda não aprendeu a como contornar essa situação. O que você faz?*\n";
            whatsappMessage += document.getElementById('p1c').value + "\n\n";
            
            whatsappMessage += "*d. O Cliente acabou de assinar a ferramenta. Qual a sua conduta inicial?*\n";
            whatsappMessage += document.getElementById('p1d').value + "\n\n";
            
            whatsappMessage += "*e1. Monte um Roteiro de atendimento para Dúvida operacional da ferramenta*\n";
            whatsappMessage += document.getElementById('p1e1').value + "\n\n";
            
            whatsappMessage += "*e2. Monte um Roteiro de atendimento para Suporte técnico*\n";
            whatsappMessage += document.getElementById('p1e2').value + "\n\n";
            
            // Parte 2
            whatsappMessage += "*PARTE 2*\n\n";
            whatsappMessage += "*a. Onde o cliente aperta para conectar uma nova conta de API OFICIAL?*\n";
            whatsappMessage += document.getElementById('p2a').value + "\n\n";
            
            whatsappMessage += "*b. Onde o cliente aperta para efetuar disparos em massa para os clientes?*\n";
            whatsappMessage += document.getElementById('p2b').value + "\n\n";
            
            whatsappMessage += "*c. O cliente deseja adicionar acessos de equipe em sua conta. Onde ele deve clicar?*\n";
            whatsappMessage += document.getElementById('p2c').value + "\n\n";
            
            whatsappMessage += "*d. O Cliente pergunta se é possível segmentar e organizar os leads para atendimento. O que você responderia?*\n";
            whatsappMessage += document.getElementById('p2d').value + "\n\n";
            
            whatsappMessage += "*e. Onde você iria para entender mais sobre o Unnichat?*\n";
            whatsappMessage += document.getElementById('p2e').value + "\n\n";
            
            whatsappMessage += "*f. Ao analisar essa tela, quais funcionalidades você imagina que o Unnichat tem?*\n";
            whatsappMessage += document.getElementById('p2f').value + "\n\n";
            
            // Parte 3
            whatsappMessage += "*PARTE 3 - Conhecimentos Específicos*\n\n";
            whatsappMessage += "*a. O que é API Oficial do WhatsApp?*\n";
            whatsappMessage += document.getElementById('p3a').value + "\n\n";
            
            whatsappMessage += "*b. Qual o custo médio de envio da API?*\n";
            whatsappMessage += document.getElementById('p3b').value + "\n\n";
            
            whatsappMessage += "*c. Qualquer pessoa pode ter uma conta API Oficial?*\n";
            whatsappMessage += document.getElementById('p3c').value + "\n\n";
            
            whatsappMessage += "*d. Conte um pouco sobre sua experiência com API Oficial de WhatsApp.*\n";
            whatsappMessage += document.getElementById('p3d').value + "\n\n";
            
            // Codificar mensagem para URL
            const encodedMessage = encodeURIComponent(whatsappMessage);
            
            // Abrir WhatsApp com a mensagem
            window.open(`https://wa.me/5511996504486?text=${encodedMessage}`, '_blank');
        });
    </script>
</body>
</html>
