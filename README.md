# 🦆 QuackImobi
 
> Infraestrutura de IA para imobiliárias modernas — CRM, portfólio, contratos e automações em uma única plataforma.
 
---
 
## Sobre o projeto
 
A **QuackImobi** é uma plataforma SaaS voltada para imobiliárias que querem operar no piloto automático. Ela combina portfólio de imóveis, CRM com inteligência artificial, contratos digitais e um dashboard analítico em tempo real, tudo servido por uma API REST leve construída em Python.
 
**Versão atual:** `v0.4.2`
 
---
 
## Funcionalidades
 
| Módulo | Descrição |
|---|---|
| 🏠 **Portfólio inteligente** | Gerenciamento de imóveis com status em tempo real, fotos, documentos e histórico de visitas |
| ⚡ **CRM com IA** | Captura de leads via WhatsApp, Instagram e portais. Qualificação e resposta automática em menos de 11s |
| 📄 **Contratos automatizados** | Geração, envio e assinatura digital com conformidade LGPD |
| 📊 **Dashboard em tempo real** | Métricas de leads, pipeline de vendas, conversões e performance da equipe |
| 🔗 **API aberta** | Integração REST com ERPs, portais de imóveis e plataformas de marketing |
| 🛡️ **Segurança e LGPD** | Criptografia, controle de acesso e conformidade com a legislação brasileira |
 
---
 
## Stack tecnológico
 
- **Backend:** Python 3.10+, FastAPI, Uvicorn
- **Banco de dados:** SQLite (padrão) → migração simples para PostgreSQL em produção
- **Validação:** Pydantic (com suporte a e-mail)
- **Fontes:** Syne, DM Sans, DM Mono (Google Fonts)
- **Conformidade:** LGPD
---
 
## Instalação e execução
 
### Pré-requisitos
 
- Python 3.10 ou superior
- pip
### Passos
 
```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/quackimobi.git
cd quackimobi
 
# 2. (Opcional) Crie e ative um ambiente virtual
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
.venv\Scripts\activate     # Windows
 
# 3. Instale as dependências
pip install fastapi uvicorn pydantic[email]
 
# 4. Inicie o servidor
uvicorn main:app --reload
```
 
O servidor estará disponível em `http://localhost:8000`.
 
Ao iniciar, o sistema automaticamente:
- Cria o banco `quackimobi.db`
- Inicializa as tabelas `leads`, `demos` e `contacts`
- Libera o CORS para o front-end
---
 
## Endpoints da API
 
A documentação interativa completa fica disponível em `http://localhost:8000/docs` (Swagger UI).
 
### Públicos
 
| Método | Rota | Descrição |
|---|---|---|
| `POST` | `/leads` | Cadastro de leads |
| `POST` | `/demos` | Agendamento de demo |
| `POST` | `/contact` | Formulário de contato |
| `GET` | `/health` | Health check da API |
 
### Admin
 
| Método | Rota | Descrição |
|---|---|---|
| `GET` | `/admin/leads` | Lista todos os leads |
| `GET` | `/admin/demos` | Lista todos os agendamentos |
| `GET` | `/admin/contacts` | Lista todas as mensagens |
| `GET` | `/admin/stats` | Resumo geral da plataforma |
 
---
 
## Números da plataforma
 
- **47+** leads capturados por imobiliária / mês (em média)
- **11s** de tempo médio de resposta ao lead (−38% vs concorrência)
- **+24%** de aumento de conversão em 30 dias
- **1h** para colocar a plataforma no ar, zero DevOps
---
 
## Estrutura de arquivos esperada
 
```
quackimobi/
├── main.py           # Aplicação FastAPI principal
├── quackimobi.db     # Banco SQLite (gerado automaticamente)
├── index.html        # Landing page de apresentação
└── README.md
```
 
---
 
## Autores
 
**Sérgio Leonardo** — Cofundador / Fullstacker
- ✉ sleonardofla2009@gmail.com
- 📱 (21) 96518-9206
- 🔗 [github.com/SixtheRunner09](https://github.com/SixtheRunner09)
**Matheus Makxuel** — Cofundador / Fullstacker
- ✉ matheusmakxuel@gmail.com
- 📱 (21) 97053-4927
- 🔗 [github.com/Makxueldev23](https://github.com/Makxueldev23)
---
 
## Licença
 
© 2026 QuackImobi · Todos os direitos reservados.
