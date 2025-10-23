🧠  Learn360 

Learn360 is Sedge Enterprise’s intelligent learning and upskilling platform — a cloud-powered system that merges AI-driven skill mapping, data analytics, and personalized learning experiences for individuals and organizations.

🧭 Project Overview

Learn360 delivers interactive, data-driven learning intelligence using Azure-native architecture.
- It helps learners, educators, and organizations visualize growth, measure skills, and automate development plans through AI, Power BI, and serverless automation.

Key Features:
🎓 Personalized learning journeys
📊 Analytics dashboards powered by Power BI
⚙️ Automated assessments & progress tracking
🔗 Integration with Microsoft Learn

🧱 Azure Architecture Blueprint
| Layer                   | Services                                    | Purpose                                         |
| ----------------------- | ------------------------------------------- | ----------------------------------------------- |
| **Frontend**            | Azure Static Web Apps, Azure CDN            | Deliver the Learn360 portal and UI              |
| **Backend**             | Azure Functions, Logic Apps                 | Manage events, triggers, and integrations       |
| **Database**            | Azure SQL, Blob Storage                     | Store learner data and training content         |
| **AI & Analytics**      | Azure Cognitive Services, Power BI Embedded | Generate insights and personalized dashboards   |
| **Identity & Security** | Azure AD, Key Vault                         | Manage secure access and authentication         |
| **Monitoring**          | Azure Monitor, App Insights                 | Track system performance and learning analytics |

🔐 Identity & Access Management

- Azure Active Directory (AAD) SSO integration
- Role-Based Access Control (RBAC) for admin, learner, and instructor roles
- Multi-Factor Authentication (MFA) enforcement
- Secrets stored in Azure Key Vault
- Conditional access policies for compliance

💰 Cost Strategy

Service Justification Table aligned to Learn360’s architecture:

| Azure Service      | Tier        | Function                             | Notes                            |
| ------------------ | ----------- | ------------------------------------ | -------------------------------- |
| Azure App Service  | Basic (B1)  | Hosts Learn360 web app               | Scalable to S1 for production    |
| Azure SQL Database | Basic       | Stores learner profiles and progress | Linked to Power BI for analytics |
| Azure Functions    | Consumption | Runs AI automation tasks             | Event-driven execution           |
| Power BI Embedded  | A1          | Displays dashboards                  | For advanced analytics           |
| Azure AD           | Premium P1  | Identity and access control          | Role-based learning access       |
| Azure Storage      | Hot Blob    | Stores course files and media        | Integrated with CDN              |

🧩 Core Modules

- AI-Powered Learning Paths – Adaptive course recommendations
- Course Management Dashboard – Admins can create, assign, and track
- Analytics & Power BI Embed – Data-driven insights
- Assessment Engine – Skill validation and testing
- Onboarding & Certification – Seamless learner integration

🗺 Roadmap
| Phase       | Goal                                              | Deliverable                                                         |
| ----------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| **Phase 1** | Develop full Azure Architecture Blueprint         | Layered Azure diagram (A2 Poster + Interactive Site)                |
| **Phase 2** | Build Service Justification Table & Cost Strategy | Resource mapping + pricing documentation                            |
| **Phase 3** | Implement Backend & Security                      | Azure Functions, Logic Apps, Key Vault, RBAC                        |
| **Phase 4** | Build Frontend                                    | Responsive web UI with icons, hover tooltips, and download features |
| **Phase 5** | Power BI Dashboard Integration                    | AI analytics, reporting, and user insights dashboard                |

🚀 Deployment Instructions
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

🧭 AI Roadmap Visual

🧩 AI Roadmap – Learn360 Growth Journey

Each phase color aligns with your Azure architecture layers:

🟦 Layer 1: Identity & Access
🟩 Layer 2: Frontend & API
🟨 Layer 3: Apps Logic & AI
🟧 Layer 4: Data & Storage
🟥 Layer 5: Security, Monitoring, Governance

Visualize progress flow — from architecture → justification → backend → frontend → insights.

✨ Vision

Learn360 empowers continuous skill growth for individuals and teams through structured, cloud-based learning intelligence.

Inspired by the success of platforms like roadmap.sh and Microsoft Learn, Learn360 blends data, AI, and education to create guided learning journeys that adapt to each learner’s goals.

Our mission:
🔹 Help individuals map their skills
🔹 Help organizations measure capability growth
🔹 Help everyone grow smarter — one insight at a time

00📄 License

This project is licensed under the MIT License.
See the LICENSE file for details.
 
