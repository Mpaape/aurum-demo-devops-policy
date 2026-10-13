---
name: time
version: 1
paths: ["**/*.py"]
---
Convencoes do time de desenvolvimento e do QA. Cada `## ` abaixo e uma regra
citavel; `severity: warning` recomenda sem bloquear o merge e `severity: error`
reprova o merge.

## PAD-001 Argumentos de linha de comando com argparse
severity: warning
Opcao de linha de comando e lida com `argparse` (ajuda, validacao e erro
claros), nunca filtrando `sys.argv` na mao.

## PAD-002 Funcao publica tem docstring
severity: warning
Funcao ou classe usada fora do proprio arquivo tem docstring de uma linha
dizendo o que faz e o que devolve.

## PAD-003 Sem print de depuracao
severity: warning
`print` serve a saida do programa; diagnostico vai para `logging`, nunca fica um
`print` de depuracao esquecido.

## PAD-004 Configuracao pelo ambiente, com padrao explicito
severity: warning
URL, modelo, porta e caminho vem de variavel de ambiente com valor padrao
declarado num lugar so, nunca espalhados como literais pelo codigo.

## QA-001 Comportamento novo tem teste
severity: error
Toda opcao ou caminho novo tem um teste que falharia sem a mudanca; uma
mudanca de comportamento sem teste nao entra.

## QA-002 Teste nao e pulado sem motivo
severity: warning
`skip`, `xfail` ou teste comentado traz o motivo e um prazo; teste que nao roda
nao protege nada.

## QA-003 Teste nao depende de rede
severity: warning
Teste unitario nao chama servico externo nem modelo de IA; a chamada e
substituida por um dublê (`mock`) com a resposta esperada.
