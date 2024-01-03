# AniMate
> AI-powered chatbot for discovering and analysing anime, built with Next.js and LangChain

A ChatGPT chatbot that uses an agent powered by the GPT-3.5-Turbo API for discovering and analysing anime. The agent relies on [OpenAI Function Calling](https://platform.openai.com/docs/guides/function-calling) to retrieve real-time information on a given anime on user request from various sources, like:
- Wikipedia
- [MyAnimeList.net](https://myanimelist.net/), one of the largest online anime/manga DBs. It is accessed via the [Jikan API](https://jikan.moe/)

The **tools** currently provided allow the agent to:
1. Get a summary of the anime from the anime's Wikipedia page
2. Look up ratings received by the anime on MyAnimeList.net
3. Get recommendations based on the anime from MyAnimeList.net
4. Get a summary of the top-rated reviews on the anime from MyAnimeList.net

As of yet, the agent does not use a vector database to provide its responses, but I plan to add this functionality in future updates to give it more in-depth anime knowledge and reduce tool usage.

## Why AniMate?
Having been an avid consumer of anime since a young age, and after working in the tech industry, I've observed the evolving intersections of entertainment and technology. This interest combined with my fascination with AI and the world of LLMs naturally steered me towards exploring the capabilities of Large Language Models (LLMs) and their applicability in niche sectors such as anime analysis and discovery. 

Driven by a genuine curiosity for the potential of AI, I undertook the development of a GPT-powered chatbot tailored for anime enthusiasts. This project not only allows me to apply and refine my skills in modern AI application development using technologies like Langchain and Next.js but is also aimed at inspiring interest in the anime community regarding how AI can be used to enhance the average anime watcher's experience.

## Tech Stack

[LangChain](https://www.langchain.com/) - LangChain is a framework that makes it easier to build scalable AI/LLM apps and chatbots. <br>
[Supabase](https://supabase.com/) - Supabase is an open-source Firebase alternative that provides a Postgres DB in place of a No-SQL DB, alongside the majority of features provided by Firebase <br>
[OpenAI](https://platform.openai.com/docs/overview) - OpenAI provides APIs that allow developers to build AI applications using their proprietary models as a base <br>
[Next.js](https://nextjs.org/) - A framework built on React that allows developers to easily build full-stack Web applications

**Prelude:** Please make sure you have already downloaded Node on your system and the version is 18 or greater.

## Repo Structure

The repo is divided into two main directories:
- **agent/**
    - All prototyping occurs here within Jupyter Notebooks. Any new chatbot functionality is first implemented in Python via Langchain, before being migrated to the main web app
- **animate/**
    - A full-stack web app utilising Next.js and Supabase to provide a UI for the chatbot. Next.js is used for the front-end, while Supabase is used for elements of back-end functionality. Currently a WIP

## Roadmap

+ **V1.0.0 (IN PROGRESS)**
    - Authentication: Allow user to log in/signup
    - Agent functionality: Interact with Wikipedia and myanimelist.net Tools provided to the agent:
        - Retrieve anime synopsis: Get the anime synopsis. _Wikipedia_
        - Retrieve anime ID: Get the MAL ID of the anime. _Jikan API endpoint: getAnimeSearch_
        - Retrieve real-time statistics: Get the live statistics on an anime. _Jikan API endpoint: getAnimeStatistics_
        - Retrieve recommendations: Get other anime recommendations based on a given anime. _Jikan API endpoint: getAnimeRecommendations_
        - Retrieve sentiment: Get sentiment around the anime. _Jikan API endpoint: getAnimeReviews_

## Setup

+ **agent/**
1. Clone the repo
2. Create a .env file in the same directory containing your OpenAI key in the form:
```
OPENAI_API_KEY=<your-key-here>
```
3. Run all cells under 'Imports'. These will install and import the required dependencies
4. Experiment with different aspects of functionality by running/modifying the relevant cells
---
+ **animate**

-- WORK IN PROGRESS --

[//]: # (1. Run `npm run dev`
2. Go to `http://localhost:3000` to interact with the chatbot via the UI)

## Demo

Stay tuned :) 

## Contact

**Email:** jxyozu3@gmail.com <br>
**Twitter:** [@tenxdev_](https://twitter.com/tenxdev_)
