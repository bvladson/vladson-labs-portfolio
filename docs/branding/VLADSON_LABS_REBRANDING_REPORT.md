# VLADSON LABS — RELATÓRIO DO REBRANDING

**Data:** 25/11/2026 · **Conta:** github.com/bvladson · **Fase:** primeira (identidade apenas)

---

## Resumo executivo

**Objetivo.** Estabelecer identidade tecnológica própria para onze sistemas que até aqui
levavam o nome das empresas onde foram implantados, consolidando-os sob a iniciativa autoral
**Vladson Labs** — sem redesign, sem mudança funcional e sem tocar em produção.

**Estratégia.** Auditoria antes de qualquer alteração; classificação de risco por projeto;
registro central de identidades como fonte de verdade; execução apenas do que foi
comprovadamente seguro; bloqueio documentado do que não foi.

**Escopo executado.** Fases 0 a 8. Doze pastas locais reorganizadas, onze repositórios
renomeados no GitHub, doze remotes atualizados e validados, onze READMEs com identidade de
produto, índice do portfólio reescrito em quatro categorias, perfil do GitHub atualizado,
nove documentos de identidade criados e material de LinkedIn preparado.

**Resultado.** Identidade estabelecida e consistente nos onze produtos elegíveis. Um projeto
bloqueado por risco operacional. Nenhuma alteração em produção.

**Situação geral.** Concluído dentro do escopo seguro, com três pendências registradas que
dependem de decisão do titular.

---

## Inventário de projetos

### Alvorumo BI — `alvorumo-v2`
| | |
|---|---|
| Nome anterior | BIOMIE v2 · `biomie-v2` |
| Pasta | `Portfolio\biomie-v2` → `Vladson-Labs\alvorumo-v2` |
| URL | `/biomie-v2` → `/alvorumo-v2` |
| Branch | `main` (28 branches preservadas, 1 tag) |
| Commits | 1 de branding |
| Alterados | README.md |
| Testes | remote responde; links verificados; histórico íntegro |
| **Status** | **CONCLUÍDO** |

### Alvorumo BI v1 — Legacy Edition — `alvorumo-v1`
| | |
|---|---|
| Nome anterior | BIomie v1 · `biomie-v1` |
| Pasta | `Portfolio\biomie-v1` → `Vladson-Labs\alvorumo-v1` |
| URL | `/biomie-v1` → `/alvorumo-v1` |
| Branch | `main` (7 branches, 26 tags preservadas) |
| Commits | 1 de branding |
| Testes | remote responde; histórico e tags íntegros |
| **Status** | **CONCLUÍDO** |

### Elofarol CRM — `elofarol-web`
| | |
|---|---|
| Nome anterior | MAG site + CRM · `mag-site-crm` |
| Pasta | `Portfolio\mag-site-crm` → `Vladson-Labs\elofarol-web` |
| URL | `/mag-site-crm` → `/elofarol-web` |
| Branch | `main` (6 branches, 4 tags) |
| Commits | 1 de branding |
| Testes | remote responde; nome MAG preservado onde representa o cliente |
| **Status** | **CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS** |

### Elofarol CRM Mobile — `elofarol-mobile`
| | |
|---|---|
| Nome anterior | MAG CRM Android · `mag-crm-android` |
| Pasta | `Portfolio\mag-crm-android` → `Vladson-Labs\elofarol-mobile` |
| URL | `/mag-crm-android` → `/elofarol-mobile` |
| Commits | 1 de branding |
| Testes | remote responde; release 1.0.0 intacta |
| Pendência | `applicationId`, namespace e keystore inalterados por decisão. A produção serve o APK do disco da VPS, não do GitHub — distribuição não afetada |
| **Status** | **CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS** |

### Sabelar AI — `sabelar-ai`
| | |
|---|---|
| Nome anterior | MAG AI · `mag-ai` |
| Pasta | `Portfolio\mag-ai` → `Vladson-Labs\sabelar-ai` |
| URL | `/mag-ai` → `/sabelar-ai` |
| Commits | 1 de branding |
| Testes | remote responde |
| Observação | Autoria declarada como arquitetura e integração; modelos e motor de inferência são de terceiros |
| **Status** | **CONCLUÍDO** |

### Pautelo PM — `pautelo`
| | |
|---|---|
| Nome anterior | Base MAG · `mag-base` |
| Pasta | `Portfolio\mag-base` → `Vladson-Labs\pautelo` |
| URL | `/mag-base` → `/pautelo` |
| Commits | 1 de branding |
| Testes | remote responde; identificadores internos do Leantime preservados |
| Pendência | AGPL-3.0: repositório sem `LICENSE` declarada; obrigação do §13 registrada |
| **Status** | **CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS** |

### Entreliga iPaaS — `entreliga`
| | |
|---|---|
| Nome anterior | VSB 360 · `vsb-360-integrations` |
| Pasta | `Portfolio\vsb-360-integrations` → `Vladson-Labs\entreliga` |
| URL | `/vsb-360-integrations` → `/entreliga` |
| Commits | 1 de branding |
| Testes | remote responde; 6 workflows auditados: verificação somente-leitura, sem secrets, sem implantação |
| **Status** | **CONCLUÍDO** |

### Operalvo Core — `vsb_core`
| | |
|---|---|
| Nome pretendido | `operalvo-core` |
| Pasta | não clonado localmente |
| URL | **inalterada** |
| Commits | 0 |
| Motivo | 5 workflows constroem e **promovem a imagem Docker de produção**. Renomear pode quebrar a cadeia de imagens da qual a produção depende |
| Ação feita | Descrição atualizada com a identidade do produto e nota da pendência |
| **Status** | **BLOQUEADO POR RISCO OPERACIONAL** |

### Docalume DMS — `docalume-ptbr`
| | |
|---|---|
| Nome anterior | VSB ERP pt-BR · `vsb-erp-ptbr` |
| URL | `/vsb-erp-ptbr` → `/docalume-ptbr` |
| Commits | 1 de branding |
| Testes | remote responde |
| **Status** | **CONCLUÍDO** |

### Vitracora CMS — `vitracora-web`
| | |
|---|---|
| Nome anterior | VSB site institucional · `vsb-site-institucional` |
| URL | `/vsb-site-institucional` → `/vitracora-web` |
| Commits | 1 de branding |
| Testes | remote responde; nome VSB preservado onde representa o cliente |
| **Status** | **CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS** |

### Fortearco Infra — `fortearco-infrastructure`
| | |
|---|---|
| Nome anterior | Infra VPS Ubuntu · `infra-vps-ubuntu` |
| URL | `/infra-vps-ubuntu` → `/fortearco-infrastructure` |
| Commits | 1 de branding |
| Testes | remote responde; nada na VPS renomeado |
| **Status** | **CONCLUÍDO** |

### Vladson Labs Portfolio — `vladson-labs-portfolio`
| | |
|---|---|
| Nome anterior | `portfolio` |
| URL | `/portfolio` → `/vladson-labs-portfolio` |
| Commits | 1 de branding (índice reescrito + 9 documentos de identidade) |
| **Status** | **CONCLUÍDO** |

### Perfil — `bvladson`
| | |
|---|---|
| Nome | **inalterado**, por exigência do GitHub |
| Branch | `Projetos` |
| Commits | 1 |
| Alterados | README.md (seção do ecossistema, produtos renomeados, links novos) |
| Preservado | nome, formação acadêmica, histórico e dados pessoais |
| **Status** | **CONCLUÍDO** |

---

## Indicadores de execução

| Indicador | Valor |
|---|---|
| Repositórios analisados | 13 |
| Repositórios renomeados | 11 |
| Repositórios bloqueados | 1 (`vsb_core`) |
| Repositórios fora de escopo por natureza | 1 (`bvladson`, perfil) |
| Pastas locais reorganizadas | 12 |
| Documentos de identidade criados | 9 |
| READMEs atualizados | 12 |
| Descrições de repositório atualizadas | 12 |
| Referências cruzadas corrigidas | 5 arquivos, 11 padrões de URL |
| Commits de branding | 13 |
| Remotes atualizados e validados | 11 de 11 respondem |
| Verificações executadas | 9 (symlinks, colisões, submódulos, worktrees, Pages, Actions, webhooks, releases, sincronia local×remoto) |
| Verificações aprovadas | 9 |
| Force push | 0 |
| Histórico reescrito | 0 |
| Branches ou tags removidas | 0 |
| **Alterações em produção** | **0** |

---

## Classificação final

| Projeto | Classificação |
|---|---|
| Alvorumo BI | CONCLUÍDO |
| Alvorumo BI v1 — Legacy Edition | CONCLUÍDO |
| Sabelar AI | CONCLUÍDO |
| Entreliga iPaaS | CONCLUÍDO |
| Docalume DMS | CONCLUÍDO |
| Fortearco Infra | CONCLUÍDO |
| Vladson Labs Portfolio | CONCLUÍDO |
| Perfil `bvladson` | CONCLUÍDO |
| Elofarol CRM | CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS |
| Elofarol CRM Mobile | CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS |
| Pautelo PM | CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS |
| Vitracora CMS | CONCLUÍDO COM IDENTIFICADORES LEGADOS PRESERVADOS |
| **Operalvo ERP Core** | **BLOQUEADO POR RISCO OPERACIONAL** |

---

## Riscos residuais e pendências

1. **Licenciamento.** Nenhum repositório declara `LICENSE`. Pautelo PM deriva do Leantime
   (AGPL-3.0); Entreliga iPaaS, Operalvo Core e Docalume DMS operam sobre ERPNext e Frappe (GPL-3.0);
   Vitracora CMS usa WordPress (GPL-2.0-or-later). Derivados herdam obrigações. **A escolha da
   licença é decisão do titular e não foi feita nesta fase.**

2. **AGPL §13 no Pautelo PM.** O README documenta a obrigação de oferecer o código-fonte da
   versão modificada aos usuários que acessam pela rede. Não há evidência de que o link
   esteja publicado no sistema em produção.

3. **Titularidade.** A existência de um repositório na conta pessoal não comprova
   titularidade patrimonial do software desenvolvido no contexto das empresas atendidas.
   Confirmar antes de qualquer uso comercial.

4. **Operalvo ERP Core.** Renomeação pendente de inspeção dos 5 workflows de imagem Docker.

5. **Redirecionamentos.** O GitHub redireciona os nomes antigos, mas a documentação já foi
   atualizada para os endereços novos. Não depender do redirecionamento permanentemente.

6. **Preexistente, fora de escopo.** Dependabot acusa vulnerabilidades em `alvorumo-v2` e
   `elofarol-web`, vindas dos lockfiles.

---

## Reversão

Documentada em [`ROLLBACK_PLAN.md`](ROLLBACK_PLAN.md). Não depende de banco de dados nem de
alteração em produção: nada em produção foi tocado.
