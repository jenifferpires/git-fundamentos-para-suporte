# Cenários Reais de Uso do Git

Este documento apresenta situações reais enfrentadas no uso do Git,
especialmente em contextos de Suporte à Aplicação, sustentação e trabalho em equipe.

---

## 1️⃣ Branch local atrás da remota (behind)

Mensagem comum:
Your branch is behind 'origin/main'

diff
Copiar código

Causa:
- Outros commits foram enviados ao repositório remoto
- O repositório local está desatualizado

Solução:
git pull origin main

yaml
Copiar código

Uso no suporte:
- Garantir que a análise seja feita na versão mais atual
- Evitar investigar problemas já corrigidos

---

## 2️⃣ Branch local e remota divergiram

Mensagem comum:
Your branch and 'origin/main' have diverged

diff
Copiar código

Causa:
- Commits locais e remotos diferentes
- Ambos precisam ser integrados

Solução:
git pull origin main

yaml
Copiar código

Passos:
1. Resolver conflitos (se existirem)
2. Finalizar o merge com `git commit`
3. Enviar as alterações com `git push`

---

## 3️⃣ Merge em andamento (MERGING)

Mensagem comum:
All conflicts fixed but you are still merging

diff
Copiar código

Causa:
- Conflitos já resolvidos
- Merge ainda não finalizado

Solução:
git commit

nginx
Copiar código
ou
git commit --no-edit

yaml
Copiar código

Uso no suporte:
- Concluir correções emergenciais
- Finalizar integração de hotfixes

---

## 4️⃣ Push rejeitado (non-fast-forward)

Mensagem comum:
! [rejected] main -> main (non-fast-forward)

makefile
Copiar código

Causa:
- O repositório remoto possui commits que não existem localmente

Solução:
git pull origin main
git push origin main

yaml
Copiar código

Uso no suporte:
- Garantir consistência do histórico
- Evitar sobrescrever correções de outros membros

---

## 5️⃣ Arquivos que não deveriam ser versionados

Exemplo:
- `__pycache__/`
- `.env`
- arquivos temporários

Solução:
- Criar ou ajustar o arquivo `.gitignore`
- Remover arquivos indevidos do versionamento

Uso no suporte:
- Manter o repositório limpo
- Evitar vazamento de informações sensíveis

---

## 🧠 Conclusão

Conhecer esses cenários permite:
- Resolução mais rápida de problemas
- Menos erros em produção
- Comunicação técnica mais eficiente com o time

---