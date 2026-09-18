## Adam Shahbari

Software engineer. I build backend services, mobile applications and the
tooling around them — with a strong bias towards systems that are tested,
reproducible and understandable by the next person who opens the repository.

My work spans the full path from data model to shipped product: relational
schemas and REST APIs on the JVM, cross-platform mobile clients, and the test
and delivery automation that keeps both honest. I care about correctness at the
boundaries — migrations, API contracts, and tests that run against real
dependencies rather than stand-ins.

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

| Area | Technologies |
|---|---|
| Languages | Java, Dart, Scala, Python, SQL |
| Backend | Spring Boot, REST APIs, JPA, Flyway |
| Databases | PostgreSQL, Firebase |
| Mobile | Flutter, iOS (Xcode), Android |
| Testing | JUnit 5, Testcontainers, Pytest |
| Build and infrastructure | Gradle, sbt, Docker, Docker Compose |
| Delivery | Git, CI/CD pipelines, App Store and Google Play releases |
| Design | UX and UI design, product design |

---

### Existing product work

Applications built and released under BARDOS IT SOLUTIONS LTD.

**UniX** — a platform connecting students with university admissions agencies.
Released on the App Store and Google Play, with the agency-facing interface
built into the same application on iOS.

- [App Store](https://apps.apple.com/gb/app/unix-university-x/id6740775299)
- [Google Play](https://play.google.com/store/apps/details?id=com.unix.com)

**UniX Partner** — a dedicated agency application for managing student
applications and agency workflows, released on Google Play.

- [Google Play](https://play.google.com/store/apps/details?id=com.bardos.unix.partner)

**Loqma** — a food ordering platform consisting of a customer application and a
separate restaurant partner application, built on Flutter and Firebase. Both
applications are built; the platform has not yet been released.

---

Source for the commercial products above is private. The engineering projects
listed here are being prepared for publication.
