# Declaração de uso de Inteligência Artificial generativa

> **Regra do trabalho:** usar IA generativa é **permitido e incentivado**, mas
> **todo e qualquer uso** precisa estar declarado e detalhado em uma seção própria
> do artigo e na apresentação (vídeo). Uso não declarado é considerado **plágio** e
> leva à **nota zero** no trabalho para todo o grupo.
>
> Este arquivo é o rascunho de trabalho da declaração: preencham **ao longo** do
> projeto (não no último dia) e copiem a tabela para o artigo. Apaguem as linhas de
> exemplo e todas as marcações TODO.

## 1. Ferramentas usadas

| Ferramenta (nome e versão/modelo)        | Como acessaram | Quem usou                        |
| ---------------------------------------- | -------------- | -------------------------------- |
| Google Gemini (interface web/4 Hydrogen) | Navegador      | Maria Eduarda da Silva Gonçalves |
| Claude (interface web/Claude Sonnet 5.5) | Navegador      | Maria Eduarda da Silva Gonçalves |
| Claude (interface web/Claude Sonnet 5.5) | Navegador      | Amanda Beatriz Carvalho de Jesus |

## 2. Usos, um por linha

| #   | Etapa | O que a IA fez | Prompt (ou resumo + link para o registro) | O que o grupo fez com o resultado |
| --- | ----- | -------------- | ----------------------------------------- | --------------------------------- |

| 1 | Documentação das fontes (`FONTES.md`) | Formatar em tabela Markdown os caminhos e links dos documentos obtidos pelo grupo | _"dado esses caminhos e esse link da url, retorne uma tabela seguindo o padrão em anexo"_ / | Revisou o retorno das informações |
| 2 | Análise exploratória dos dados, Seção 2. Dados | Criação do código em python das análises solicitas e criação de gráficos adicionais para auxiliar na análise | "Com base nesse notebook em que preciso construir um chatbot, atue como um analista de dados sênior para fazer uma análise exploratória - tamanho das mensagens por classe, palavras mais
frequentes por intenção, exemplos de negativos difíceis, diferenças entre frases
humanas e de LLM dos meus dados em dados/treino.csv e dados/teste.csv, pensando nesse caso de uso coloque algo a mais na análise exploratória que não foi indicada por mim nesse prompt e seja relevante para entender meu conjunto de dados e a sua qualidade. Isto é, me mande o codigo que preenche a célula de analise exploratoria dos dados e depois explqiue." | Revisou o retorno e utilizou os gráficos criados para tomada de decisão |
| 3 | Escolha de hiperparametros | Definir a grade de hiperparâmetros para vetorização TF-IDF e classificadores do Scikit-learn | "Atue como um Engenheiro de Machine Learning sênior. Com base no meu problema de classificação de intenções, indicados pelas tabelas e gráficos acima, para um chatbot (com os dados em dados/treino.csv e dados/teste.csv, que possuem textos curtos, exemplos negativos difíceis e mistura de frases humanas e sintéticas de LLM), sugira uma estratégia de busca de hiperparâmetros e indique quais hiperparâmetros priorizar para os modelos baseline e para a vetorização utilizadas, explicando o impacto de cada um no controle de overfitting e na generalização para frases reais. Me envie o código Python completo e reproduzível para executar essa validação cruzada e justifique as escolhas técnicas." / | Analisou as justificativas de regularização e vocabulário, executou o código de busca e selecionou a melhor combinação com base nas métricas de validação cruzada |

## 3. O que NÃO foi feito com IA

Decisão das intenções
Busca dos documentos
Decisão dos algoritmos utilizados
Escolha dos dados de treino
Escrita e escolha dos dados de teste
Correção dos dados
Análise dos dados
Representações de texto

## 4. Reflexão (2 a 4 frases)
