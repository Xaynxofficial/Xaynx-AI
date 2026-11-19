# Sub-Processors & Infrastructure List — XaynxAI

**Last Updated:** November 19, 2026

To deliver reliable, secure, and low-latency AI services, **XaynxAI** works with carefully vetted third-party technical sub-processors. All transfers are protected by encryption in transit (TLS 1.3), access controls, and applicable data protection safeguards under **KVKK (Law No. 6698)** and **GDPR Chapter V (Standard Contractual Clauses)**.

---

## 1. Core Cloud, Authentication & Payment Sub-Processors

| Sub-Processor | Role / Service Purpose | Data Region |
| :--- | :--- | :--- |
| **Cloudflare, Inc.** | Edge network, CDN, DDoS protection, Workers runtime (including scheduled autonomous agents), D1 database, and R2 object storage | Global / EU & US |
| **Contabo GmbH** | High-availability failover & disaster-recovery backup infrastructure | European Union (Germany) |
| **Clerk, Inc.** | User authentication, session security, and identity management | US / EU |
| **Lemon Squeezy, LLC** | Merchant of Record, global subscription billing, tax compliance, and payment processing | US / Global |
| **Shopier** | Local payment gateway processing (PCI-DSS compliant) | Turkey |
| **Resend, Inc.** | Transactional email delivery (security alerts, billing notices, verification) | US / EU |

---

## 2. Enterprise AI Inference Providers

XaynxAI routes user prompts to enterprise AI inference providers strictly to generate requested responses. We do **not** authorize the use of private user conversations to train public foundation models.

| Provider | Purpose |
| :--- | :--- |
| **Google LLC (Gemini API)** | Multimodal AI chat, reasoning, vision, and code generation |
| **OpenAI** | AI text, reasoning, and code inference |
| **Groq, Inc.** | High-speed LLM inference and speech-to-text transcription |
| **OpenRouter** | Multi-model enterprise API routing |

---

## 3. User-Authorized Third-Party OAuth Extensions (Optional)

The following services are **never** accessed unless explicitly connected by the user via `/extensions` and may be revoked with one click at any time:

- **Google Workspace** (Gmail, Google Drive, Google Calendar) — governed by our [Google API User Data Policy](./policies/GOOGLE_API_PRIVACY_POLICY.md)
- **GitHub**, **LinkedIn**, **Slack**, **Notion**, **Spotify**, **Canva**, and **Epic Games**

---

## 4. Sub-Processor Updates & Inquiries

We update this list whenever core sub-processors are added or replaced. For GDPR/KVKK Data Processing inquiries, contact **[contact@xaynx.com](mailto:contact@xaynx.com)**.
