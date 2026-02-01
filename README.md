# hotel-info-agent
hotel agent desc
# Hotel Information Agent (Azure AI Foundry)

## Project Overview
The Hotel Information Agent is an AI-powered assistant built using Azure AI Foundry. It is designed to help hotel guests quickly find accurate information about hotel services, policies, and nearby attractions through natural language conversations. The agent handles common guest inquiries such as check-in/check-out times, amenities, dining options, and local recommendations, while applying safety guardrails and clear response boundaries suitable for real-world hospitality environments.

---

## Architecture Overview (Under the Hood)
This agent follows a **Perception → Reasoning → Action** lifecycle:
- **Perception:** User messages are received through an API endpoint or the Azure AI Foundry Playground.
- **Reasoning:** The agent processes input using a configured Azure OpenAI model, applying system instructions, prompt engineering, and safety constraints.
- **Action:** The agent generates a response and returns it to the user. All interactions are managed through conversation threads, ensuring consistent context handling.

Authentication is handled securely using Azure-managed credentials (e.g., `DefaultAzureCredential`) to prevent exposure of API keys.

---

## Setup and Installation

### Prerequisites
- Azure account with access to **Azure AI Foundry**
- Python 3.9+
- Azure CLI (logged in)
- GitHub account

### Installation Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/hotel-info-agent.git
   cd hotel-info-agent
