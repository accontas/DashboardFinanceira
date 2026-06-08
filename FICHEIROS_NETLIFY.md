# 📦 Ficheiros Necessários para Netlify

## ✅ FICHEIROS QUE PRECISAS CARREGAR (6 ficheiros HTML)

Copia **APENAS ESTES** para uma pasta:

```
dashboard-netlify/
├─ index.html                          (NOVO - página inicial)
├─ admin.html                          (Admin para carregar dados)
├─ dashboard.html                      (Dashboard para cliente)
├─ setup.html                          (Configuração Google Drive)
├─ dados_teste.json                    (Dados de exemplo)
└─ README.md                           (Instruções)
```

**Total: 6 ficheiros HTML + 1 JSON + 1 README**

---

## 📝 Ficheiro 1: index.html

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard Financeiro</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #0F1419 0%, #1a2f40 100%);
            color: #E8F0F3;
            min-height: 100vh;
            padding: 40px 20px;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }
        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #0EA5A0;
        }
        p {
            font-size: 1.1rem;
            margin-bottom: 30px;
            color: #a0b4c7;
            line-height: 1.6;
        }
        .buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 30px;
        }
        @media (max-width: 600px) {
            .buttons { grid-template-columns: 1fr; }
        }
        .btn {
            padding: 15px 30px;
            font-size: 1rem;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        .btn-admin {
            background: linear-gradient(135deg, #3b82f6, #1d4ed8);
            color: white;
        }
        .btn-admin:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(59, 130, 246, 0.3);
        }
        .btn-dashboard {
            background: linear-gradient(135deg, #0EA5A0, #0d8f8a);
            color: white;
        }
        .btn-dashboard:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(14, 165, 160, 0.3);
        }
        .btn-setup {
            background: linear-gradient(135deg, #C9A84C, #a07c2c);
            color: white;
        }
        .btn-setup:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(201, 168, 76, 0.3);
        }
        .info {
            background: rgba(14, 165, 160, 0.1);
            border: 1px solid #0EA5A0;
            border-radius: 8px;
            padding: 20px;
            margin-top: 30px;
            text-align: left;
        }
        .info h3 {
            color: #0EA5A0;
            margin-bottom: 10px;
        }
        .info p {
            font-size: 0.9rem;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>📊 Dashboard Financeiro</h1>
        <p>Gestão de dados financeiros com sincronização automática</p>
        
        <div class="buttons">
            <button class="btn btn-setup" onclick="window.location.href='setup.html'">
                ⚙️ Setup (Configuração)
            </button>
            <button class="btn btn-admin" onclick="window.location.href='admin.html'">
                👤 Admin (Carregar Dados)
            </button>
            <button class="btn btn-dashboard" onclick="window.location.href='dashboard.html'">
                📈 Dashboard (Visualizar)
            </button>
        </div>

        <div class="info">
            <h3>🎯 Como Usar</h3>
            <p><strong>1️⃣ Primeira vez:</strong> Clique em "Setup" para configurar Google Drive</p>
            <p><strong>2️⃣ Mensalmente:</strong> Clique em "Admin" para carregar dados CSV</p>
            <p><strong>3️⃣ Sempre:</strong> Clique em "Dashboard" para visualizar os dados</p>
            <p style="margin-top: 15px; color: #10b981;"><strong>✅ Nota:</strong> Dados sincronizam automaticamente. Cliente apenas visualiza dashboard.</p>
        </div>
    </div>
</body>
</html>
```

---

## 🎨 Ficheiro 2: setup.html

**Use o ficheiro existente:** `SETUP_GOOGLE_DRIVE.html`

(Copie o conteúdo e renomeie para `setup.html`)

---

## ⚙️ Ficheiro 3: admin.html

**Use o ficheiro corrigido:** `admin_CORRIGIDO.html`

(Copie o conteúdo e renomeie para `admin.html`)

---

## 📊 Ficheiro 4: dashboard.html

**Use o ficheiro:** `dashboard_cliente_final.html`

(Copie o conteúdo e renomeie para `dashboard.html`)

---

## 📄 Ficheiro 5: dados_teste.json

**Use o ficheiro existente:** `dados_teste.json`

(Copia exatamente como está)

---

## 📝 Ficheiro 6: README.md

```markdown
# 📊 Dashboard Financeiro - Netlify

## 🚀 Como Usar

### 1️⃣ Setup (Uma Única Vez)
1. Abra: https://seu-site.netlify.app/setup.html
2. Introduza ID da pasta Google Drive: `1O3gknpISXL7kMl7e3kEQ_-kLHjlSqYl6`
3. Clique "Guardar Configuração"

### 2️⃣ Admin (Mensal)
1. Abra: https://seu-site.netlify.app/admin.html
2. Carregue CSV com dados do mês
3. Clique "Guardar Dados"
4. Clique "Sincronizar com Google Drive"

### 3️⃣ Cliente Visualiza
1. Compartilhe este link: https://seu-site.netlify.app/dashboard.html
2. Cliente abre e vê dados atualizados
3. Pode selecionar período (mês/trimestre/ano)

## 📋 Estrutura

```
dashboard-netlify/
├─ index.html (página inicial)
├─ setup.html (configuração)
├─ admin.html (carregar dados)
├─ dashboard.html (visualização)
├─ dados_teste.json (dados de exemplo)
└─ README.md (este ficheiro)
```

## 🔑 ID Google Drive

```
1O3gknpISXL7kMl7e3kEQ_-kLHjlSqYl6
```

## 💾 Dados Persistem

localStorage guarda:
- Configuração Google Drive
- Dados do dashboard
- Data da última atualização

Tudo sincroniza automaticamente em Netlify!

## 📞 Support

Se algo não funcionar:
1. Verifique se completou Setup
2. Verifique se carregou dados em Admin
3. Recarregue a página (Ctrl+F5)
4. Limpe cache do navegador

---

**Criado com ❤️ para gestão financeira eficiente**
```

---

## 📂 ESTRUTURA FINAL

```
dashboard-netlify/
├─ index.html
├─ setup.html
├─ admin.html
├─ dashboard.html
├─ dados_teste.json
└─ README.md
```

**Total: 6 ficheiros**

---

## ✅ Próximo Passo

Criei a lista de ficheiros. Agora vou dar:
1. Instruções GitHub
2. Instruções Netlify
3. Links prontos a copiar

Continua? 🚀
