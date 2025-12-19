# Resolução de Conflitos de Merge no Git

Conflitos de merge acontecem quando duas ou mais alterações afetam
a mesma parte de um arquivo e o Git não consegue decidir automaticamente
qual versão deve ser mantida.

Eles são comuns em ambientes colaborativos e fazem parte do dia a dia
de equipes de desenvolvimento e suporte.

---

## 1️⃣ Como identificar um conflito

Ao executar um `git pull` ou `git merge`, o Git pode exibir mensagens como:

CONFLICT (content): Merge conflict in arquivo.txt
Ou o `git status` pode indicar:
You have unmerged paths

---

## 2️⃣ Como o conflito aparece no arquivo

O arquivo afetado conterá marcações como:

```txt
<<<<<<< HEAD
Código local
=======
Código remoto
>>>>>>> origin/main

Significado:

HEAD: versão local

origin/main: versão do repositório remoto

3️⃣ Como resolver o conflito
Passo a passo:

Abrir o arquivo com conflito
Analisar qual trecho deve ser mantido
Remover as marcações <<<<<<<, =======, >>>>>>>
Ajustar o código final corretamente
Salvar o arquivo

Depois disso:

```bash
git add arquivo.txt
git commit

4️⃣ Finalizando o merge
Após resolver todos os conflitos:

```bash

git commit

```
Ou, se desejar usar a mensagem padrão:

```bash

git commit --no-edit

```

5️⃣ Boas práticas para evitar conflitos

Atualizar o repositório com frequência (git pull)
Fazer commits pequenos e objetivos.
Comunicar alterações relevantes ao time.
Evitar editar os mesmos arquivos simultaneamente.

🧠 Relação com Suporte à Aplicação
No suporte técnico, saber resolver conflitos permite:

Integrar hotfixes rapidamente.
Corrigir erros sem atrasar deploys.
Colaborar com desenvolvedores de forma eficaz.
Evitar retrabalho e inconsistências.

📌 Conclusão
Conflitos fazem parte do trabalho em equipe.
Saber resolvê-los com calma e método é uma habilidade essencial
para profissionais de suporte e tecnologia.