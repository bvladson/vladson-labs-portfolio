# Fase 0 — auditoria do rebranding

**Data:** 25/11/2026 · **Conta:** github.com/bvladson · **Executor:** sessão Claude Code

Auditoria feita **antes** de qualquer alteração, conforme exigido. Nenhum arquivo foi
modificado durante esta fase.

## Inventário

**13 repositórios** na conta, **12 clonados localmente** (`vsb_core` nunca foi clonado).
Todas as cópias locais estavam **em sincronia com o GitHub** — nenhum commit local pendente,
nenhuma alteração não commitada, em nenhum dos 12.

| Repositório | Visibilidade | Branch padrão | Branches | Commits |
| --- | --- | --- | --- | --- |
| biomie-v1 | privado | main | 7 | 202 |
| biomie-v2 | privado | main | 28 | 269 |
| mag-site-crm | público | main | 6 | 45 |
| mag-crm-android | público | main | 1 | 1 |
| mag-ai | público | main | 1 | 4 |
| mag-base | público | main | 1 | 2 |
| vsb-360-integrations | privado | main | 1 | 66 |
| vsb_core | privado | main | — | não clonado |
| vsb-erp-ptbr | público | main | 1 | 2 |
| vsb-site-institucional | público | main | 1 | 2 |
| infra-vps-ubuntu | público | main | 1 | 2 |
| portfolio | público | main | 1 | 3 |
| bvladson | público | **Projetos** | 1 | 6 |

> `biomie-v1` e `biomie-v2` estavam públicos em 18/11 e constam privados em 25/11. A mudança
> não foi feita nesta sessão. A visibilidade não será alterada.

## Verificações estruturais

| Item | Resultado |
| --- | --- |
| Submódulos Git | nenhum |
| Worktrees | nenhum |
| Links simbólicos versionados | nenhum |
| Colisões de maiúscula/minúscula | nenhuma |
| Caminho versionado mais longo | 95 caracteres |
| GitHub Pages | nenhum repositório publica Pages |
| Webhooks | nenhum |
| Releases | 1, em `mag-crm-android` (APK 1.0.0) |

## Automações

| Repositório | Workflows | Natureza |
| --- | --- | --- |
| biomie-v1, biomie-v2, mag-site-crm | Dependabot | gerado pelo GitHub, sem risco |
| **vsb-360-integrations** | 6 próprios | **verificação somente-leitura** — `permissions: contents: read`, sem secrets, sem SSH, sem passo de implantação; nenhum cita o nome do repositório |
| **vsb_core** | 5 próprios | **constroem e promovem a imagem Docker de produção** (`build-image`, `exportar-imagem`, `homologacao`, `promover-imagem`, `testes`) |
| demais | nenhum | — |

## Dependências de produção sobre os nomes

- **APK do Elofarol Mobile:** a produção serve o arquivo do disco da própria VPS
  (`/opt/mag-site/data/app-android`), **não** da release do GitHub. Renomear o repositório
  não interrompe a distribuição interna. Links externos apontados para a release passam a
  depender do redirecionamento automático do GitHub.
- **Infraestrutura:** nenhum `COMPOSE_PROJECT_NAME`, container, volume, rede, serviço
  systemd, crontab ou caminho na VPS deriva do nome de um repositório. Nada na VPS precisa
  mudar — e nada mudará nesta fase.

## Classificação

| Classe | Projetos |
| --- | --- |
| **SEGURO** (10) | alvorumo-v1, alvorumo-v2, elofarol-web, sabelar-ai, pautelo, entreliga, docalume-ptbr, vitracora-web, fortearco-infrastructure, vladson-labs-portfolio |
| **CONTROLADO** (1) | elofarol-mobile — tem release com APK; exige atualizar referências e conferir links |
| **BLOQUEADO POR RISCO OPERACIONAL** (1) | operalvo-core (`vsb_core`) — a cadeia de imagem Docker de produção passa por este repositório |
| **NÃO SE APLICA** (1) | `bvladson` — repositório de perfil, nome preservado por exigência do GitHub |

## Pendências encontradas, fora do escopo desta fase

1. **Nenhum repositório declara `LICENSE`.** Pautelo deriva do Leantime (AGPL-3.0);
   Entreliga, Operalvo Core e Docalume operam sobre ERPNext e Frappe (GPL-3.0); Vitracora
   usa WordPress (GPL-2.0-or-later). Derivados herdam obrigações. A escolha da licença é
   decisão do titular e não foi feita aqui.
2. **AGPL §13 no Pautelo.** O README documenta a obrigação de oferecer o código-fonte da
   versão modificada aos usuários que acessam pela rede. Não há evidência de que o link
   esteja publicado no sistema em produção.
3. **Titularidade.** A existência de um repositório na conta pessoal não comprova
   titularidade patrimonial do software desenvolvido no contexto das empresas atendidas.
4. **Dependabot** acusa vulnerabilidades em `biomie-v2` e `mag-site-crm` (lockfiles).
   Problema preexistente, fora do escopo do rebranding.
