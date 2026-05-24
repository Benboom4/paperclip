## Template Titles

**Railway Title:** `Paperclip [Updated May '26]`
**Railway Description:** `Paperclip [May '26] (Orchestrate AI Agent Teams & Run Autonomous Companies) Self Host`
**Spreadsheet Title:** `Paperclip (Open-Source AI Agent Orchestration & Autonomous Company Platform)`
**GitHub Description:** `Paperclip — AI agent orchestration platform for autonomous companies. Deploy on Railway with one click.`

---

![Paperclip AI agent orchestration platform banner](https://res.cloudinary.com/dojdzamvk/image/upload/v1/paperclip-banner.png "Hosting Paperclip on Railway")

# Deploy and Host self hosted Paperclip (AI Agent Orchestration) on Railway

Paperclip is an open-source orchestration platform for managing AI agent teams to run autonomous companies. With 67,000+ GitHub stars, it provides a single dashboard to hire AI agents, delegate tasks, approve risky decisions, and track work. It unifies multiple AI coding assistants under one control plane with org charts, budgets, governance, and audit trails.

## About Hosting Paperclip open-source software on Railway (self hosted Paperclip template)

Self-hosting Paperclip on Railway gives you full control over your AI agent infrastructure and data. Every decision, task assignment, and agent interaction stays within your own environment with no third-party access to your workflows. Railway handles PostgreSQL, persistent volumes, and SSL certificates while you focus on managing your AI-powered organization.

## Why Deploy Paperclip, the AI Agent Management alternative on Railway (Railway Free Trial)

Running Paperclip on Railway costs a fraction of managed AI orchestration platforms. With Railway's $5 free trial, you can deploy a fully functional Paperclip instance with PostgreSQL and persistent storage without upfront commitment. Railway's usage-based pricing means you only pay for resources your agents consume.

### Railway vs Other Hosting Providers and VPS for Paperclip self hosting

| Provider          | What You Get with Railway           | What You Get with the Other Provider     |
| ----------------- | ----------------------------------- | ---------------------------------------- |
| **DigitalOcean**  | One-click deploy with managed PostgreSQL and automatic SSL | Manual droplet setup, separate database provisioning, Nginx config |
| **AWS**           | Simple env vars and service linking, pay-per-use pricing | Complex IAM roles, VPC networking, ECS task definitions |
| **Hetzner**       | Auto builds from GitHub, instant rollbacks, health checks | Cheap compute but full DevOps setup with Docker Compose |

## Common Use Cases for hosted Paperclip

- **AI development teams** managing multiple coding agents like Claude Code, Codex, and Cursor with centralized governance and budget controls
- **Startup founders** building AI-first companies where autonomous agents handle engineering and operations with human approval for critical decisions
- **Enterprise innovation labs** experimenting with agentic workflows while maintaining audit trails and compliance for AI decision-making
- **Open-source maintainers** using AI agents to triage issues, review pull requests, and manage releases across repositories
- **Consulting firms** running client-specific AI agent teams with isolated workspaces and per-project budgets

![Paperclip dashboard showing AI agent management](https://res.cloudinary.com/dojdzamvk/image/upload/v1/paperclip-dashboard.png "Paperclip AI Agent Dashboard on Railway")

## Dependencies for Paperclip Docker hosted on Railway

Paperclip runs as a self-contained Node.js application with a React frontend served from the same process. It requires a PostgreSQL database for storing agent state, user sessions, company data, and audit logs. A persistent volume stores configuration files, database backups, and encryption keys.

### Deployment Dependencies for Managed Paperclip Service (AI Agent Orchestration)

This template deploys the Paperclip application built from source using a multi-stage Docker build, and a Railway-managed PostgreSQL database. A persistent volume at /paperclip stores configuration, logs, and automated backups.

### Implementation Details for Paperclip (Using Paperclip official Docker build)

The template builds the Paperclip monorepo from source including the TypeScript server, React UI, and plugin SDK. It runs on port 3100 with authenticated deployment mode. The start script creates a config.json, launches the server, and runs the CEO bootstrap to generate an admin invite URL in Railway logs.

## How does Paperclip compare against other AI agent orchestration platforms

### Paperclip vs CrewAI (CrewAI Alternative)
* **Agent Management:** Paperclip provides a visual dashboard with org charts while CrewAI is a Python framework requiring code-level configuration
* **Multi-Agent Support:** Paperclip integrates Claude Code, Codex, Cursor natively whereas CrewAI focuses on LLM agents within its own framework

### Paperclip vs AutoGen (AutoGen Alternative)
* **Deployment:** Paperclip ships as a ready-to-deploy web app with persistent state while AutoGen is a research library needing custom scaffolding
* **Audit Trail:** Paperclip logs every agent action and cost with full traceability whereas AutoGen lacks enterprise audit features

### Paperclip vs LangGraph (LangGraph Alternative)
* **User Interface:** Paperclip offers a complete management UI for non-technical users while LangGraph is a developer-focused graph framework
* **Team Operations:** Paperclip handles multi-user access and task delegation out of the box whereas LangGraph requires LangSmith and custom code

## How to use Paperclip (the OSS AI Agent Orchestration)?

After deploying on Railway, check the service logs for your CEO bootstrap invite URL, open it to create your admin account, then start adding AI agent adapters and creating your first autonomous company from the dashboard.

## How to self host Paperclip on other VPS Services (Paperclip self hosting guide)

### Clone the Repository
Clone the Paperclip repository from GitHub with `git clone https://github.com/paperclipai/paperclip.git` and navigate into the project directory.

### Install Dependencies
Ensure Node.js 20+ and pnpm 9.15+ are installed. Run `pnpm install` to install all workspace dependencies across the monorepo.

### Configure Environment Variables
Create a `.env` file with DATABASE_URL pointing to your PostgreSQL instance, BETTER_AUTH_SECRET as a random 64-character string, and PAPERCLIP_PUBLIC_URL set to your server domain.

### Start the Paperclip Application
Run `pnpm paperclipai onboard --yes` to initialize the instance, then start the server with `node server/dist/index.js`. Run `pnpm paperclipai auth bootstrap-ceo` to generate your first admin invite URL.

## Official Pricing of Paperclip (Paperclip pricing)

Paperclip is fully open-source under the MIT license and free to self-host with no restrictions. There is no cloud offering or paid tier. All features including multi-agent orchestration, budget controls, plugin system, and audit logging are available at no cost. You only pay for hosting infrastructure and API keys for the AI providers your agents use.

## Paperclip cloud vs self hosted comparison (Pricing, features, costs, and more)

Paperclip is exclusively self-hosted with no managed cloud version. Self-hosting gives you complete control over data, agent configurations, and API keys while costs stay limited to infrastructure and AI provider usage.

### Monthly cost of self hosting Paperclip on Railway

Running Paperclip on Railway typically costs $5 to $15 per month depending on usage. The Node.js application uses 512MB to 1GB RAM during active agent operations. Railway's usage-based pricing means idle periods cost very little, making it economical for on-demand agent usage.

### System Requirements for Hosting Paperclip on a VPS

Paperclip requires minimum 2 CPU cores, 2GB RAM, and 10GB storage. Docker is needed for containerized deployment. Node.js 20+ and pnpm 9.15+ are required for source builds. PostgreSQL 14+ is mandatory.

## Frequently Asked Questions (FAQs)

### What is Paperclip self hosted?
Paperclip self hosted is an open-source AI agent orchestration platform you deploy on your own infrastructure. It provides a web dashboard for managing teams of AI coding agents, delegating tasks, setting budgets, and maintaining full control over your data without relying on third-party services.

### How much does Paperclip self hosting cost on Railway?
Self-hosting Paperclip on Railway costs approximately $5 to $15 per month based on resource usage. Railway offers a $5 free trial credit to get started. The main cost drivers are CPU and memory during active agent sessions, plus PostgreSQL storage.

### Is Paperclip free to use?
Yes, Paperclip is completely free and open-source under the MIT license. There are no paid tiers, usage limits, or feature restrictions. The only costs are hosting infrastructure and API keys for AI providers like Anthropic or OpenAI that power your agents.

### What AI agents does Paperclip support?
Paperclip supports Claude Code, OpenAI Codex, Cursor, Gemini, Grok, OpenCode, and Pi through its adapter system. Each agent can be configured with specific roles, budgets, and permissions. The plugin SDK allows extending support to additional frameworks.

### Where can I download Paperclip?
Paperclip is available on GitHub at github.com/paperclipai/paperclip with over 67,000 stars. You can clone the repository, use the Dockerfile for containerized deployment, or deploy on Railway using the one-click template.

### What are some alternatives to Paperclip?
Popular alternatives include CrewAI for Python-based multi-agent workflows, AutoGen from Microsoft for agent collaboration, LangGraph for custom agent graphs, and MetaGPT for development agent teams. Paperclip differentiates with its production-ready web UI, multi-agent adapter support, and enterprise governance.
