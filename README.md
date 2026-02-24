Diligence AI - Supplier Risk Analysis Agent

Diligence AI is a specialized conversational agent designed for compliance and risk analysis. It automates the process of validating Brazilian company IDs (CNPJ) and calculating security scores by integrating Microsoft Copilot Studio with Power Automate and the BrasilAPI.

🚀 Features
Automated CNPJ Validation: Captures user input and verifies corporate data in real-time.

Smart Error Handling: A custom logic flow that identifies invalid inputs and prompts for correction without restarting the conversation.

Inter-Topic Redirection: Seamlessly transitions from error-handling routines directly to the risk analysis engine.

Low-Code Integration: Uses Power Automate to fetch data from external APIs (BrasilAPI).

🛠️ Technical Architecture
1. Conversational Flow & UX
The bot is structured to prioritize user experience (UX) by avoiding "dead ends." When a user provides an incorrect CNPJ format:

The Error Topic triggers.

The bot requests the correct 14-digit number using a Global Variable (Global.Var_CNPJ).

Once corrected, the flow uses a "Go to step" or "Go to another topic" action to jump directly into the Risk Analysis Agent topic.

2. Tools Used
Microsoft Copilot Studio: Agent orchestration and natural language processing.

Power Automate: Backend automation and API communication.

BrasilAPI: Data source for Brazilian corporate records.

📂 Project Structure
/solutions: Contains the exported .zip solution file for environment deployment.

📝 How to Use
Import the solution into your Power Platform environment.
Trigger the bot by saying "Quero analisar uma empresa" (I want to analyze a company).

Enter the CNPJ when prompted. If an error occurs, the bot will guide you back to the analysis phase automatically.
