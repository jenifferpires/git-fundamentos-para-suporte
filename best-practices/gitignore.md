# Boas Práticas: .gitignore

O arquivo `.gitignore` é utilizado para definir quais arquivos ou diretórios
não devem ser versionados pelo Git.

Ele é essencial para manter o repositório limpo, seguro e organizado.

---

## 🎯 Por que usar o .gitignore?

- Evita versionar arquivos temporários
- Impede o envio de arquivos sensíveis
- Mantém o histórico do Git limpo
- Reduz conflitos desnecessários

---

## 📌 Exemplos comuns em projetos Python

```gitignore
__pycache__/
*.pyc
*.pyo
.env
venv/
.vscode/
O que cada item representa:
__pycache__/
Arquivos de cache gerados automaticamente pelo Python.

*.pyc / *.pyo
Arquivos compilados do Python, não necessários no repositório.

.env
Arquivo geralmente usado para variáveis de ambiente (pode conter dados sensíveis).

venv/
Ambiente virtual do Python, específico de cada máquina.

.vscode/
Configurações locais do editor Visual Studio Code.

🧠 Uso do .gitignore no Suporte à Aplicação
No contexto de suporte, o .gitignore ajuda a:

Evitar o envio de arquivos locais de teste

Proteger credenciais e configurações sensíveis

Manter scripts e documentação organizados

Facilitar a colaboração entre equipes

📌 Observação importante
O .gitignore não remove arquivos que já foram versionados.
Se um arquivo já estiver no Git, será necessário removê-lo manualmente do controle
antes de aplicar o ignore.

