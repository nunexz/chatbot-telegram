# Chatbot de Clima - Telegram & n8n

Este projeto é um chatbot automatizado via n8n que fornece a temperatura atual de qualquer cidade enviada pelo Telegram.

## 🚀 Funcionalidades
- Identifica nomes de cidades (ex: Curitiba ou Curitiba, PR).
- Remove acentos e padroniza a entrada.
- Consulta a API do OpenWeather.
- Retorna a temperatura arredondada.
- Possui tratamento para cidades não encontradas.

## 🛠️ Configuração de Credenciais
Para este workflow funcionar, você deve configurar no n8n:
- **TELEGRAM_BOT_TOKEN**: Token gerado pelo @BotFather.
- **OPENWEATHER_API_KEY**: Chave de API gerada no site do OpenWeather.
- **APIs**: As APIs oficiais foram removidas do JSON para garantir a segurança do projeto
