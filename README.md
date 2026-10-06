# Análise Exploratória — Diabetes (Pima Indians)

Análise exploratória de dados (EDA) sobre o dataset Pima Indians Diabetes, usando Python para investigar quais fatores clínicos mais se relacionam com o diagnóstico de diabetes.

## Objetivo

Explorar os dados de 768 pacientes, tratar problemas de qualidade e identificar quais variáveis têm maior relação com o diagnóstico de diabetes, apresentando os achados em gráficos claros.

## Tecnologias

- Python 3.14
- Pandas — manipulação de dados
- NumPy — tratamento de valores
- Matplotlib e Seaborn — visualização de dados
- Jupyter Notebook (VS Code)

## Estrutura do Dataset

768 pacientes e 9 colunas:

- **Pregnancies** — número de gestações
- **Glucose** — nível de glicose no sangue
- **BloodPressure** — pressão arterial
- **SkinThickness** — espessura da pele
- **Insulin** — nível de insulina
- **BMI** — índice de massa corporal (IMC)
- **DiabetesPedigreeFunction** — histórico familiar de diabetes
- **Age** — idade
- **Outcome** — diagnóstico (0 = não tem, 1 = tem diabetes)

## Arquivos

- `analise.ipynb` — notebook com toda a análise e os gráficos
- `diabetes.csv` — base de dados utilizada
- `README.md` — este arquivo

## Análises Realizadas

### 1. Qualidade dos dados

Colunas como Glucose, BloodPressure, SkinThickness, Insulin e BMI apresentavam valor mínimo igual a zero — medicamente impossível. Esses zeros eram dados faltantes disfarçados.

> **Insight:** antes de qualquer análise, foi preciso substituir os zeros pela mediana de cada coluna. Sem esse tratamento, as conclusões estariam distorcidas.

### 2. Distribuição dos diagnósticos

Dos 768 pacientes, cerca de 35% têm diabetes (268 casos) e 65% não têm (500 casos).

> **Insight:** a base é desbalanceada, com mais casos negativos — um ponto de atenção para futuros modelos preditivos.

### 3. Glicose por diagnóstico

Quem tem diabetes apresenta mediana de glicose em torno de 140, contra cerca de 107 em quem não tem.

> **Insight:** a glicose se mostrou o separador mais claro entre os dois grupos.

### 4. Correlação entre variáveis

A glicose tem a maior correlação com o diagnóstico (0,49), seguida por BMI (0,31), idade (0,24) e número de gestações (0,22).

> **Insight:** glicose e IMC são os fatores mais associados ao diabetes nesta base — informação útil para priorizar quais indicadores monitorar.

## Conceitos Demonstrados

- Carregamento e inspeção de dados com Pandas
- Detecção e tratamento de dados faltantes
- Estatística descritiva
- Visualização de dados (gráfico de barras, boxplot e mapa de calor)
- Análise de correlação

## Como Executar

1. Instale as bibliotecas: `python -m pip install pandas numpy matplotlib seaborn`
2. Abra o `analise.ipynb` no VS Code ou Jupyter
3. Clique em **Run All** para rodar todas as células

---

**Nathan Filipe Rosa de Souza**
[GitHub](https://github.com/nathanfilipekz) · [LinkedIn](https://www.linkedin.com/in/nathan-filipe-rosa-de-souza/)