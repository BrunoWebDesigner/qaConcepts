# Review Activities in Software Testing

<br>
<img src="./img/review.png" width="600">
<br>

Review activities are part of **static testing**, where defects are found without executing code. Reviews help improve quality early in the software lifecycle.

---

## Full Set of Common Review Activities

Here are the **typical stages** of a **formal review** (like an inspection), including the ones you already mentioned:

| Step | Activity Name                       | Description                                                                                               |
| ---- | ----------------------------------- | --------------------------------------------------------------------------------------------------------- |
| 1️⃣   | **Planning**                        | Identify review type, goals, participants, schedule, and entry criteria.                                  |
| 2️⃣   | **Review Initiation / Kick-off**    | Introduce the work product, explain objectives, assign roles (author, moderator, reviewers, scribe).      |
| 3️⃣   | **Individual Review (Preparation)** | Each reviewer examines the document/code alone, noting issues using checklists or guidelines.             |
| 4️⃣   | **Review Meeting / Discussion**     | Team meets to discuss defects found, clarify misunderstandings, and log issues.                           |
| 5️⃣   | **Rework**                          | Author corrects the identified defects. May be done with or without a follow-up review.                   |
| 6️⃣   | **Follow-Up**                       | Moderator verifies that all major issues were resolved and exit criteria are met.                         |
| 7️⃣   | **Analysis and Reporting**          | Collect metrics (e.g. number of defects, time spent), identify process improvements, and report outcomes. |

---

## Optional or Supporting Activities

Some additional elements might be included depending on the organization or process maturity:

- **Defect Logging**  
  Track issues formally in a defect tracker or log sheet.

- **Checklist Creation/Review**  
  Develop or tailor checklists that guide reviewers (e.g. for requirements, test cases, or code).

- **Exit Review / Approval**  
  Final check that the document/code meets quality standards and can move forward (often used in compliance-heavy domains).

---

## Example in Code Review Context

A practical example for a **code review**:

1. **Planning** → Decide to review a new module before integration
2. **Kick-off** → Dev lead explains what the module does
3. **Individual Review** → Reviewers read the code and log potential bugs
4. **Review Meeting** → Discuss potential issues (e.g., logic bugs, naming conventions)
5. **Rework** → Author fixes the code
6. **Follow-Up** → Dev lead checks that issues are resolved
7. **Reporting** → Capture how many issues were found to improve future development

---

## TL;DR – Main Activities (Full Cycle)

```
1. Planning
2. Review Initiation (Kick-off)
3. Individual Review (Preparation)
4. Review Meeting (Discussion)
5. Rework
6. Follow-Up
7. Communication, Analysis & Reporting
```

---

## Why Reviews Matter

- Catch defects **before costly rework.**
- Improve quality and clarity of documents and code.
- Encourage **collaboration and shared understanding.**

Both informal and formal reviews are crucial for delivering high-quality software!
