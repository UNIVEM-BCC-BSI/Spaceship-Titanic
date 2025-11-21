# Trabalho Final - Machine Learning 🤖

**Disciplina:** Machine Learning  
**Professor:** Luis Hilario

---

## 📋 Sobre o Projeto

Este repositório contém o código fonte desenvolvido como trabalho final para a disciplina de Machine Learning. O projeto aborda o desafio **Spaceship Titanic**, onde o objetivo é criar um modelo preditivo para determinar quais passageiros foram transportados para uma dimensão alternativa.

## 🚀 Tecnologias Utilizadas

* **Python 3**
* **Pandas:** Manipulação e análise de dados.
* **NumPy:** Computação numérica.
* **Scikit-Learn:** Pré-processamento e modelo de Árvore de Decisão.
* **Matplotlib / Seaborn:** Visualização de dados.

## ⚙️ Funcionalidades do Script

O código executa um pipeline completo de Ciência de Dados:

1.  **Coleta de Dados:** Download automático dos arquivos `train.csv` e `test.csv` via Google Drive.
2.  **Engenharia de Atributos:**
    * Extração de `Group` e `GroupNumber` do `PassengerId`.
    * Decomposição da coluna `Cabin` em `Deck`, `CabinNum` e `Side`.
    * Criação da feature `TotalSpend` (soma de todos os gastos).
3.  **Tratamento de Dados (Limpeza Inteligente):**
    * Preenchimento de gastos nulos com `0`.
    * **Lógica de CryoSleep:** Dedução baseada nos gastos (se gastou > 0, não estava dormindo).
    * Imputação de idade pela **mediana** e categóricos pela **moda**.
4.  **Pré-processamento:**
    * Conversão de booleanos para inteiros.
    * **One-Hot Encoding** para variáveis categóricas.
5.  **Modelo de Machine Learning:**
    * Treinamento de um classificador **Decision Tree** (`DecisionTreeClassifier`).
    * Geração automática do arquivo `submission.csv`.

## 📦 Como Executar

### Pré-requisitos

Certifique-se de ter as bibliotecas instaladas. Você pode instalar tudo com o comando:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
