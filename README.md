# Back-end RAG - Atividade Avaliativa FIAP

# Integrantes do grupo:
# Bernardo Braga Perobeli | RM 562468
# Felipe Stefani Honorato | RM 563380
# Igor Paixão Sarak | RM 563726
# Lucca Phelipe Masini | RM 564121
# Luiz Henrique Poss | RM 562177

Este projeto consiste na evolução do back-end de um chatbot RAG, mantendo total compatibilidade com o front-end original em Streamlit. Toda a lógica de roteamento e serviços foi refatorada para utilizar um banco vetorial real (Qdrant) e modelos avançados da OpenAI.

## ⚙️ Manutenção do Contrato (Back-end Only)
Conforme as instruções, o back-end preserva os endpoints consumidos pela interface:
*   `POST /chat`: Recebe `message` e `history`, retorna `answer` e `context_used`.
*   `POST /index`: Endpoint de ingestão de conhecimento (compatível com a lógica de coleções).

## 🚀 Como Executar no Google Colab
1. Abra o notebook e instale as dependências: `fastapi`, `uvicorn`, `qdrant-client`, `openai`.
2. Configure sua `OPENAI_API_KEY` nos Secrets do Colab.
3. Execute as células de serviço e roteamento.
4. Na última célula, copie o **IP Público** gerado e clique no link do LocalTunnel.
5. Após liberar o acesso no navegador, use a URL gerada (ex: `https://...loca.lt`) como base para o seu Front-end.

## 🛠️ Tecnologias
*   **FastAPI:** Framework assíncrono para a API.
*   **Qdrant:** Banco vetorial para busca semântica (Requisito 1).
*   **OpenAI GPT-4o-Mini:** Motor de resposta (Requisito 2).
*   **Recursive Character Splitter:** Melhoria na qualidade dos chunks (Requisito 3).
