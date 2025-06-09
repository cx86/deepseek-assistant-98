# deepseek-assistant-98
(Estilo Windows 98)
git clone https://github.com/tu-usuario/deepseek-assistant-98.git
<!DOCTYPE html>
<html>
<head>
    <title>DeepSeek Assistant '98</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=MS+Sans+Serif" rel="stylesheet">
</head>
<body>
    <div class="window">
        <div class="title-bar">
            <span class="title">DeepSeek Assistant</span>
            <button class="close-btn">X</button>
        </div>
        <div class="content">
            <img src="assets/images/deepseek-bot.png" class="assistant" id="assistant">
            <div class="message" id="message">
                ¡Hola! Soy tu asistente. ¿En qué puedo ayudarte hoy?
            </div>
            <input type="text" id="userInput" placeholder="Escribe aquí...">
            <button id="sendBtn">Enviar</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: 'MS Sans Serif', sans-serif;
    background: #008080; /* Fondo azul de Windows 98 */
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.window {
    width: 300px;
    background: #c0c0c0;
    border: 2px solid #000;
    box-shadow: 3px 3px 0 #dfdfdf;
}

.title-bar {
    background: #000080;
    color: white;
    padding: 3px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.close-btn {
    background: #c0c0c0;
    border: 1px solid #000;
    width: 20px;
    height: 20px;
    font-weight: bold;
}

.content {
    padding: 10px;
    text-align: center;
}

.assistant {
    width: 80px;
    height: 80px;
}

input, button {
    font-family: 'MS Sans Serif', sans-serif;
    margin-top: 10px;
}
document.getElementById('sendBtn').addEventListener('click', async () => {
    const userInput = document.getElementById('userInput').value;
    const messageBox = document.getElementById('message');
    const assistantImg = document.getElementById('assistant');

    // Animación de "pensando"
    assistantImg.src = 'assets/images/deepseek-thinking.gif';
    messageBox.textContent = "Pensando...";

    // Simular llamada a la API de DeepSeek (reemplaza con tu implementación real)
    setTimeout(async () => {
        try {
            // Aquí iría la llamada real a la API de DeepSeek
            // const response = await fetch("https://api.deepseek.com/chat", { ... });
            // const data = await response.json();
            
            // Simulación de respuesta
            const responses = [
                "¡Claro! Aquí tienes la información que necesitas.",
                "No estoy seguro, ¿puedes reformular la pregunta?",
                "Parece que estás trabajando en un documento. ¿Necesitas ayuda con el formato?"
            ];
            messageBox.textContent = responses[Math.floor(Math.random() * responses.length)];
            assistantImg.src = 'assets/images/deepseek-bot.png';
        } catch (error) {
            messageBox.textContent = "¡Ups! Algo salió mal.";
            assistantImg.src = 'assets/images/deepseek-error.png';
        }
    }, 1500);
document.getElementById('sendBtn').addEventListener('click', async () => {
    const userInput = document.getElementById('userInput').value;
    const messageBox = document.getElementById('message');
    const assistantImg = document.getElementById('assistant');

    // Animación de "pensando"
    assistantImg.src = 'assets/images/deepseek-thinking.gif';
    messageBox.textContent = "Pensando...";

    // Simular llamada a la API de DeepSeek (reemplaza con tu implementación real)
    setTimeout(async () => {
        try {
            // Aquí iría la llamada real a la API de DeepSeek
            // const response = await fetch("https://api.deepseek.com/chat", { ... });
            // const data = await response.json();
            
            // Simulación de respuesta
            const responses = [
                "¡Claro! Aquí tienes la información que necesitas.",
                "No estoy seguro, ¿puedes reformular la pregunta?",
                "Parece que estás trabajando en un documento. ¿Necesitas ayuda con el formato?"
            ];
            messageBox.textContent = responses[Math.floor(Math.random() * responses.length)];
            assistantImg.src = 'assets/images/deepseek-bot.png';
        } catch (error) {
            messageBox.textContent = "¡Ups! Algo salió mal.";
            assistantImg.src = 'assets/images/deepseek-error.png';
        }
    }, 1500);
});
