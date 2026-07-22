# Zyprova — Software Engineering Intern (June 2025 -- Sept 2025)

Role: Software Engineering Intern (resume title).
Team: 5-person team, extensive codebase, multiple repos.
My scope: HR, Finance, and CAP table microservices, commonlib, and API gateway.
Worked across multiple microservices and across repos on code/features.

## Product

Zyprova built a service giving companies agentic management of company data.
- Agents have access to company data and internal databases — store and act on data.
- Managed permissions, capabilities, and enforced least-privilege access.
- Microagents fetch, edit, and manage company data across HR, Finance, and
  CAP table microservices.
- Data involved: incorrect edits could have severe consequences (HR/Finance/CAP
  table records) — so robust human-in-the-loop was implemented for those actions.

## Architecture

- Engineered a subagent network with an orchestrator agent managing the microagents.
- MCP-compliant, used Agent2Agent for cross-microagent/service communication.
- I contributed heavily to design decisions and architecture discussions.

## Query optimization (the 50% number)

- Refactored query logic to narrow scope: fewer rows iterated per query.
- Replaced O(n) iteration with hash-based DB fetches where possible.
- Result: cut information/data retrieval time 50%.

## Agent pass-rate improvement (the 15% number)

- Zyprova had a pre-determined, extensive internal test suite spanning multiple
  microservices and queries.
- Added new GraphQL resolvers/tools/integrations.
- Result: agentic task pass rate on that test suite improved 15%.

## Other contributions

- Agile sprints, code reviews (no metric attached — cut from resume, too vague
  without one).

## Resolved

- GPA change (unrelated to Zyprova, same session): 3.96 -> 3.92, grad year
  2027 -> 2028 (both Summary and Education sections).
