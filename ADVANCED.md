# Conceitos Avançados de Git

Este documento aborda conceitos intermediários e avançados de Git,
com foco em cenários reais enfrentados em ambientes colaborativos
e no contexto de Suporte à Aplicação.

---

## 1️⃣ git pull

O comando `git pull` atualiza o repositório local com as alterações do repositório remoto.

Uso:
git pull origin main

Esse comando realiza duas ações:
- `git fetch`: busca as alterações remotas
- `git merge`: integra essas alterações ao branch local

Exemplo no suporte:
- Atualizar o código antes de investigar um incidente
- Garantir que a análise seja feita na versão mais recente

---

## 2️⃣ Divergência entre branch local e remota

A divergência ocorre quando:
- Existem commits locais que ainda não foram enviados
- Existem commits remotos que ainda não foram baixados

Mensagem comum:
Your branch and 'origin/main' have diverged

Como resolver:
1. Executar `git pull origin main`
2. Resolver possíveis conflitos
3. Finalizar o merge com `git commit`
4. Enviar as alterações com `git push`

---

## 3️⃣ git merge

O comando `git merge` une alterações de uma branch a outra.

Exemplo:
git merge nome-da-branch


No contexto de suporte:
- Integrar hotfixes
- Unir correções emergenciais
- Consolidar ajustes feitos em paralelo

---

## 4️⃣ git commit --no-edit

O parâmetro `--no-edit` permite finalizar um merge usando a mensagem padrão.

Uso:
git commit --no-edit


Quando usar:
- Merge simples
- Mensagem padrão suficiente
- Evitar abrir editor durante o processo

---

## 5️⃣ git rebase (conceito)

O `git rebase` reaplica commits em outra base.

Uso:
git rebase main

Diferença entre merge e rebase:
- Merge mantém o histórico completo
- Rebase cria um histórico linear

⚠️ Em ambientes colaborativos, o rebase deve ser usado com cuidado.

---

## 🧠 Relação com Suporte à Aplicação

Esses conceitos permitem:
- Resolver conflitos rapidamente
- Manter o código sincronizado
- Trabalhar com hotfixes em produção
- Colaborar com desenvolvedores de forma eficiente

---
