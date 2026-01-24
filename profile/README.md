<div align="center">
  <h1>⚡ Thordata</h1>
  <p>
    <strong>The AI-Native Web Data Infrastructure for Developers & Agents</strong>
  </p>
  <p>
    <a href="https://www.thordata.com">🌐 Website</a> • 
    <a href="https://doc.thordata.com">📚 Documentation</a> • 
    <a href="https://dashboard.thordata.com">📊 Dashboard</a> •
    <a href="mailto:support@thordata.com">📧 Support</a>
  </p>
  <p>
    <img src="https://img.shields.io/badge/Uptime-99.99%25-success" alt="Uptime">
    <img src="https://img.shields.io/badge/Proxies-60M+%2B-blue" alt="Proxies">
    <img src="https://img.shields.io/badge/AI-Ready-purple" alt="AI Ready">
    <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
  </p>
</div>

---

## 🚀 Why Thordata?

Thordata is the next-generation web scraping and proxy infrastructure designed for the **AI era**. While traditional providers focus on manual scraping, we build pipelines that feed data directly into **LLMs, RAG systems, and AI Agents**.

We process over **100M+ requests daily** with a focus on speed, success rates, and developer experience.

### 🌟 Core Value Proposition
*   **AI-First Architecture**: Native support for MCP (Model Context Protocol) and LangChain.
*   **Unblockable Infrastructure**: Proprietary **Web Unlocker** technology that handles Captchas, fingerprints, and JS rendering automatically.
*   **Massive IP Network**: Ethical access to 60M+ Residential, Mobile, and ISP IPs in 181+ locations.
*   **Developer Centric**: Modern SDKs, strictly typed responses, and "Copy-Paste" ready examples.

---

## 🛠️ The Ecosystem

### 1. 🧠 AI & LLM Integrations (Next-Gen)
Empower your AI agents to browse the web and fetch real-time context.

| Repository | Description | Status |
| :--- | :--- | :--- |
| [**thordata-mcp-server**](https://github.com/Thordata/thordata-mcp-server) | 🤖 **AI Bridge**: Connect Claude Desktop / OpenAI directly to real-world web data via MCP protocol. | ✅ Stable |
| [**thordata-rag-pipeline**](https://github.com/Thordata/thordata-rag-pipeline) | 🔍 **RAG Ready**: Clean, structured data extraction pipeline optimized for Vector Databases. | 🚧 Beta |
| [**thordata-langchain-tools**](https://github.com/Thordata/thordata-langchain-tools) | 🦜🔗 **LangChain**: Official tools to turn Thordata into a web-browsing tool for your agents. | 🚧 TBD |

### 2. ⚡ Official SDKs
Type-safe, robust, and production-ready libraries for your stack.

| Language | Repository | Features |
| :--- | :--- | :--- |
| **Python** | [**thordata-python-sdk**](https://github.com/Thordata/thordata-python-sdk) | The flagship SDK. Async support, full typing, deeply integrated with Pandas/AI stacks. |
| **Node.js** | [**thordata-js-sdk**](https://github.com/Thordata/thordata-js-sdk) | TypeScript ready. Perfect for serverless and puppeteer/playwright integrations. |
| **Go** | [**thordata-go-sdk**](https://github.com/Thordata/thordata-go-sdk) | High-concurrency client for enterprise-grade scraping systems. |
| **Java** | [**thordata-java-sdk**](https://github.com/Thordata/thordata-java-sdk) | Enterprise compliant, thread-safe implementation. |

### 3. 🕸️ Scraping Solutions
From raw HTML to structured JSON, we handle the complexity.

*   **[SERP API](https://doc.thordata.com/interface-documentation/serp-api)**: Real-time search results from Google, Bing, Yandex (Search, Shopping, Maps, News).
*   **[Web Scraper API](https://doc.thordata.com/interface-documentation/web-scraper)**: "Swiss Army Knife" for any URL. Handles rendering, waiting, and extraction.
*   **[Scraping Browser](https://doc.thordata.com/interface-documentation/scraping-browser)**: Headless browsers hosted on our cloud. Connect via CDP/Selenium/Puppeteer.

---

## 💻 Quick Start (Python)

Install our flagship SDK:

```bash
pip install thordata
```

**Scenario: Search Google for "AI Agents" and get JSON results**

```python
import os
from thordata import ThorClient

# Initialize with your tokens
client = ThorClient(
    scraper_token=os.getenv("THORDATA_SCRAPER_TOKEN"),
    public_token=os.getenv("THORDATA_PUBLIC_TOKEN"),
    public_key=os.getenv("THORDATA_PUBLIC_KEY")
)

# 1. SERP Search (Google)
results = client.serp.search(
    engine="google",
    q="AI Agents using Web Data",
    location="United States",
    num=5
)

for item in results.get('organic_results', []):
    print(f"Title: {item['title']}")
    print(f"Link: {item['link']}")

# 2. Universal Scrape (Any URL)
html_content = client.universal.request(
    url="https://www.example.com",
    js_render=True,
    country="us"
)
```

---

## 🌍 Global Proxy Network

We provide the foundation for anonymous web access.

| Type | Repository / Docs | Use Case |
| :--- | :--- | :--- |
| **Residential** | [Docs](https://doc.thordata.com) | 60M+ IPs. Perfect for high-trust scraping (Social, E-commerce). |
| **Datacenter** | [Docs](https://doc.thordata.com) | High speed, low cost. Best for market intelligence. |
| **ISP** | [Docs](https://doc.thordata.com) | Static residential IPs. Keep the same session for banking/login flows. |
| **Mobile** | [Docs](https://doc.thordata.com) | 3G/4G/5G IPs for mobile-only app verification. |

---

## 🤝 Community & Support

We are building for the developers.

*   🐛 **Found a bug?** Open an issue in the respective repository.
*   💡 **Feature Request?** Check our [Roadmap](https://github.com/orgs/Thordata/projects) or discuss in Discussions.
*   📧 **Enterprise Inquiry?** Contact `business@thordata.com` for custom plans (>1TB/month).

<br>

<div align="center">
  <sub>© 2024-2026 Thordata Inc. All rights reserved. Built with ❤️ for the data community.</sub>
</div>