---
name: entrega
version: 1
paths: ["**"]
---
Convencoes de entrega do time de engenharia. `severity: warning` recomenda sem
bloquear o merge.

## ENT-001 Mudanca pequena e com um proposito
severity: warning
Uma pull request faz uma coisa; refatoracao, formatacao e mudanca de
comportamento nao vem juntas, para o parecer e a revisao humana conseguirem
dizer o que mudou.

## ENT-002 Arquivo gerado ou credencial de ambiente nao e versionado
severity: warning
`.env`, chaves, builds e saidas de ferramenta ficam fora do repositorio
(`.gitignore`); o que e gerado se regenera.
