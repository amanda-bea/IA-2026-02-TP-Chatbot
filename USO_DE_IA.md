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
| OpenRouter (OpenAI GPT 6 Luna)           | API            | Amanda Beatriz Carvalho de Jesus |

## 2. Usos, um por linha

| #   | Etapa | O que a IA fez | Prompt (ou resumo + link para o registro) | O que o grupo fez com o resultado |
| --- | ----- | -------------- | ----------------------------------------- | --------------------------------- |

| 1 | Documentação das fontes (`FONTES.md`) | Formatar em tabela Markdown os caminhos e links dos documentos obtidos pelo grupo | _"dado esses caminhos e esse link da url, retorne uma tabela seguindo o padrão em anexo"_ / | Revisou o retorno das informações |  
| 2 | Análise exploratória dos dados, Seção 2. Dados | Criação do código em python das análises solicitas e criação de gráficos adicionais para auxiliar na análise | "Com base nesse notebook em que preciso construir um chatbot, atue como um analista de dados sênior para fazer uma análise exploratória - tamanho das mensagens por classe, palavras mais
frequentes por intenção, exemplos de negativos difíceis, diferenças entre frases
humanas e de LLM dos meus dados em dados/treino.csv e dados/teste.csv, pensando nesse caso de uso coloque algo a mais na análise exploratória que não foi indicada por mim nesse prompt e seja relevante para entender meu conjunto de dados e a sua qualidade. Isto é, me mande o codigo que preenche a célula de analise exploratoria dos dados e depois explqiue." | Revisou o retorno e utilizou os gráficos criados para tomada de decisão |
| 3 | Escolha de hiperparametros | Definir a grade de hiperparâmetros para vetorização TF-IDF e classificadores do Scikit-learn | "Atue como um Engenheiro de Machine Learning sênior. Com base no meu problema de classificação de intenções, indicados pelas tabelas e gráficos acima, para um chatbot (com os dados em dados/treino.csv e dados/teste.csv, que possuem textos curtos, exemplos negativos difíceis e mistura de frases humanas e sintéticas de LLM), sugira uma estratégia de busca de hiperparâmetros e indique quais hiperparâmetros priorizar para os modelos baseline e para a vetorização utilizadas, explicando o impacto de cada um no controle de overfitting e na generalização para frases reais. Me envie o código Python completo e reproduzível para executar essa validação cruzada e justifique as escolhas técnicas." / | Analisou as justificativas de regularização e vocabulário, executou o código de busca e selecionou a melhor combinação com base nas métricas de validação cruzada |
| 4 | Classificação das intenções dos dados humanos de treino e teste | Utilizou IA generativa para sugerir os rótulos de intenção das frases humanas dos conjuntos de treino e teste | Solicitou à ferramenta de IA que classificasse cada frase com origem `humano` em uma das intenções do domínio, em `chitchat` ou em `fora_dominio` | O grupo revisou todas as classificações sugeridas pela IA nos dois conjuntos, corrigiu divergências e confirmou manualmente os rótulos finais; as frases mantiveram a origem `humano` |  
| 5 | Geração de dados sintéticos com LLM (scripts/gerar_dados_llm.py) | Gerar 550 frases sintéticas sem duplicatas (350 de domínio em 7 intenções + 100 de chitchat + 100 de fora_dominio com negativos difíceis) usando o modelo openai/gpt-6-luna | Prompts parametrizados variando 5 perfis de estilo (educado, informal/WhatsApp, com erros de digitação, ansioso/com pressa e curto de 1–4 palavras) e restrições negativas explícitas entre classes para evitar sobreposição. Exemplo: "Contexto: um chatbot de atendimento sobre 'Esportes na UFMS'. Gere 10 mensagens DIFERENTES que um estudante universitário brasileiro enviaria ao chatbot sobre o assunto: [classe]. Estilo: [perfil]. As mensagens NÃO podem ser sobre estes outros assuntos: [demais classes]..." (Registro completo gerado por scripts/gerar_dados_llm.py) | Revisou manualmente as frases geradas, filtrou ruídos/ambiguidades e selecionou os melhores exemplos para compor o conjunto de treino |  
| 6 | Verificação dos entregáveis antes da submissão | Utilizou IA para comparar o estado atual do repositório com as instruções e a checklist do trabalho, identificando entregáveis presentes e itens que ainda faltavam | Solicitou a verificação dos requisitos obrigatórios, dos arquivos do repositório, do notebook, dos modelos, dos dados, da documentação de IA e dos itens finais de entrega | Conferiu manualmente os resultados apontados pela IA, executou o verificador oficial do projeto e decidiu quais pendências precisavam ser resolvidas antes da entrega |  
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
