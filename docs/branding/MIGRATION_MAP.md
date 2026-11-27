# Mapa de migração

Fonte estruturada: [`PRODUCT_REGISTRY.json`](PRODUCT_REGISTRY.json).

| Produto | Repositório antigo | Repositório novo | Pasta local | Classe |
| --- | --- | --- | --- | --- |
| Alvorumo BI v1 — Legacy Edition | `biomie-v1` | `alvorumo-v1` | `Vladson-Labs/alvorumo-v1` | SEGURO |
| Alvorumo BI | `biomie-v2` | `alvorumo-v2` | `Vladson-Labs/alvorumo-v2` | SEGURO |
| Elofarol CRM | `mag-site-crm` | `elofarol-web` | `Vladson-Labs/elofarol-web` | SEGURO |
| Elofarol CRM Mobile | `mag-crm-android` | `elofarol-mobile` | `Vladson-Labs/elofarol-mobile` | CONTROLADO |
| Sabelar AI | `mag-ai` | `sabelar-ai` | `Vladson-Labs/sabelar-ai` | SEGURO |
| Pautelo PM | `mag-base` | `pautelo` | `Vladson-Labs/pautelo` | SEGURO |
| Entreliga iPaaS | `vsb-360-integrations` | `entreliga` | `Vladson-Labs/entreliga` | SEGURO |
| Operalvo Core | `vsb_core` | `operalvo-core` | não clonado | **BLOQUEADO** |
| Docalume DMS | `vsb-erp-ptbr` | `docalume-ptbr` | `Vladson-Labs/docalume-ptbr` | SEGURO |
| Vitracora CMS | `vsb-site-institucional` | `vitracora-web` | `Vladson-Labs/vitracora-web` | SEGURO |
| Fortearco Infra | `infra-vps-ubuntu` | `fortearco-infrastructure` | `Vladson-Labs/fortearco-infrastructure` | SEGURO |
| Vladson Labs Portfolio | `portfolio` | `vladson-labs-portfolio` | `Vladson-Labs/vladson-labs-portfolio` | SEGURO |
| Vladson Bezerra (perfil) | `bvladson` | `bvladson` *(não muda)* | `Vladson-Labs/bvladson` | NÃO SE APLICA |

## O que NÃO é renomeado

| Camada | Permanece |
| --- | --- |
| Empresas atendidas | MAG Móveis Corporativos, VSB Soluções Técnicas |
| Domínios e subdomínios | magmoveiscorporativos.com.br, vsbseguranca.com.br, portal.vsbseguranca.com.br |
| Infraestrutura | `COMPOSE_PROJECT_NAME`, containers, volumes, redes, systemd, crontabs, caminhos |
| Android | `applicationId`, namespace, keystore, certificados |
| Leantime | namespace `Leantime\`, `window.leantime`, tabelas `zp_*`, `leantime-version` |
| Bancos de dados | nomes de bancos, esquemas, tabelas, colunas |
| Histórico | registros, evidências, relatórios e documentos datados |
