# ClearBank — Análise Financeira com Python

Desafio final do módulo de Python aplicado a análise de dados. O notebook lê o histórico
mensal de transações exportado pela ClearBank, valida e limpa os registros, calcula
métricas financeiras por mês, sinaliza transações suspeitas e exporta o resultado em JSON.

## Como executar

1. Abra `desafio-final.ipynb` no Google Colab ou no Jupyter Notebook local (Python 3.10+).
2. Garanta que o arquivo `transacoes.csv` esteja na mesma pasta do notebook.
3. Execute todas as células em ordem (leitura → validação → datas/métricas → exibição →
   exportação → célula de execução principal).

Para rodar localmente sem Jupyter, a mesma lógica também pode ser executada como script:
o notebook não depende de bibliotecas externas na parte obrigatória (usa apenas
`csv`, `json` e `datetime` da biblioteca padrão).

## O que o notebook gera

- Um resumo de limpeza no terminal (total de linhas lidas, válidas e inválidas).
- Um relatório mensal formatado no terminal (transações, total de crédito/débito, saldo,
  média, maior e menor valor por mês) e a lista de transações suspeitas
  (valor acima de `LIMITE_SUSPEITO = R$ 10.000,00`).
- O arquivo `relatorio.json`, com o mesmo conteúdo do relatório em formato estruturado.
