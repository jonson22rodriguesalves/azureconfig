* 📊Azure AI Search - Configuração e Análise de Sentimentos
* Este repositório contém um guia passo a passo para configurar uma pesquisa cognitiva com Azure AI Search,
* integrada a modelos de análise de sentimentos do Azure AI Language. Além disso, apresenta insights,
* ferramentas complementares e aprendizados adquiridos durante o processo.
* 
* 📌 Passo a Passo para Configurar uma Pesquisa com Azure AI Search
* 1. Criar um Recurso no Azure
*    Acesse o Portal Azure.
* 
* Crie um recurso do Azure AI Search.
* 
* Defina nome, região e tipo de pricing tier (ex: Free para testes).
* 
* 2. Configurar um Index (Índice de Pesquisa)
*    No serviço criado, vá para "Índices" e clique em "+ Novo Índice".
* 
* Defina campos como:
* 
* id (chave primária)
* 
* text (texto a ser analisado)
* 
* sentiment (resultado da análise)
* 
* confidenceScores (pontuação de confiança)
* 
* 3. Integrar com Azure AI Language (Análise de Sentimentos)
*    Habilite "Habilidades Cognitivas" (Cognitive Skills) no seu índice.
* 
* Adicione a habilidade "Sentiment Analysis" e associe-a ao campo text.
* 
* Configure para extrair frases-chave e sentimentos.
* 
* 4. Carregar Dados (Dataset de Exemplo)
*    Use "Importar Dados" para subir um arquivo .json ou .csv com mensagens para análise.
* 
* Exemplo de estrutura:
* 
* {
* "id": "1",
* "text": "The system is very slow today.",
* "source": "user_feedback"
* }
* 
* Executar a Pesquisa e Visualizar Resultados
* No Search Explorer, teste consultas como:
* 
* sentiment:positive (filtrar por sentimentos positivos)
* 
* search=slow&highlight=text (buscar termos negativos)
* 
* 🔍 Insights e Aprendizados
* ✅ Padronização de Dados:
* 
* A análise de sentimentos funciona melhor quando os textos estão bem estruturados (evite gírias ou linguagem muito informal).
* 
* ✅ Filtros Úteis:
* 
* É possível segmentar resultados por nível de confiança (ex: confidenceScores.positive gt 0.7).
* 
* ✅ Aplicações Práticas:
* 
* Chatbots: Melhorar respostas automáticas com base no tom do usuário.
* 
* Helpdesk: Priorizar tickets com sentimentos negativos/urgentes.
* 
* Pesquisa de Satisfação: Analisar feedbacks de clientes em escala.
* 
* ⚠️ Desafios Encontrados:
* 
* Falsos positivos: Frases como "Não é ruim"* podem ser classificadas erroneamente.
* 
* Limitação de idioma: O modelo padrão tem melhor desempenho em inglês.
* 
* 🛠️ Ferramentas que se Beneficiam
* Ferramenta	Aplicação
* Power BI	Dashboard de análise de feedbacks
* Microsoft Teams	Alertas automáticos para mensagens críticas
* Azure Logic Apps	Automação de respostas com base no sentimento
* CRM (Dynamics 365)	Priorização de leads/clientes insatisfeitos