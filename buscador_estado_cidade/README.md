## Descrição

Este script em Python é projetado para buscar informações de localização (estado e cidade) a partir de uma lista de Códigos de Endereçamento Postal (CEPs) brasileiros. Ele utiliza a API pública do ViaCEP para obter os dados e, em seguida, grava as informações em um arquivo CSV.

## Funcionalidades

- **Busca de CEPs**: O script consulta a API do ViaCEP para cada CEP fornecido.
- **Tratamento de Erros**: Caso um CEP inválido seja fornecido, o script lida com a situação sem interromper a execução.
- **Geração de CSV**: Os resultados são salvos em um arquivo CSV, facilitando o acesso e a análise posterior.

## Requisitos

- Python 3.x
- Bibliotecas:
  - `requests`: Para realizar requisições HTTP.
  - `csv`: Para manipulação de arquivos CSV.

Você pode instalar a biblioteca `requests` utilizando o seguinte comando:

```bash
pip install requests
```

## Como Usar

1. **Clone o repositório ou copie o código** para um arquivo Python (por exemplo, `consulta_cep.py`).
2. **Edite a lista de CEPs** na variável `ceps` se desejar consultar outros CEPs.
3. **Execute o script**:

   ```bash
   python consulta_cep.py
   ```

4. Após a execução, um arquivo chamado `resultado.csv` será criado no mesmo diretório do script, contendo os CEPs, estados e cidades correspondentes.

## Estrutura do Código

### Importações

```python
import csv
import requests
```

As bibliotecas `csv` e `requests` são importadas para manipulação de arquivos e requisições HTTP, respectivamente.

### Lista de CEPs

```python
ceps = ['35171103', '35181204', ...]
```

Aqui, você pode adicionar ou remover CEPs conforme necessário.

### Função `obter_estado_cidade`

```python
def obter_estado_cidade(cep):
    ...
```

Esta função realiza a requisição à API do ViaCEP e retorna o estado e a cidade correspondentes ao CEP informado. Se o CEP for inválido, retorna `None`.

### Loop de Processamento

```python
for cep in ceps:
    ...
```

O loop percorre cada CEP na lista, chama a função `obter_estado_cidade` e armazena os resultados.

### Geração do Arquivo CSV

```python
with open('resultado.csv', 'w', newline='') as csvfile:
    ...
```

Os resultados são gravados em um arquivo CSV, com cabeçalhos apropriados.

## Exemplo de Saída

Após a execução do script, o arquivo `resultado.csv` terá a seguinte estrutura:

```
CEP,Estado,Cidade
35171103,MG,Governador Valadares
35181204,MG,Ipatinga
...
```
