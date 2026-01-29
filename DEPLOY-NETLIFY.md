# 🚀 Como Subir no Netlify (GRATUITO)

## Método 1: Arrastar e Soltar (Mais Fácil) 🎯

### Passo 1: Preparar os Arquivos
1. Coloque TODOS os arquivos em uma pasta:
   - `index.html`
   - `admin.html`
   - `netlify.toml`

### Passo 2: Criar Conta no Netlify
1. Acesse: https://www.netlify.com/
2. Clique em **"Sign up"** (Cadastrar)
3. Pode usar sua conta do GitHub, GitLab, ou Email

### Passo 3: Fazer Deploy
1. No dashboard do Netlify, procure a área que diz:
   **"Want to deploy a new site without connecting to Git?"**
2. **Arraste a pasta** com todos os arquivos para essa área
   OU
3. Clique em **"Browse to upload"** e selecione os arquivos

### Passo 4: Pronto! 🎉
- O Netlify vai gerar um link tipo: `https://nome-aleatorio-123.netlify.app`
- Seu site está NO AR!

### Passo 5: Mudar o Nome (Opcional)
1. Clique em **"Site settings"**
2. Clique em **"Change site name"**
3. Escolha um nome: `bbb-votacao-2025` 
4. Seu site ficará: `https://bbb-votacao-2025.netlify.app`

---

## Método 2: Pelo GitHub (Para quem quer usar Git)

### Passo 1: Criar Repositório no GitHub
1. Acesse: https://github.com/new
2. Nome do repositório: `bbb-voting`
3. Marque como **Public**
4. Clique em **"Create repository"**

### Passo 2: Fazer Upload dos Arquivos
1. Na página do repositório, clique em **"uploading an existing file"**
2. Arraste os arquivos:
   - `index.html`
   - `admin.html`
   - `netlify.toml`
3. Clique em **"Commit changes"**

### Passo 3: Conectar com Netlify
1. No Netlify, clique em **"Add new site"** → **"Import an existing project"**
2. Escolha **"GitHub"**
3. Autorize o Netlify a acessar seus repositórios
4. Selecione o repositório `bbb-voting`
5. Clique em **"Deploy site"**

### Passo 4: Pronto! 🎉
- Netlify vai fazer o deploy automaticamente
- Toda vez que você atualizar no GitHub, o site atualiza sozinho!

---

## ⚙️ Configurar o Firebase

Depois de fazer o deploy, você precisa colocar as credenciais do Firebase:

### Via Netlify (Recomendado)
1. No dashboard do Netlify, clique em **"Site settings"**
2. Vá em **"Build & deploy"** → **"Environment variables"**
3. **NÃO PRECISA** fazer isso para o Firebase (ele já está no código)
4. Apenas **edite os arquivos** `index.html` e `admin.html` localmente
5. Substitua as credenciais do Firebase
6. Faça upload novamente (ou commit no GitHub)

### Diretamente nos Arquivos
1. Abra `index.html` e `admin.html` em um editor de texto
2. Procure por:
```javascript
const firebaseConfig = {
    apiKey: "SUA_API_KEY",
    ...
};
```
3. Substitua pelas suas credenciais do Firebase
4. Salve os arquivos
5. Faça upload novamente no Netlify

---

## 🔑 Mudar a Senha do Admin

Abra o arquivo `admin.html` e procure por:

```javascript
// ALTERE A SENHA AQUI! 🔑
const ADMIN_PASSWORD = "bbb2025";
```

Mude `"bbb2025"` para a senha que você quiser!

Exemplo:
```javascript
const ADMIN_PASSWORD = "minhasenhasupersecreta123";
```

**IMPORTANTE:** Depois de mudar a senha, faça upload novamente!

---

## 📸 Como Adicionar Fotos dos Participantes

Você tem 2 opções:

### Opção 1: Upload Direto (Recomendado)
1. Entre no painel admin: `https://seu-site.netlify.app/admin.html`
2. Digite a senha
3. Clique em **"📷 Clique para fazer upload da foto"**
4. Escolha a foto do seu computador
5. Preencha o nome
6. Clique em **"Adicionar Participante"**

**IMPORTANTE:** As fotos ficam salvas como Base64 no Firebase. Para fotos grandes (>500kb), use a Opção 2!

### Opção 2: URL de Imagem
1. Faça upload da foto em um site como:
   - https://imgur.com/ (gratuito)
   - https://postimages.org/ (gratuito)
   - https://imgbb.com/ (gratuito)
2. Copie o link da imagem
3. No painel admin, cole o link no campo **"URL da Imagem"**
4. A imagem vai aparecer automaticamente!

---

## 🔄 Atualizar o Site

### Se usou Arrastar e Soltar:
1. Faça as mudanças nos arquivos localmente
2. Arraste os arquivos novamente para o Netlify
3. Netlify atualiza automaticamente!

### Se usou GitHub:
1. Faça as mudanças nos arquivos
2. Faça commit e push para o GitHub
3. Netlify detecta e atualiza automaticamente!

---

## 🆘 Problemas Comuns

**"Meu site não carrega"**
- Verifique se todos os arquivos foram enviados
- Veja os logs no Netlify: Site settings → Deploy logs

**"Não consigo votar"**
- Verifique se colocou as credenciais do Firebase
- Abra o Console (F12) e veja se há erros

**"Senha do admin não funciona"**
- Verifique se mudou a senha no arquivo `admin.html`
- Certifique-se que fez upload da versão atualizada

**"As imagens não aparecem"**
- Se usou URL, verifique se o link está correto
- Se fez upload, a imagem pode estar muito grande (tente <500kb)

---

## 💡 Dicas Pro

1. **Domínio Personalizado** (opcional):
   - Netlify → Site settings → Domain management
   - Você pode comprar um domínio ou usar um que já tem

2. **HTTPS Automático**:
   - Netlify ativa HTTPS automaticamente
   - Seu site é seguro por padrão! 🔒

3. **Analytics**:
   - Netlify tem analytics gratuito
   - Veja quantas pessoas votaram!

4. **Backup**:
   - Netlify guarda todas as versões antigas
   - Pode voltar para versão anterior a qualquer momento

---

## 🎉 Tudo Pronto!

Seu site de votação BBB está no ar, GRATUITO e profissional!

**Links importantes:**
- Página de votação: `https://seu-site.netlify.app/`
- Painel admin: `https://seu-site.netlify.app/admin.html`
- Senha padrão: `bbb2025` (lembre de mudar!)

**Compartilhe:**
- Envie o link da votação para as pessoas
- Guarde o link do admin só para você!

---

Qualquer dúvida, o Netlify tem suporte muito bom (em inglês):
https://docs.netlify.com/

Boa sorte com sua simulação! 🏠✨
