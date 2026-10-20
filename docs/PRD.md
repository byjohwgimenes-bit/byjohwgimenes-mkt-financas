# PRD simplificado

## Produto

ByJohwGimenes MKT — organização financeira para profissionais de marketing.

## Público

Freelancers de marketing, social media e criadores que precisam organizar os recebimentos de seus serviços e os custos de sua atividade.

## Problema

O controle manual e fragmentado dificulta acompanhar entradas, ferramentas, freelancers, anúncios e a formação de uma reserva.

## Objetivo

Permitir registrar movimentações, consultar um resumo mensal e estabelecer uma meta de economia em um fluxo simples.

## Fluxo principal

Registrar receita ou despesa → visualizar saldo mensal → simular economia → criar meta → acompanhar valor reservado.

## Escopo implementado

| Área | Comportamento |
| --- | --- |
| Painel | Receitas, despesas, saldo, quantidade de metas e despesas por categoria no mês selecionado |
| Movimentações | Adicionar, editar e excluir lançamentos; cliente ou fornecedor; filtro por tipo |
| Metas | Criar, excluir e atualizar o total reservado manualmente |
| Plano | Dividir valor da meta pelo prazo em meses e comparar com o saldo mensal |
| Persistência | Salvar dados apenas no navegador |

## Regras

- Valores de lançamentos e metas devem ser positivos.
- Meses do plano devem ser inteiros entre 1 e 120.
- O usuário confirma exclusões.
- O plano não promete rendimentos nem executa transações.
- Metas não deduzem valores automaticamente do saldo.
- Repasses de mídia devem ficar identificados em categoria própria.

## Agente de IA proposto para evolução

Interpretar mensagens como “Recebi R$ 1.500 do cliente X pela gestão de redes sociais”; sugerir descrição, valor, data, cliente e categoria; pedir dados ausentes; apresentar o registro para confirmação. Analisar somente dados disponíveis e explicar a base de suas sugestões. Não salvar nem movimentar valores sem confirmação.

Este agente ainda não está implementado. A versão atual contém um simulador local de planejamento.

## Critérios de aceitação

1. Um lançamento confirmado aparece no mês correto e atualiza o saldo.
2. Edição e exclusão recalculam os totais.
3. Uma meta de R$ 3.000 em seis meses produz R$ 500 por mês.
4. O plano informa quando o saldo registrado é inferior à economia mensal desejada.
5. A página informa claramente que o assistente é uma simulação.
6. Recarregar a página preserva dados quando o armazenamento do navegador está disponível.

## Fora do escopo atual

IA real, integração bancária, pagamentos, previsão de receitas, investimentos, gestão fiscal, backup remoto e múltiplos usuários.
