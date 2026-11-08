# Livro-Caixa: controle financeiro pessoal

Aplicativo web de uma página só (HTML + JavaScript, sem dependências) para controlar as finanças pessoais.

## Funcionalidades

- **Contas bancárias**: cadastro com saldo inicial, saldo atual e previsto, e extrato mensal com saldo após cada lançamento.
- **Cartões de crédito**: limite, dia de fechamento e de vencimento. Cada compra entra automaticamente na fatura certa, e você pode trocar a fatura manualmente. Também aceita compras parceladas (uma parcela por fatura), estornos e pagamento total ou parcial da fatura, à vista ou agendado.
- **Categorias** de despesa e de receita, com uma lista padrão para começar.
- **Lançamentos pendentes** (contas a pagar e a receber): não alteram o saldo até serem efetivados. Na efetivação dá para ajustar a data, o valor (juros ou desconto) e a conta.
- **Planejamento**: limite de gasto por categoria em cada mês, com previsto versus realizado, status (dentro, atenção ou estourou), ritmo do mês, valor disponível por dia, gastos fora do planejamento, média dos últimos 3 meses e cópia do planejamento do mês anterior.
- **Balanço mensal**: receitas e despesas do mês por categoria, em duas colunas, com o saldo do mês no topo, setas para trocar de mês e opção de incluir ou não os pendentes.
- **Repetição mensal** de despesas e receitas (contas fixas).
- **Painel** com saldo, valores a pagar e a receber, saldo previsto, vencimentos dos próximos 30 dias e despesas do mês por categoria.
- **Importar do Excel**: duas importações (transações em contas e compras no cartão, com cartão e mês de vencimento da fatura). Cada uma tem um modelo .xlsx para baixar, com uma linha de exemplo e uma aba de instruções, além de prévia antes de gravar, aviso de duplicados e opção de desfazer a importação.
- **Backup** em JSON (copiar e importar).

## Como usar

- **Publicado no claude.ai**: os dados ficam salvos na conta Claude do usuário, em uma área privada que só ele vê.
- **Localmente**: abra o `index.html` no navegador. Nesse caso, os dados ficam salvos só naquele navegador (localStorage).

## Regra da fatura

A fatura é identificada pelo mês de vencimento. Uma compra feita **no dia do fechamento ou depois dele** vai para a fatura seguinte.
