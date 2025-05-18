# CinemAI

![image](https://github.com/user-attachments/assets/d9e2ebab-23fd-400b-813f-8a00c3712dbf)



[![Status do Projeto](https://img.shields.io/badge/Status-Concluído-brightgreen.svg)](https://github.com/seu-usuario/seu-repositorio)
[![Linguagem](https://img.shields.io/badge/Linguagem-Python-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Framework-Google_ADK-orange.svg)](https://developers.google.com/assistant/sdk)
[![Modelo Gemini](https://img.shields.io/badge/Modelo-Gemini_2.0_Flash-purple.svg)](https://ai.google.dev/models/gemini)

## 🏆 Projeto Final da Semana de Imersão Alura IA com Gemini

Este projeto foi desenvolvido como parte da semana de imersão em Gemini, com o objetivo de demonstrar a aplicação prática e o potencial da API Gemini e do framework de agentes do Google (ADK) na criação de soluções inteligentes e interativas.

## ✨ Demonstração em Vídeo

https://github.com/user-attachments/assets/de9a5d62-53c2-4b0a-9bd6-0c6bb8bde32a


## 💡 Ideia Central do Projeto

Este projeto visa simplificar a experiência de ir ao cinema, fornecendo aos usuários recomendações personalizadas de filmes e sessões com base em suas preferências de data, áudio, companhia, gênero e horário, utilizando o poder dos agentes Gemini para buscar, filtrar e analisar informações em tempo real.

## 🎯 Funcionalidades Principais


* **Busca Inteligente de Cinemas:** Utiliza o Google Search através de um agente para encontrar os cinemas mais próximos de um endereço fornecido pelo usuário.
* **Consulta Detalhada de Programação:** Um agente especializado busca a programação completa dos cinemas, incluindo horários e tipo de áudio (dublado/legendado) para uma data específica.
* **Filtragem Personalizada:** Permite aos usuários refinar a programação com base em suas preferências de áudio e período do dia.
* **Recomendação Inteligente:** Um agente avançado seleciona as melhores opções de sessões, considerando avaliações de filmes, gênero preferido e o tipo de companhia do usuário, fornecendo uma breve justificativa para cada recomendação.
* **Validação de Entrada com Feedback:** Implementa agentes para validar as respostas dos usuários durante a interação, fornecendo feedback amigável em caso de informações inválidas.

## ⚙️ Como Funciona

O projeto é construído utilizando o framework de agentes do Google (ADK) e a API Gemini. Ele orquestra o fluxo de informações através de uma série de agentes especializados:

1.  Um agente (`agente_busca_cinema`) recebe o endereço do usuário e utiliza a ferramenta de busca do Google para listar os cinemas próximos.
2.  Com a lista de cinemas e a data desejada, o agente (`agente_busca_programacao`) consulta a programação detalhada de cada cinema.
3.  O agente (`agente_filtra_programacao`) refina essa programação com base nas preferências de áudio e período do dia do usuário.
4.  Finalmente, o agente (`agente_seleciona_melhor_sessao_final`) analisa a programação filtrada, busca avaliações e sinopses de filmes, e recomenda as melhores sessões considerando o gênero preferido e a companhia do usuário.
5.  Agentes auxiliares (`agente_validador_resposta_booleano` e `agente_feedback_elaborado`) garantem a qualidade da interação com o usuário através da validação de entradas e feedback informativo.

## 🚀 Como Executar


1.  **Pré-requisitos:**
    * Certifique-se de ter uma chave de API do Google Gemini configurada no Google Colab (conforme as células de código fornecidas).
    * Execute as células de instalação das bibliotecas necessárias:
        ```python
        %pip -q install google-genai
        !pip install -q google-adk
        ```
    * A variável de ambiente `GOOGLE_API_KEY` deve estar configurada através do `userdata.get('GOOGLE_API_KEY')`.

2.  **Execução:**
    * Execute as células de código sequencialmente no ambiente Google Colab fornecido.
    * O script irá solicitar as informações necessárias (data, preferência de áudio, companhia, gênero, período do dia e endereço) através da função `obter_resposta_validada_com_feedback`.
    * Responda às perguntas no prompt interativo.
    * Ao final da execução, as recomendações de sessões de cinema personalizadas serão exibidas na saída.

## 🛠️ Tecnologias Utilizadas

* **Google Gemini API:** Modelo de linguagem avançado para processamento de linguagem natural e geração de texto.
* **Google Agents Development Kit (ADK):** Framework para a criação e orquestração de agentes inteligentes.
* **Python:** Linguagem de programação principal.
* **`google-genai`:** Biblioteca Python para interagir com a API Gemini.
* **`google-adk`:** Biblioteca Python do framework de agentes do Google.
* **`google_search` (ADK Tool):** Ferramenta integrada ao ADK para realizar buscas no Google.
* **Google Colaboratory:** Ambiente de desenvolvimento utilizado.

## 🧠 Aprendizados e Desafios

Durante esta semana de imersão em Gemini, aprendi sobre o poder da inteligência artificial generativa na criação de soluções complexas e personalizadas. O framework de agentes do Google se mostrou uma ferramenta poderosa para modularizar tarefas e criar fluxos de trabalho inteligentes.

Um dos principais desafios foi orquestrar a comunicação entre os diferentes agentes para garantir que a informação fosse passada de forma eficiente e que o resultado final atendesse às expectativas do usuário. A depuração do fluxo dos agentes e a otimização das instruções para cada um deles também exigiram atenção e experimentação.

## 🚀 Próximos Passos

* Implementar uma interface gráfica de usuário (GUI) para facilitar a interação.
* Integrar um sistema de recomendação baseado no histórico de preferências do usuário.
* Explorar outros modelos Gemini para comparar desempenho e qualidade das respostas.
