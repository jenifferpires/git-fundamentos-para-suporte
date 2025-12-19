code BASICS.md

# Conceitos Básicos de Git

Este documento apresenta os principais comandos de Git utilizados no dia a dia,
com foco em quem atua em Suporte à Aplicação e precisa entender o estado do código,
acompanhar alterações e colaborar com times de desenvolvimento.

---

## 1️⃣ git status

O comando `git status` exibe o estado atual do repositório.

Ele informa:
- Arquivos modificados
- Arquivos não rastreados
- Arquivos prontos para commit
- Situações de merge ou conflitos

Uso:


git status


Exemplo de uso no suporte:
- Verificar se há alterações locais antes de atualizar o código
- Confirmar se um arquivo foi corretamente versionado
- Identificar se um merge está em andamento

---

## 2️⃣ git add

O comando `git add` adiciona arquivos à área de staging, preparando-os para commit.

Adicionar um arquivo específico:


git add arquivo.txt


Adicionar todos os arquivos modificados:


git add .


Exemplo de uso no suporte:
- Versionar logs de testes
- Preparar scripts de correção
- Registrar ajustes feitos durante a análise de um incidente

---

## 3️⃣ git commit

O comando `git commit` cria um registro permanente das alterações versionadas.

Uso:


git commit -m "Mensagem clara e objetiva"


Boas práticas:
- Mensagens curtas e descritivas
- Explicar o motivo da alteração
- Evitar mensagens genéricas como "ajustes"

Exemplo de mensagem adequada:


git commit -m "Ajusta validação de payload no endpoint de pedidos"


---

## 4️⃣ git push

O comando `git push` envia os commits locais para o repositório remoto (GitHub).

Uso:


git push origin main


Exemplo de uso no suporte:
- Enviar correções para revisão
- Compartilhar documentação técnica
- Atualizar scripts usados por outros membros do time

---

## 5️⃣ Fluxo básico de trabalho com Git

Um fluxo simples e comum no dia a dia:



git status
git add .
git commit -m "Descrição da alteração"
git push origin main


Esse fluxo garante:
- Controle de versões
- Rastreabilidade
- Colaboração segura

---

## 🧠 Relação com Suporte à Aplicação

No contexto de suporte, esses comandos permitem:
- Entender rapidamente o estado do projeto
- Registrar evidências técnicas
- Trabalhar de forma organizada
- Reduzir erros durante correções emergenciais

---