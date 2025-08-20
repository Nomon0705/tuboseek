<a href="https://www.turboseek.io">
  <img alt="TurboSeek" src="./public/og-image.png">
  <h1 align="center">TurboSeek</h1>
</a>

<p align="center">
  Open-source AI search engine powered by Together AI.
</p>

> Want to learn how to build this? Check out the [tutorial](https://docs.together.ai/docs/ai-search-engine).

## Tech Stack

- **Next.js (App Router)** with Tailwind CSS  
- **Together AI** for LLM inference  
- **Llama 3.1** (8B & 70B) models  
- **Bing / Serper API** for search  
- **Helicone** for observability  
- **Plausible** for analytics  

## How It Works

1. Accept the user’s question.  
2. Query the Bing/Serper API for the top 6 results.  
3. Scrape and store text from those results as context.  
4. Send the user’s question + context to **Llama 3.1 70B** and stream the answer.  
5. Use **Llama 3.1 8B** to generate 3 related follow-up questions.  

## Getting Started

1. Fork or clone this repository.  
2. Create an account at [Together AI](https://togetherai.link) for LLM access.  
3. Create an account at [Serper](https://serper.dev/) or [Bing Search API](https://www.microsoft.com/en-us/bing/apis/bing-web-search-api).  
4. (Optional) Set up [Helicone](https://www.helicone.ai/) for observability.  
5. Create a `.env` file (based on `.example.env`) and add your API keys.  
6. Install dependencies and run the dev server:  

   ```bash
   npm install
   npm run dev
