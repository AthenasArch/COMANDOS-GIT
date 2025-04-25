# Documentação dos principais comandos do Git

## 🔗 Clonar um repositório

1. **Login no GitLab Safesoft:**
   - URL: `http://192.168.20.10/`
   - Usuário: `leonardo.hilgemberg`
   - Senha: `18@4...`

2. **Encontrar o repositório:**
   - Navegue até o repositório desejado.

3. **Copiar o link de clone:**
   - Clique no botão **"Clone"** ou **"Clone with SSH/HTTPS"**.
   - Copie o link da opção **"Clone with HTTP"**.

4. **Clonar o repositório localmente:**
   - Abra o prompt de comando e navegue até o diretório desejado.
   - Execute:
     ```bash
     git clone <URL-HTTPS>
     ```
     > Substitua `<URL-HTTPS>` pelo link copiado.

   - Caso solicitado, informe as credenciais:
     - Usuário: `leonardo.hilgemberg`
     - Senha: `18@4...`

5. **Verificar o clone:**
   - Entre no diretório do repositório:
     ```bash
     cd nome-do-repositorio
     ```
   - Verifique se está correto:
     ```bash
     git status
     ```

---

## 🌳 Selecionar e gerenciar branches

- **Alternar branch atual:**
  ```bash
  git switch nome_do_branch
  ```

- **Listar branches remotos:**
  ```bash
  git branch -r
  ```

- **Listar branches locais:**
  ```bash
  git branch
  ```

- **Selecionar branch local existente:**
  ```bash
  git checkout nome-do-branch
  ```

- **Baixar e selecionar branch remoto:**
  ```bash
  git checkout -b nome-do-branch origin/nome-do-branch
  ```

- **Atualizar branch local com o remoto:**
  ```bash
  git pull
  ```

- **Confirmar branch ativo:**
  ```bash
  git branch
  ```
  - O branch ativo estará marcado com um asterisco `*`.

---

## 📦 Comitar alterações

1. Abra o prompt de comandos na pasta raiz do repositório.

2. Verifique o branch atual:
   ```bash
   git branch
   ```

3. Verifique alterações pendentes:
   ```bash
   git status
   ```

4. Adicione arquivos para commit:
   ```bash
   git add .
   ```
   > **Atenção:** confirme se os arquivos são corretos antes de adicionar.

5. Faça o commit das alterações:
   ```bash
   git commit -m "Comentário claro e objetivo aqui"
   ```

6. Envie as alterações para o repositório remoto:
   ```bash
   git push
   ```
   - Caso seja o primeiro push do branch:
     ```bash
     git push --set-upstream origin nome_do_branch
     ```

---

## 🚀 Criar e subir um novo branch

1. Abra o prompt de comandos na pasta raiz do repositório.

2. Verifique o branch atual:
   ```bash
   git branch
   ```

3. Verifique alterações pendentes:
   ```bash
   git status
   ```

4. Crie e alterne para o novo branch:
   ```bash
   git checkout -b nome_do_novo_branch
   ```

5. Envie o novo branch para o repositório remoto (apenas no primeiro push):
   ```bash
   git push -u origin nome_do_novo_branch
   ```

6. Confirme o novo branch ativo:
   ```bash
   git branch
   ```

---

📌 **Observações gerais:**
- Utilize sempre comentários claros e objetivos nos commits para facilitar a compreensão do histórico.
- Verifique regularmente o status dos arquivos com `git status` para evitar commits incorretos.
