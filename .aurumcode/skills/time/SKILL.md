---
name: time
version: 1
paths: ["**/*.py"]
---
Convencoes do time de desenvolvimento e do QA. Cada `## ` abaixo e uma regra
citavel; `severity: warning` recomenda sem bloquear o merge.

## PAD-001 Argumentos de linha de comando com argparse
severity: warning
Opcao de linha de comando e lida com `argparse` (ajuda, validacao e erro
claros), nunca filtrando `sys.argv` na mao.

## QA-001 Comportamento novo tem teste
severity: warning
Toda opcao ou caminho novo tem um teste que falharia sem a mudanca.
