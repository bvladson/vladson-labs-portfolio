# Portfólio — sistemas em produção

Nove projetos construídos e mantidos em produção para duas empresas, entre 2026 e hoje:
o **Grupo MAG** (móveis corporativos) e a **VSB Soluções Técnicas** (elétrica, eletrônica e
segurança). Todos rodam no mesmo servidor Ubuntu, descrito no último item desta lista.

Não são exercícios. São sistemas que gente usa para trabalhar, com dados reais, com
horário comercial que não pode cair.

---

## Inteligência comercial

### [BIOMIE v2](https://github.com/bvladson/biomie-v2) · *em produção*
BI comercial multiempresa sobre o ERP Omie, para 5 empresas. Cockpit, Plano de Voo, Vendas,
Clientes 360°, Estoque com curvas e reposição, Financeiro, e um assistente conversacional
ligado a um LLM local.

Autorização no banco por RLS (a tela é só dica), uma única definição por métrica, e 36
scripts de operação que publicam, validam, fotografam e revertem a produção.

`TanStack Start` `React` `TypeScript` `PostgreSQL` `PostgREST` `Python` `Docker`

### [BIOMIE v1](https://github.com/bvladson/biomie-v1) · *desativado em 23/10/2026*
A primeira geração, em PHP 8 sem framework: 166 endpoints, 503 classes, 125 migrations, 86
contratos de teste e 138 documentos de decisão. Camada canônica bronze → silver → gold,
isolamento multiempresa com guardas que falham o release, e uma barreira estrutural contra
escrita acidental em produção — nascida de um incidente real.

`PHP 8` `MariaDB` `nginx`

---

## Comercial e atendimento

### [Site MAG + CRM comercial](https://github.com/bvladson/mag-site-crm) · *em produção*
Uma aplicação, duas audiências: o site público com catálogo vindo do ERP, e o sistema interno
onde a equipe comercial trabalha — CRM, funil, propostas com versões e alçadas, atendimento
por WhatsApp real, carreiras e CMS.

A conversão de proposta em Pedido de Venda no ERP nasce de um *retrato congelado* com
`sha256`, nunca do estado atual da tela — correção de uma brecha encontrada em homologação.

`TanStack Start` `React` `TypeScript` `SQLite` `WAHA` `Docker`

### [MAG CRM — app Android](https://github.com/bvladson/mag-crm-android) · *em produção*
O CRM no celular da equipe comercial: atendimento por WhatsApp com foto, PDF e áudio, funil com
a ficha do negócio, propostas, catálogo e clientes. Interface nativa em React Native, falando
com o CRM por uma API própria, distribuída por APK fora da Google Play
([baixar a 1.0.0](https://github.com/bvladson/mag-crm-android/releases/latest)).

Nenhuma mensagem sai duas vezes: cada envio tem uma chave idempotente guardada com uma
impressão SHA-256 — nunca com o texto. E o script de release abre o APK assinado e varre os
mais de mil arquivos atrás de segredos antes de aprovar.

`React Native` `Expo` `TypeScript` `Android`

### [Base de tarefas MAG](https://github.com/bvladson/mag-base) · *em produção*
Sistema de tarefas da empresa a partir do Leantime 3.10, sem nenhuma marca, loja ou
telemetria do original: 704 chaves de idioma traduzidas, os 38 passos dos 5 tours guiados em
português, identidade visual própria e banco em instância dedicada. Tudo gerado por scripts
idempotentes, com o diff legível versionado.

`PHP` `MariaDB` `Python`

---

## Inteligência artificial

### [MAG AI — LLM local](https://github.com/bvladson/mag-ai) · *em produção*
Modelo de linguagem rodando na própria VPS (Ollama + gateway em container isolado), para que
dado comercial não saia para nuvem de terceiros. Em CPU, sem GPU, dividindo 2 vCPUs com nove
sistemas em produção.

O trabalho interessante foi o isolamento: a evidência arquivada mostra o container tentando
todas as portas internas do servidor e sendo bloqueado em todas.

`Ollama` `Docker` `Node.js`

---

## VSB Soluções Técnicas

### [VSB 360°](https://github.com/bvladson/vsb-360-integrations) · *em produção*
CRM, Helpdesk e automações n8n sobre o ERPNext, com central de acesso única. Distribuição de
leads por turno, encaminhadores, conta técnica para auditoria e testes de segurança na cópia
antes de cada promoção.

`ERPNext` `Frappe` `n8n` `Docker` `Python`

### [Site institucional VSB](https://github.com/bvladson/vsb-site-institucional) · *em produção*
Site com identidade visual própria, CMS headless, captação de leads, catálogo e hub de
vídeos. O diferencial está em `ops/`: 40 scripts que auditam acessibilidade, consentimento,
integrações Google e a logo publicada — no site servido, não em ambiente de teste.

`TanStack Start` `React` `TypeScript` `WordPress` `Docker`

### [ERPNext em português de verdade](https://github.com/bvladson/vsb-erp-ptbr) · *em produção*
Formatos de impressão em pt-BR para ERPNext v16. Os orçamentos saíam em inglês mesmo com o
ERP em português — e cada palavra tinha uma causa diferente: texto fixo no template,
dois-pontos dentro da chave de tradução, `No` traduzido como negação, `num2words` caindo no
português de Portugal. Mais sete defeitos no papel timbrado, dois deles visíveis só no PDF.

`Frappe` `Jinja` `Python`

---

## A infraestrutura

### [Uma VPS Ubuntu, nove sistemas](https://github.com/bvladson/infra-vps-ubuntu)
Como todos os projetos acima convivem em **um servidor de 2 vCPUs e 7,75 GiB** sem derrubar
uns aos outros: manifesto por serviço, janela de operação verificada por código, release com
foto de produção como portão, backup cifrado com restauração testada tabela a tabela
(119/119, 2.670.587 linhas), e segredo que nunca passa pela máquina de desenvolvimento.

Inclui a lista honesta dos incidentes e o que cada um mudou.

---

## Autoria

Todos os sistemas desta página são meus, do desenho à operação: concepção, arquitetura,
modelagem de dados, implementação, implantação e manutenção em produção — inclusive o
servidor onde rodam. Cada decisão técnica listada aqui foi tomada e executada por mim,
contra um sistema real, com gente usando do outro lado.

Durante o desenvolvimento usei assistentes de IA (Codex e Claude) como ferramenta de apoio,
do mesmo jeito que se usa um editor, um depurador ou documentação. A condução, a integração
entre as partes e a responsabilidade pelo que foi para produção são minhas.

## Observação sobre as cópias públicas

Todos os repositórios são cópias publicadas dos projetos reais. Em todos:

- o endereço da VPS foi trocado pelo IP de documentação `203.0.113.10` (RFC 5737);
- foram removidos logs e capturas que continham metas de faturamento e a lista nominal da
  equipe de vendas;
- nenhuma credencial foi versionada em momento algum — o histórico do git confirma.

Os contatos que aparecem são canais públicos das empresas, já publicados nos próprios sites.
