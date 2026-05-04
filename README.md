# Regression House Price

Projeto de análise e modelagem de regressão para previsão de preços de imóveis, usando o conjunto de dados do desafio Ames Housing.

## Estrutura do repositório

- `README.md` - documentação do projeto.
- `requirements.txt` - dependências Python / Jupyter.
- `notebooks/analise_exploratoria.ipynb` - notebook principal com exploração de dados e testes iniciais.
- `src/data-processing.py` - módulo de processamento de dados (ponto de partida para limpeza e engenharia de features).
- `data/raw/` - dados originais:
  - `train.csv` - dados de treinamento com `SalePrice`.
  - `test.csv` - dados de teste sem `SalePrice`.
  - `sample_submission.csv` - modelo de submissão.
  - `data_description.txt` - descrição detalhada das features.
- `data/processed/` - saída de dados pré-processados (atualmente vazio).
- `venv/` - ambiente virtual local.

## Objetivo

Construir um pipeline de regressão que estime o preço de venda de imóveis com base nas características do dataset. A análise exploratória inicial está no notebook `notebooks/analise_exploratoria.ipynb`.

## Como preparar o ambiente

1. Abra o projeto em VS Code.
2. Ative o ambiente virtual existente ou crie um novo:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

3. Atualize o pip e instale dependências:

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

> Observação: o arquivo `requirements.txt` está em UTF-16. Se o pip reclamar de encoding, re-salve-o em UTF-8 antes de instalar.

## Como rodar

1. Certifique-se de que o ambiente virtual está ativado (veja seção anterior).
2. Para executar a análise exploratória, abra o notebook:

```bash
jupyter notebook notebooks/analise_exploratoria.ipynb
```

Ou no VS Code, clique com o botão direito no arquivo `notebooks/analise_exploratoria.ipynb` e selecione "Open in Notebook Editor".

3. Para executar scripts Python, use:

```bash
python src/data-processing.py
```

4. Para testar modelos ou gerar previsões, execute células no notebook ou crie novos scripts em `src/`.

## Fluxo de trabalho sugerido

1. Abra `notebooks/analise_exploratoria.ipynb` para revisar a análise e as ideias de modelagem.
2. Adicione funções de pré-processamento e engenharia de features em `src/data-processing.py`.
3. Importe os dados de `data/raw/` e gere saídas em `data/processed/`.
4. Teste modelos de regressão e valide com o conjunto de treino.
5. Gere previsões finais para `test.csv` e salve em um arquivo no formato de `sample_submission.csv`.

## Pontos importantes

- O arquivo `src/data-processing.py` está vazio no momento, então é o local ideal para começar a implementar o pipeline de limpeza e transformação.
- `data/processed/` está disponível para armazenar datasets tratados e facilitar reuso.
- O notebook `notebooks/analise_exploratoria.ipynb` contém a principal investigação dos dados.
- A `.gitignore` já ignora `venv/`, `__pycache__/` e arquivos temporários do notebook.

## Próximos passos recomendados

- Definir funções de carregamento, limpeza e feature engineering em `src/data-processing.py`.
- Implementar validação cruzada e métricas de erro (RMSE, MAE, R2).
- Testar diferentes modelos de regressão e comparar resultados.
- Automatizar a criação de submissão com um script ou notebook claro.
- Atualizar este README com notas de experimentos e os melhores modelos encontrados.
