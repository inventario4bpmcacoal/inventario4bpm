# GUIA COMPLETO — PUBLICAR SISTEMA NO GITHUB PAGES
## 4º Batalhão de Polícia Militar — P4 / Inventário

---

## O QUE VOCÊ VAI FAZER

Publicar os 4 arquivos do sistema (index, login, dashboard, config) no GitHub Pages.
O resultado será um link público tipo:
```
https://SEU-USUARIO.github.io/inventario-4bpm/
```
Qualquer computador do batalhão abre esse link e acessa o sistema.

---

## PARTE 1 — CRIAR CONTA NO GITHUB

1. Abra o navegador e acesse: **https://github.com**

2. Clique em **"Sign up"** (canto superior direito)

3. Preencha os campos:
   - **Username** (nome de usuário): use algo relacionado ao batalhão
     - Sugestão: `inventario4bpm` ou `p4-4bpm`
   - **Email**: use o e-mail oficial da seção (ex: `p4@4bpm.pm.ro.gov.br`)
   - **Password**: crie uma senha forte (mínimo 8 caracteres, com números)

4. Clique em **"Continue"**

5. Resolva o puzzle de verificação (arrastar peça ou similar)

6. Escolha o plano **"Free"** e clique em **"Continue for free"**

7. Verifique seu e-mail: o GitHub envia um código de confirmação.
   - Abra o e-mail → copie o código de 6 dígitos → cole no GitHub

8. Conta criada! ✅

---

## PARTE 2 — CRIAR O REPOSITÓRIO

1. Após fazer login no GitHub, clique no ícone **"+"** no canto superior direito

2. Clique em **"New repository"**

3. Preencha:
   - **Repository name**: `inventario-4bpm`
   - **Description**: `Sistema de Inventário Patrimonial — 4º BPM P4`
   - Marque **"Public"** (obrigatório para GitHub Pages gratuito)
   - ✅ Marque **"Add a README file"**

4. Clique em **"Create repository"**

5. O repositório foi criado! ✅

---

## PARTE 3 — OBTER A URL DO APPS SCRIPT (NOVA IMPLANTAÇÃO)

⚠️ Esta etapa é obrigatória — o sistema precisa saber o endereço da nova planilha.

1. Abra a **planilha do 4º BPM** no Google Drive

2. Clique em **Extensões → Apps Script**

3. No Apps Script, clique em **"Implantar" → "Nova implantação"**

4. Em "Tipo", selecione **"Aplicativo da Web"**

5. Configure:
   - **Descrição**: `Inventario 4BPM v1`
   - **Executar como**: `Eu (seu e-mail)`
   - **Quem tem acesso**: `Qualquer pessoa`

6. Clique em **"Implantar"**

7. Copie a URL que aparece — ela tem este formato:
   ```
   https://script.google.com/macros/s/XXXXXXXXXXXXXXXXXX/exec
   ```

8. **Guarde essa URL** — você vai precisar dela no próximo passo.

---

## PARTE 4 — ATUALIZAR O config.js COM A URL CORRETA

Abra o arquivo `config.js` (que você baixou aqui) em qualquer editor de texto
(Bloco de Notas, Notepad++, etc.).

Encontre esta linha:
```javascript
API_URL: 'COLE_AQUI_A_URL_DO_APPS_SCRIPT',
```

Substitua pelo endereço que você copiou no passo anterior:
```javascript
API_URL: 'https://script.google.com/macros/s/SUA_URL_AQUI/exec',
```

Salve o arquivo.

---

## PARTE 5 — FAZER UPLOAD DOS ARQUIVOS NO GITHUB

1. Acesse o repositório que você criou: `github.com/SEU-USUARIO/inventario-4bpm`

2. Clique em **"Add file" → "Upload files"**

3. Arraste os 4 arquivos para a área de upload (ou clique em "choose your files"):
   - `index.html`
   - `login.html`
   - `dashboard.html`
   - `config.js`  ← o que você acabou de editar com a URL correta

4. Na seção **"Commit changes"** (lá embaixo da página):
   - Em "Add files via upload", pode deixar como está
   - Clique em **"Commit changes"** (botão verde)

5. Upload concluído! ✅

---

## PARTE 6 — ATIVAR O GITHUB PAGES

1. No repositório, clique em **"Settings"** (ícone de engrenagem, na barra superior)

2. No menu lateral esquerdo, clique em **"Pages"**

3. Em **"Branch"**, clique no seletor e escolha **"main"**

4. Deixe a pasta como **"/ (root)"**

5. Clique em **"Save"**

6. Aguarde 1 a 3 minutos

7. Recarregue a página de Settings → Pages

8. Aparecerá uma mensagem verde:
   ```
   ✅ Your site is live at https://SEU-USUARIO.github.io/inventario-4bpm/
   ```

9. Clique no link e teste o sistema! ✅

---

## PARTE 7 — TESTAR O SISTEMA

1. Acesse o link do GitHub Pages
2. Clique em **"ACESSAR SISTEMA"**
3. Use as credenciais padrão:
   - **Matrícula**: `ADMIN`
   - **Senha**: `admin123`
4. Se o login funcionar, o sistema está 100% integrado com a planilha ✅

---

## COMO ATUALIZAR OS ARQUIVOS NO FUTURO

Sempre que precisar alterar algo (ex: mudar a URL do Apps Script após reimplantar):

1. Acesse o repositório no GitHub
2. Clique no arquivo que quer editar (ex: `config.js`)
3. Clique no ícone de lápis ✏️ (Edit this file)
4. Faça a alteração
5. Clique em **"Commit changes"**

O site atualiza automaticamente em 1-2 minutos.

---

## COMO COMPARTILHAR O LINK COM AS SEÇÕES

O link do sistema é sempre o mesmo após a ativação:
```
https://SEU-USUARIO.github.io/inventario-4bpm/
```

Você pode:
- Salvar nos favoritos de todos os computadores do batalhão
- Enviar pelo WhatsApp/e-mail para os responsáveis de cada seção
- Criar um atalho na área de trabalho dos computadores

---

## RESUMO RÁPIDO — ORDEM DAS ETAPAS

```
1. Criar conta no GitHub (github.com → Sign up)
2. Criar repositório "inventario-4bpm" (público + README)
3. Obter URL do Apps Script (Extensões → Apps Script → Implantar → Nova implantação)
4. Editar config.js — colar a URL na linha API_URL
5. Fazer upload dos 4 arquivos no repositório
6. Ativar GitHub Pages (Settings → Pages → Branch: main → Save)
7. Aguardar 2 min → testar o link
```

---

*Sistema de Inventário Patrimonial — 4º BPM / P4 — PMRO*
