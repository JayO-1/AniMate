# AniMate
> AI-powered chatbot for discovering and analysing anime, built with Next.js and LangChain

A ChatGPT chatbot that uses an agent powered by the GPT-3.5-Turbo API for discovering and analysing anime. The agent relies on [OpenAI Function Calling](https://platform.openai.com/docs/guides/function-calling) to retrieve real-time information on a given anime on user request from various sources, like:
- Wikipedia
- [MyAnimeList.net](https://myanimelist.net/), one of the largest online anime/manga DBs. It is accessed via the [Jikan API](https://jikan.moe/)

The **tools** currently provided allow the agent to:
1. Get a summary of the anime from the anime's Wikipedia page
2. Look up ratings received by the anime on MyAnimeList.net
3. Get recommendations based on the anime from MyAnimeList.net
4. Get a summary of the top five reviews on the anime from MyAnimeList.net

As of yet, the agent does not use retrieval augmented generation (RAG) to provide its responses, but I plan to add this functionality in future updates to give it more in-depth anime knowledge.

## Tech Stack

[LangChain](https://www.langchain.com/) - LangChain is a framework that makes it easier to build scalable AI/LLM apps and chatbots. <br>
[Supabase](https://supabase.com/) - Supabase is an open-source Firebase alternative that provides a Postgres DB in place of a No-SQL DB, alongside the majority of features provided by Firebase <br>
[OpenAI](https://platform.openai.com/docs/overview) - OpenAI provides APIs that allow developers to build AI applications using their proprietary models as a base <br>
[Next.js](https://nextjs.org/) - A framework built on React that allows developers to easily build full-stack Web applications

**Prelude:** Please make sure you have already downloaded Node on your system and the version is 18 or greater.

## Repo Structure

The repo is divided into two main directories:
- **agent/** -> All prototyping occurs here within Jupyter Notebooks. Any new chatbot functionality is first implemented in Python via Langchain, before being migrated to the main web app
- **animate/** -> A full-stack web app utilising Next.js and Supabase to provide a UI for the chatbot. Next.js is used for the front-end, while Supabase is used for elements of back-end functionality. Currently a WIP

## Setup

WIP

## Demo

Stay tuned :) 

## Contact

Email: jxyozu3@gmail.com <br>
Twitter: @tenxdev_
