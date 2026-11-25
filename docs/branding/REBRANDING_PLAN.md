# Plano do rebranding

Fase inicial: **identidade apenas**. Nomes, documentação, metadados e portfólio.
Sem redesign, sem logotipo, sem mudança funcional, sem implantação.

| Fase | O que faz | Situação |
| --- | --- | --- |
| 0 | Auditoria e classificação de risco | concluída — [`REBRANDING_AUDIT.md`](REBRANDING_AUDIT.md) |
| 1 | Registro central de identidades | concluída — [`PRODUCT_REGISTRY.json`](PRODUCT_REGISTRY.json) |
| 2 | Reorganização local em `Vladson-Labs/` | concluída |
| 3 | Nomes de produto dentro dos projetos | em andamento |
| 4 | Renomeação dos repositórios no GitHub | em andamento |
| 5 | Padronização dos READMEs | em andamento |
| 6 | Reestruturação do portfólio | em andamento |
| 7 | Perfil do GitHub | em andamento |
| 8 | Material para o LinkedIn | concluída — [`LINKEDIN_PROFILE.md`](LINKEDIN_PROFILE.md) |
| 9 | Propriedade intelectual | pendências registradas na auditoria |
| 10 | Testes e validações | por etapa executada |

## Regra de decisão para cada ocorrência de nome

| Categoria | Ação |
| --- | --- |
| A — nome comercial do produto | substituir |
| B — nome de empresa atendida | preservar |
| C — identificador operacional | preservar |
| D — registro histórico | preservar |
| E — referência documental desatualizada | atualizar |
| F — terceiro ou licença | preservar |
| G — ambígua | registrar, não alterar |

O objetivo não é eliminar toda ocorrência dos nomes antigos: é estabelecer a nova identidade
sem comprometer o funcionamento.

## Versionamento

Commits pequenos, isolados e reversíveis. Branding nunca misturado com mudança funcional.
Sem force push, sem reescrita de histórico, sem remoção de branches ou tags.
