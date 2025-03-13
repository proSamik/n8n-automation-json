# AI System for Viral Reels - Setup Guide

This guide will walk you through setting up an AI-powered system for analyzing and creating viral social media reels. The entire setup process takes approximately 5 minutes.

## Prerequisites

Before you begin, you'll need to create accounts with the following services:

1. [n8n](https://n8n.io/) - Workflow automation platform
2. [Airtable](https://airtable.com/) - Database to store influencer data
3. [Apify](https://apify.com/) - Web scraping and automation
4. [Google AI Studio](https://aistudio.google.com/) - Access to Gemini AI model

## Setup Instructions

### Step 1: Set up n8n

1. Create an account at [n8n.io](https://n8n.io/)
2. Create a new workflow (it will be empty initially)
3. Import the system template:
   - Click the 3 dots in the top right corner
   - Choose "Import from file"
   - Select the JSON file from the repository

### Step 2: Set up Airtable

1. Copy the Airtable database by visiting [this link](https://airtable.com/appoQM8cbMoz4HHlh/shr7QEBcfPy8sA7kt)
2. Click "Copy Base" in the top left corner
3. Create an Airtable access token:
   - Go to [https://airtable.com/create/tokens](https://airtable.com/create/tokens)
   - Generate a new token with necessary permissions
4. Insert the Airtable token inside the n8n Airtable node

### Step 3: Set up Apify

1. Create an account at [Apify.com](https://apify.com/)
2. Create an Apify access token:
   - Go to [https://console.apify.com/settings/integrations](https://console.apify.com/settings/integrations)
   - Generate a new API token
3. Insert the Apify token inside the n8n Apify node

### Step 4: Set up Google AI (Gemini)

1. Create a Google AI Studio account at [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Create an API key for Gemini through the same link
3. Insert the Gemini API key inside the n8n Google nodes

### Step 5: Configure Influencers

1. Open your Airtable database
2. Add the influencers you want to analyze to the database

## Completion

🏁 Congratulations! 👏 Your AI system for viral reels is now fully set up and ready to use. Refer to the main README in the repository root for usage instructions. 