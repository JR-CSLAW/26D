# Team D - NewEra POS

Software Engineering course · Beihang University (BUAA) · Repository: https://github.com/bhsei/26D

## Project overview

**NewEra POS** is a point-of-sale system for a retail store. The cashier uses it to record a customer's purchase, calculate totals and taxes, take payment, update inventory and print a receipt. It also handles returns and equipment rentals.

We chose this project because it is a proven object-oriented analysis and design (OOAD) teaching case: requirements, actors and business rules are already well defined, so our effort goes into the engineering process (requirements, use cases, domain model, contracts, design diagrams, design class diagram) rather than inventing a domain.

### System scope

| Item                       | Details                                                                                    |
| -------------------------- | ------------------------------------------------------------------------------------------ |
| Use cases (4)              | Process Sale, Handle Returns, Process Rental, Start Up                                     |
| Primary actors             | Cashier (operates the POS terminal), Customer (purchases, returns or rents items and pays) |
| External systems (4)       | Payment Service (authorization), Tax Calculator, Accounting System, HR System              |
| Payment methods (3 listed) | Cash, credit card                                                                          |

## Team

| Name               | Major / background                                                     | Strengths for the project                                                                | Proposed role\* | GitHub username | Student ID |
| ------------------ | ---------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | --------------- | --------------- | ---------- |
| Alfonso Pinto      | Double degree in Computer Science and Business (Spain)                 | C++, Java, Python; software engineering knowledge; communication                         |                 |                 |            |
| Haifa Chkoundali   | Telecommunications / Computer Science, INSA Lyon (Tunisia)             | Full-stack development; coding practices; AI / LLM integration; creative problem-solving |                 |                 |            |
| Borja Nicolás      | Computer Engineering, major in Cyberspace Security                     | Java; UML modeling; teamwork; documentation and presentation                             | UML modeling | borjacyberesc | LS2639207 |
| Yasmine Chkoundali | Telecommunications & Digital Services Engineering, INSA Lyon (Tunisia) | UI/UX design; system design and information-system overview; programming                 |                 |                 |            |
| Josué Rodríguez    | Cyberspace Security (Ecuador)                                          | Secure design, privacy and compliance; requirements traceability; risk analysis          |                 |                 |            |
| Avni Oflaz         | Computer Engineering (exchange student)                                | C/C++; ROS2 and Gazebo; Python                                                           |                 |                 |            |

\* Roles are a first proposal based on each member's strengths and will be confirmed by the team.

## Repository structure

| Folder                                   | Content                                                  |
| ---------------------------------------- | -------------------------------------------------------- |
| `src/`                                   | Source code                                              |
| `tests/`                                 | Automated and manual test assets                         |
| `docs/requirements/`                     | SRS and requirement-related artifacts                    |
| `docs/design/`                           | Architecture and detailed design documents               |
| `docs/testing/`                          | Test plan, test cases and test report                    |
| `docs/release/`                          | Release notes and final pitch materials                  |
| `plans/`                                 | Project plan, iteration plans, schedules                 |
| `worklogs/team/`, `worklogs/individual/` | Team and individual work logs                            |
| `weekly-reports/Wxx/`                    | Weekly progress-report slides (`Weekly_Report_Wxx.pptx`) |
| `assets/`                                | Images, diagrams, demo media, datasets                   |

## Progress

| Week | Report                                                              | Summary                                                 |
| ---- | ------------------------------------------------------------------- | ------------------------------------------------------- |
| W01  | [Weekly_Report_W01.pptx](weekly-reports/W01/Weekly_Report_W01.pptx) | Found the idea, researched feasibility, discussed roles |

## Working rules

The full rules (Git workflow, file naming, branches and reviews with GitHub Issues) are in [CONTRIBUTING.md](CONTRIBUTING.md). In short:

- Run `git pull --rebase` before editing.
- One document (or one coherent change) per commit.
- Commit message format: `W<week> - <change summary>; <change description>`
  Example: `W2 - Initial project plan; completed work breakdown and milestone schedule`
- Never commit passwords, tokens, API keys or other secrets.
