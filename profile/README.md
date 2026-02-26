<div align="center">
  <h1>⚡ Thordata</h1>
  <p>
    <strong>The AI‑Native Web Data Infrastructure for Developers & Agents</strong>
  </p>
  <p>
    <a href="https://www.thordata.com">🌐 Website</a> ·
    <a href="https://doc.thordata.com">📚 Documentation</a> ·
    <a href="https://dashboard.thordata.com">📊 Dashboard</a> ·
    <a href="mailto:support@thordata.com">📧 Support</a>
  </p>
  <p>
    <img src="https://img.shields.io/badge/Uptime-99.99%25-success" alt="Uptime">
    <img src="https://img.shields.io/badge/Network-100M%2B_IPs-blue" alt="Proxies">
    <img src="https://img.shields.io/badge/AI-Native-purple" alt="AI Native">
    <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
  </p>
</div>

---

## 🚀 What is Thordata?

Thordata is the next‑generation web data and proxy infrastructure built for the **AI era**, providing a stable, scalable **AI‑native web data layer** for developers and agents.  
Unlike traditional scraping vendors that only focus on raw HTML, Thordata is designed from the ground up for **LLMs, RAG systems, and agents**, delivering clean, structured web data directly into your AI workflows.

- **100M+ requests / day** across mission‑critical and enterprise workloads  
- **100M+ compliant Residential / Mobile / ISP IPs** in 180+ locations worldwide  
- **Web Unlocker & Scraping Browser** to abstract away fingerprints, captchas, and JS rendering  
- **MCP / LangChain / SDK integrations** to plug Thordata directly into your agents and data pipelines

---

## 🧩 Product Pillars

- **1. Global Proxy Network**: Unified ingress layer for Residential / Mobile / ISP / Datacenter traffic  
- **2. Web Unlocker Engine**: Automatically bypasses complex anti‑bot systems and returns stable HTML / JSON  
- **3. Scraping Browser**: Cloud‑hosted browser fleet (CDP / Selenium / Puppeteer / Playwright)  
- **4. AI & LLM Integrations**: Native support for MCP, LangChain, RAG pipelines, and multi‑language SDKs  

All capabilities are exposed through a single, consistent interface—fast enough for MVPs, robust enough for serious production workloads.

---

## 🧠 AI & LLM Integrations

Give your agents and LLMs real‑time **browsing, search, and monitoring** superpowers:

| Repository | Description | Status |
| :--- | :--- | :--- |
| [**thordata-mcp-server**](https://github.com/Thordata/thordata-mcp-server) | 🤖 **AI Bridge**: MCP server that connects Claude Desktop / OpenAI clients directly to Thordata web data. | ✅ Stable |
| [**thordata-rag-pipeline**](https://github.com/Thordata/thordata-rag-pipeline) | 🔍 **RAG Pipeline**: End‑to‑end pipeline to clean → structure → chunk → embed web data for retrieval. | 🚧 Beta |
| [**thordata-langchain-tools**](https://github.com/Thordata/thordata-langchain-tools) | 🦜🔗 **LangChain Tools**: Official toolset that turns Thordata into plug‑and‑play browsing / scraping tools. | 🚧 TBD |

---

## ⚙️ Official SDKs

Production‑grade, type‑safe clients for every major stack. All four language SDKs are live and ready for production use:

| Language | Repository | Highlights |
| :--- | :--- | :--- |
| **Python** | [**thordata-python-sdk**](https://github.com/Thordata/thordata-python-sdk) | Flagship SDK · Async‑first · Full type hints · Deep integrations with data & AI tooling. |
| **Node.js** | [**thordata-js-sdk**](https://github.com/Thordata/thordata-js-sdk) | TypeScript‑first · Ideal for serverless, edge runtimes, and Puppeteer / Playwright workloads. |
| **Go** | [**thordata-go-sdk**](https://github.com/Thordata/thordata-go-sdk) | High‑concurrency, low‑latency client for large‑scale scraping and data pipelines. |
| **Java** | [**thordata-java-sdk**](https://github.com/Thordata/thordata-java-sdk) | Enterprise‑ready, thread‑safe implementation for regulated and legacy environments. |

---

## 🕸️ Scraping Solutions

From raw HTML to structured JSON, Thordata hides the complexity so you can focus on products and models:

- **[SERP API](https://doc.thordata.com/interface-documentation/serp-api)**: Structured Google / Bing / Yandex results across Search, Shopping, Maps, and News.  
- **[Web Scraper API](https://doc.thordata.com/interface-documentation/web-scraper)**: A "Swiss Army Knife" endpoint for any URL, with rendering, waiting, and custom extraction.  
- **[Scraping Browser](https://doc.thordata.com/interface-documentation/scraping-browser)**: Cloud‑hosted headless browsers compatible with CDP / Selenium / Puppeteer.  

You describe the data you want; the infrastructure handles the rest.

**Companion repositories (selected):**

- [**thordata-web-qa-agent**](https://github.com/Thordata/thordata-web-qa-agent): Web‑native QA agent built on Thordata (Perplexity‑style experience on your own stack).  
- [**google-play-reviews-rag**](https://github.com/Thordata/google-play-reviews-rag): Turns app‑store reviews into a production‑grade RAG knowledge base.  
- [**apify-amazon-search-product-scraper**](https://github.com/Thordata/apify-amazon-search-product-scraper): Multi‑marketplace Amazon search & product scraper with filters and enrichment.  
- [**thordata-proxy-examples**](https://github.com/Thordata/thordata-proxy-examples): End‑to‑end examples of proxy configuration, rotation, and Web Unlocker usage.  

---

## 💻 Quick Start (Python)

Install the official SDK:

```bash
pip install thordata
```

**Example: search Google for "AI Agents using Web Data" and fetch the HTML of any page**

```python
import os
from thordata import ThorClient

# Initialize with your tokens
client = ThorClient(
    scraper_token=os.getenv("THORDATA_SCRAPER_TOKEN"),
    public_token=os.getenv("THORDATA_PUBLIC_TOKEN"),
    public_key=os.getenv("THORDATA_PUBLIC_KEY"),
)

# 1. SERP Search (Google)
results = client.serp.search(
    engine="google",
    q="AI Agents using Web Data",
    location="United States",
    num=5,
)

for item in results.get("organic_results", []):
    print(f"Title: {item['title']}")
    print(f"Link: {item['link']}")

# 2. Universal Scrape (Any URL)
html_content = client.universal.request(
    url="https://www.example.com",
    js_render=True,
    country="us",
)
```

---

## 🌍 Global Proxy Network

The foundation for anonymous access and large‑scale web collection:

| Type | Docs | Typical Use Case |
| :--- | :--- | :--- |
| **Residential** | [Docs](https://doc.thordata.com) | High‑trust platforms such as social networks, ecommerce, and ticketing sites. |
| **Datacenter** | [Docs](https://doc.thordata.com) | High‑throughput, cost‑efficient workloads like market intelligence and monitoring. |
| **ISP** | [Docs](https://doc.thordata.com) | Static residential IPs for login flows, banking journeys, and long‑lived sessions. |
| **Mobile** | [Docs](https://doc.thordata.com) | 3G/4G/5G IPs for mobile‑only content, app verification, and risk systems. |

---

## 🤝 Community & Support

We build Thordata in close collaboration with the developer community:

- 🐛 **Bug reports**: Open an Issue in the corresponding repository.  
- 💡 **Feature requests / Roadmap**: Check [GitHub Projects](https://github.com/orgs/Thordata/projects) or start a Discussion.  
- 📧 **Enterprise & high‑volume use cases (> 1TB / month)**: Reach out to `business@thordata.com`.  

<br>

<div align="center">
  <sub>© 2024‑2026 Thordata Inc. All rights reserved. Built with ❤️ for the data community.</sub>
</div>