# Nask — AI Calendar & Task Scheduler

Nask is an intelligent personal scheduling assistant. It combines calendar management, task tracking, and AI-driven scheduling to automatically plan your days. Tell it what you need to do, and it finds the right time.

**Status:** Early development. Not production-ready.

---

## License

This software is **source-available for personal use only**. You may view, run, and modify the code for your own personal, non-commercial purposes. Commercial use, redistribution as a service, and incorporation into commercial products are **strictly prohibited** without a separate commercial license.

See [LICENSE](LICENSE) for the full terms.

**I do not accept code contributions at this time.** The repository is public for portfolio review and personal use.

---

## Architecture

Nask is a microservice backend built with FastAPI and Python. Architecture will be explained in detail as project grows.

---

## Roadmap

Roadmap is tentative — items will be added, updated, or removed as the project evolves.

- Common:
    - [ ] Move shared dependencies (Pydantic models, auth utilities, event schemas) into `common`
    - [ ] Standardize API error responses across services
    - [ ] Shared middleware for request logging and correlation IDs

- AAA:
    - [ ] Email/password registration and login
    - [ ] User preferences (timezone, working hours, default meeting duration)
    - [ ] JWT-based authentication flow
    - [ ] Implement ABAC authorization

- Calendar:
    - [ ] Event CRUD (single and recurring)
    - [ ] Free/busy availability queries
    - [ ] Timezone-aware scheduling
    - [ ] Conflict detection on overlapping events

- AI Scheduler:
    - [ ] Natural language input parsing ("schedule gym every weekday at 7am")
    - [ ] Automatic time-slot suggestion based on calendar availability
    - [ ] Task-to-calendar slot allocation
    - [ ] Smart rescheduling when conflicts arise
    - [ ] User feedback loop (accept/reject suggestions)

- Notifications:
    - [ ] Event reminders (push, email, in-app)
    - [ ] Task due date alerts
    - [ ] Schedule proposal notifications

- DevOps:
    - [ ] Docker Compose for full local development
    - [ ] CI/CD pipeline (lint, test, build images)
    - [ ] Kubernetes manifests or Helm chart
    - [ ] Observability (logs, metrics, traces)
