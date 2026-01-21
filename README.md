# Análise de Churn – TelecomX

Projeto de análise exploratória de dados de churn de uma operadora de telecom, utilizando Python e Pandas.

## Dados

- Arquivo JSON com informações de cliente, telefone, internet, conta e indicador de churn.
- Após normalização, os dados foram combinados em um único DataFrame (`df_final`) com 7.267 clientes e 21 colunas.

## Etapas da análise

1. Leitura do JSON e normalização dos campos aninhados (`customer`, `phone`, `internet`, `account`).
2. Junção das tabelas em `df_final` e merge com `customerID` e `Churn`.
3. Limpeza e transformação:
   - Conversão de respostas `Yes/No` para 0 e 1.
   - Conversão de `Churn` para tipo numérico.
4. Análises descritivas:
   - Médias de `tenure` e `Charges.Monthly` por `Churn` e por tipo de contrato.
   - Taxas de churn por serviços contratados e método de pagamento.
5. Visualizações:
   - Quantidade de clientes por `Churn`.
   - Percentual de clientes em churn por método de pagamento.
   - Taxa de churn por tipo de contrato.

## Principais conclusões

- A maior parte dos clientes não cancela, mas a taxa de churn é significativamente mais alta em contratos *Month‑to‑month* em comparação com contratos de 1 ou 2 anos.
- Cerca de 42% dos clientes com contrato *Month‑to‑month* dão churn, tornando esse grupo o principal foco de risco.
- Contratos de 1 e 2 anos apresentam churn bem menor, indicando efeito de fidelização.
- Clientes que pagam via *Electronic check* têm o maior percentual de churn entre os métodos de pagamento.

## Próximos passos (possíveis)

- Criar segmentações adicionais por tipo de serviço de internet e suporte.
- Testar modelos preditivos de churn com base nas variáveis tratadas.
