# Banco de Soluções e Radar de Artigos

Projeto feito com apoio de IA para a seleção GoHacks Talent 2026, por Maria Vitória Sales Farias (Engenharia Civil, UFC).

## O problema

Projetos de extensão enfrentam problemas recorrentes (engajamento de membros, liderança, organização de eventos) e precisam de um lugar para registrar o problema, a solução e o que foi aprendido. Na Diretoria de Pesquisa e Desenvolvimento do CEMP (UFC) também há a produção de artigos, que parte desses casos.

## O que construí

1. **Banco de Soluções (planilha):** abas por área, prioridade calculada por impacto × probabilidade, análise de quick win, painel automático e registro de conversas com fontes. Hoje tem 4 problemas e 2 soluções reais, 1 delas implantada, com retorno qualitativo e sem medição com números ainda.
2. **Radar de Artigos (fórmulas na planilha):** pontua cada solução de 0 a 6 por regra simples, sugere o caso com mais potencial de artigo, monta um prompt para uma IA e organiza a revisão humana do rascunho.
3. **Radar de Artigos (página com IA):** um agente simples. A IA chama a função `listar_casos`, escolhe um caso, chama `ler_caso` e escreve um rascunho de resumo. O arquivo `radar-demo.html` é a versão de demonstração, com dados fictícios.

## Como usei IA

- A IA propôs a estrutura da planilha e as regras de prioridade.
- Eu registrei os casos reais e depois pedi à IA que revisasse o arquivo. Ela apontou problemas como linhas de exemplo contando no painel, uma fórmula quebrada e um status "resolvido" sem dados de resultado. Eu corrigi o que dependia de mim.
- A IA escreve apenas o rascunho. A pontuação é por regra, e todo rascunho passa por uma revisão humana de 4 itens: conferir os fatos, resolver os [A CONFIRMAR], não manter número que não esteja no banco e descrever o resultado sem exagero.

## Limites

- O banco é pequeno e o único resultado registrado é qualitativo.
- A escolha do caso é por regra; a IA entra na escolha apenas quando o botão da página é usado.
- O botão de IA da página usa a conta de quem a abre dentro do Claude. Fora dele, o botão aparece desativado e vale o exemplo ilustrativo.
- Não há automação com macro nem chave de API: planilhas compartilhadas não são lugar seguro para isso.

## Arquivos

- `README.md`: esta descrição.
- `radar-demo.html`: página do Radar de Artigos (código HTML e JavaScript) com dados fictícios.

## Privacidade

Os dados reais do banco são internos do CEMP e não estão neste repositório. Os casos de `radar-demo.html` são fictícios.
