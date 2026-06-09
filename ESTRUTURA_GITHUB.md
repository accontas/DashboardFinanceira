# 📦 Estrutura Correta para GitHub

## ⚠️ CORREÇÃO: 3 Ficheiros Separados (Não 1!)

A solução completa tem **3 ficheiros HTML distintos**:

```
seu-repositorio/
├── SETUP_GOOGLE_DRIVE.html      ← Configuração inicial (one-time)
├── admin.html                    ← Admin: Carregar dados mensalmente
├── index.html                    ← Cliente: Visualizar dados
├── README.md
├── DEPLOY.md
├── netlify.toml
└── .gitignore
```

---

## 📋 Explicação de Cada Ficheiro

### 1️⃣ **SETUP_GOOGLE_DRIVE.html** (19 KB)
**Quando usar**: Uma única vez no início
**O que faz**:
- Configura autenticação Google Drive
- Obtém OAuth token
- Cria pasta no Google Drive
- Guarda credenciais no browser

**Fluxo**:
```
Abrir SETUP_GOOGLE_DRIVE.html
        ↓
Clicar "Autorizar Google Drive"
        ↓
Fazer login com Google
        ↓
Permitir acesso ao Drive
        ↓
✅ Setup completo
```

---

### 2️⃣ **admin.html** (15 KB)
**Quando usar**: Mensalmente (ou quando há dados novos)
**Quem usa**: Administrador / Equipa Financeira
**O que faz**:
- Interface para carregar ficheiro CSV/Excel
- Validação de dados
- Preview antes de guardar
- Sincroniza com Google Drive automaticamente
- Guarda em localStorage

**Fluxo Mensal**:
```
Abrir admin.html (com credenciais do setup)
        ↓
Arrasta ficheiro CSV/Excel
        ↓
Sistema valida dados
        ↓
Mostra prévia
        ↓
Clicar "Guardar Dados"
        ↓
✅ Sincroniza Google Drive
✅ Guarda localStorage
```

---

### 3️⃣ **index.html** (92 KB)
**Quando usar**: Sempre (cliente final)
**Quem usa**: Cliente (apenas leitura)
**O que faz**:
- Visualização dos dados
- Gráficos e tabelas
- Filtros por período
- Exportações Excel/PDF
- Lê dados de localStorage (carregados por admin)

**Fluxo Cliente**:
```
Abrir index.html
        ↓
Carrega dados de localStorage
        ↓
Visualiza mapa de exploração
        ↓
Clica em contas para detalhar
        ↓
Exporta Excel/PDF
```

---

## 🔄 Fluxo Completo de Dados

```
MÊS 1:
├─ Admin executa SETUP_GOOGLE_DRIVE.html (one-time)
├─ Admin abre admin.html
├─ Carrega ficheiro de Junho
├─ Dados sincronizados Google Drive + localStorage
└─ Cliente abre index.html e visualiza

MÊS 2:
├─ Admin abre admin.html
├─ Carrega ficheiro de Julho
├─ Dados sincronizados Google Drive + localStorage
└─ Cliente abre index.html (dados atualizados)

MÊS 3:
└─ ... repete (apenas admin.html + index.html)
```

---

## 🎯 Checklist GitHub

- [ ] **SETUP_GOOGLE_DRIVE.html** (19 KB) - Configuração inicial
- [ ] **admin.html** (15 KB) - Admin carregar dados
- [ ] **index.html** (92 KB) - Cliente visualizar
- [ ] **README.md** - Documentação
- [ ] **DEPLOY.md** - Instruções deploy
- [ ] **netlify.toml** - Config Netlify
- [ ] **.gitignore** - Ficheiros a ignorar

**Total: ~240 KB**

---

## 🚀 Deploy Netlify

Todos os 3 HTML são deployados:
```
https://seu-site.netlify.app/index.html          ← Cliente
https://seu-site.netlify.app/admin.html          ← Admin
https://seu-site.netlify.app/SETUP_GOOGLE_DRIVE.html ← Setup
```

---

## 🔐 Segurança

- **SETUP**: Autentica com Google (OAuth)
- **ADMIN**: Usa credenciais armazenadas no browser
- **CLIENTE**: Lê dados de localStorage (sem acesso a brutos)
- Dados **nunca** saem do browser (tudo client-side)

---

## 📝 URLs de Acesso

**Para o Cliente:**
```
https://seu-site.netlify.app/index.html
```

**Para o Admin (mensal):**
```
https://seu-site.netlify.app/admin.html
```

**Setup (one-time):**
```
https://seu-site.netlify.app/SETUP_GOOGLE_DRIVE.html
```

---

**Esta é a solução COMPLETA! 🎉**
