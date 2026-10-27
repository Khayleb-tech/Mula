# Mula
AI Phone Receptionist &amp; Order Agent
An autonomous, open-source AI voice receptionist built with Spring Boot. This application answers inbound phone calls via Twilio, leverages TwiML for media streaming or call control, interprets customer intent using generative AI, and automates order entry. It frees up business owners from managing the phones so they can focus on their core day-to-day operations.

🚀 Features

• Automated Order Processing: Extracts menu items, quantities, and customer details directly from the voice stream using AI function calling.
• TwiML Stream Integration: Connects seamlessly with Twilio over webhooks using local development tunnels like ngrok.
• 24/7 Availability: Handles customer FAQs, reservation requests, or order status checks simultaneously without dropping calls.
• Human Hand-off: Seamlessly routes complex requests or escalation situations back to a human-operated line.

🛠️ Tech Stack

• Backend Framework: Java 21 / Spring Boot 4.1.2
• Build & Dependency Tool: Maven
• Telephony API: Twilio (TwiML Java SDK)
• Local Tunneling: ngrok
• AI Engine: OpenAI / LangChain4j (or Spring AI for LLM orchestration)

📦 Architecture Overview

1. Inbound Call: A user dials the business's Twilio phone number.
2. Webhook Trigger: Twilio forwards the call event to the Spring Boot backend using a public ngrok tunnel URL.
3. TwiML Response: The application returns TwiML instructions to capture speech input or initiate a bidirectional media stream.
4. AI Processing: The audio or transcribed text is processed by an LLM to determine intent (e.g., placing an order, checking hours).
5. Business Logic: Spring Boot services execute order placement workflows when a matching intent is found.
