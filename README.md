# devops-policy — padrões de engenharia (mantidos pelo time de engenharia)

Todo serviço que aponta para este repositório (`standards_repository` no workflow do
AurumCode) recebe as skills e os analistas daqui, **abaixo** da política de segurança:
uma skill de mesmo nome na segurança vence; este repositório nunca declara gate,
ignore ou exceções (um `config.yml` com essas seções é recusado).

| Arquivo | O que decide |
|---|---|
| `.aurumcode/skills/time/SKILL.md` | **PAD-001** argparse, **PAD-002** docstring, **PAD-003** sem print de depuração, **PAD-004** configuração pelo ambiente (`warning`); **QA-001** comportamento novo tem teste (`error`: sem teste, o merge não entra), **QA-002** teste não é pulado sem motivo, **QA-003** teste sem rede (`warning`) |
| `.aurumcode/skills/entrega/SKILL.md` | **ENT-001** mudança pequena e com um propósito, **ENT-002** nada gerado ou credencial versionada (`warning`) |
| `.aurumcode/profiles.yml` | os analistas `padroes` e `qa`, que o serviço seleciona em `review.profiles` |
