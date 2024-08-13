# Gerador de CPFs Válidos

Este código Python gera uma lista de 10.981 CPFs (Cadastro de Pessoas Físicas) válidos e os salva em um arquivo CSV.

## Requisitos

- Python 3.x
- Biblioteca `pandas`

## Instalação

1. Certifique-se de ter o Python 3.x instalado em seu sistema.
2. Instale a biblioteca `pandas` usando o seguinte comando:
   ```
   pip install pandas
   ```

## Uso

1. Abra o arquivo Python contendo o código.
2. Execute o script.
3. O programa gerará 10.981 CPFs válidos e salvará em um arquivo CSV chamado `cpfs_gerados.csv`.
4. O número de CPFs gerados pode ser alterado modificando o valor `10981` na linha `while len(unique_cpfs) < 10981:`.

## Variáveis

- `existing_cpfs`: conjunto para armazenar os CPFs gerados, evitando duplicatas.
- `unique_cpfs`: conjunto para armazenar os CPFs únicos gerados.
- `cpfs_df`: dataframe do pandas para armazenar os CPFs gerados.
- `csv_file_name`: nome do arquivo CSV onde os CPFs serão salvos.

## Funções

1. `calculate_check_digit(cpf_base)`: calcula o dígito verificador de um CPF base.
2. `generate_valid_cpf(existing_cpfs)`: gera um CPF válido único.

## Saída

O programa imprime o número de CPFs duplicados gerados.

Certifique-se de que o número de CPFs a serem gerados seja adequado para suas necessidades. Caso queira gerar um número diferente de CPFs, altere o valor na linha `while len(unique_cpfs) < 10981:`.