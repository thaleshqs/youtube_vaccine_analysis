# Análise do Discurso Sobre Vacinação no YouTube Brasileiro

Este repositório reúne os códigos e procedimentos utilizados no artigo **Análise do Discurso Sobre Vacinação no YouTube Brasileiro**. O objetivo do projeto é analisar comentários e conteúdos do YouTube relacionados à vacinação, utilizando técnicas de processamento de linguagem natural, modelos de linguagem de grande escala (LLMs) e modelagem de tópicos.

O fluxo metodológico do projeto é dividido em diferentes etapas, cada uma implementada em um repositório específico.
---

## Estrutura dos Repositórios

### `data`

O repositório **data** apresenta os dados (comprimidos em formato `.zip`) dos vídeos e comentários coletados do YouTube.

---

### `semantic_filtering`

O repositório **semantic_filtering** implementa a etapa de filtragem semântica do conjunto de dados.

Nessa etapa, os textos coletados são analisados utilizando o modelo **GPT-4o-mini** por meio da **API da OpenAI**. O objetivo é identificar e manter apenas conteúdos semanticamente relacionados ao tema de vacinação, removendo vídeos irrelevantes ou fora de contexto.

Essa etapa funciona como um filtro inicial para garantir maior qualidade nas análises subsequentes.

---

### `sample`

O repositório **sample** apresenta o processo de validação manual das classificações produzidas na etapa de filtragem semântica.

Para avaliar a qualidade das respostas do modelo GPT-4o-mini, foi construída uma amostra estratificada das saídas geradas. Essa amostra é analisada manualmente para medir o desempenho da filtragem e verificar possíveis erros de classificação.

---

### `topic_modeling`

O repositório **topic_modeling** contém os códigos utilizados para a extração e análise de tópicos presentes nos títulos dos vídeos e comentários.

A modelagem de tópicos é realizada com a biblioteca **BERTopic**, que combina embeddings semânticos, redução de dimensionalidade e algoritmos de clusterização para identificar temas recorrentes nos dados.

Essa etapa permite identificar os principais assuntos discutidos nos comentários sobre vacinação.

---

### `stance_detection`

O repositório **stance_detection** implementa a etapa de detecção de posicionamento (*stance detection*) em relação às vacinas.

Utilizando novamente o modelo GPT-4o-mini via API da OpenAI, os comentários são classificados em três categorias (Favorável, Contrário, Neutro) em relação à vacinação.

Essa classificação permite analisar a distribuição de opiniões presentes no discurso online sobre vacinas.

---

### `plots`

O repositório **plots** é responsável pela geração de visualizações e estatísticas descritivas do conjunto de dados.
