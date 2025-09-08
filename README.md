# Desafio de Ciência de Dados: Análise Cinematográfica para PProductions

---

## 📝 Visão Geral do Projeto

Este repositório contém a solução para o **Desafio de Cientista de Dados da Indicium**. O objetivo é realizar uma análise detalhada sobre um banco de dados cinematográfico para orientar o estúdio de Hollywood **PProductions** na tomada de decisões.


---

## 🎯 Entregas

✅ Análise Exploratória (EDA) completa com visualizações

✅ Modelo Preditivo para notas IMDB (Random Forest)

✅ Respostas às perguntas de negócio

✅ Previsão para "The Shawshank Redemption"

✅ Modelo salvo em formato .pkl

✅ Relatório completo em PDF

---

## 📁 Estrutura do Repositório

O projeto está organizado da seguinte forma:

```
/desafio-indicium-dados
|
|-- 📂 data/raw
|   |-- desafio_indicium_imdb.csv # Dataset original utilizado no projeto.
|
|-- 📂 models/
|   |-- imdb_rating_predictor.pkl
|   |-- mlb_binarizer.pkl
|   |-- tfidf_vectorizer.pkl
|
|-- 📂 notebooks/
|   |-- {arquivo}.ipynb  # Jupyter Notebook com toda a análise, desde o EDA até a modelagem.
|
|-- 📂 outputs/
|   |-- arquivos .xlsx e .png
|
|-- relatorio_analise.pdf          # Versão em PDF do relatório final.
|-- .gitignore                    # Arquivo para ignorar arquivos e pastas desnecessários.
|-- README.md                     # Este arquivo, com a documentação do projeto.
|-- requirements.txt              # Lista de dependências para reprodução do ambiente.
```

---

## 🚀 Como Executar o Projeto

Para reproduzir este projeto em sua máquina local, siga os passos abaixo:

**1. Pré-requisitos:**
- Ter o [Git](https://git-scm.com/) instalado.
- Ter o [Python 3.10](https://www.python.org/downloads/) ou superior instalado.

**2. Clone o Repositório:**
```bash
git clone [https://github.com/HeuerBcH/indicium-lighthouse-data-challenge.git](https://github.com/HeuerBcH/indicium-lighthouse-data-challenge.git)
cd SEU_REPOSITORIO
```

**3. Crie e Ative um Ambiente Virtual:**
```bash
# Criar o ambiente
python -m venv venv

# Ativar no Windows
venv\Scripts\activate

# Ativar no macOS/Linux
source venv/bin/activate
```

**4. Instale as Dependências:**
```bash
# Instalando requisitos do projeto
pip install -r requirements.txt
```

**5. Execute o Jupyter Notebook**

Após executar o comando, o JupyterLab abrirá em seu navegador. Navegue até a pasta `notebooks/` e abra o arquivo `relatorio_analise.ipynb` para ver e executar o código.

---

### Respondendo às Perguntas do Desafio

Qual filme você recomendaria para uma pessoa que você não conhece? <b> Recomendo os filmes identificados na análise de filmes populares, que combinam altas notas do IMDB, boa avaliação crítica (Meta_score) e grande engajamento do público (número de votos). Esses filmes representam opções consolidadas e de baixo risco, pois foram bem recebidos tanto pela crítica quanto pelo público em geral. Base da Resposta: Análise do DataFrame filme_popular que filtrou filmes acima do terceiro quartil em IMDB_Rating, Meta_score e No_of_Votes, ordenados por maior faturamento. </b>

Quais são os principais fatores que estão relacionados com alta expectativa de faturamento de um filme? <b> Número de votos no IMDB, Combinações específicas de gêneros (Action+Adventure+Sci-Fi, Adventure+Animation+Comedy…), Ano de lançamento (Filmes mais recentes tendem a maior faturamento) e Duração do filme (Filmes mais longos associados a maiores produções). Base da Resposta: Análise de correlação de Spearman/Kendall e estudo de performance por combinações de gêneros. </b>

Quais insights podem ser tirados com a coluna Overview? É possível inferir o gênero do filme a partir dessa coluna? <b> Sim, é possível inferir o gênero a partir da coluna Overview. A análise TF-IDF identificou padrões textuais específicos. Palavras como "family", "love", "life" associadas a Drama e Romance. Termos como "war", "world", "army" relacionados a Action e Adventure. "murder", "police", "crime" característicos de Crime e Thriller. Base da Resposta: Matriz de importância de palavras por gênero gerada pelo heatmap e análise TF-IDF. </b>

Explique como você faria a previsão da nota do imdb a partir dos dados. Quais variáveis e/ou suas transformações você utilizou e por quê? Qual tipo de problema estamos resolvendo (regressão, classificação)? Qual modelo melhor se aproxima dos dados e quais seus prós e contras? Qual medida de performance do modelo foi escolhida e por quê? <b>
A previsão foi realizada através de: 
Tipo de problema: Regressão
Variáveis utilizadas: 5 numéricas, 20 de gênero (MultiLabelBinarizer), 20 textuais (TF-IDF)
Modelo escolhido: Random Forest
Métricas de performance: MAE (erro médio em pontos) e R² (variância explicada)
Justificativa: O Random Forest foi superior à Regressão Linear por capturar relações não-lineares e oferecer feature importance. </b>

Qual seria a nota do IMDB de “The Shawshank Redemption”? <b> Para "The Shawshank Redemption", a nota prevista é 8.80, enquanto a nota real é 9.30, resultando em um erro de 0.50 pontos. Base da Resposta: Aplicação do modelo Random Forest treinado nas características do filme exemplo. </b>

---

Entre em contato:

[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bernardo-heuer-45571334b/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HeuerBcH)
