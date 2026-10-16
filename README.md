# CI1026 - Visão Computacional e Percepção — TA04
## Trabalho 4: Análise Exploratória e Classificação no Dataset Iris

Este repositório contém o relatório técnico desenvolvido em [Quarto](https://quarto.org/) com experimentos de análise estatística, redução de dimensionalidade (PCA), validação cruzada repetida (*Repeated Stratified K-Fold*) e classificação com K-NN sobre o dataset Iris.

---

## 1. Pré-requisitos

### 1.1 Python e dependências do projeto

1. Crie e ative um ambiente virtual:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate   # No Windows: .venv\Scripts\activate
   ```

2. Instale as dependências listadas no `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```

3. Registre o kernel do ambiente virtual para que o Quarto o encontre:
   ```bash
   python -m ipykernel install --user --name=trabalho4 --display-name "Python (Trabalho 4)"
   ```

---

## 2. Instalação e Configuração do Quarto

### 2.1 Download e instalação do Quarto CLI

- **macOS (via Homebrew):**
  ```bash
  brew install --cask quarto
  ```
  *Ou baixe o instalador oficial `.pkg` em [quarto.org/docs/get-started](https://quarto.org/docs/get-started/).*

- **Linux (Ubuntu/Debian):**
  ```bash
  # Baixe o pacote .deb na página de releases do Quarto
  sudo dpkg -i quarto-*.deb
  ```

- **Windows:**
  Baixe e execute o instalador `.msi` disponível em [quarto.org/docs/get-started](https://quarto.org/docs/get-started/).

### 2.2 Motor LaTeX para geração de PDF (TinyTeX)

Para renderizar documentos em formato PDF, o Quarto requer uma distribuição LaTeX. A forma mais leve e recomendada é instalar o **TinyTeX** diretamente pelo Quarto:

```bash
quarto install tinytex
```

---

## 3. Como Renderizar o Relatório em PDF

Com o ambiente virtual ativado e o Quarto instalado, execute o comando abaixo na raiz do repositório:

```bash
quarto render Trabalho_4.qmd --to pdf
```

Ao finalizar a execução, o arquivo compilado **`Trabalho_4.pdf`** será gerado automaticamente no mesmo diretório.

> **Dica:** Caso queira visualizar em formato HTML interativo:
> ```bash
> quarto render Trabalho_4.qmd --to html
> ```
