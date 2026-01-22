# Chatbot de Clima - Telegram & n8n

Este projeto consiste em um chatbot automatizado desenvolvido no **n8n** que fornece a temperatura atual de cidades enviadas via **Telegram**. O bot utiliza a API do **OpenWeatherMap** para obter dados climáticos em tempo real.

## 🚀 Funcionalidades
- **Identificação Inteligente**: Reconhece nomes de cidades simples ou com estado (ex: Curitiba ou Curitiba, PR).
- **Tratamento de Dados**: Remove acentos e padroniza a entrada para garantir a precisão da busca.
- **Arredondamento**: Retorna a temperatura arredondada para o valor inteiro mais próximo.
- **Tratamento de Erros**: Caso a cidade não seja encontrada, o bot envia uma mensagem de orientação ao usuário.

## 📦 Passos para Importar o Workflow
1. No seu n8n, crie um novo workflow.
2. No menu superior direito (ícone de três pontos), selecione **Import from File**.
3. Selecione o arquivo `workflow-chatbot-telegram.json` presente neste repositório.

## 🛠️ Configuração de Credenciais
Para que o workflow funcione, você deve configurar as seguintes variáveis no n8n:

1. **TELEGRAM_BOT_TOKEN**:
   - Obtenha o token criando um bot com o [@BotFather](https://t.me/botfather).
   - No n8n, crie uma credencial de "Telegram API" e insira este token.
   
2. **OPENWEATHER_API_KEY**:
   - Crie uma conta em [OpenWeatherMap](https://openweathermap.org/api) e gere sua chave de API.
   - No nó **HTTP Request**, localize o parâmetro `appid` e insira sua chave.

## 🎮 Como Executar o Chatbot
1. Certifique-se de que o workflow está salvo e com o botão **Publish** ativo (verde).
2. No Telegram, abra o chat com o seu bot.
3. **Teste de Sucesso**: Envie o nome de uma cidade (ex.: `São Paulo, SP`).
   - **O que esperar**: O bot responderá algo como: `🌤️ A temperatura em São Paulo é de 17°C.`.
4. **Teste de Erro**: Envie um nome inexistente (ex.: `CidadeFicticia123`).
   - **O que esperar**: O bot responderá: `❌ Cidade não encontrada. Use o formato Cidade,UF (ex.: São Paulo,SP).`.
