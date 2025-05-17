# Projeto-Alura
# ChatBot de Combate à Desinformação (Fact-Checking Simplificado)

## Descrição do Projeto

Este projeto consiste em um ChatBot desenvolvido no Google Colab com o objetivo de combater a desinformação de forma simplificada. Ele utiliza uma arquitetura de múltiplos agentes de inteligência artificial para analisar textos fornecidos pelos usuários, identificar alegações factuais e, através da busca de evidências em fontes confiáveis, determinar a veracidade dessas alegações. O ChatBot também se esforça para fornecer os links das fontes utilizadas na análise, promovendo a transparência e permitindo que os usuários verifiquem as informações por si mesmos.

## Funcionalidades Principais

* **Identificação de Reivindicações Fatuais:** O primeiro agente analisa o texto do usuário e extrai as afirmações que podem ser verificadas.
* **Busca de Evidências Confiáveis:** Um agente especializado utiliza a busca do Google para encontrar informações relevantes em fontes com alta credibilidade e segurança (agências de notícias renomadas, organizações de pesquisa, sites de fact-checking, etc.).
* **Extração de Links de Fontes:** Um agente intermediário tenta extrair os links das páginas da web utilizadas como evidência durante a busca.
* **Avaliação da Veracidade:** Com base nas evidências e nos links encontrados, um agente avalia se a reivindicação é verdadeira, falsa ou inconclusiva.
* **Geração de Resposta Clara:** O ChatBot fornece uma resposta concisa ao usuário, indicando o veredicto para cada alegação verificada, um breve resumo das evidências e os links das fontes utilizadas.

## Como Utilizar

1.  **Execute o código no ambiente Google Colab.**
2.  Quando solicitado, digite o texto que você gostaria de verificar na caixa de entrada.
3.  O ChatBot processará o texto através de seus diferentes agentes e exibirá os resultados da análise, incluindo as reivindicações identificadas, as evidências encontradas, os links das fontes e o veredicto final.

## Arquitetura do Projeto

O ChatBot é composto por cinco agentes principais:

1.  **Agente Identificador de Reivindicações:** `agente_identificador`
2.  **Agente Buscador de Evidências (Fact-Checker):** `agente_buscador_evidencias`
3.  **Agente Extrator de Links:** `agente_extrator_links`
4.  **Agente Avaliador de Fatos (Veredicto):** `agente_avaliador`
5.  **Agente de Resposta ao Usuário:** `agente_resposta`

O fluxo de execução principal é orquestrado pela função `chatbot_fact_checking_com_links()`.

## Tecnologias Utilizadas

* **Python:** Linguagem de programação principal.
* **Google Colab:** Ambiente de desenvolvimento e execução.
* **Vertex AI Agents:** Framework para criação e gerenciamento de agentes de IA.
* **Modelo Gemini:** Modelo de linguagem grande utilizado pelos agentes.
* **Google Search Tool (via Vertex AI Agents):** Ferramenta para realizar buscas na web.
* **IPython.display:** Para exibir resultados formatados no Colab.
* **datetime:** Para manipulação de datas (utilizado no projeto original de criação de posts).
* **re (módulo Python):** Para extração de links (estratégia alternativa considerada).

## Próximos Passos e Melhorias Potenciais

* **Aprimorar a identificação de reivindicações complexas e nuances na linguagem.**
* **Melhorar a precisão na extração de links das respostas do agente buscador.**
* **Integrar APIs de fact-checking específicas para fontes de informação mais direcionadas.**
* **Adicionar um sistema de pontuação de confiabilidade para as fontes encontradas.**
* **Implementar um mecanismo de feedback do usuário para melhorar a qualidade das verificações.**
* **Considerar a criação de uma interface de usuário mais interativa (fora do Colab).**
