Markdown
# TechBot - Assistente Virtual Especialista TechFix Pro

O **TechBot** é uma solução de atendimento automatizado desenvolvida em Python para atuar como um assistente especialista sobre os serviços, garantias e planos corporativos da empresa fictícia **TechFix Pro**. O projeto foi projetado para responder dúvidas operacionais estritamente com base em um contexto de dados privados fornecidos na inicialização do Modelo de Linguagem (LLM), utilizando técnicas de Engenharia de Prompt para impedir alucinações de conteúdo ou respostas sobre informações que não estejam publicamente disponíveis na internet. Além disso, o sistema implementa uma regra de negócio rígida que controla o fluxo da conversa: ao receber e responder à terceira pergunta do usuário, o assistente gera um resumo consolidado de toda a interação mantida no chat e encerra a sessão automaticamente, desabilitando novos envios de mensagens.

## Arquitetura e Tecnologias
O projeto utiliza o modelo **Gemini 2.5 Flash** integrado através do SDK oficial `google-genai` da Google Cloud, garantindo respostas rápidas e baixo tempo de latência. A interface gráfica e a gestão do fluxo de mensagens em tempo real no ambiente interativo foram construídas com a biblioteca **Panel** (`panel`). A gestão de credenciais e segurança é realizada via variáveis de ambiente, garantindo que chaves privadas de API não sejam expostas nos commits do repositório.

## Estrutura do Repositório
```text
.
├── main.py              # Script principal com a lógica do chatbot e interface Panel
├── requirements.txt     # Dependências do projeto (google-genai, panel, python-dotenv)
├── .env.example         # Modelo de configuração de variáveis de ambiente sem credenciais
├── .gitignore           # Regras de exclusão para arquivos sensíveis e temporários
└── README.md            # Documentação completa do projeto
Passo a Passo para Reprodução da Execução
Opção 1: Execução Local
Clonar o Repositório:

Bash
git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
cd seu-repositorio
Criar e Ativar o Ambiente Virtual:

Bash
python -m venv venv
# No Linux/macOS:
source venv/bin/activate
# No Windows:
venv\Scripts\activate
Instalar as Dependências:

Bash
pip install -r requirements.txt
Configurar as Variáveis de Ambiente:
Crie um arquivo chamado .env na raiz do projeto com base no modelo .env.example:

Snippet de código
Gemini_API_Key=COLE_SUA_CHAVE_AQUI
Iniciar a Aplicação:
Execute a interface do Panel via terminal:

Bash
panel serve main.py --show
Opção 2: Execução no Google Colab
Abra um novo notebook no Google Colab.

No menu lateral esquerdo, clique no ícone de Chave (Secrets), adicione um novo segredo com o nome Gemini_API_Key, cole sua chave de API obtida no Google AI Studio e ative a chave "Acesso ao Notebook".

Execute o comando de instalação das bibliotecas:

Bash
!pip install -q google-genai panel python-dotenv
Cole o código do arquivo main.py em uma célula e execute para renderizar a interface do chat diretamente na tela do notebook.
