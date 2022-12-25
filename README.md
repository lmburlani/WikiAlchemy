# WikiAlchemy

WikiAlchemy é uma plataforma de análise de dados que combina o poder da Wikipedia e do SQLAlchemy. Com WikiAlchemy, é possível extrair informações da Wikipedia e armazená-las em um banco de dados SQL para análise posterior.

## Recursos

- Extração de dados da Wikipedia: com WikiAlchemy, é possível puxar uma amostragem de artigos e links da Wikipedia para armazenamento em um banco de dados SQL.
- Pré-processamento de dados: o WikiAlchemy inclui funções de pré-processamento de dados, como seleção de uma amostra de artigos e adição de uma coluna com os links dos artigos.
- Armazenamento em banco de dados SQL: o WikiAlchemy armazena os dados extraídos da Wikipedia em um banco de dados SQL, permitindo análises posteriores.

## Instalação

WikiAlchemy

O WikiAlchemy é uma ferramenta de análise de dados que permite extrair informações da Wikipedia e armazená-las em um banco de dados SQL para análise posterior. O WikiAlchemy inclui funções de pré-processamento de dados e é compatível com o SQLAlchemy.
Instalação

Para instalar o WikiAlchemy, basta clonar o repositório do Github e instalar as dependências usando o pip:
 
 ```
 git clone https://github.com/lmburlani/WikiAlchemy
cd WikiAlchemy
pip install -r requirements.txt
 ```

## Uso
Para usar o WikiAlchemy, basta seguir os seguintes passos:

1. Inicie a sessão no banco de dados SQL:

 ```
 engine = create_engine("postgresql://user:password@localhost:5432/database")
 ```
 
 2. Chame a função preprocessar_dados_wikipedia() passando a URL da página da Wikipedia que deseja extrair:
 
 ```
 url_pagina = "https://pt.wikipedia.org/wiki/Lista_de_fil%C3%B3sofos"
df = preprocessar_dados_wikipedia(url_pagina)
 ```
 
 3. Armazene o dataframe no banco de dados usando o método to_sql() do Pandas:

```
df.to_sql("artigos", engine, if_exists="replace")
```

Agora os dados extraídos da Wikipedia estão armazenados no banco de dados SQL e prontos para análise.
 
