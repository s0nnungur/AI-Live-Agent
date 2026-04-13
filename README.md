# AI Live Agent

AI Live Agent is an experimental serverless chat application built on the Cloudflare Developer Platform.

## Overview

This project combines a React frontend with a Cloudflare Worker backend, Durable Objects for per-session state, and Workers AI for response generation.

It was built as a hands-on exploration of:
- serverless application structure
- stateful conversations with Durable Objects
- AI integration in a web application
- deployment on Cloudflare Pages and Workers

## Stack

- React
- TypeScript
- Cloudflare Pages
- Cloudflare Workers
- Durable Objects
- Workers AI

## Architecture

Frontend (React on Cloudflare Pages)  
→ sends chat requests to a Worker  
→ Worker routes conversation state to a Durable Object  
→ Durable Object stores session history  
→ Worker sends conversation context to Workers AI

## Features

- Browser-based chat interface
- Serverless backend
- Per-session conversation memory
- AI-generated responses
- End-to-end Cloudflare deployment

## Project Structure

- `my-react-app/` – frontend
- `cf-ai-worker/` – backend Worker and Durable Object logic
- `PROMPTS.md` – prompt/design notes used during development

## Notes

This was an exploratory project and learning exercise rather than a production-ready application. My focus was understanding how the different Cloudflare components fit together and iterating on a working AI-enabled system.

## Local Development

### Frontend
```bash
cd my-react-app
npm install
npm run dev
