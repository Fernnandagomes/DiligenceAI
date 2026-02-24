# Diligence AI – Supplier Risk Analysis Agent

**Diligence AI** is a specialized conversational agent built for compliance and supplier risk analysis. It automates the validation of Brazilian company IDs (CNPJ) and generates security scores in real time by integrating Microsoft Copilot Studio, Power Automate, and BrasilAPI.


## 🚀 Features

### 🔍 Automated CNPJ Validation  
Captures user input and validates corporate data in real time through API integration.

### 🧠 Smart Error Handling  
Implements a custom logic flow that detects invalid CNPJ inputs and prompts the user for correction without restarting the conversation.

### 🔄 Inter-Topic Redirection  
Ensures a seamless user journey by redirecting from error-handling routines directly to the Risk Analysis Engine topic.

### ⚡ Low-Code Integration  
Leverages Power Automate to securely fetch and process external data from BrasilAPI.

---

## 🛠️ Technical Architecture

### 1. Conversational Flow & UX

The agent is structured to prioritize user experience (UX) by avoiding conversational “dead ends.”  

When a user provides an incorrect CNPJ format:

1. The **Error Topic** is triggered.  
2. The bot requests the correct 14-digit number using a Global Variable (`Global.Var_CNPJ`).  
3. Once corrected, the flow uses a **“Go to step”** or **“Go to another topic”** action to jump directly into the **Risk Analysis Agent** topic.

---

### 2. Tools Used

- **Microsoft Copilot Studio** – Agent orchestration and natural language processing  
- **Power Automate** – Backend automation and API communication  
- **BrasilAPI** – Data source for Brazilian corporate records  

---

## 📂 Project Structure

```
/solutions
 └── diligence-ai-solution.zip
```

Contains the exported `.zip` solution file for environment deployment.

---

## 📝 How to Use

1. Import the solution into your Power Platform environment.  
2. Trigger the bot by saying:  

   ```
   Quero analisar uma empresa
   ```

3. Enter the CNPJ when prompted.  

