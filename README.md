 <div align="center">

<img src="https://images.unsplash.com/photo-1521737711867-e3b97375f902?auto=format&fit=crop&w=1600&q=85" alt="Professional team collaborating on career and technology projects" width="100%" />

# 🎯 Auto AI Internship Applier

### Your internship workflow, reimagined with AI.

  An intelligent workflow automation project built with **n8n, Google Gemini, and Gmail** to streamline internship-related content generation   and email delivery.

  <p>
  <img src="https://img.shields.io/badge/AI-Google%20Gemini-4285F4?style=flat-square&logo=google&logoColor=white" alt="Google Gemini" />
  <img src="https://img.shields.io/badge/Automation-n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" alt="n8n" />
  <img src="https://img.shields.io/badge/Email-Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Gmail" />
  <img src="https://img.shields.io/badge/Workflow-AI%20Powered-7952B3?style=flat-square" alt="AI-powered workflow" />
  <img src="https://img.shields.io/badge/License-MIT-2EA44F?style=flat-square" alt="MIT License" />
  </p>
  
  **Build smarter workflows. Save repetitive effort. Focus on your career.**

</div>

---

## 01 · The Vision

  Finding internship opportunities and preparing professional application-related communication can take time. AI and automation offer a way to simplify some of these repetitive tasks.
  
  **Auto AI Internship Applier** explores how a scheduled n8n workflow can use Google Gemini to generate structured content and Gmail to deliver the resulting message automatically.
  
  This project demonstrates the foundation of an AI-assisted internship workflow that can be extended with job discovery, resume matching, application tracking, and other career-focused features.
  
  > **The idea:** Connect AI reasoning with practical automation to make internship-related workflows more efficient.
  
## 02 · What Makes It Useful?

  <table>
  <tr>
  <td width="50%">
  
  ### 🧠 AI Content Generation
  
  Use Google Gemini to generate content according to the instructions configured in the LLM Chain.
  
  </td>
  <td width="50%">

### ⏱️ Scheduled Execution

  Use n8n's Schedule Trigger to initiate the workflow at a configured time.
  
  </td>
  </tr>
  <tr>
  <td width="50%">

### 🧩 Structured Responses

  Use the Structured Output Parser to help format AI responses into a defined structure.
  
  </td>
  <td width="50%">
  
### 📩 Email Automation

  Connect the workflow to Gmail to deliver the generated message to the configured recipient.
  
  </td>
  </tr>
  </table>

## 03 · Workflow Architecture

<div align="center">

<img src="https://res.cloudinary.com/dntdfccdk/image/upload/v1792165752/Screenshot_2026-10-16_211818_axc7vo.png" alt="Auto AI Internship Applier n8n workflow screenshot" width="100%" />

*Actual workflow preview — Schedule Trigger → Basic LLM Chain → Gmail, with Google Gemini and Structured Output Parser connected.*

</div>

### The automation pipeline
  
  ```mermaid
  flowchart TD
      A["⏰ Schedule Trigger"] --> B["✨ Basic LLM Chain"]
      C["🧠 Google Gemini Chat Model"] -.-> B
      D["🧩 Structured Output Parser"] -.-> B
      B --> E["📧 Gmail - Send a Message"]
  
      style A fill:#172554,color:#FFFFFF,stroke:#60A5FA
      style B fill:#312E81,color:#FFFFFF,stroke:#A5B4FC
      style C fill:#1D4ED8,color:#FFFFFF,stroke:#93C5FD
      style D fill:#155E75,color:#FFFFFF,stroke:#67E8F9
      style E fill:#991B1B,color:#FFFFFF,stroke:#FCA5A5
  ```

### How it works

**Step 1 — Schedule**

  The Schedule Trigger initiates the workflow based on the configured execution interval.

**Step 2 — Generate**

  The Basic LLM Chain sends the configured prompt to the connected Google Gemini Chat Model.

**Step 3 — Structure**

  The Structured Output Parser helps format the generated response according to the configured output schema.

**Step 4 — Deliver**

  The Gmail node sends the generated message to the configured recipient using the configured email settings.

  *The exact content generated and delivered depends on your prompt, parser schema, credentials, and Gmail node configuration.*

## 04 · Technology Stack

  | Technology | Role in the project |
  |---|---|
  | n8n | Visual workflow orchestration and automation |
  | Google Gemini Chat Model | AI-powered content generation |
  | Basic LLM Chain | Connects prompts with the language model |
  | Structured Output Parser | Helps produce structured AI responses |
  | Gmail | Automated email delivery |
  | Mermaid | Workflow architecture visualization in this README |

## 05 · Get Started

### Prerequisites

  - An n8n account or self-hosted n8n instance.
  - Access to a supported Google Gemini model.
  - Google Gemini credentials configured in n8n.
  - A Google account with Gmail access.
  - The exported workflow JSON file.

### Installation

**1. Import the workflow**

  Export the workflow from your n8n workspace as JSON, then import it into your own n8n instance.

**2. Configure Google Gemini**

  Set up the required credentials and confirm that the model is connected to the Basic LLM Chain.

**3. Configure the prompt**

  Customize the instructions to generate the internship-related content you need, such as a draft application email, an internship inquiry,     or a professional follow-up message.

**4. Configure structured output**

  Review the output schema and ensure the generated response matches the format expected by your workflow.

**5. Connect Gmail**

  Authorize the required Gmail account and configure the recipient, subject, message content, and other required fields.

**6. Test the workflow**

  Execute it manually first. Review the AI output and verify that the email is delivered as intended.

**7. Enable the workflow**

  Once the configuration and test results are correct, activate or publish the workflow according to your n8n version.

## 06 · Potential Upgrades

  The current workflow is a foundation. These enhancements could make it a more complete internship application assistant.

  - [ ] Retrieve internship opportunities from suitable RSS feeds or authorized job APIs.
  - [ ] Filter opportunities by role, location, skills, and eligibility.
  - [ ] Match internship descriptions against a resume or skills profile.
  - [ ] Generate personalized application email drafts.
  - [ ] Add a human approval step before sending application emails.
  - [ ] Track opportunities and application status in Google Sheets.
  - [ ] Detect duplicate opportunities.
  - [ ] Send reminders for deadlines and follow-ups.
  - [ ] Add error handling and execution notifications.

## 07 · Security & Responsible Automation

  - Keep API keys, OAuth tokens, and passwords out of GitHub.
  - Store credentials in n8n's credential manager.
  - Inspect exported workflow JSON before publishing it.
  - Avoid exposing private email addresses or personal information in screenshots.
  - Verify generated content before using it in a real application.
  - Obtain human approval before sending personalized application emails.
  - Follow the terms of use of any job platform or data source you integrate.

## 08 · What This Project Demonstrates

  Building this workflow provides practical experience with:
  
  - Visual workflow automation using n8n.
  - Integrating generative AI into a real-world workflow.
  - Prompt design and structured AI output.
  - Gmail integration and automated communication.
  - Workflow testing and troubleshooting.
  - Credential management and responsible AI usage.

## 09 · Project Information

  | Detail | Information |
  |---|---|
  | Project | Auto AI Internship Applier |
  | Category | AI & Workflow Automation |
  | Workflow Platform | n8n |
  | AI Model | Google Gemini Chat Model |
  | Email Integration | Gmail |
  | License | MIT |

## 10 · About the Creator

**Kalikowsik**

  Aspiring Full Stack Developer · AI & Automation Enthusiast
  
  I'm exploring practical applications of AI, automation, and modern technology by building projects that connect intelligent systems with everyday tasks.
  
  - GitHub: https://github.com/kanithikalikowsik
  - LinkedIn: www.linkedin.com/in/kanithi-kali-kowsik

## License

Distributed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

<div align="center">

### ✦ Automate the routine. Make room for opportunity.

  **Designed with n8n · Powered by Google Gemini · Connected with Gmail**

  If this project inspires you, consider giving the repository a ⭐.

</div>
