# NASF Tec - Landing Page Final (Sem Leads) | Mooca-SP

Landing page estática, 1 arquivo, sem backend, sem painel admin.
Versão corrigida para deploy no Render - render.yaml validado.

## 📸 Preview
Card central com imagem estilizada do técnico arrumando computador, logo NASF Tec em pill por cima, glow azul/verde, sem formulário.

## 📁 Estrutura Final
```
nasf-tec/
├── index.html (ARQUIVO ÚNICO - 734KB com imagem base64 embutida)
├── public/
│   └── index.html (cópia para compatibilidade)
├── render.yaml (configuração CORRETA para Render Static)
├── .gitignore
└── README.md (este arquivo)
```

## 🛠️ O que foi corrigido (falha anterior no Render)
- **render.yaml** anterior tinha campo `routes` inválido para `env: static` -> causava erro de YAML "falha em linguagem natural"
- Novo `render.yaml` minimalista e validado conforme spec oficial Render
- `staticPublishPath: ./` aponta para raiz onde está index.html
- `buildCommand: ""` vazio - não precisa build
- HTML com imagem em base64 - zero dependências externas além de Tailwind CDN e Google Fonts

## 💻 VS Code - Como abrir
1. Baixe o ZIP `NASF-TEC-CORRIGIDO-VSCODE-RENDER.zip`
2. Extraia
3. VS Code > File > Open Folder > selecione pasta `nasf-tec-REVISADO-FINAL`
4. Clique direito em `index.html` > Open with Live Server (extensão Ritwick Dey)
5. Ou duplo clique no index.html para abrir no navegador

## 🌐 Deploy no Render - Passo a Passo

### Opção A - Mais Fácil (Static Site manual - RECOMENDADO)
1. Crie repositório no GitHub:
```bash
git init
git add .
git commit -m "NASF Tec final corrigido"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/nasf-tec.git
git push -u origin main
```
2. Acesse https://dashboard.render.com
3. Clique em **New + > Static Site**
4. Conecte seu GitHub e selecione o repositório `nasf-tec`
5. Preencha:
   - **Name**: nasf-tec
   - **Build Command**: (deixe em branco)
   - **Publish Directory**: `.` (ponto)
6. Clique em **Create Static Site**
7. Deploy em 30-60 segundos - URL: https://nasf-tec.onrender.com

### Opção B - Via Blueprint (usa render.yaml)
1. Mesmo push para GitHub
2. Render > New + > Blueprint
3. Selecione o repositório
4. Render lê automaticamente o `render.yaml` corrigido
5. Aplica e faz deploy

### Domínio Próprio
Render Dashboard > seu site > Settings > Custom Domains > Add Custom Domain

## 📞 Contato
- WhatsApp: (11) 98595-6363 - https://wa.me/5511985956363
- Mooca - SP - Presencial + Remoto Brasil todo
- Serviços: Manutenção Notebook/Desktop, Assessoria MEI, Representação Comercial Remota

## ✅ Checklist Final
- [x] Sem captura de leads (removido conforme solicitado)
- [x] Card central com imagem estilizada + logo por cima
- [x] Imagem embutida base64 - 1 arquivo só
- [x] render.yaml corrigido e validado
- [x] Pronto para VS Code e Render

© 2026 NASF Tec - Nilson Amado
