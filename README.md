<div align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" height="100" alt="Logo git">
</div>

# **Análise de Sentimentos em Avaliações de E-commerce**

## **Objetivo**

O projeto visa identificar padrões de sentimento nos comentários e relacioná-los às notas atribuídas pelos compradores, utilizando e comparando técnicas de Análise de Sentimentos em avaliações textuais de clientes com as ferramentas VADER, LeIA e TextBlob.

## **Autores**

João Pedro Caçula dos Santos

Juan Matheus de Oliveira Lopes 

Luiz Henrique dos Santos

Patrick Muniz de Aguiar

## **Disciplina**

**Projeto Integrador Interdisciplinar**

Prof. Dr. Felipe de Almeida Camargo

## **Sobre o projeto**

O projeto é organizado em três notebooks principais:

- **`01_analise_exploratoria.ipynb`** — Carregamento e exploração dos dados brutos do banco de dados (avaliações, clientes, pedidos, produtos, entre outros). Inclui tratamento de tipos, limpeza dos comentários (remoção de pontuação e maiúsculas), junção dos campos de título e mensagem, e exportação do dataset processado.

- **`02_analise_sentimentos.ipynb`** — Aplicação dos três modelos de análise de sentimentos sobre os comentários limpos. Cada modelo atribui uma pontuação numérica (compound score) ao texto, que é então classificada em cinco categorias: Muito Negativo, Negativo, Neutro, Positivo e Muito Positivo.

- **`03_discussoes.ipynb`** — Visualização e comparação da distribuição dos sentimentos gerados por cada ferramenta, utilizando gráficos de contagem para análise comparativa.

## **Como executar**

### Pré-requisitos

Certifique-se de ter o **Python** instalado. Em seguida, instale as dependências com:

```bash
pip install pandas numpy matplotlib seaborn
pip install vaderSentiment
pip install leia-br
pip install textblob
```

### Estrutura esperada de diretórios

```
projeto/
├── data/
│   ├── raw/           # CSVs originais (avaliacoes, clientes, pedidos, etc.)
│   └── processed/     # Arquivos parquet processados
├── docs/
│   ├── dicionario_de_dados.xlsx
│   ├── entidade_relacionamento.jpeg
│   ├── modelo_logico.jpeg
├── notebooks/
│   ├── 01_analise_exploratoria.ipynb
│   ├── 02_analise_sentimentos.ipynb
│   ├── 03_discussoes.ipynb
├── README.md
└── requirements.txt
```

### Executando os notebooks

Execute os notebooks **na ordem numérica**, pois cada um depende dos dados gerados pelo anterior:

1. `01_analise_exploratoria.ipynb` — Gera `avaliacoes.parquet`
2. `02_analise_sentimentos.ipynb` — Gera `resultados.parquet`
3. `03_discussoes.ipynb` — Utiliza os resultados para gerar os gráficos

---

<div align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/8/8c/SENAI_S%C3%A3o_Paulo_logo.png" height="100" alt="Logo SENAI">
</div>
