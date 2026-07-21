# Agent Operating Model

This document defines how I decompose software delivery into bounded engineering agents.

The agents are not autonomous decision-makers. They are execution roles with clear responsibilities, inputs, outputs, and review gates.

The technical specification remains the source of truth.

---

## 1. Platform Architecture Agent

### Responsibilities

- Translate business and brand strategy into system architecture
- Define application boundaries
- Choose infrastructure and deployment patterns
- Identify technical risks
- Define integration points between workstreams

### Inputs

- Brand strategy handover
- Product objectives
- User journeys
- KPIs
- Existing codebase
- Operational constraints

### Outputs

- Architecture plan
- System boundaries
- Technical decisions
- Dependency map
- Delivery sequence
- Acceptance criteria

### Review Gate

The architecture must support the business objective without introducing unnecessary complexity.

---

## 2. Frontend Experience Agent

### Responsibilities

- Implement approved designs and user journeys
- Maintain the design system
- Build responsive and accessible interfaces
- Connect frontend states to backend services
- Preserve consistency across the product

### Inputs

- Approved design direction
- Component specification
- API contracts
- User journeys
- Acceptance criteria

### Outputs

- Reusable components
- Responsive pages
- Loading, empty, success, and error states
- Accessible interaction patterns
- Tested frontend integration

### Review Gate

The implementation must match the intended brand experience and complete the defined user journey.

---

## 3. Backend and API Agent

### Responsibilities

- Implement business logic
- Build API routes and service boundaries
- Validate requests and responses
- Handle failure states
- Protect data access

### Inputs

- Business rules
- API contracts
- Database schema
- Permission model
- Acceptance criteria

### Outputs

- Services and API routes
- Validation logic
- Error handling
- Integration tests
- API documentation

### Review Gate

Business rules must be enforced consistently and not depend solely on frontend behavior.

---

## 4. Database and Data Integrity Agent

### Responsibilities

- Design and maintain data models
- Create migrations
- Define relationships and constraints
- Enforce normalization where required
- Preserve auditability
- Prevent invalid state transitions

### Inputs

- Entity definitions
- Business rules
- Status lifecycle
- Permission requirements
- Reporting needs

### Outputs

- Schema changes
- Migrations
- Constraints
- Indexes
- Triggers
- Generated types
- Rollback notes

### Review Gate

The database must prevent invalid data rather than relying on callers to behave correctly.

---

## 5. Authentication and Authorization Agent

### Responsibilities

- Define user roles
- Implement authentication flows
- Enforce permissions
- Review row-level security
- Test privilege boundaries
- Prevent unauthorized data access

### Inputs

- Role definitions
- Permission matrix
- User journeys
- Database schema
- Sensitive operations

### Outputs

- Authentication flows
- Authorization rules
- RLS policies
- Permission tests
- Security review notes

### Review Gate

Each user must only see and perform actions explicitly allowed by the specification.

---

## 6. Analytics and Instrumentation Agent

### Responsibilities

- Define measurable product events
- Instrument acquisition and conversion journeys
- Configure analytics platforms
- Validate event payloads
- Connect technical activity to business KPIs

### Inputs

- Success metrics
- Conversion funnel
- User journeys
- Channel strategy
- Reporting requirements

### Outputs

- Event taxonomy
- Analytics implementation
- Conversion tracking
- Attribution logic
- Validation report
- Dashboard requirements

### Review Gate

Every important user action must be measurable and tied to an actual business question.

---

## 7. Technical SEO and AI-Search Agent

### Responsibilities

- Define crawlable site architecture
- Implement metadata and structured data
- Manage sitemaps and canonical rules
- Improve internal linking
- Monitor Core Web Vitals
- Prepare content for search engines and AI discovery systems

### Inputs

- Information architecture
- Content model
- Audience intent
- Target queries
- Public page structure
- Performance requirements

### Outputs

- Metadata rules
- Schema markup
- Sitemap strategy
- Canonical strategy
- Internal-link structure
- Indexation checks
- Performance recommendations

### Review Gate

Public content must be technically discoverable, context-rich, and connected to measurable search outcomes.

---

## 8. QA and Regression Agent

### Responsibilities

- Test acceptance criteria
- Validate end-to-end user journeys
- Test permissions and failure states
- Identify regressions
- Review agent-generated changes critically

### Inputs

- Technical specification
- Completed implementation
- Known risks
- Previous defects
- Release checklist

### Outputs

- Test results
- Defect report
- Regression findings
- Release recommendation
- Unresolved risk list

### Review Gate

A feature is not complete because it works once. It must also fail safely and avoid breaking existing behavior.

---

## 9. Deployment and Reliability Agent

### Responsibilities

- Validate build and release readiness
- Maintain CI/CD
- Define rollback procedures
- Review environment configuration
- Monitor deployments
- Preserve atomic and reversible releases

### Inputs

- Approved implementation
- Migration plan
- Environment requirements
- Test results
- Release checklist

### Outputs

- Deployment plan
- CI/CD updates
- Environment validation
- Rollback procedure
- Monitoring checks
- Release record

### Review Gate

No release ships without a known rollback path and verified production configuration.

---

# Multi-Agent Coordination

Workstreams may run in parallel, but dependencies must be explicit.

Typical dependency order:

```text
Strategy Handover
        ↓
Architecture
        ↓
Specification
        ↓
Database / Backend / Frontend / Analytics / SEO
        ↓
Integration
        ↓
QA and Security Review
        ↓
Deployment
        ↓
Measurement
