## 🧠  Learn360 

Learn360 is Sedge Enterprise’s intelligent learning and upskilling platform — a cloud-powered system that merges AI-driven skill mapping, data analytics, and personalized learning experiences for individuals and organizations.

## ✨ Vision: Skills Before Certificates

Learn360 is a South African-built digital learning platform designed to solve South African challenges.
It empowers individuals, schools, and businesses to grow through practical, cloud-based, and project-driven learning.

Inspired by the success of roadmap.sh and Microsoft Learn, Learn360 brings that same intelligent, guided learning experience — but reimagined for South Africa’s work environment.

## 🎯 Our Mission

🔹 Equip South Africans with real, employable skills, not just qualifications. 

🔹 Help organizations identify, grow, and retain capable local talent.

🔹 Build a sustainable skills pipeline that fuels job creation and innovation.

## 🇿🇦 Built for South Africa — Empowering South Africans

🟢 Built in South Africa, inspired by South African challenges.

🟢 Managed by South Africans, empowering local educators, developers, and SMEs.

🟢 Focused on South African jobs, industries, and career readiness.

Learn360 combines AI, Azure Cloud, and data-driven learning intelligence to close the gap between what people learn and what the job market needs.
It’s not just a platform — it’s a movement to get more South Africans hired, skilled, and building the future.

## 🧭 Project Overview

Learn360 delivers interactive, data-driven learning intelligence using Azure-native architecture.
- It helps learners, educators, and organizations visualize growth, measure skills, and automate development plans through AI, Power BI, and serverless automation.

# Key Features:
🎓 Personalized learning journeys 

📊 Analytics dashboards powered by Power BI

⚙️ Automated assessments & progress tracking

🔗 Integration with Microsoft Learn

# 🧱 Azure Architecture Blueprint
| Layer                   | Services                                    | Purpose                                         |
| ----------------------- | ------------------------------------------- | ----------------------------------------------- |
| **Frontend**            | Azure Static Web Apps, Azure CDN            | Deliver the Learn360 portal and UI              |
| **Backend**             | Azure Functions, Logic Apps                 | Manage events, triggers, and integrations       |
| **Database**            | Azure SQL, Blob Storage                     | Store learner data and training content         |
| **AI & Analytics**      | Azure Cognitive Services, Power BI Embedded | Generate insights and personalized dashboards   |
| **Identity & Security** | Microsoft Entra ID, Key Vault               | Manage secure access and authentication         |
| **Monitoring**          | Azure Monitor, App Insights                 | Track system performance and learning analytics |

# 🔐 Identity & Access Management

- Microsoft Entra ID SSO integration
- Role-Based Access Control (RBAC) for admin, learner, and instructor roles
- Multi-Factor Authentication (MFA) enforcement
- Secrets stored in Azure Key Vault
- Conditional access policies for compliance

# 💰 Cost Strategy

Service Justification Table aligned to Learn360’s architecture: 
| **Azure Service**             | **Tier/SKU**     | **Function**                                                         | **Notes** |
|-------------------------------|------------------|----------------------------------------------------------------------|-----------------------------|
| Azure App Service (Web App)   | Basic            | Hosts the Learn360 front-end (React/Next.js) and backend API (Java). | For testing and learning |
| Azure SQL Database            | Basic            | Stores user profiles, content metadata, and learning progress. | Linked to Power BI for analytics dashboards |
| Azure Storage Accounts (Blob) | Hot Tier         | Stores PDFs, slides, and uploaded course files. | Cost depends on content storage size |
| Azure AI Services (Cognitive) | Standard (PAYG)  | Provides vision, speech, and language AI for tagging and summarization. | Pay-as-you-go model |
| Azure OpenAI Service          | GPT-4 (PAYG)     | Powers adaptive chat, summaries, and intelligent tutoring. | Pay-as-you-go model |
| Azure Functions               | Consumption Plan | Runs background triggers (e.g., completion notifications). | | Scales automatically |
| Azure Machine Learning        | Basic Workspace  | Personalizes recommendations and adaptive learning logic. | Core AI workspace |
| Azure Monitor                 | Standard         | Tracks app performance and logs. | Includes Log Analytics workspace |
| Azure Defender for Cloud      | Free (Basic)     | Provides basic threat protection. | Upgradeable to Standard tier |
| Azure Policy                  | Basic            | Manages governance and compliance. | Integrated with Azure Monitor |

# 🧩 Core Modules

- AI-Powered Learning Paths – Adaptive course recommendations
- Course Management Dashboard – Admins can create, assign, and track
- Analytics & Power BI Embed – Data-driven insights
- Assessment Engine – Skill validation and testing
- Onboarding & Certification – Seamless learner integration

# 🗺 Roadmap
| Phase       | Goal                                              | Deliverable                                                         |
| ----------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| **Phase 1** | Develop full Azure Architecture Blueprint         | Layered Azure diagram (A2 Poster + Interactive Site)                |
| **Phase 2** | Build Service Justification Table & Cost Strategy | Resource mapping + pricing documentation                            |
| **Phase 3** | Implement Backend & Security                      | Azure Functions, Logic Apps, Key Vault, RBAC                        |
| **Phase 4** | Build Frontend                                    | Responsive web UI with icons, hover tooltips, and download features |
| **Phase 5** | Power BI Dashboard Integration                    | AI analytics, reporting, and user insights dashboard                |

# 🚀 Deployment Instructions
 Clone the repo
git clone https://github.com/Sedge-Enterprise/learn360.git

 Open project folder
cd learn360

 Install dependencies
npm install

 Run local dev server
npm run dev

Azure Deployment:

- Deploy frontend to Azure Static Web Apps
- Backend via Azure Functions
- Database with Azure SQL
- Dashboards integrated using Power BI Embedded

# 🧭 AI Roadmap Visual

# 🧩 AI Roadmap – Learn360 Growth Journey

Each phase color aligns with your Azure architecture layers:

🟦 Layer 1: Identity & Access

🟩 Layer 2: Frontend & API

🟨 Layer 3: Apps Logic & AI

🟧 Layer 4: Data & Storage

🟥 Layer 5: Security, Monitoring, Governance

Visualize progress flow — from architecture → justification → backend → frontend → insights.


 📄 License

This project is licensed under the MIT License.
See the LICENSE file for details.
 
