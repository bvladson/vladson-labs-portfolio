# Vladson Labs

**Software Engineering · Business Intelligence · Artificial Intelligence · Automation**

> Tecnologia criada para transformar negócios.
>
> Iniciativa tecnológica autoral de **Vladson Bezerra**.

Onze sistemas projetados, construídos e operados por mim para resolver problemas reais de
operação em duas empresas — **MAG Móveis Corporativos** e **VSB Soluções Técnicas**. Não são
exercícios: são sistemas que equipes usam todo dia, com dados reais, em horário comercial que
não pode cair.

A identidade dos produtos é minha; a identidade das empresas atendidas é delas. Os nomes MAG
e VSB permanecem onde representam o cliente, os dados, os domínios e o registro histórico.

**Registro de identidades:** [`docs/branding/`](docs/branding/) — identidade da marca,
registro dos produtos, mapa de migração, convenções, auditoria e plano de reversão.

---

## Business Intelligence & Data

### [Alvorumo](https://github.com/bvladson/alvorumo-v2) · *em produção*
**Business Intelligence & Analytics Platform** — *Clareza para decidir. Inteligência para crescer.*

**O problema.** A operação comercial de cinco empresas vivia dentro do ERP, mas o ERP não
responde às perguntas que a diretoria faz: qual vendedor está fora do ritmo da meta hoje, que
cliente sumiu, qual atividade econômica compra mais e onde ela está. Planilha resolve uma vez;
não resolve toda segunda-feira, para cinco empresas, com números que precisam bater.

**A solução.** Plataforma multiempresa com Cockpit, Plano de Voo, Vendas, Clientes 360°,
Produtos, Estoque com curvas e reposição, Financeiro, Qualidade dos Dados e um assistente
conversacional ligado a um modelo de linguagem local.

**Diferenciais técnicos.** Autorização aplicada no banco por RLS — a tela é só dica, se a
interface errar o banco ainda recusa. Uma única definição por métrica, em um registro central;
nenhuma fórmula dentro de componente. "Hoje" vem de uma função do banco, nunca de `new Date()`,
o que torna testes e SSR determinísticos. Escrita sensível só por função não exposta, com
auditoria. Publicação com foto dos números antes e depois como portão de release.

**Tecnologias.** TanStack Start · React 19 · TypeScript · PostgreSQL · PostgREST · Drizzle · Python · Docker

**Minha contribuição.** Desenvolvimento original — arquitetura, modelagem, implementação,
implantação e operação.

### [Alvorumo v1 — Legacy Edition](https://github.com/bvladson/alvorumo-v1) · *desativado em 23/10/2026*
**Business Intelligence & Analytics Platform**

A primeira geração, em PHP 8 sem framework — decisão deliberada: precisava começar em
hospedagem compartilhada e migrar para servidor próprio sem reescrita. 166 endpoints, 503
classes, 125 migrations, 86 contratos de teste, 138 documentos de decisão.

**Diferenciais técnicos.** Camada canônica bronze → silver → gold: o ERP é a fonte, não a
verdade. Isolamento multiempresa com guardas que reprovam o release se houver vazamento.
Barreira estrutural que aborta qualquer migration apontada ao banco de produção — nasceu de um
incidente real. Segredos cifrados em repouso e mascarados em log, com teste que falha se uma
credencial aparecer em texto claro.

**Tecnologias.** PHP 8 · MariaDB · nginx · Python

**Minha contribuição.** Desenvolvimento original. Substituído pela segunda geração sem
interromper a operação.

---

## Business Software

### [Elofarol](https://github.com/bvladson/elofarol-web) · *em produção*
**CRM & Sales Platform** — *Conecte pessoas. Conduza negócios.*

**O problema.** A equipe comercial trabalhava entre o ERP, o WhatsApp pessoal e planilhas de
proposta. Nada conversava, e o que foi combinado com o cliente não sobrevivia à negociação.

**A solução.** Uma aplicação com duas audiências: o site público, com catálogo vindo do ERP,
busca tolerante a erro, carreiras e SEO; e o espaço interno, com CRM, funil, propostas com
versões e alçadas, atendimento por WhatsApp real e conversão para pedido no ERP.

**Diferenciais técnicos.** A conversão é **congelada**: ao aceitar, o sistema guarda um retrato
da proposta com `sha256`, e o pedido no ERP nasce desse retrato, nunca do estado atual da tela
— fechou uma brecha real encontrada em homologação. Escrita no ERP é sempre janela explícita,
com vigia; o padrão é desligada. Testes dedicados falham se uma chave de API aparecer no HTML
servido. Endereços de produto são permanentes: renomear no ERP não quebra link indexado.

**Tecnologias.** TanStack Start · React · TypeScript · SQLite · WAHA · Docker · nginx

**Minha contribuição.** Desenvolvimento original.

### [Elofarol Mobile](https://github.com/bvladson/elofarol-mobile) · *em uso interno*
**CRM & Sales Platform**

A interface Android do Elofarol — segunda interface do mesmo ecossistema, não um produto
separado. Aplicativo nativo em React Native, distribuído internamente, compatível com a
instalação existente.

**Tecnologias.** React Native · Expo

**Minha contribuição.** Desenvolvimento original.

### [Pautelo](https://github.com/bvladson/pautelo) · *em produção*
**Project & Task Management** — *Do planejamento à execução.*

**O problema.** A empresa precisava de gestão de tarefas em português, sem a marca, a loja de
aplicativos nem a telemetria do produto original.

**A solução.** Camada de personalização sobre o Leantime 3.10: 704 chaves de idioma
traduzidas, os 38 passos dos 5 tours guiados em português, identidade visual própria, banco em
instância dedicada. Tudo gerado por scripts idempotentes, com o diff legível versionado.

**Tecnologias.** PHP · MariaDB · Python

**Minha contribuição.** Customização, localização, empacotamento de releases e operação.
O software base é o **Leantime (AGPL-3.0)**, de terceiros — licença, avisos de copyright e
atribuições preservados.

### Operalvo Core · *em produção · repositório privado*
**Enterprise Management Extensions** — *Controle operacional. Visão empresarial.*

Aplicativo Frappe próprio com campos, permissões e lógica de negócio que adaptam o ERPNext v16
à operação atendida.

**Tecnologias.** Frappe · ERPNext v16 · Python · Docker

**Minha contribuição.** Extensões e personalizações. ERPNext e Frappe são de terceiros (GPL-3.0).

### [Docalume](https://github.com/bvladson/docalume-ptbr) · *em produção*
**Document Engineering & Localization** — *Precisão em cada documento.*

**O problema.** Os orçamentos saíam em inglês mesmo com o ERP configurado em português. Cada
palavra tinha uma causa diferente: texto fixo no template, dois-pontos dentro da chave de
tradução, `No` de *número* traduzido como negação, `num2words` caindo no português de Portugal
— e descrevendo o total arredondado, não o impresso.

**A solução.** Formatos de impressão em pt-BR para orçamento, pedido de venda, fatura, guia de
remessa e pedido de compra, mais sete correções no cabeçalho e cinco no rodapé do papel
timbrado — duas delas visíveis só no PDF, que é justamente o que o cliente recebe.

**Diferenciais técnicos.** Os testes comparam a saída renderizada **e** o PDF gerado pelo
próprio servidor: é a única forma de pegar defeito que só existe no PDF.

**Tecnologias.** Frappe · Jinja · Python · wkhtmltopdf

**Minha contribuição.** Desenvolvimento original dos formatos e do diagnóstico.

---

## Artificial Intelligence & Automation

### [Sabelar AI](https://github.com/bvladson/sabelar-ai) · *em produção*
**Private Artificial Intelligence Engine** — *Inteligência que trabalha com você.*

**O problema.** Usar IA sobre dados comerciais sem enviá-los para a nuvem de terceiros.

**A solução.** Modelo de linguagem rodando no próprio servidor (Ollama + gateway em container
isolado), em CPU, sem GPU, dividindo duas vCPUs com nove sistemas em produção.

**Diferenciais técnicos.** O trabalho não foi fazer funcionar, foi provar o isolamento: uma
sonda a partir do container tentou todas as portas internas do servidor e de outros
containers, e **todas as linhas dizem bloqueado**. A evidência ficou arquivada e datada no
repositório.

**Tecnologias.** Ollama · Node.js · Docker

**Minha contribuição.** Arquitetura, integração, isolamento e operação. Os modelos de
linguagem e o motor de inferência são de terceiros e não são de minha autoria.

### [Entreliga](https://github.com/bvladson/entreliga) · *em produção · repositório privado*
**Integration & Automation Hub** — *Tudo conectado. Tudo fluindo.*

**O problema.** Sistemas empresariais que não se falam, cada um com seu login.

**A solução.** CRM, Helpdesk e automações n8n sobre o ERPNext, com central de acesso única,
distribuição de leads por turno, encaminhadores e conta técnica para auditoria. Testes de
segurança na cópia antes de cada promoção.

**Tecnologias.** ERPNext · Frappe · n8n · Docker · Python · GitHub Actions

**Minha contribuição.** Arquitetura de integração, automações e operação. ERPNext, Frappe e
n8n são de terceiros.

---

## Digital Experience & Infrastructure

### [Vitracora](https://github.com/bvladson/vitracora-web) · *em produção*
**Digital Experience Platform** — *Presença digital que gera resultados.*

**O problema.** Presença digital que precisa captar oportunidade sem prometer o que não se
pode comprovar.

**A solução.** Site institucional com identidade própria, CMS headless, captação de leads,
catálogo, páginas legais e hub de vídeos.

**Diferenciais técnicos.** O diferencial não é o site, é o rigor da publicação: 40 scripts
auditam acessibilidade, consentimento, integrações e até se a logo publicada é mesmo o arquivo
oficial — no site servido, não em ambiente de teste. Publicidade e análise são escolhas
independentes, e aceitar análise não aceita publicidade. O checklist proíbe depoimento, número
de clientes ou certificação que não possa ser comprovada.

**Tecnologias.** TanStack Start · React · TypeScript · WordPress (CMS headless) · Docker · Python

**Minha contribuição.** Desenvolvimento original do site e das auditorias.

### [Fortearco](https://github.com/bvladson/fortearco-infrastructure)
**Infrastructure & DevOps Engineering** — *A estrutura por trás da inovação.*

**O problema.** Nove sistemas em produção, de duas empresas, em **um** servidor de 2 vCPUs e
7,75 GiB — sem derrubarem uns aos outros.

**A solução.** Documentação e arquitetura operacional: manifesto por serviço, janela de
operação verificada por código, modelo de release com foto de produção como portão, isolamento
entre serviços, e backup cifrado fora do servidor com restauração exercitada tabela a tabela
(119/119, 2.670.587 linhas idênticas) antes de desligar o sistema legado.

Inclui a lista honesta dos incidentes e o que cada um mudou.

**Tecnologias.** Ubuntu 24.04 LTS · Docker · nginx · Bash · systemd · UFW

**Minha contribuição.** Arquitetura, documentação e operação. Não é um serviço comercial de
hospedagem: é a engenharia de um servidor real.

---

## Números verificáveis

| | |
|:--|:--|
| **9 sistemas** em um servidor de 2 vCPUs e 7,75 GiB | **5 empresas** atendidas pela plataforma de BI |
| **119/119 tabelas · 2.670.587 linhas** conferidas idênticas em ensaio de restauração | **3,5 GB** foi a memória livre mínima em 17 dias de amostragem a cada 5 minutos |

---

## Observações

As cópias públicas têm o endereço da VPS substituído pelo IP de documentação `203.0.113.10`
(RFC 5737), e delas foram removidos logs e capturas que continham metas de faturamento e a
lista nominal da equipe de vendas. Nenhuma credencial foi versionada em momento algum.

Vladson Labs é uma iniciativa tecnológica autoral, **não** uma empresa formalmente
constituída, marca registrada ou fornecedora comercial estabelecida.

As licenças e atribuições dos componentes de terceiros estão preservadas. As pendências de
licenciamento estão registradas em
[`docs/branding/REBRANDING_AUDIT.md`](docs/branding/REBRANDING_AUDIT.md).
