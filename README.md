
# SkillPath

## What

SkillPath is a tool for accounting students and recent graduates who want to understand which skills are relevant to their career goals and keep track of evidence they have gained through coursework, projects, or internships.

The user selects a career path and sees its related skills. They can then attach evidence to a skill, and the system updates its status once the evidence is saved. For HW5, the project is adding F-06, an exportable skill summary, so students can use their skills and evidence in a resume or portfolio.

The project is based on user research, including an interview with INT-03, a 2025 accounting graduate who said she had not figured out which skills to develop for her career.

## See It Work

The application lets a student:
- Select an accounting career path.
- View the skills associated with that path.
- Add evidence from coursework, projects, or internships.
- See whether a skill is evidenced or not yet evidenced.
- Export a summary of their skills and evidence.

![SkillPath application](docs/image.png)

## How to Run

1. Clone or download this repository.
2. Open the project folder.
3. Install the required dependencies:

   ```bash
   npm install
   ```

4. Start the local development environment using the project's configured command:

   ```bash
   npx wrangler dev
   ```

5. Open the local URL shown in the terminal.

The application uses a Cloudflare Worker and D1 database for saving evidence. The database must be configured according to the project setup before testing save functionality.

To run the automated tests:

```bash
API=<your-worker-url> npm test
```

Replace `<your-worker-url>` with the URL of the Worker you are testing.

## Status

The existing F-03 evidence log is implemented using a Cloudflare Worker and D1 database. The application supports selecting career paths, viewing skills, attaching evidence, and displaying saved evidence.

The HW3 browser-storage approach was replaced with the Worker/D1 architecture in HW4, so evidence is no longer stored in `localStorage`. The HW4 SQL implementation also uses parameterized `bind()` values rather than string-concatenated SQL.

F-06, the exportable skill summary, is the feature selected for HW5. Its specification and acceptance criteria are documented in `context/FEATURES.md`. The implementation, evaluation, and verification were completed as part of this assignment.

## Delegation

For HW5, Bolt.new was used to generate an implementation of F-06 from the project's existing context files and committed specification.

The generated code was preserved, reviewed, tested, and corrected before being accepted into the project. The delegated output and review process are documented in the `delegated/` folder and in the decision records.

AI Studio was also attempted with the same F-06 context and instruction, but it returned an invalid-argument error before producing an implementation. Therefore, no AI Studio implementation was available for a code comparison.

## Links

- Project repository: https://github.com/ReginaChoi/mgt3745-hw5
- Deployed application: https://mgt3745-hw4.rchoi47.workers.dev/entries
- Previous HW4 project: https://github.com/ReginaChoi/mgt3745-hw4

## AI Use

AI tools were used to support development, review code, and help identify issues. The project specification and acceptance criteria were written before the delegated implementation was generated.

Bolt.new was used for the HW5 F-06 feature. The generated code was checked against the project's requirements, design tokens, and security standards. AI Studio was attempted for comparison, but it returned an invalid-argument error before producing an implementation. Testing results, corrections, and decisions are documented in the evaluation files and decision records.
