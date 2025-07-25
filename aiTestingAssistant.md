# 🚀 Getting Started with AI Testing Assistant

**What is AI Testing Assistant?**

AI Testing Assistant is a tool designed to help manual testers quickly generate high-quality manual test cases for any web page. Instead of writing test cases from scratch, you can use this assistant to automatically analyze a web page’s user interface and produce detailed, structured test cases in Markdown format.

**How does it help manual testers?**

- **Saves Time:** Automates the initial creation of test cases, so you can focus on reviewing and executing them.
- **Improves Coverage:** Ensures that important UI elements and user flows are not missed.
- **Easy to Use:** No coding required—just follow the steps to analyze a page and generate test cases.
- **Customizable:** You can adjust the prompts and scripts to fit your team’s needs or specific testing requirements.

Whether you’re new to manual testing or an experienced QA professional, AI Testing Assistant streamlines the process of documenting what needs to be tested, making your workflow faster and more reliable.

---

This guide will walk you through setting up, running, and using the **AI Testing Assistant** project to generate high-quality manual test cases from any web page.

---

## 1. Prerequisites

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

---

## 2. Project Setup

### a. Clone the Repository

```bash
git clone https://github.com/BrunoWebDesigner/ManualTestGenerator.git
cd aiTestingAssistant
```

### b. Install Dependencies

```bash
npm install
```

### c. Install Playwright Browsers

```bash
npx playwright install
```

---

## 3. Analyzing a Web Page

The project uses Playwright to extract UI metadata from a target web page.

### a. Configure the Target URL

Open [`analyzePage.spec.ts`](analyzePage.spec.ts) and set the URL of the page you want to analyze.

### b. Run the Playwright Analysis

```bash
npx playwright test analyzePage.spec.ts
```

- This will visit the target page and generate a [`rich-analysis.json`](rich-analysis.json) file containing structured UI data.

---

## 4. Generating Manual Test Cases

### a. Use the Prompt

- The prompt in [`copilotPrompt.md`](copilotPrompt.md) guides an AI assistant to generate Markdown test cases based on `rich-analysis.json`.

### b. Generate Test Cases

- Use your preferred AI assistant (such as GitHub Copilot Chat or ChatGPT) and provide:
  - The content of `copilotPrompt.md`
  - The latest `rich-analysis.json`
- The AI will output a Markdown file (e.g., [`testCases/youtube-manual-test-cases.md`](testCases/youtube-manual-test-cases.md)) with manual test cases.

---

## 5. Reviewing & Using Test Cases

- Find generated test cases in the [`testCases/`](testCases/) directory.
- Review and execute them as part of your manual QA process.
- Share with your team for collaborative testing.

---

## 6. Example Workflow

```bash
# 1. Install dependencies and browsers
npm install
npx playwright install

# 2. Analyze a web page
npx playwright test analyzePage.spec.ts

# 3. Generate test cases using copilotPrompt.md and rich-analysis.json
#    (Use your AI assistant as described above)
```

---

## 7. Customization

- **Prompt:** Edit [`copilotPrompt.md`](copilotPrompt.md) to change test case format or coverage.
- **Playwright Script:** Modify [`analyzePage.spec.ts`](analyzePage.spec.ts) to target different URLs or extract more data.

---

## 8. Troubleshooting

- If Playwright fails, ensure your Node.js and browser versions are up to date.
- Check that the target URL is accessible and not behind authentication (unless handled in your script).

---

## 9. Resources

- [Playwright Documentation](https://playwright.dev/)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [AI Testing Assistant README](https://github.com/BrunoWebDesigner/ManualTestGenerator)

---
