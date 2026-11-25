# Histórico de versões

Registro das mudanças de cada versão do Fine. A mais recente fica no topo.
Cada versão publicada também tem uma *tag* no GitHub (aba **Releases/Tags**), para dar para voltar a ela.

Numeração: `MAIOR.MENOR`. Muda o MENOR em melhorias e correções; muda o MAIOR quando algo deixa de ser compatível (por exemplo, o formato dos dados).

---

## Pessoal

### pessoal-v1.5 — 2026-11-25
- Planejar › Projeção: gastos variáveis estimados pelas metas enquanto não houver 3 meses fechados (por grupo, meses reais + meta menos o já previsto no grupo). O histórico começa no primeiro mês fechado com gasto do dia a dia; valores com estimativa aparecem com "~". O alerta de mês no vermelho do Início usa a mesma estimativa.

### pessoal-v1.4 — 2026-11-18
- Correção: compras no cartão que caem na fatura do mês seguinte passam a contar na ordem dos grupos do Lançar.
- Lançar: a ordem dos grupos e subgrupos segue o que você mais lança à mão (fixos, dívidas e parcelas automáticas não contam), com mais peso para os meses recentes.
- Planejar › Dicas: regra 50/30/20 aplicada à renda e ao histórico (metas sugeridas com botão Aplicar), reserva de emergência, peso das dívidas e qual quitar primeiro, onde cortar e quanto investir por mês. Classificação dos grupos e renda ajustáveis.
- Subgrupos podem ser movidos para outro grupo, levando lançamentos e fixos antigos. Restaurante passa a ficar em Lazer na configuração inicial.
- Demonstração com mais gastos de estilo de vida (delivery, compras online) para exibir as dicas.
- Modo demonstração: na tela de entrada, "Experimentar sem conta" abre o app com dados de exemplo (fixos, cartão, parcelas, dívidas e investimentos) para testar tudo; nada é salvo.
- Login: o Google sempre pergunta qual conta usar, permitindo entrar com outra conta depois de sair.
- Extrato: lançamentos previstos dos meses futuros (receitas e despesas fixas, parcelas de dívidas) podem ser abertos e editados; ao salvar, ficam registrados naquele mês. Excluir um previsto tira só daquele mês.
- Topo e barra de baixo ficam fixos; só o conteúdo do meio rola (corrige a barra sumindo ao rolar no celular).
- Aviso de direitos reservados no app e arquivo LICENSE; repositório passa a ser privado e a ponte antiga do GitHub Pages foi removida.
- Funciona sem internet: o app fica guardado no aparelho (service worker), abre offline com os últimos dados e envia os lançamentos quando a conexão voltar.
- iPhone: botão + não fica mais cortado, a barra de baixo respeita a área do gesto de início e o campo de data não passa da borda.
- Planejar › Economias reformulado: cadastro de investimentos (tipo, instituição, meta, rentabilidade esperada em % do CDI ou % a.a., liquidez/vencimento).
- Atualização mensal de aportes, resgates e saldo de cada investimento; o app calcula o rendimento do mês e do ano e compara com o esperado.
- Patrimônio, cashback e tabela do ano (aplicado, cashback, rendeu, patrimônio).
- Aportes não entram como despesa: o mês mostra quanto sobrou, quanto foi aplicado e quanto ficou livre.
- Valores antigos de Caixinha e Outros investimentos convertidos automaticamente em investimentos.
- Início avisa quando um investimento vence nos próximos 30 dias.
- Excel completo e Excel backup acompanham o novo formato.

### pessoal-v1.3.1 — 2026-11-17
- Instalável como aplicativo: ao adicionar à tela inicial, abre em tela cheia, sem a barra do navegador.
- Início esconde os quadros Atenção e Próximos 10 dias quando estão vazios.

### pessoal-v1.3 — 2026-11-17
- Grupos e subgrupos: renomear e excluir tocando no nome; ao excluir um grupo com lançamentos, escolhe-se o grupo de destino (lançamentos, fixos e meta vão junto). DÍVIDAS e ANTECIPAÇÃO são protegidos.
- Grupos e subgrupos sempre em ordem alfabética; vários subgrupos de uma vez (separados por vírgula ou um por linha).
- Tela Lançar: mostra os 6 grupos e 6 subgrupos mais usados (últimos 4 meses) e um botão "⋯ mais" com o restante.
- Fixos recorrentes (valor igual todo mês) e não recorrentes (valor varia): os não recorrentes entram com a média dos 3 últimos valores confirmados, marcados como "estimado", até o valor real ser informado.
- Edição de lançamento: marcar como fixo (com término opcional) e como recorrente ou não; em lançamento já fixo, alterar recorrência, usar o valor nos próximos meses ou encerrar o fixo.
- Compra parcelada: "Valor é o total" vem primeiro e já marcado.
- Correção: a descrição do lançamento anterior não volta mais ao campo no celular.
- Teste local (localhost) usa dados separados dos reais.
- Dívidas: juros efetivos com 3 casas decimais, ao mês ou ao ano (padrão: financiamento ao ano; empréstimo e consignado ao mês), com a taxa equivalente na outra unidade.
- Dívidas: preenchidos dois entre parcela (1ª parcela no SAC), nº de parcelas e juros, o terceiro é calculado, em Price e SAC; aviso quando os três não batem.
- Dívidas: ponto de partida pelo saldo de hoje ou pelos dados do contrato (valor, prazo total e 1ª parcela), com saldo atual e parcelas pagas calculados.
- Dívidas: encargos mensais opcionais (seguros, taxas), somados ao lançamento sem entrar no cálculo de juros.
- Dívidas: resumo antes de salvar (total a pagar, juros, encargos, 1ª e última parcela no SAC, quitação).
- Correção: botões de opção não somem mais em formulários longos.

### pessoal-v1.2 — 17/11/2026
- Logo Fine (opção 6): "fin" + cifrão formado pelo "e" e pelo "a".
- Nome do app: Fine. Ícone na aba do navegador e na tela inicial.
- Exportações: `fine-completo-AAAA.xlsx` e `fine-backup-AAAA-MM-DD.xlsx`.

### pessoal-v1.1 — 17/11/2026
- Publicada no Cloudflare Pages (fine-pessoal.pages.dev), pasta `pessoal/`.
- Nome provisório fin$nce.

### pessoal-v1.0 — 14/11/2026
- Primeira versão com Firebase e login Google.
- Telas Lançar, Extrato, Resumo, Relatórios e Mais.
- Relatórios de planejamento e economias; Dívidas movidas para Mais.
- Excel completo (formato do modelo) e Excel backup; importação de backup.
- Nova navegação: Início · Extrato · (+) Lançar · Planejar · Mais. O app continua abrindo em Lançar (botão + central).
- Início: resumo do mês, comprometido x livre, quadro "Atenção" (metas estouradas, fixos estimados, meses que vão fechar no vermelho), próximos 10 dias de vencimentos e os 5 maiores grupos com "Ver todos".
- Planejar com sub-abas: Orçamento (gasto por grupo, orçado x realizado, para onde vai, receitas por fonte), Projeção (12 meses, gráfico de 6 meses, quanto sobrou), Economias e Dívidas.
- Dívidas saiu de Mais; Resumo e Relatórios foram absorvidos por Início e Planejar.
- Tema escuro por padrão; em Mais › Aparência dá para escolher Escuro, Claro ou Igual ao celular (a escolha fica salva no aparelho).

## Comercial

### comercial-v0.2 — 17/11/2026
- Logo Fine (opção 6) e novos ícones do app.
- Nome Fine no app instalado.

### comercial-v0.1 — 17/11/2026
- Primeira versão de teste: sem login e sem servidor, dados no aparelho de quem usa.
- Instalável e funciona sem internet.
- Aviso para fazer backup a cada 30 dias.
