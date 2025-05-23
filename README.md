# Análise-Ambiental
Relatório analítico sobre desmatamento e desenvolvimento social em comunidades do Pará, utilizando técnicas de clusterização e análise espacial. O estudo identifica áreas críticas com alto desmatamento (>67,5%) e baixo desenvolvimento, propondo o uso de inteligência artificial para apoiar políticas públicas e ações de mitigação.

🎯 **Objetivo**
Identificar padrões de risco em comunidades com:

Alto índice de desmatamento (>67,5%)

Baixa densidade populacional

Ausência de infraestrutura essencial (escolas e unidades de saúde)

Propor o uso de algoritmos de clusterização para automatizar a identificação dessas comunidades e apoiar políticas públicas.


🛠️ **Metodologia**
Análise exploratória de dados (EDA)

Criação de métricas de risco: índice de desmatamento, densidade e desenvolvimento social

Clusterização (agrupamento de comunidades)

Visualização espacial com mapa baseado em latitude e longitude das comunidades críticas

📊 ***Resultados**
Identificação de clusters com múltiplos fatores de risco

Mapa com a localização das comunidades mais vulneráveis

Recomendações para aplicação de técnicas de IA, como K-Means e DBSCAN

📈 **Gráficos e Visualizações**

O repositório inclui gráficos gerados a partir da análise exploratória e de clusterização, como:

Distribuição dos Índices de Desmatamento e Densidade: evidenciando comunidades com alto risco socioambiental.

Mapa Geográfico das Comunidades Críticas: visualização espacial das localidades com alto desmatamento e baixo desenvolvimento, usando latitude e longitude.

Gráfico de Clusters: separação das comunidades em grupos com características socioambientais semelhantes, facilitando a identificação de padrões.

As imagens podem ser encontradas na pasta /imagens deste repositório.

**Análise Inicial das Comunidades**

Na primeira etapa da análise, examinamos as comunidades considerando as seguintes colunas numéricas do dataset: desmatamento, densidade populacional, desenvolvimento e renda.

O índice de desenvolvimento foi criado a partir da soma das variáveis binárias escola e saúde, representando a presença ou ausência de infraestrutura básica (escola e unidade de saúde) em cada comunidade. Dessa forma, o desenvolvimento varia de 0 (sem escola nem saúde) a 2 (com ambas).

Essa métrica permitiu relacionar o nível de infraestrutura com os índices de desmatamento e densidade, auxiliando na identificação de comunidades com alto impacto ambiental e baixa oferta de serviços essenciais.

![image](https://github.com/user-attachments/assets/ef3bbb5b-aca6-4fe5-b7a1-4d69fa2533bd)

As correlações entre as variáveis são muito fracas (próximas de 0).

Não há relação forte entre desmatamento, densidade, desenvolvimento e renda.


🤖 **Aplicação de Técnicas de Inteligência Artificial**

1. Clusterização
Utilizei métodos não supervisionados, como o K-Means, para agrupar automaticamente comunidades com perfis semelhantes de risco ambiental e social. Acredito que essa abordagem ajudaria a identificar grupos prioritários para políticas públicas e ações de mitigação de forma mais eficiente.

- Clustering com K-means (3 clusters) usando StandardScaler para padronizar os dados
- Agrupa as comunidades com base em 'renda', 'desmatamento' e 'densidade' (se disponíveis)
- Exibe a distribuição dos clusters e médias das variáveis e do desenvolvimento em cada grupo

![image](https://github.com/user-attachments/assets/34c992b7-d6f4-4f82-a499-d8d07a046c66)

O gráfico apresentado tem como objetivo facilitar a compreensão das características das comunidades analisadas, agrupadas em clusters segundo os índices de desmatamento, densidade populacional, renda e desenvolvimento social. Ao comparar visualmente as médias desses indicadores para cada cluster, é possível identificar padrões e diferenças importantes entre os grupos. Por exemplo, ele evidencia quais comunidades enfrentam maior desmatamento aliado a baixa densidade e menor acesso a serviços essenciais, revelando suas vulnerabilidades socioambientais. 


3. Random Forest
Aplicação da Random Forest para classificar e prever os níveis de desenvolvimento das comunidades, utilizando variáveis como desmatamento, densidade e infraestrutura. Considero essa técnica importante para construir modelos preditivos robustos, que podem antecipar áreas em risco e apoiar a tomada de decisões estratégicas.

Importância das variáveis:
  renda: 0.338
  desmatamento: 0.337
  densidade: 0.325

O modelo Random Forest indicou que as variáveis renda, desmatamento e densidade 
possuem importâncias semelhantes na predição do desenvolvimento, com valores próximos a 33% cada uma. Isso mostra que o desenvolvimento das comunidades é influenciado de forma equilibrada por fatores econômicos (renda), ambientais (desmatamento) e sociais/urbanos (densidade populacional).


## 📊 Resultados Visuais

Aqui estão alguns gráficos que geraram insights importantes na análise:  

![Distribuição de Desmatamento](imagens/desmatamento.png)  
*Distribuição dos índices de desmatamento por comunidade.*

![Mapa das Comunidades](imagens/mapa_comunidades.png)  
*Mapa com as localizações geográficas das comunidades críticas.*

![Clusters Identificados](imagens/clusters.png)  
*Gráfico mostrando a segmentação das comunidades em clusters com características socioambientais similares.*





📝 Como usar
Clone o repositório:

git clone https://github.com/JaelinePina/An-lise-Ambiental.git  


Navegue até a pasta:

Visualize os arquivos de análise (relatorio.pdf, mapa_comunidades.png, analise_clusters.ipynb).

✅ Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

🖊️ Autoria
Relatório desenvolvido por Jaeline Pina
