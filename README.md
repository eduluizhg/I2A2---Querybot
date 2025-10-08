Querybot - Curso I2A2 🤖💬
Converse com seus dados. Faça perguntas em linguagem natural e receba análises, gráficos e insights instantaneamente.

Este projeto foi desenvolvido como parte do curso I2A2, demonstrando a aplicação de múltiplos agentes de IA para análise de dados.

🎯 O que é o Querybot?
O Querybot é seu assistente pessoal para análise de dados. Esqueça planilhas complexas e códigos demorados. Com ele, você pode simplesmente "conversar" com seus arquivos CSV para:

✅ Fazer perguntas diretas sobre seus dados e obter respostas claras.

✅ Visualizar informações através de gráficos interativos gerados sob demanda.

✅ Extrair insights de negócio com interpretações feitas por IA.

✅ Receber o código Python utilizado para replicar qualquer análise.

✅ Manter o histórico de suas conversas para futuras consultas.

🏗️ Como Funciona?
A aplicação utiliza 5 agentes especializados que trabalham em conjunto:

1. CoordinatorAgent 🎯
O que faz: Analisa sua pergunta e decide qual agente é mais adequado

Quando usar: Sempre - é o agente que organiza todo o sistema

2. DataAnalystAgent 📈
O que faz: Realiza análises estatísticas detalhadas

Quando usar: Para perguntas como:

"Qual a média da coluna X?"

"Quantos registros temos?"

"Existe correlação entre as colunas A e B?"

"Quais são os valores únicos?"

3. VisualizationAgent 📊
O que faz: Gera código para criar gráficos interativos

Quando usar: Para pedidos como:

"Mostre um gráfico de barras da coluna X"

"Crie um histograma da idade"

"Faça um scatter plot entre preço e tamanho"

"Gere um heatmap de correlação"

4. ConsultantAgent 💡
O que faz: Interpreta os dados e fornece insights de negócio

Quando usar: Para perguntas como:

"O que esses dados significam para meu negócio?"

"Quais são as principais descobertas?"

"Que decisões devo tomar baseado nestes dados?"

"Quais são os riscos e oportunidades?"

5. CodeGeneratorAgent ⚙️
O que faz: Gera código Python completo para suas análises

Quando usar: Para pedidos como:

"Me dê o código para esta análise"

"Gere um notebook Jupyter"

"Crie um script Python para automatizar isso"

🚀 Como Usar
1. Instalação
Bash

# 1. Clone o repositório
cd rhein-ai-agent-challenge

# 2. Crie um ambiente virtual
python -m venv .venv

# 3. Ative o ambiente
# Windows:
.venv\Scripts\activate
# Linux/Mac:
source .venv/bin/activate

# 4. Instale as dependências
pip install -r requirements.txt
2. Configuração das Chaves de API
O Querybot precisa de chaves para o Google Gemini e (opcionalmente) para o Supabase.

Método 1: Streamlit Secrets (Recomendado)
Crie o arquivo .streamlit/secrets.toml com o seguinte conteúdo:

Ini, TOML

[custom]
google_api_key = "sua_chave_aqui"
supabase_url = "https://seu-projeto.supabase.co"
supabase_key = "sua_chave_supabase_aqui"
Método 2: Variáveis de Ambiente
Crie um arquivo .env baseado no .env.example:

Bash

cp .env.example .env
Edite o .env com suas chaves:

GOOGLE_API_KEY: Obtenha em Google AI Studio

SUPABASE_URL e SUPABASE_KEY: Obtenha em Supabase Dashboard

3. Executar a Aplicação
Bash

streamlit run app.py
Acesse a aplicação no navegador em http://localhost:8501.

4. Usando a Aplicação
Faça o Upload: Arraste um arquivo CSV para a barra lateral.

Converse com os Dados: Use o chat para fazer suas perguntas em português.

Explore Ideias: Clique nas perguntas sugeridas para guiar sua análise.

💡 Ideias de Conversa com os Dados
Veja como o Querybot transforma perguntas em respostas valiosas.

Cenário 1: Gestão de Vendas
Dataset: vendas.csv (colunas: produto, categoria, valor, data, regiao)

Imagine que você é um gestor de vendas. Você pode perguntar:

"Qual produto teve o pico de vendas no último mês?"

"Me mostre as vendas por categoria em um gráfico de pizza."

"A performance de qual região se destaca e por quê?"

"Gere o código Python para eu analisar a sazonalidade das vendas."

Cenário 2: Recursos Humanos
Dataset: funcionarios.csv (colunas: nome, idade, salario, departamento, tempo_casa)

Como analista de RH, você poderia investigar:

"Qual a média salarial por departamento?"

"Crie um histograma para visualizar a distribuição de idade na empresa."

"Existe alguma relação entre tempo de casa e salário? Mostre em um gráfico."

"Baseado nos dados, que insights temos sobre a retenção de talentos?"

Cenário 3: Marketing Digital
Dataset: campanhas.csv (colunas: campanha, canal, investimento, conversoes, receita)

Sendo um profissional de marketing, você pode perguntar:

"Qual canal de marketing apresenta o melhor Retorno Sobre Investimento (ROI)?"

"Faça um gráfico de dispersão mostrando a relação entre o investimento e a receita gerada."

"O que podemos concluir sobre a eficácia de nossas campanhas recentes?"

"Me dê o script para calcular as métricas de performance de cada campanha."

Datasets de Exemplo para Testar
Não tem um CSV à mão? Sem problemas. Use um destes datasets públicos para começar:

Titanic Dataset (sobreviventes do Titanic)

Baixar CSV

Iris Dataset (flores - dados científicos)

Baixar CSV

Wine Quality (avaliação de vinhos)

Baixar CSV

House Prices (preços de imóveis)

Baixar CSV

Obrigatórios
✅ Python 3.8 ou superior

✅ Chave da API do Google Gemini

Opcionais (mas recomendados)
✅ Conta no Supabase (para salvar histórico)

✅ Git (para controle de versão)

🔧 Dependências Principais
Biblioteca	Propósito
streamlit	Interface web da aplicação
langchain	Framework para agentes de IA
google-generativeai	Modelo de IA (Gemini)
pandas	Manipulação de dados
plotly	Criação de gráficos interativos
supabase	Banco de dados para histórico

Exportar para as Planilhas
🎨 Funcionalidades Avançadas
Cache Inteligente
Os gráficos são armazenados em cache para evitar recriação desnecessária.

Melhora a performance e reduz custos com API.

Histórico Persistente
Suas conversas e análises são salvas automaticamente.

Recupere sessões anteriores a qualquer momento.

Sugestões Dinâmicas
A IA sugere perguntas relevantes baseadas no contexto.

Melhora a experiência de exploração dos dados.

Execução Segura de Código
O código Python gerado é executado em ambiente isolado.

Previne execução de código malicioso.

🛠️ Estrutura do Projeto
rhein-ai-agent-challenge/
├── agents/               # Agentes especializados de IA
│   ├── coordinator.py    # Decide qual agente usar
│   ├── data_analyst.py   # Análises estatísticas
│   ├── visualization.py  # Geração de gráficos
│   ├── consultant.py     # Insights de negócio
│   └── code_generator.py # Geração de código
├── components/           # Componentes da interface
│   ├── ui_components.py  # Elementos visuais
│   └── suggestion_generator.py # Sugestões inteligentes
├── utils/                # Utilitários e helpers
│   ├── config.py         # Configurações da app
│   ├── data_loader.py    # Carregamento de CSVs
│   ├── memory.py         # Integração com banco
│   └── chart_cache.py    # Cache de gráficos
├── app.py                # Arquivo principal
├── requirements.txt      # Dependências Python
└── README.md             # Este arquivo
📊 Tipos de Análise Suportados
Análises Estatísticas
Estatísticas descritivas (média, mediana, desvio padrão)

Contagem de valores únicos e nulos

Identificação de outliers

Análise de correlação

Testes de hipóteses

Visualizações Disponíveis
Histogramas e distribuições

Gráficos de barras e colunas

Scatter plots e dispersão

Box plots e violin plots

Heatmaps de correlação

Gráficos de linha e área

Insights de Negócio
Interpretação de tendências

Identificação de padrões

Recomendações estratégicas

Análise de oportunidades

Detecção de anomalias

🔒 Segurança e Privacidade
✅ Dados locais: Seus arquivos CSV nunca saem do seu computador ou da sessão.

✅ Código isolado: Análises são executadas em ambiente seguro.

✅ API keys protegidas: Use o sistema de segredos do Streamlit.

✅ Histórico opcional: O uso do Supabase é totalmente opcional.

🆘 Suporte e Troubleshooting
Problemas Comuns
1. "Chave da API não configurada"

Bash

# Verifique se a chave está no arquivo .streamlit/secrets.toml
# ou nas variáveis de ambiente
2. "Erro ao carregar CSV"

Verifique se o arquivo é um CSV válido, separado por vírgulas.

Garanta que o arquivo possui cabeçalho e pelo menos uma linha de dados.

3. "Gráfico não aparece"

Aguarde alguns segundos, a geração pode levar um tempo.

Verifique se os dados nas colunas solicitadas são adequados para o gráfico pedido.

Logs e Debug
Para ver logs detalhados, altere a variável DEBUG_MODE para True no arquivo app.py.

❓ FAQ - Perguntas Frequentes
🔑 Configuração e API
P: Como obter a chave da API do Google Gemini?
R: Acesse https://makersuite.google.com/app/apikey, crie uma nova chave e copie para seu arquivo de configuração.

P: A aplicação funciona sem o Supabase?
R: Sim! O Supabase é opcional, usado apenas para salvar o histórico de conversas. Sem ele, a aplicação funciona normalmente, mas o histórico será perdido ao fechar a aba.

P: Quais são os custos da API do Google?
R: O Google Gemini oferece uma cota gratuita generosa. Para uso moderado, os custos são geralmente nulos ou muito baixos. Consulte a página de preços oficial.

📊 Dados e Análises
P: Quais formatos de arquivo são suportados?
R: Atualmente, apenas arquivos no formato .csv.

P: Há limite de tamanho para os arquivos?
R: Não há um limite fixo, mas datasets muito grandes (>100MB) podem deixar a aplicação lenta. Recomendamos começar com arquivos menores para uma melhor experiência.

P: Posso fazer perguntas em português?
R: Sim! O Querybot foi projetado para entender e responder em português brasileiro.

🔧 Problemas Técnicos
P: A aplicação não inicia. O que fazer?
R: Verifique se todas as dependências do requirements.txt foram instaladas no ambiente virtual correto e se a chave de API do Google está configurada.

P: Os gráficos não aparecem. Como resolver?
R: Reformule sua pergunta de forma mais direta, por exemplo: "crie um gráfico de barras da coluna X". Verifique também o console do terminal onde o Streamlit está rodando para ver se há mensagens de erro.

🚀 Uso Avançado
P: Como exportar o código gerado?
R: O código aparece diretamente na interface do chat. Você pode usar o botão de copiar e colar em seu editor de código ou notebook.

P: Posso usar outros modelos de IA?
R: A arquitetura atual é otimizada para o Google Gemini. Para usar outros modelos, seria necessário modificar os módulos dos agentes.

🔒 Limitações Conhecidas
O desempenho pode variar com datasets muito grandes.

A interpretação de perguntas muito complexas ou ambíguas pode não ser precisa.

O conhecimento da IA é limitado aos dados fornecidos no arquivo CSV.

🤝 Como Contribuir
Este é um projeto de aprendizado e exploração. Sugestões são bem-vindas!

Faça um fork do projeto

Crie uma branch para sua feature (git checkout -b feature/nova-feature)

Commit suas mudanças (git commit -m 'Adiciona nova feature')

Push para a branch (git push origin feature/nova-feature)

Abra um Pull Request

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para detalhes.

🙏 Principais ferramentas utilizadas
Google Gemini

Streamlit

LangChain

Plotly

Supabase