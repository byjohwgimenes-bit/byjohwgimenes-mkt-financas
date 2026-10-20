# Prompt final — pronto para testar no Copilot ou Lovable

Este arquivo preserva o briefing inicial da versão demonstrativa e sua evolução com IA. Posteriormente, um briefing ampliado preparado no ChatGPT/Codex foi executado no Microsoft Copilot para revisar o conceito, agente, telas e MVP. As capturas reais dessa etapa estão em [prints/README.md](prints/README.md). Não houve uso do Lovable.

---

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
