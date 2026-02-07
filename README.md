# 🦜🔗 LangChain — Do Básico ao RAG

Trilha prática de 6 exercícios progressivos para dominar os fundamentos do LangChain, cobrindo desde chains simples até Retrieval-Augmented Generation (RAG).

## Sobre o projeto

Esta trilha foi construída com foco em aprendizado incremental. Cada exercício adiciona um novo conceito sobre o anterior, consolidando o entendimento antes de avançar.

**Stack utilizada:** Python, LangChain, OpenAI (GPT-4o-mini), FAISS

## Exercícios

### 1. Chain Básica — Prompt + Modelo + Parser
Crie uma chain que recebe o nome de um país e retorna 3 curiosidades sobre ele.

**Conceitos:** `ChatPromptTemplate`, `ChatOpenAI`, `StrOutputParser`, operador `|`

---

### 2. Chain Sequencial — Saída alimenta a próxima chain
Crie duas chains: a primeira gera uma receita a partir de ingredientes, a segunda avalia e sugere melhorias. A saída da primeira alimenta diretamente a segunda.

**Conceitos:** Composição de chains, fluxo de dados entre etapas

---

### 3. Structured Output + RunnableParallel
Crie uma chain que recebe uma mensagem de suporte, classifica a categoria (bug, feature request, dúvida) usando Pydantic, e gera uma resposta adequada ao tipo.

**Conceitos:** `BaseModel` (Pydantic), `with_structured_output`, `RunnableParallel`, `lambda`

---

### 4. Branching — Caminhos condicionais
Expanda o exercício anterior: dependendo da categoria, a chain segue por caminhos diferentes. Bug pede reprodução do problema, feature request pede justificativa, dúvida recebe uma resposta direta.

**Conceitos:** `RunnableBranch`, `RunnableLambda`, lógica condicional em chains

---

### 5. Memória e Conversação
Crie um chatbot cinéfilo que mantém contexto de conversa. O bot deve lembrar o que já recomendou e quais preferências o usuário mencionou.

**Conceitos:** `MessagesPlaceholder`, `RunnableWithMessageHistory`, `InMemoryChatMessageHistory`, `session_id`

---

### 6. RAG — Retrieval-Augmented Generation
Crie uma chain que carrega um PDF (FAQ), divide em chunks, armazena em um vector store e responde perguntas com base no conteúdo do documento.

**Conceitos:** `PyPDFLoader`, `RecursiveCharacterTextSplitter`, `OpenAIEmbeddings`, `FAISS`, retriever, chain de QA com contexto

## Estrutura do repositório

```
├── README.md
├── respostas/
│   ├── desafios_claude.ipynb
└── arquivos/
    └── faq.pdf
```

## Como rodar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/langchain-exercises.git
cd langchain-exercises
```

2. Instale as dependências:
```bash
pip install langchain langchain-openai langchain-community faiss-cpu pypdf python-dotenv pydantic
```

3. Configure sua API key da OpenAI no arquivo `.env`:
```
OPENAI_API_KEY=sk-sua-chave-aqui
```

4. Abra os notebooks na ordem e siga os exercícios.

## Pré-requisitos

- Python 3.10+
- Conta na OpenAI com API key
- Conhecimento básico de Python

## Progresso de aprendizado

| # | Exercício | Conceito principal |
|---|-----------|-------------------|
| 1 | Chain Básica | Prompt → Modelo → Parser |
| 2 | Chain Sequencial | Composição de chains |
| 3 | Structured Output | Pydantic + RunnableParallel |
| 4 | Branching | RunnableBranch |
| 5 | Memória | RunnableWithMessageHistory |
| 6 | RAG | Embeddings + Vector Store + Retriever |