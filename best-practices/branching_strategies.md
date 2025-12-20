# Boas Práticas: Estratégias de Branch

As branches permitem que múltiplas pessoas trabalhem em paralelo
sem interferir diretamente no código principal.

Em times de Suporte à Aplicação, o uso correto de branches ajuda
a organizar correções, hotfixes e ajustes emergenciais.

---

## 🎯 Por que usar branches?

- Evitar impacto direto em produção
- Isolar correções específicas
- Facilitar revisões de código
- Manter o histórico organizado

---

## 📌 Branch principal (main)

A branch `main` representa o código estável.

Boas práticas:
- Evitar commits diretos sem revisão
- Utilizar apenas código testado
- Usada como base para deploys

---

## 🔧 Branch de correção (hotfix)

Utilizada para corrigir problemas urgentes em produção.

Exemplo:
hotfix/corrige-erro-pagamento


Fluxo comum:
1. Criar branch a partir da `main`
2. Aplicar correção
3. Testar
4. Fazer merge de volta na `main`

Uso no suporte:
- Correção de bugs críticos
- Ajustes emergenciais solicitados por clientes

---

## 🛠 Branch de ajuste ou melhoria

Usada para ajustes não críticos ou melhorias incrementais.

Exemplo:
feature/ajusta-log-integracao


Uso no suporte:
- Melhorar logs
- Ajustar mensagens de erro
- Pequenas melhorias operacionais

---

## 🧠 Boas práticas gerais

- Manter branches pequenas e objetivas
- Nomear branches de forma clara
- Evitar branches muito longas
- Sincronizar frequentemente com a `main`

---

## 📌 Relação com Suporte à Aplicação

Para profissionais de suporte, entender estratégias de branch permite:
- Trabalhar com hotfixes de forma segura
- Acompanhar correções feitas pelo time de desenvolvimento
- Apoiar deploys e validações
- Reduzir riscos em produção

---