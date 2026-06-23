Here's a LinkedIn post draft you can use, written to highlight both the technical build and the persistence through debugging:

🚀 Built my first AI-powered WhatsApp automation — and survived the debugging marathon!
Over the past few days, I built an end-to-end AI Customer Service Assistant that automatically receives, classifies, and responds to customer messages on WhatsApp — fully self-hosted, no third-party SaaS.
Tech stack:

🔹 n8n (workflow automation, self-hosted)

🔹 Evolution API (WhatsApp Business API gateway via Baileys)

🔹 Ollama + Llama 3.2 (local LLM for message classification)

🔹 Docker (Postgres + Redis + Evolution API containers)

🔹 Google Sheets (logging classified tickets by category)
How it works:

1️⃣ Customer sends a message on WhatsApp

2️⃣ Evolution API captures it and forwards it to n8n via webhook

3️⃣ An AI Agent (powered by a local LLM) classifies the message into categories: Complaint, Delivery, Refund, or Product

4️⃣ The system logs it into the matching Google Sheet for the support team

5️⃣ A personalized auto-reply is sent back to the customer in real time — confirming their message was received
The journey wasn't smooth (and that's the fun part):

❌ Redis disconnected errors on every container restart

❌ Docker container name conflicts

❌ A known Evolution API bug where QR codes returned count: 0 indefinitely

❌ Webhook URLs silently point to the wrong IP after network changes

❌ "Bad request" errors from malformed JSON body parameters

❌ AI Agent failed because Ollama wasn't even running 😅
✅ ...and after methodically isolating each layer (network → containers → API → workflow logic), everything finally clicked into place.
This project reinforced something I keep relearning: most "AI automation" failures aren't AI problems — they're infrastructure problems. Knowing how to read logs, trace a request end-to-end, and isolate variables matters just as much as design prompts.
Next step: expanding the classifier to trigger different automated workflows per category, and adding sentiment analysis for priority escalation.
#n8n #Automation #AI ​​#WhatsAppBusiness #Docker #SelfHosted #NoCode #CustomerService #Ollama #LLM
