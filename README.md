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

Não foram realizadas interações com Copilot ou Lovable nesta implementação. O [prompt final](docs/PROMPT_FINAL.md) está preparado para esses testes. A entrega completa descrita pelo desafio ainda exige capturas dessas interações e uma reflexão pessoal do estudante.

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
