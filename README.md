# 🩳 Bermudas

Projeto em **R** voltado para **análise de dados**!
Importe, explore, manipule e visualize informações de vendas de um jeito simples e eficiente.

## ✨ Funcionalidades principais

* 📥 **Importação** de planilhas Excel
* 🔍 **Exploração** inicial dos dados
* 🛠 **Manipulação** com `dplyr`
* 📊 **Visualização** com `ggplot2`

## 🛠 Pré-requisitos

Antes de começar, instale o **R** e os pacotes necessários:

```r
install.packages("dplyr")
install.packages("readxl")
install.packages("ggplot2")
```

## 🚀 Como usar

1. **Clone o repositório ou baixe os arquivos**
2. **Deixe o arquivo `Vendas.xlsx` na mesma pasta do script**
3. **Execute o script no R**:

```r
library(dplyr)
library(readxl)
library(ggplot2)

# Importação dos dados
vendas_df <- read_excel("Vendas.xlsx")

# Visualização inicial
View(vendas_df)      # 👀 ver tabela completa
head(vendas_df)      # 🔝 6 primeiras linhas
str(vendas_df)       # 🧬 estrutura dos dados
```

4. **Adicione sua própria análise!** (exemplo divertido):

```r
# Filtrando vendas altas
vendas_filtradas <- vendas_df %>%
  filter(Valor > 1000)

# Criando gráfico 💹
ggplot(vendas_filtradas, aes(x = Produto, y = Valor)) +
  geom_col(fill = "skyblue") +
  labs(title = "Produtos com vendas acima de 1000")
```

## 📂 Estrutura do projeto

```
Bermudas/
│── README.md
│── script.R
│── Vendas.xlsx
```

## 📜 Licença

Distribuído sob a licença **MIT** – pode usar, modificar e compartilhar sem moderação! 😎
