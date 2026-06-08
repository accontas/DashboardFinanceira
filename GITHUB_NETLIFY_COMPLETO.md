# 🚀 Guia Completo: GitHub + Netlify Deploy

## 📋 O QUE VAI FAZER

1. ✅ Criar repositório GitHub
2. ✅ Carregar ficheiros lá
3. ✅ Ligar Netlify a GitHub
4. ✅ Deploy automático
5. ✅ Ter site funcional em 10 minutos

---

## 🔧 PASSO 1: Preparar Ficheiros Localmente (5 min)

### 1.1 Criar Pasta

```
No seu PC:
C:\dashboard-netlify\

ou em Mac/Linux:
~/dashboard-netlify/
```

### 1.2 Copiar Ficheiros

Copia ESTES ficheiros para a pasta:

1. **index.html** (cria novo, vê conteúdo em FICHEIROS_NETLIFY.md)
2. **setup.html** (copia de SETUP_GOOGLE_DRIVE.html)
3. **admin.html** (copia de admin_CORRIGIDO.html)
4. **dashboard.html** (copia de dashboard_cliente_final.html)
5. **dados_teste.json** (copia o ficheiro existente)
6. **README.md** (cria novo, vê conteúdo em FICHEIROS_NETLIFY.md)

### 1.3 Estrutura Final

```
C:\dashboard-netlify\
├─ index.html
├─ setup.html
├─ admin.html
├─ dashboard.html
├─ dados_teste.json
└─ README.md
```

---

## 🐙 PASSO 2: Criar Repositório GitHub (3 min)

### 2.1 Abrir GitHub

```
Ir a: https://github.com
```

### 2.2 Criar Novo Repositório

```
1. Clique no + (canto superior direito)
2. "New repository"
3. Nome: dashboard-financeiro
4. Descrição: Dashboard financeiro com sincronização Google Drive
5. Público (Public)
6. Clique "Create repository"
```

### 2.3 Resultado

Vai receber URL:
```
https://github.com/SEU_USERNAME/dashboard-financeiro
```

---

## 💾 PASSO 3: Carregar Ficheiros no GitHub (3 min)

### 3.1 Via GitHub Web (Mais Fácil)

```
1. Abra GitHub no navegador
2. https://github.com/SEU_USERNAME/dashboard-financeiro
3. Clique em "Add file" → "Upload files"
4. Arraste a pasta dashboard-netlify para lá
5. Clique "Commit changes"
```

### 3.2 Via Git (Se Souber)

```bash
cd C:\dashboard-netlify

git init
git add .
git commit -m "Initial commit - Dashboard Financeiro"
git branch -M main
git remote add origin https://github.com/SEU_USERNAME/dashboard-financeiro.git
git push -u origin main
```

---

## 🌐 PASSO 4: Deploy em Netlify (2 min)

### 4.1 Conectar Netlify a GitHub

```
1. Ir a: https://netlify.com
2. Clique "Sign up" (use GitHub)
3. Autorize Netlify no GitHub
4. Confirme email
```

### 4.2 Criar Site

```
1. Em Netlify, clique "Add new site"
2. "Import an existing project"
3. Escolha GitHub
4. Procure "dashboard-financeiro"
5. Clique para conectar
6. Clique "Deploy site"
```

### 4.3 Esperar Deploy

```
Netlify processa:
⏳ Deploying (30-60 segundos)
✅ Published
```

### 4.4 Receber URL

```
Algo como:
https://dashboard-financeiro-123abc.netlify.app

Esta é a sua URL pública!
```

---

## ✅ PASSO 5: Testar (5 min)

### 5.1 Abrir Site

```
https://dashboard-financeiro-123abc.netlify.app/
```

Deve aparecer página inicial com 3 botões.

### 5.2 Setup

```
1. Clique "Setup"
2. Preencha: 1O3gknpISXL7kMl7e3kEQ_-kLHjlSqYl6
3. Clique "Guardar"
4. ✅ Configuração guardada
```

### 5.3 Admin

```
1. Clique "Admin"
2. Carregue dados_teste.json (ou CSV)
3. Clique "Guardar Dados"
4. ✅ Dados guardados
```

### 5.4 Dashboard

```
1. Clique "Dashboard"
2. Deve aparecer com dados
3. Seletor período funciona
4. ✅ Tudo OK!
```

---

## 🎯 PASSO 6: Dar Link ao Cliente (1 min)

### 6.1 URL para Cliente

```
https://dashboard-financeiro-123abc.netlify.app/dashboard.html
```

### 6.2 Enviar por Email

```
Assunto: Dashboard Financeiro - Acesso

Olá,

Segue em anexo o seu Dashboard Financeiro:

https://dashboard-financeiro-123abc.netlify.app/dashboard.html

Pode visualizar os dados a qualquer hora.

Obrigado
```

---

## 🔄 PASSO 7: Atualizar Dados Mensalmente (5 min)

### 7.1 Você (Admin)

```
1. Abra: https://dashboard-financeiro-123abc.netlify.app/admin.html
2. Carregue CSV do mês
3. Clique "Guardar Dados"
4. Clique "Sincronizar"
5. ✅ Pronto!
```

### 7.2 Cliente

```
Cliente apenas:
1. Abre: https://dashboard-financeiro-123abc.netlify.app/dashboard.html
2. Vê dados atualizados
3. Sem fazer mais nada!
```

---

## 🚀 Resumo Rápido

| Etapa | O Quê | Tempo |
|-------|-------|-------|
| 1 | Preparar ficheiros | 5 min |
| 2 | Criar GitHub | 3 min |
| 3 | Carregar GitHub | 3 min |
| 4 | Deploy Netlify | 2 min |
| 5 | Testar | 5 min |
| 6 | Enviar cliente | 1 min |
| **Total** | | **19 min** |

---

## 💡 Dicas

### Mudar Nome da URL Netlify

```
1. Em Netlify, vá a "Site settings"
2. "Change site name"
3. Digite: seu-nome-bonito
4. Nova URL: https://seu-nome-bonito.netlify.app
```

### Atualizar Ficheiros

```
GitHub → Faz push
    ↓
Netlify → Detecta mudança
    ↓
Deploy automático (5-10 seg)
```

### Ver Logs de Deploy

```
Em Netlify:
1. Clique em "Deploys"
2. Vê histórico
3. Clique em deploy para ver logs
```

---

## 🎉 Pronto!

Depois destes passos:

✅ Site funcional em Netlify
✅ GitHub com versão control
✅ Cliente pode visualizar
✅ Dados sincronizam automaticamente
✅ Atualiza mensalmente em 5 minutos

---

**Comece agora! Vai demorar menos de 20 minutos! 🚀**

