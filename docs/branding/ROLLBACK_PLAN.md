# Plano de reversão

A reversão **não depende** de banco de dados nem de alteração em produção: nada em produção
foi tocado por este trabalho.

## 1. Pastas locais

As pastas foram **movidas** (não copiadas) de `C:\Users\VLADSON\Portfolio\<antigo>` para
`C:\Users\VLADSON\Vladson-Labs\<novo>`, preservando `.git`, branches, tags e configuração.

Reverter = mover de volta com os nomes da coluna "Repositório antigo" do
[`MIGRATION_MAP.md`](MIGRATION_MAP.md). Nenhum sistema aponta para esses caminhos.

## 2. Cópia no pendrive

`D:\Vladson-Labs\` é uma **cópia**, não a fonte. Apagá-la não afeta nada.
A pasta `D:\MAG-CUSTODIA-TI` não foi tocada e não faz parte deste trabalho.

## 3. Repositórios renomeados no GitHub

Renomear de volta, pelo mesmo caminho: Settings → General → Repository name.
O GitHub mantém o redirecionamento do nome antigo nos dois sentidos.

Depois de reverter um nome, corrigir o remote local:

    git remote set-url origin https://github.com/bvladson/<nome-antigo>.git
    git ls-remote --heads origin      # confirmar que responde

## 4. Commits de branding

Cada commit de rebranding é pequeno, isolado e reversível com `git revert`. Nenhum histórico
foi reescrito, nenhum force push foi feito, nenhuma branch ou tag foi removida.

Para listar o que entrou:

    git log --oneline --grep="branding\|naming\|Vladson Labs"

## 5. O que não precisa de reversão

Nada foi alterado em: produção, VPS, Docker, nginx, systemd, crontabs, bancos de dados,
domínios, DNS, certificados, credenciais, `applicationId` do Android, keystore, licenças ou
atribuições de terceiros.
