# 🚀 Learn360 Deployment Pipeline Plan
**Author:** Khutjo Satekge  
**Project:** Learn360 Architecture Blueprint

---

## ⚙️ 1. Overview
This document describes the CI/CD pipeline used to build, test, and deploy Learn360 components (frontend + backend) to Azure.  
Goal: secure, repeatable, and simple automation so we can iterate fast while keeping environments consistent.

---

## 🧩 2. CI/CD Tool – GitHub Actions
We use **GitHub Actions** (YAML workflows stored in `.github/workflows/`) to orchestrate build and deploy stages.  
Triggers:
- `push` to `main`
- Pull request merges to `main`

### Workflow stages (summary)
1. **Checkout** repository
2. **Build** — frontend (Node) and backend (Java / functions)
3. **Test** — run unit tests where available
4. **Package** — produce artifacts for deployment
5. **Deploy** — deploy to Azure App Service using publish profile
6. **Notify** — optional notifications to Teams / email

---

## 🧱 3. Deployment approach — Infrastructure as Code (IaC)
- Use **Azure Bicep** for provisioning core infrastructure (`/infra/*.bicep`).  
- Bicep templates manage: App Service, Function Apps, Storage Accounts, SQL Database, Key Vault, Cognitive Service resources, Log Analytics.  
- IaC is applied separately (via a separate GH Action or manual gated deploy) to keep infrastructure changes auditable.

> Best practice: keep infra changes in `/infra` and templates parameterized for `dev`, `test`, `prod`.

---

## 🔐 4. Configuration & Secrets
- **Secrets in GitHub**: store credentials and publish profiles in `Settings → Secrets`:
  - `AZURE_PUBLISH_PROFILE` — publish profile XML for App Service (secure)
  - `AZURE_CREDENTIALS` — service principal JSON (if needed for Bicep/ARM deployments)
  - `DB_CONN_STRING` — connection string (or reference Key Vault via Managed Identity)
- **Runtime config**: App settings are set in Azure App Service (Configuration → Application settings) and map to environment variables.
- **Secrets at runtime**: store production secrets in **Azure Key Vault** and let App Service use a **Managed Identity** to fetch secrets.

---

## 🔁 5. Pipeline security & governance
- Principle of least privilege for service principals and publish profiles.  
- Audit deployment operations via Azure Monitor and Log Analytics.  
- Use Azure Policy to enforce required tags, SKUs, and security posture.  
- Integrate deployments with pull request reviews (protect `main` branch).

---

## 📁 6. Placement & file names
- GitHub Action workflow file: `.github/workflows/deploy.yml`
- IaC templates: `infra/*.bicep`
- Frontend app folder: `frontend/` (or root if single app)
- Backend functions: `api/` (or `functions/`)

---

## 🔧 7. How to trigger & test locally
- Push to `main` to trigger full pipeline.
- For testing, create a feature branch and open PR—CI runs but Deploy job can be gated to `main` only.

---

## ✅ 8. Summary
This pipeline keeps Learn360 aligned with the project goals: simple, secure automation to deploy the web app and services to Azure. Later phases will add IaC deployment steps (Bicep) and more advanced testing / blue/green or slot-based deployments.
