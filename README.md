# ATIVIDADE-PROGRAMA-O

## NUVEM ESCOLHIDA
Serviços de PLN da Microsoft Azure
## SERVIÇOS
### Text Analytics
#### DESCRIÇÃO
O Text Analytics é um serviço de análise de texto para extrair insights de dados não estruturados. Ele oferece as seguintes funcionalidades:
#### FUNCIONALIDADES/ USOS PARA APLICAÇÕES

Análise de sentimentos: Classifica sentimentos (positivo/negativo) de frases. Ex: Analisar reviews de clientes para descobrir a satisfação geral.
Detecção de idioma: Detecta o idioma do texto. Ex: colocar texto para tradução automática para o idioma correto.
Extração de frases-chave: Identifica frases que capturam as ideias centrais de um texto. Ex: Resumir um grande corpus de texto.
Marcação de entidades: Identifica e categoriza entidades (pessoas, locais, organizações) em um texto. Ex: Análise de menções a produtos/serviços em posts de mídia social.


### Translator Text
#### DESCRIÇÃO
- O Translator Text é um serviço de tradução automática neural que traduz entre mais ou menos 70 idiomas.
#### FUNCIONALIDADES/ USOS PARA APLICAÇÕES

- Tradução de texto: Traduz entre pares de idiomas com um alto grau de precisão . Ex: Traduzir o conteúdo de um site para vários idiomas.
- Detecção de idioma: Detecta automaticamente o idioma de origem de uma entrada de texto.
- Glosário: Permite criar um dicionário com termos de tradução customizados. Ex: Traduzir abreviações específicas de um domínio.

### QnA Maker
#### DESCRIÇÃO
- O QnA Maker é um serviço de perguntas e respostas que permite criar um sistema de QnA a partir de uma base de dados de perguntas e respostas.

#### FUNCIONALIDADES/ USOS PARA APLICAÇÕES
- Criação de conhecimento: Permite adicionar pares de perguntas/respostas e treinar um modelo de reconhecimento.
- Detecção de intenção: Classifica a intenção por trás de uma pergunta de usuário. Ex. FAQ, feedback, suporte técnico.


## TODAS ESSAS FUNCIONALIDADES SÃO POSSÍVEIS SER ACESSADAS POR REQUISIÇÕES HTTPS
### PEQUENO EXEMPLO COM Text Analytics

import requests

url = "https://westus.api.cognitive.microsoft.com/text/analytics/v2.1/sentiment"
key = "sua_chave_api"
documents = {
    "documents": [
        { "id": "1", "language": "en", "text": "I love Azure!" },
}
headers = { "Ocp-Apim-Subscription-Key": key }
response = requests.post(url, headers=headers, json=documents)
print(response.json())

