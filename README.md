# AI-Powered Instagram Post Automation Workflow (n8n)

Automate your Instagram content creation using AI-driven viral idea generation, caption writing, image creation, and publishing — all orchestrated seamlessly with n8n.

---

## Overview

This workflow automates the end-to-end process of creating viral Instagram posts based on the latest news in a chosen industry (e.g., Healthcare). It performs the following:

- Fetches the top 10 news articles via RSS feed.
- Uses AI (Google Gemini) to generate viral post ideas based on the news.
- Generates engaging Instagram captions with storytelling and emoji use.
- Creates Instagram-ready images with text overlays using AI image synthesis.
- Uploads images to an image hosting service and publishes posts via Instagram Graph API.
- Fully built and managed within n8n workflow automation platform.

---

## Features

- Dynamic industry news scraping via Google News RSS.
- AI-generated viral content ideas with unique hooks and emotional appeal.
- Natural, authentic, and conversational Instagram captions.
- Modern, clean, and readable Instagram post images with bold text overlays.
- Automated image hosting and post publishing to Instagram business accounts.
- Robust error handling and JSON parsing inside code nodes.
- Modular design with clear separation of data fetching, AI processing, and publishing.

---

## Challenges Encountered

- Parsing and transforming AI text responses correctly from JSON strings.
- Managing API quotas, rate limits, and authentication for multiple services (Google PaLM API, Hugging Face, IMGBB, Facebook Graph API).
- Ensuring image text overlays are clean, bold, and highly readable on Instagram's square format.
- Coordinating asynchronous API calls reliably inside n8n.
- Maintaining workflow flexibility to easily switch industries by changing input parameters.

---

## Prerequisites

- An n8n instance up and running (self-hosted or n8n cloud).
- Google PaLM API credentials for Google Gemini language models.
- Hugging Face API key for AI image generation.
- IMGBB API key for image hosting.
- Facebook Developer account with Instagram Graph API access and appropriate permissions.
- Basic familiarity with n8n workflow creation and credential management.

---

## Setup & Installation

1. Clone or import the n8n workflow JSON into your n8n instance.
2. Configure all credentials:
   - Google PaLM API
   - Hugging Face API
   - IMGBB API
   - Facebook Graph API (Instagram)
3. Modify the `Set Industry` node to your desired industry keyword.
4. Trigger the workflow manually or schedule as needed.

---

## Workflow Breakdown

- **Set Industry**: Define the target industry for news scraping.
- **Fetch News RSS**: Retrieves the latest top news articles.
- **Limit, Aggregate, and Parse News**: Filters and formats news into AI-friendly input.
- **Generate Viral Ideas**: Calls Google Gemini to create viral post ideas based on news.
- **Parse and Split Ideas**: Processes returned JSON array of ideas.
- **Generate Caption**: Creates engaging Instagram captions for each idea.
- **Generate Image Prompt**: Prepares AI image generation prompts.
- **Generate Image**: Uses Hugging Face API for creating Instagram post images.
- **Save Image**: Uploads the generated image to IMGBB.
- **Prepare Post Data**: Sets up image URLs and captions for publishing.
- **Connect Graph API & Publish Post**: Publishes posts to Instagram via Facebook Graph API.
- <img width="1157" height="600" alt="Screenshot 2025-10-22 190639" src="https://github.com/user-attachments/assets/e4abd288-5f63-4a27-8133-fe55a483ea7b" />


---

##Results & Outputs
<img width="1457" height="948" alt="Screenshot 2025-10-22 190709" src="https://github.com/user-attachments/assets/eeeee295-e1cc-4ad5-afbb-cae7a980730b" />
<img width="1433" height="826" alt="Screenshot 2025-10-22 190657" src="https://github.com/user-attachments/assets/b323acb3-960f-4e2d-ad69-59678072578d" />


## Resources & References

- [n8n Documentation](https://docs
