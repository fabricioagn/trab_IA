# TechBot - Chatbot Especialista TechFix Pro

## Descrição do Projeto
Este projeto implementa um chatbot especialista desenvolvido em Python com a biblioteca `google-genai` e a interface `Panel`. O objetivo é responder a dúvidas sobre procedimentos internos e planos da empresa fictícia **TechFix Pro** sem sofrer alucinações sobre tópicos não informados.

## Funcionalidades
- Responde estritamente com base na base de conhecimento privada.
- Recusa-se a responder sobre tópicos fora do contexto interno.
- Limite estrito de 3 perguntas por sessão.
- Gera um resumo automático do atendimento ao responder à 3ª pergunta e encerra a sessão.

## Como Executar
1. Clone o repositório:
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   cd seu-repositorio
