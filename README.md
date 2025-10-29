# 🚀 Elixir Devcontainer Starter

A simple, ready-to-use **VS Code Dev Container** configuration for **Elixir development**.  
Get a consistent, pre-configured environment with zero local setup — just open in container and start coding!

---

## ✨ Features

✅ **Elixir & Erlang**  
• Elixir **1.19.1** + Erlang **28.1** (built from `erlang:28.1-alpine`)

✅ **PostgreSQL Database**  
• `postgres:18-alpine` service included.

✅ **Expert LSP Support**  
• Uses the nightly **Expert** LSP via Lexical Extension (`lexical-lsp.lexical`)

✅ **VS Code Extensions Pre-Installed**
- Lexical LSP (`lexical-lsp.lexical`)
- Credo Linting (`pantajoe.vscode-elixir-credo`)
- Phoenix Tools (`phoenixframework.phoenix`)

✅ **Phoenix Ready**
- `phx_new` archive automatically installed 🏗️

✅ **Hex & Rebar Auto-Install**
- Installed during container startup

---

## 🧑‍💻 Getting Started

### 1️⃣ Clone your project

```bash
git clone <your-project-repo>
cd <your-project-folder>
