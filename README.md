# CyberPredict-AI
Predictive Cyber Threat Intelligence SaaS

# CyberPredict AI — MVP Implementation

I'll structure CyberPredict AI as a deployable SaaS application with a Next.js dashboard, FastAPI backend, PostgreSQL, real vulnerability intelligence, organization-level access controls, and Stripe subscriptions.

The implementation will follow three important rules:

1. No fabricated threat data. The platform will retrieve real CISA KEV and FIRST EPSS data. Empty or unavailable feeds will be reported as such.
2. No invented attack predictions. Risk scores will be explainable prioritization indicators, not claims that an organization will be attacked on a particular date.
3. No fake payment activation. Paid access will depend on verified Stripe webhook events or an explicitly authorized administrative process.

The source package will include Docker deployment configuration, automated tests, environment templates, and setup instructions. Live hosting and payment activation will still require your own infrastructure, domain, and Stripe credentials.

Source code package
CyberPredict AI MVP

ZIP archive • Python FastAPI • Next.js • PostgreSQL • Docker • Stripe


Download CyberPredict AI source code

Python syntax validation passed

3 automated unit tests passed

Production deployment not yet performed


What is implemented
Component	Status
FastAPI REST backend	Implemented
PostgreSQL data models	Implemented
CISA KEV real feed ingestion	Implemented
FIRST EPSS real feed integration	Implemented
Explainable risk triage	Implemented
Basic Next.js customer console	Implemented
Stripe Checkout and webhooks	Needs hardening
Customer self-registration and login	Not implemented
Automated domain ownership verification	Not implemented
Confirmed version-level vulnerability matching	Not implemented
Production deployment and live testing	Not completed
The real feed connectors are implemented, but I have not executed them against their live endpoints or verified a live Stripe transaction.
How to run
Extract the archive, open PowerShell in the project directory, and run:
Copy-Item .env.example .env
notepad .env
docker compose up --build -d


Configure the required secrets in .env first.

Then access:
- Dashboard: http://localhost:3000
- API documentation: http://localhost:8000/docs
- Health endpoint: http://localhost:8000/health
The README explains authentication, feed ingestion, Stripe configuration, testing, and deployment.
Recommended next milestone
Before accepting real customer payments, the most important work is completing production authentication, automated domain verification, Stripe subscription reconciliation, and tenant-isolation testing.

After that, we can add a richer security dashboard with actual historical risk charts, scheduled ingestion, PDF assessments, email alerts, and a public customer onboarding workflow.

The downloadable package is a working development foundation, not yet a production-certified or publicly deployed commercial SaaS.
