# Convenções de nomenclatura

## Nomes de produto

Escrita em caixa normal, sem versalete e sem maiúsculas integrais: **Alvorumo BI**, não ALVORUMO BI.
Exceção: `Sabelar AI`, onde "AI" é sigla.

A geração só aparece quando distingue: *Alvorumo BI* é a segunda geração; a primeira é
*Alvorumo BI v1 — Legacy Edition*.

Interfaces do mesmo produto levam o nome do produto mais o sufixo da interface:
*Elofarol CRM Web*, *Elofarol CRM Mobile*. Nunca apresentadas como produtos distintos.

## Sigla da categoria

Todo nome de produto carrega uma sigla curta que diz, em dois segundos, o que o sistema faz.
Quem abre o perfil não precisa ler a descrição para saber se aquilo é um BI ou um CRM.

| Produto | Sigla | O que indica |
| --- | --- | --- |
| Alvorumo BI | `BI` | Business Intelligence & Analytics |
| Elofarol CRM | `CRM` | Customer Relationship Management & Sales |
| Elofarol CRM Mobile | `CRM` + interface | a mesma plataforma, no Android |
| Sabelar AI | `AI` | motor de inteligência artificial |
| Pautelo PM | `PM` | Project Management |
| Entreliga iPaaS | `iPaaS` | integração entre aplicações |
| Operalvo ERP Core | `ERP` | extensões de gestão empresarial |
| Docalume DMS | `DMS` | engenharia e gestão documental |
| Vitracora CMS | `CMS` | conteúdo e experiência digital |
| Fortearco Infra | `Infra` | infraestrutura e operações |

A sigla vem **depois** do nome, separada por espaço, e faz parte do nome exibido. Ela não
entra no slug nem no nome do repositório: `Alvorumo BI` mora em `alvorumo-v2`. Nome técnico
estável, nome comercial descritivo.

A geração, quando existe, vem depois da sigla: *Alvorumo BI v1 — Legacy Edition*.

## Repositórios

Minúsculas, separadas por hífen, sem acento: `alvorumo-v2`, `fortearco-infrastructure`.
O sufixo indica a natureza quando o nome sozinho é ambíguo (`-web`, `-mobile`, `-core`,
`-infrastructure`, `-ptbr`).

Exceção permanente: `bvladson`, repositório de perfil do GitHub, cujo nome é imposto pela
plataforma.

## Pastas locais

Espelham o nome do repositório, sob `Vladson-Labs/`. Pastas internas só são renomeadas
quando forem exclusivamente de identidade comercial e houver comprovação de que a mudança
não afeta a execução.

## Assinatura nos READMEs

    NOME DO PRODUTO

    Categoria da solução

    A Vladson Labs Project
    Developed by Vladson Bezerra

Em projetos derivados de software de terceiros, a linha de autoria distingue explicitamente
desenvolvimento original de customização, integração, localização e implantação.

## Idioma

Nome do produto, categoria e slogan: iguais em qualquer idioma. Descrições: português e
inglês, nesta ordem, quando ambas existirem.
