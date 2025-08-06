# <center> Projeto de Estudos com LangChain 

Este projeto tem como objetivo o estudo e experimentação das ferramentas do **LangChain**, uma framework voltada para o desenvolvimento de aplicações que integram **Large Language Models (LLMs)** com **dados externos** e **pipelines personalizados**. O projeto utiliza exemplos práticos para manipulação de documentos, geração de embeddings, criação de chains e agentes inteligentes.

## <center> Estrutura do Projeto

- Scripts de manipulação de documentos (PDF, TXT)
- Criação de embeddings e armazenamento em vetores
- Chains customizadas para consulta e interação com dados
- Estudos de agentes utilizando LangChain Agents & Tools

## <center> Requisitos de Ambiente (.env)

Para o funcionamento correto do projeto, é necessário configurar as seguintes variáveis de ambiente no arquivo .env na raiz do projeto:

```dotenv
OPENAI_API_KEY=chave-da-sua-api-openai
PINECONE_API_KEY=sua-chave-pinecone
```

### Observações:
- Crie um arquivo **.env** e adicione suas chaves.
- A variável **OPENAI_API_KEY** é necessária para utilizar os modelos da OpenAI.
- As variáveis **PINECONE_API_KEY** e **PINECONE_ENVIRONMENT** são necessárias caso utilize armazenamento vetorial no Pinecone.

## <center> Instalação

1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   cd <nome-do-projeto>
   ```

2. Crie e ative um ambiente virtual (recomendado):
   ```bash
   python -m venv .venv
   pip install -r requirements.txt
   ```

<br>

## <center> Funcionamento do Fluxo de Respostas

O projeto realiza a consulta e geração de respostas a partir de documentos ou bases de dados externas através do seguinte fluxo:

1. **Carregamento dos Documentos**:
   - Os arquivos (PDF/TXT) são processados e convertidos em chunks de texto.
   
2. **Geração de Embeddings**:
   - Cada chunk de texto é transformado em um vetor de embeddings utilizando modelos da OpenAI ou outras fontes.
   
3. **Armazenamento Vetorial**:
   - Os embeddings são armazenados em um banco vetorial (ex: Pinecone) para buscas rápidas por similaridade.
   
4. **Consulta e Recuperação de Contexto**:
   - O usuário faz uma pergunta, que é transformada em embedding e comparada com os vetores salvos.
   - Os trechos mais relevantes são recuperados e enviados como contexto ao LLM.

5. **Geração da Resposta Final**:
   - O modelo LangChain compõe uma resposta utilizando os trechos recuperados (contextualização RAG).
   - A resposta final é retornada ao usuário de forma clara e objetiva.

Este fluxo garante que as respostas estejam sempre embasadas nas informações dos documentos fornecidos, combinando capacidade de raciocínio dos LLMs com dados contextuais reais.

<center> Projeto de estudos e exploração de **LangChain**.