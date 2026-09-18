## Adam Shahbari

Software engineer working across backend services, mobile applications, testing
and engineering tooling.

I build REST APIs on the JVM with relational databases behind them,
cross-platform mobile clients released to the App Store and Google Play, and the
test and delivery automation that keeps both honest. I care most about
correctness at the boundaries — migrations, API contracts, and tests that run
against real dependencies rather than stand-ins.

---

### Core engineering areas

**Backend and APIs**
Java 21 and Spring Boot services backed by PostgreSQL. Versioned schema
migrations with Flyway, transactional service layers, REST APIs with consistent
error semantics and request validation.

**Mobile engineering**
Cross-platform applications in Flutter and Dart, released through the App Store
and Google Play. Native build and signing pipelines on both iOS (Xcode) and
Android, Firebase for authentication, data and messaging.

**Testing and automation**
Unit testing with JUnit 5, and integration testing with Testcontainers against
real PostgreSQL instances rather than in-memory substitutes — so that schema
constraints, SQL behaviour and migrations are part of what is under test.

**CI/CD and tooling**
Gradle builds with committed wrappers for reproducibility, Docker and Docker
Compose for local infrastructure, and automated pipelines running the same
checks locally and on CI.

**Product engineering**
Taking a problem from requirements through to a released application: domain
modelling, interface design, implementation and iteration. A background in
UX and product design informs how I scope and sequence work rather than
replacing the engineering.

---

### Selected engineering projects

**Engineering Specification Platform**

An internal engineering tool for authoring, versioning, reviewing and validating
technical specifications. Specifications are held in a structured domain model
rather than as documents, which makes their quality mechanically checkable.

- Java 21, Spring Boot, Gradle, PostgreSQL, Flyway, Docker Compose
- REST API covering projects, specifications, sections, requirements,
  references, comments and reviews
- Immutable versioning: only draft versions are editable, and a revision
  deep-copies the previous version rather than amending it in place
- A configurable validation engine that detects duplicate requirement
  identifiers, references to requirements that do not exist, malformed
  identifiers, empty sections and non-normative requirement wording
- Review workflow with decisions and comments anchored to individual
  requirements
- 49 passing automated tests: unit tests for the validation rules, and
  integration tests that start a real PostgreSQL container through
  Testcontainers and exercise the HTTP layer end to end

**specctl** — *In development*

A command-line client for the specification platform, intended to make
specification validation a build step rather than a review-time discussion.
Java 21 and Picocli.

**spec-analysis-engine** — *In development*

Graph analysis over requirement dependency structures: cycle detection,
dependency and reachability analysis, and specification metrics. Scala 3 and
sbt.

**cross-platform-test-lab** — *In development*

A black-box test suite that treats the platform as a running system, covering
the REST API and browser behaviour against a deployed environment. Python,
Pytest and Playwright.

---

### Current technology stack

Technologies I have used to build and complete working software.

| Area | Technologies |
|---|---|
| Languages | Java, Dart, SQL |
| Backend | Spring Boot, REST APIs, JPA, Flyway |
| Databases | PostgreSQL, Firebase |
| Mobile | Flutter, iOS (Xcode), Android |
| Testing | JUnit 5, Testcontainers |
| Build and infrastructure | Gradle, Docker, Docker Compose |
| Delivery | Git, CI/CD pipelines, App Store and Google Play releases |
| Design | UX and UI design, product design |

---

### Existing product work

Selected product work under BARDOS IT SOLUTIONS LTD.

**UniX** — the student-facing application of a platform connecting students with
university admissions agencies. Released on the App Store and Google Play.

- [App Store](https://apps.apple.com/gb/app/unix-university-x/id6740775299)
- [Google Play](https://play.google.com/store/apps/details?id=com.unix.com)

**UniX Partner** — the agency-facing application, used by admissions agencies to
manage student applications and their own workflows. Released on Google Play.

- [Google Play](https://play.google.com/store/apps/details?id=com.bardos.unix.partner)

**Loqma** — a multi-application food ordering and delivery platform built with
Flutter and Firebase. It comprises separate customer, restaurant partner and
rider applications alongside an internal administration console, sharing a
common set of domain, service and design-system packages. Currently in
development and not yet publicly released.

---

Source for the commercial products above is private. The engineering projects
listed here are not yet public; repositories will be published as they reach a
releasable state.
