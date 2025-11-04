# Processamento de Linguagem Natural: Projeto Prático - Hacker News Podcast Generator

Este projeto prático, desenvolvido como parte da disciplina de Processamento de Linguagem Natural da UFABC, demonstra a aplicação de Grandes Modelos de Linguagem (LLMs) e o framework LangChain para automatizar a criação de conteúdo a partir de notícias online.

### Objetivo

O objetivo principal deste projeto é extrair as notícias mais relevantes do site Hacker News, processá-las utilizando técnicas de PLN e gerar um roteiro de podcast, que pode ser transformado em áudio.

### Tecnologias Utilizadas

*   **Grandes Modelos de Linguagem (LLMs):** Gemini e/ou OpenAI (configuráveis)
*   **Framework de Orquestração:** LangChain
*   **Extração de Dados Web:** `requests`, `BeautifulSoup`, `newspaper3k`
*   **Geração de Áudio:** API Gemini TTS (`gemini-2.5-flash-preview-tts`)
*   **Ambiente:** Google Colab

### Fluxo do Projeto

O projeto segue as seguintes etapas principais:

1.  **Extração de Notícias:** Busca e extração das notícias principais da página inicial do Hacker News.
2.  **Extração de Conteúdo:** Utilização da biblioteca `newspaper3k` para acessar as URLs das notícias e extrair o conteúdo completo dos artigos.
3.  **Processamento de Linguagem Natural com LangChain:**
    *   **Sumarização:** Aplicação de uma cadeia de sumarização (Map-Reduce) para criar resumos concisos dos artigos (em inglês).
    *   **Tradução:** Tradução dos resumos para o Português do Brasil.
4.  **Geração de Roteiro de Podcast:** Criação de uma cadeia LangChain para formatar os resumos traduzidos em um roteiro de podcast dinâmico, com falas alternadas para dois apresentadores.
5.  **Geração de Áudio:** Utilização da API Gemini TTS para converter o roteiro do podcast em um arquivo de áudio.

Este projeto demonstra o potencial da combinação de web scraping, LLMs e frameworks como LangChain para criar pipelines automatizados de processamento e geração de conteúdo.
