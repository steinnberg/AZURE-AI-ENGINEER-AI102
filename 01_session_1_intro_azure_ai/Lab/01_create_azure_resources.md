# Lab 01 — Create Azure AI Resources

## 🎯 Objective
In this lab, you will:
- Create an Azure **Resource Group**
- Create an **Azure AI Services** resource
- Retrieve the **API key and endpoint**
- Prepare your environment for future AI API calls

This lab is the foundation for all upcoming sessions.

---

## 🧩 Prerequisites
- An active **Azure account**
- Access to the **Azure Portal**
- Basic familiarity with cloud concepts

---

## 🚀 Step 1 — Create a Resource Group

1. Go to the **Azure Portal**  
   👉 https://portal.azure.com

2. In the search bar, type **Resource groups**

3. Click **Create**

4. Fill in the following information:

```text
Subscription: Your Azure subscription
Resource Group name: rg-ai102-lab
Region: West Europe
Click Review + Create, then Create
```

 ✅ A Resource Group is now available to host your AI resources.
---

## 🧠 Step 2 — Create an Azure AI Services Resource

1. In the Azure Portal search bar, type Azure AI services

2. Select Azure AI services

3. Click Create

4. Configure the resource:

```text
Subscription: Your Azure subscription
Resource Group: rg-ai102-lab
Region: West Europe
Name: ai102-ai-service
Pricing tier: Free (F0) or Standard (S0)
```

5. Click Review + Create, then Create

⏳ Deployment usually takes less than a minute.

---

## 🔑 Step 3 — Retrieve API Key and Endpoint

1. Open your **Azure AI services** resource

In the left menu, click **Keys and Endpoint**

Copy and save:

* **Endpoint**

* **Key 1**

⚠️ Treat your API keys as secrets.
Never commit them to GitHub.

---

## 🧪 Step 4 — Configure Environment Variables

Create environment variables to store your credentials securely.

▶️ Windows (PowerShell)
```bash
setx AZURE_AI_ENDPOINT "https://<your-endpoint>.cognitiveservices.azure.com/"
setx AZURE_AI_KEY "<your-api-key>"
```

Restart your terminal after running these commands.

▶️ macOS / Linux
```bash
export AZURE_AI_ENDPOINT="https://<your-endpoint>.cognitiveservices.azure.com/"
export AZURE_AI_KEY="<your-api-key>"
```

✅ Validation Checklist

Before moving forward, verify that:

 * Resource Group rg-ai102-lab exists

 * Azure AI services resource is deployed

 * API key and endpoint are accessible

 * Environment variables are correctly set

🧠 Key Takeaway

> Cloud AI starts with resource management.
> Every production AI system begins with correct infrastructure setup.