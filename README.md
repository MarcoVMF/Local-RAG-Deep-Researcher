# Local-RAG-Deep-Researcher

Este projeto foi inspirado no tutorial do LangChain. Para mais informações, consulte os seguintes recursos:

- [Repositório do tutorial](https://github.com/langchain-ai/ollama-deep-researcher/)
- [Vídeo explicativo](https://www.youtube.com/watch?v=sGUjmyfof4Q)

---

## Configuração do Projeto

### Passo 1: Instalar o Ollama e Baixar os Modelos

Certifique-se de instalar o [Ollama](https://ollama.com/) e baixe os modelos necessários para o funcionamento do projeto. Utilize o seguinte dicionário para configurar os modelos no código:

```python
models = {
    "deepseek": "deepseek-r1:8b",
    "llama": "llama3.2:3b"
}
```

Os modelos usados nesse projeto podem ser instalados da seguinte maneira:

```bash
ollama pull deepseek-r1:8b
ollama pull llama3.2:3b
```
---

### Passo 2: Instalação de Dependências

Execute os seguintes comandos para instalar as bibliotecas necessárias:

```bash
pip install langchain_ollama  
pip install langchain_community  
pip install langgraph  
```

---

### Passo 3: Configuração da API do Tavily

1. Crie uma conta no [Tavily](https://tavily.com/).
2. Gere uma **API Key** no painel do Tavily.
3. Configure a variável de ambiente para a API Key no seu código:

```python
_set_env("TAVILY_API_KEY")
os.environ["TOKENIZERS_PARALLELISM"] = "true"
```

---

### Passo 4: Configuração do LangGraph

1. Cadastre-se no [LangGraph](https://www.langchain.com/langgraph).
2. Gere uma **API Key** e configure as seguintes variáveis de ambiente no seu projeto:

```python
_set_env("LANGSMITH_API_KEY")
os.environ["LANGCHAIN_TRACING_V2"] = "true"
os.environ["LANGCHAIN_PROJECT"] = "local-deepseek-8b-researcher"
```

---

### Passo 5: Estrutura de Dados

O fluxo de dados e as visualizações do projeto dependem do LangGraph. Certifique-se de configurá-lo corretamente para obter o máximo de informações durante a execução.

---

## Observações

- Certifique-se de estar usando uma versão compatível do Python (recomenda-se Python 3.8 ou superior).
- O projeto utiliza modelos avançados. Portanto, verifique os requisitos mínimos de hardware ao trabalhar com o Ollama.

---
