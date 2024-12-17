# Teste Ikigai 🌟

Este é um projeto para o **Teste Ikigai**, desenvolvido para ajudar você a identificar o seu propósito de vida.

---

## 🔧 Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- Biblioteca jsPDF

---

## 🚀 Código-Fonte

### HTML (`index.html`)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teste Ikigai</title>
    <style>
         /* Estilos globais */
         body {
            font-family: Arial, sans-serif;
            margin: 0px;
            padding: 0px;
            background-color: #fdfdfe;
            color: #000000;
        }

        .container {
            max-width: 900px;
            margin: 15px auto;
            padding: 15px;
            background: linear-gradient(90deg, #eceded, #ced1d8, #aeb6c4);
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(184, 163, 163, 0.1);
        }

        header {
            background-color: #e1d6d6;
            color: #de5252;
            padding: 15px 0;
            text-align: center;
        }

        h1 {
            background: linear-gradient(90deg, #edeef0, #c0cbe1, #839ac5);
            border: 5px solid #8d7fd5;
            border-radius: 30px;
            padding: 15px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            text-align: center;
            color: #100909;
        }
        h1:hover {
            background: linear-gradient(90deg, #88afb5, #9ec7d7, #26a5db);
            transform: scale(1.05);
        }
        p {
            background: linear-gradient(90deg, #edeef0, #c0cbe1, #839ac5);
            border: 5px solid #8d7fd5;
            border-radius: 30px;
            padding: 10px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            text-align: center;
            color: #100909;
        }
        p:hover {
            background: linear-gradient(90deg, #88afb5, #9ec7d7, #26a5db);
            transform: scale(1.05);
        }

        
         th, table td {
            border: 2px solid #e1d9d9;
            background: linear-gradient(90deg, #edeef0, #93afe6, #467cdf);
            padding: 10px;
            border-radius: 10px;
            text-align: center;
        }
        table th, table td:hover {
            background: linear-gradient(90deg, #88afb5, #9ec7d7, #26a5db);
            transform: scale(1.05);
          
        }
        /* Layout da lista de perguntas */
        .questions {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .question {
            background-color: #f7f7f7;
            border: 5px solid #8d7fd5;
            border-radius: 30px;
            padding: 15px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            text-align: center;
        }

        .question:hover {
            background: linear-gradient(90deg, #88afb5, #9ec7d7, #26a5db);
            transform: scale(1.05);
        }

        .question input[type="radio"] {
            display: none;
        }

        .question label {
            display: inline-block;
            margin-right: 15px;
            cursor: pointer;
            text-align: center;
        }

        .circle {
            width: 40px;
            height: 40px;
            border-radius: 100%;
            background-color: #9b59b6;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            transition: background-color 0.3s;
        }

        .circle:hover {
            background-color: #ffbb33
        }

.question input[type="radio"]:checked + label .circle {
    background-color: #18b63a;
    color: #fff;
}

/* Estilos de formulário */
form {
    display: flex;
    flex-direction: column;
    gap: 30px;
    text-align: center;
}

button {
    padding: 10px 20px;
    background: linear-gradient(90deg, #c2aea6, #bf4444, #ed410c);
    color: rgb(248, 241, 241);
    border: none;
    padding: 10px 20px; 
    border-radius: 15px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    transition: background-color 0.3s, transform 0.10s;
}

button:hover {
    background: linear-gradient(90deg, #bbc8b8, #82d755, #3deb11);
    transform: scale(1.1);
}


.error-message {
    color: rgb(234, 11, 11);
    margin-top: 10px;
}

/* Responsividade para dispositivos maiores */

@media (max-width: 320px) {
    h1 {
        font-size: 20px;
        text-align: center;
    }

    .container {
        padding: 10px;
    }

    .circle {
        width: 25px;
        height: 25px;
        font-size: 12px;
    }

    button {
        padding: 4px 10px;
        font-size: 14px;
    }

    table th, table td {
        font-size: 10px;
        padding: 2px;
    }
}
/* Responsividade para imagens */
img {
    max-width: 100%;
    height: auto;
}

/* Responsividade para navegação */
@media (max-width: 768px) {
    .navbar {
        flex-direction: column;
        align-items: center;
    }

    .navbar a {
        padding: 10px;
        font-size: 16px;
    }

    table-container {
        overflow-x: auto; /* Permite rolagem horizontal */
        -webkit-overflow-scrolling: touch; /* Suaviza a rolagem em dispositivos móveis */
    }

    table {
        display: block; /* Transforma a tabela em um elemento rolável */
        overflow-x: auto; /* Adiciona barra de rolagem horizontal */
    }


    table th, table td {
        font-size: 12px; /* Reduz o tamanho da fonte */
        padding: 5px; /* Ajusta o espaçamento */
        word-wrap: break-word; /* Quebra o texto longo para evitar estouro */
    }
}

@media (max-width: 768px) {
    button {
        width: 100%; /* Botão ocupa toda a largura */
        font-size: 14px; /* Tamanho do texto reduzido */
        padding: 12px; /* Mais espaçamento interno */
    }
}
/* Responsividade para formulários */
@media (max-width: 480px) {
    form input, form textarea {
        width: 100%;
        font-size: 14px;
    }

    form button {
        width: 100%;
        padding: 10px;
    }
}

/* Ocultar elementos irrelevantes em telas pequenas */
@media (max-width: 768px) {
    .sidebar {
        display: none;
    }
}

    </style>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.4.0/jspdf.umd.min.js"></script>
</head>
<body>
    <div class="container">
        <h1>Teste Ikigai</h1>
        <form id="ikigaiForm">
            <div class="section">
                <h2>1. O que você ama (paixão):</h2>
                <div class="circ">
                    <p>Quais atividades você gosta de fazer em seu tempo livre?</p>
                    <textarea id="love1" name="love1" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>O que você faria, mesmo que não fosse pago?</p>
                    <textarea id="love2" name="love2" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>Quais são seus hobbies e interesses?</p>
                    <textarea id="love3" name="love3" rows="2" required></textarea>
                </div>
            </div>

            <div class="section">
                <h2>2. O que você é bom (vocação):</h2>
                <div class="circ">
                    <p>Quais habilidades você possui?</p>
                    <textarea id="good1" name="good1" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>Em quais áreas você recebe elogios ou reconhecimentos?</p>
                    <textarea id="good2" name="good2" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>Em que atividades você se destaca?</p>
                    <textarea id="good3" name="good3" rows="2" required></textarea>
                </div>
            </div>

            <div class="circ">
                <h2>3. O que o mundo precisa (missão):</h2>
                <div class="circ">
                    <p>Que problemas ou necessidades você vê no mundo que gostaria de ajudar a resolver?</p>
                    <textarea id="world1" name="world1" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>Que tipo de impacto positivo você gostaria de causar na sociedade?</p>
                    <textarea id="world2" name="world2" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>O que você acredita que poderia fazer para tornar o mundo um lugar melhor?</p>
                    <textarea id="world3" name="world3" rows="2" required></textarea>
                </div>
            </div>

            <div class="circ">
                <h2>4. Pelo que você pode ser pago (profissão):</h2>
                <div class="circ">
                    <p>Quais são suas qualificações e experiências profissionais?</p>
                    <textarea id="paid1" name="paid1" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>Em que áreas ou setores você pode encontrar oportunidades de emprego?</p>
                    <textarea id="paid2" name="paid2" rows="2" required></textarea>
                </div>
                <div class="circ">
                    <p>Por quais atividades ou serviços as pessoas estão dispostas a pagar?</p>
                    <textarea id="paid3" name="paid3" rows="2" required></textarea>
                </div>
            </div>

            <button type="button" onclick="generateIkigai()">Gerar Resultado</button>
        </form>
        <div class="result" id="result" style="display:none;">
            <h2>Resultado</h2>
            <p id="ikigaiOutput"></p>
            <button class="download-btn" onclick="downloadPDF()">Baixar Resultado em PDF</button>
        </div>
    </div>

    <script>
        function generateIkigai() {
            const love1 = document.getElementById('love1').value;
            const love2 = document.getElementById('love2').value;
            const love3 = document.getElementById('love3').value;

            const good1 = document.getElementById('good1').value;
            const good2 = document.getElementById('good2').value;
            const good3 = document.getElementById('good3').value;

            const world1 = document.getElementById('world1').value;
            const world2 = document.getElementById('world2').value;
            const world3 = document.getElementById('world3').value;

            const paid1 = document.getElementById('paid1').value;
            const paid2 = document.getElementById('paid2').value;
            const paid3 = document.getElementById('paid3').value;

            const result = `Resultado:\n\n- O que você ama: Missão e paixão.\n    - ${love1}\n    - ${love2}\n    - ${love3}\n\n- O que o mundo precisa: Vocação.\n    - ${world1}\n    - ${world2}\n    - ${world3}\n\n- Pelo que você pode ser pago: Profissão.\n    - ${paid1}\n    - ${paid2}\n    - ${paid3}`;

            document.getElementById('ikigaiOutput').innerText = result;
            document.getElementById('result').style.display = 'block';
        }

        function downloadPDF() {
            const { jsPDF } = window.jspdf;
            const pdf = new jsPDF();

            const love1 = document.getElementById('love1').value;
            const love2 = document.getElementById('love2').value;
            const love3 = document.getElementById('love3').value;

            const good1 = document.getElementById('good1').value;
            const good2 = document.getElementById('good2').value;
            const good3 = document.getElementById('good3').value;

            const world1 = document.getElementById('world1').value;
            const world2 = document.getElementById('world2').value;
            const world3 = document.getElementById('world3').value;

            const paid1 = document.getElementById('paid1').value;
            const paid2 = document.getElementById('paid2').value;
            const paid3 = document.getElementById('paid3').value;

            const result = `Resultado:\n\n- O que você ama: Missão e paixão.\n    - ${love1}\n    - ${love2}\n    - ${love3}\n\n- O que o mundo precisa: Vocação.\n    - ${world1}\n    - ${world2}\n    - ${world3}\n\n- Pelo que você pode ser pago: Profissão.\n    - ${paid1}\n    - ${paid2}\n    - ${paid3}`;

            pdf.text(result, 10, 10);
            pdf.save('ikigai_resultado.pdf');
        }
    </script>



---

### O que isso faz:

1. **Blocos de código**: Usam a sintaxe ````` para exibir os arquivos HTML, CSS e JavaScript formatados.
2. **Prévia Online**: Dá um link direto para onde o projeto está hospedado (ex: GitHub Pages).
3. **Organização**: O código está dividido em seções, facilitando a visualização e entendimento.

---

### Como usar:

1. **Crie ou atualize** o arquivo `README.md` no repositório.
2. Cole o código acima.
3. Substitua os links e nomes (ex: `seu-usuario`, `nome-do-repositorio`).
4. Suba as alterações no GitHub.

Pronto! O seu código aparecerá no README e será exibido formatado na página principal do repositório! 🚀

</body>
</html>

