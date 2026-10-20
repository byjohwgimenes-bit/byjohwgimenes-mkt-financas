# ByJohwGimenes MKT — Finanças para profissionais de marketing

Aplicativo web desenvolvido com Vibe Coding para organizar receitas, despesas e metas financeiras de quem trabalha com marketing, social media e criação de conteúdo.

**Projeto de estudos para o Bootcamp DIO.**

[Acessar o protótipo](https://saldo-studio-marketing.wisereed8.chatgpt.site)

## Problema e proposta

Profissionais de marketing precisam acompanhar pagamentos de clientes, projetos avulsos, assinaturas de ferramentas, freelancers e anúncios. Registros dispersos dificultam entender o saldo e planejar uma reserva.

O aplicativo reúne esses registros em um painel mensal e oferece um simulador de economia que compara a meta com o saldo informado. A proposta adapta o tema de organização de finanças pessoais ao contexto de trabalho do profissional de marketing. Ainda não existe separação completa entre orçamento pessoal e profissional.

## Funcionalidades implementadas

- Registro, edição e exclusão de receitas e despesas confirmadas.
- Identificação de cliente ou fornecedor e categoria.
- Resumo mensal de receitas, despesas e saldo.
- Filtros por mês e tipo de movimentação.
- Despesas agrupadas por categoria.
- Criação de metas e atualização manual do valor reservado.
- Simulador de economia mensal e criação de uma meta a partir do plano.
- Persistência local usando `localStorage`.
- Identidade visual ByJohwGimenes e layout responsivo.

## Como executar

Não exige instalação de dependências nem chave de API.

1. Baixe ou clone o repositório.
2. Na pasta do projeto, execute `python3 -m http.server 8000` (no Windows, pode ser `python -m http.server 8000`).
3. Acesse `http://localhost:8000`.

Também é possível abrir `index.html` diretamente para uma demonstração rápida, mas o servidor local oferece um endereço estável para o armazenamento do navegador.

## Teste rápido

1. Observe os dados fictícios do mês atual: receitas de R$ 4.200,00, despesas de R$ 1.170,00 e saldo de R$ 3.030,00.
2. Adicione uma despesa de R$ 100,00 no mesmo mês. O saldo deve passar para R$ 2.930,00.
3. Edite ou exclua o lançamento e confira a atualização.
4. Em “Plano de economia”, simule uma meta de R$ 3.000,00 em seis meses. A economia mensal deve ser de R$ 500,00.
5. Crie a meta e atualize manualmente o total reservado.
6. Recarregue a página e confira a persistência dos registros.

O cálculo de R$ 500,00/mês e sua comparação com o saldo de R$ 3.030,00 foram verificados na interface durante o desenvolvimento. Os demais passos acima são um roteiro para reprodução, e não uma declaração de testes automatizados executados.

## Tecnologias

HTML, CSS e JavaScript, sem frameworks ou bibliotecas externas. Os cálculos e os dados ficam no navegador.

## IA e Vibe Coding: o que foi realmente utilizado

O aplicativo foi construído por conversa com o ChatGPT/Codex e publicado por meio de Sites. O conceito foi refinado durante a conversa: finanças pessoais → conexão com marketing → finanças para profissionais de marketing → nome e logos da marca.

**O assistente do aplicativo não possui IA conectada.** Ele executa cálculos determinísticos e apresenta orientações predefinidas com base nos dados registrados. A evolução proposta é conectar um modelo de IA para interpretar mensagens em linguagem natural e elaborar sugestões explicáveis, sempre pedindo confirmação antes de salvar registros.

O conceito foi revisado no Microsoft Copilot em 20/10/2026. As 19 capturas reais estão no [índice de evidências](docs/prints/README.md). O Lovable não foi utilizado. O desenvolvimento do protótipo ocorreu com ChatGPT/Codex.

## Limitações

- Sem login, banco de dados remoto, sincronização entre dispositivos ou integração bancária.
- Limpar os dados do navegador apaga os lançamentos; não existe exportação de backup implementada.
- Metas são controles separados: atualizar uma reserva não altera o saldo nem transfere dinheiro.
- Lançamentos representam valores recebidos ou pagos; não há contas a pagar ou a receber.
- O saldo não representa lucro contábil e não considera valores ainda não lançados.
- Repasses de mídia devem ser identificados e registrados corretamente para não serem confundidos com honorários.
- Dados iniciais são fictícios e foram incluídos apenas para demonstração.

## Documentação do desafio

- [PRD simplificado](docs/PRD.md)
- [Prompt final](docs/PROMPT_FINAL.md)
- [Evolução dos prompts](docs/PROCESSO.md)
- [Roteiro para reflexão pessoal](docs/REFLEXAO.md)
- [Orientações para prints e entrega](docs/ENTREGA.md)

## Estrutura

- `index.html`: interface, estilos e lógica do aplicativo.
- `assets/`: logos fornecidas pelo autor e arquivos de apresentação dessas imagens.
- `docs/`: briefing, prompts e documentação da experiência.

## Autoria e uso

Marca: ByJohwGimenes MKT. Projeto criado com assistência de IA para fins de estudo. As logos são elementos de identidade da marca; este repositório não concede autorização de reutilização dessas marcas. Nenhuma licença aberta foi definida.

## Prompt final (PRD)

O briefing abaixo registra a etapa inicial com ChatGPT/Codex. Um prompt ampliado, preparado nesta conversa para revisão do conceito no Copilot, pediu PRD, agente, fluxo de telas e MVP; a execução é documentada nas capturas em [docs/prints](docs/prints/README.md).


Crie um aplicativo web responsivo, em português do Brasil, chamado **ByJohwGimenes MKT**, para organização financeira de profissionais autônomos de marketing e social media.

O problema é o controle manual de pagamentos dos clientes e despesas com ferramentas, edição, freelancers e anúncios. O aplicativo deve facilitar a leitura do saldo e a criação de reservas para meses de demanda menor.

Use a identidade visual fornecida: logo completa branca em fundos escuros e símbolo preto em fundos claros. Preserve proporção e legibilidade. Crie uma interface simples, com painel, navegação lateral no desktop e adaptação para celular.

Implemente um MVP com:

1. Painel com filtro de mês, receitas, despesas, saldo, metas em andamento e despesas por categoria.
2. Cadastro, edição e exclusão de receitas e despesas confirmadas, com descrição, valor em reais, data, cliente/fornecedor e categoria.
3. Categorias: honorários, projetos avulsos, ferramentas e assinaturas, anúncios próprios, repasse de mídia, freelancers, equipamentos e outros.
4. Metas com nome, valor desejado, total reservado e barra de progresso. Atualizar uma meta não movimenta dinheiro nem altera o saldo automaticamente.
5. Plano de economia com valor e prazo em meses. Calcule valor/prazo e compare com o saldo do mês selecionado, explicando as limitações dos dados.
6. Persistência local e dados fictícios claramente identificados.

Valide valores positivos, meses inteiros entre 1 e 120, campos obrigatórios e confirme exclusões. Inclua estados vazios, contraste adequado e rótulos acessíveis.

**Evolução com IA:** adicione um chat somente se houver integração real com um modelo. Ele deve interpretar mensagens de recebimentos e despesas, pedir dados ausentes e apresentar um resumo para confirmação antes de salvar. Explique quais registros embasam as sugestões. Não invente dados, rendimentos ou resultados. Não realize transferências.

Caso não exista integração, identifique o assistente como simulação e implemente apenas cálculos locais, sem alegar que o aplicativo possui IA conectada. Nunca inclua chaves de API no código do navegador.

Ao finalizar, apresente o fluxo principal, o que funciona, o que está simulado, como executar e os próximos passos do MVP. Teste uma meta de R$ 3.000 em seis meses e uma despesa que atualize o saldo do mês.

## Reflexão sobre o processo

O desenvolvimento mostrou que a qualidade do briefing altera diretamente o resultado. Ao pedir uma relação com marketing, a primeira interpretação desviou para um organizador de conteúdos. A correção “mas de finanças” restabeleceu o objetivo e levou a uma solução voltada aos recebimentos e custos do profissional de marketing.

A experiência também evidencia a diferença entre desenvolver com IA e integrar IA ao produto: a conversa ajudou a construir o código e refinar a interface, mas o assistente atual executa cálculos locais. Nomear essa limitação e revisar o que foi gerado faz parte do processo.

Esta síntese foi redigida com assistência de IA a partir das interações registradas. A análise do teste no Copilot está registrada abaixo. O estudante pode complementar este relato com suas próprias percepções.

## Evidências das interações

Foram incluídas **19 capturas reais do Microsoft Copilot**, fornecidas pelo estudante em 20/10/2026, cobrindo o pedido de revisão do briefing, a proposta de produto, as funções do agente, o fluxo de telas e o MVP. Não são evidências de uso do Lovable nem de testes do código.

![Pedido ao Copilot e início da revisão do PRD](docs/prints/copilot-01.png)

![Personalidade proposta para o agente](docs/prints/copilot-08.png)

![Proposta de MVP no Copilot](docs/prints/copilot-17.png)

[Ver as 19 capturas com descrições](docs/prints/README.md)

### O que a revisão do Copilot ensinou

A resposta ajudou a detalhar o público, separar honorários de verba de mídia e visualizar módulos do produto. Também expandiu o escopo para impostos, investimentos e previsões. Essas propostas exigem revisão: percentuais ilustrativos não são regras tributárias; saldo não equivale a lucro contábil; e a queda de faturamento não determina, sozinha, a variação da margem. O aprendizado é usar a resposta como material de planejamento e revisar premissas, cálculos e limites antes de implementar.

No protótipo, o assistente continua sendo uma simulação local. As telas e funções descritas pelo Copilot são propostas conceituais.

## Repositório-base do desafio

[Laboratório oficial da DIO](https://github.com/digitalinnovationone/dio-lab-vibe-coding-app-financas). As instruções de entrega solicitam um fork desse repositório. Este repositório do aplicativo foi criado de forma independente; a entrega deve ser organizada no fork para cumprir essa etapa.
