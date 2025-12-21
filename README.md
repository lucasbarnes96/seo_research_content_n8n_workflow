# SEO Research & Content Strategy n8n Workflow

A streamlined n8n workflow designed to analyze SERP data (Google & YouTube) and generate actionable content strategy insights for YouTube creators.

## 🚀 Overview

This workflow performs the following:
1.  **Triggers** manually or via Google Sheets.
2.  **Fetches** search data from Google and YouTube via SerpAPI.
3.  **Consolidates** results and sends them to Google Gemini.
4.  **Analyzes** the data across 9 key metrics in 3 tiers:
    *   **Tier 1: Opportunity Signals** (Should I make this?)
    *   **Tier 2: Positioning** (What angle?)
    *   **Tier 3: Execution** (How to package?)
5.  **Outputs** a final verdict with a recommendation to make the video or not, confidence score, and suggested title/format.

## 🛠 Setup

### Prerequisites
- An [n8n](https://n8n.io/) instance.
- [SerpAPI](https://serpapi.com/) credentials.
- [Google Gemini (Google Cloud)](https://ai.google.dev/) API key.
- A Google Sheet to store research data.

### Configuration
1.  **Import the JSON**: Copy the contents of `seo-research-content.json` and import it into your n8n workspace.
2.  **Update Credentials**:
    *   Set up your **SerpAPI** credentials.
    *   Set up your **Google Gemini** credentials.
    *   Set up your **Google Sheets** credentials.
3.  **Connect Google Sheet**:
    *   Update the `documentId` in the "Get row(s) in sheet" and "Update row in sheet" nodes with your specific Sheet ID.
    *   Ensure your sheet has the required columns (Search Query, Status, etc.).

## 📊 Metrics Analyzed

- **Video Deficit Score**: Ratio of Google results to YouTube results.
- **Distress Signal**: Presence of forums (Reddit, Quora) in top results.
- **David vs Goliath**: Count of small channels in top results.
- **Implementation Gap**: Percentage of \"how-to\" content.
- **Authority Dominance**: Enterprise vs. Peer content mix.
- **Topic Freshness**: Average age of top videos.
- **Contrarian Potential**: Sentiment analysis for unique angles.
- **Velocity Signal**: Identification of high-growth content formats.
- **Format Void**: Missing content types (e.g., Masterclasses, Shorts).

## 📄 License

MIT
