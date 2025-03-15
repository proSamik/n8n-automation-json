# YouTube Transcript Analyzer - Setup Guide

This guide will walk you through setting up an AI-powered system for summarizing YouTube videos. The system extracts video transcripts, analyzes key points, and generates actionable summaries specifically tailored for SaaS developers and entrepreneurs. The entire setup process takes approximately 5 minutes.

## Prerequisites

Before you begin, you'll need to create accounts with the following services:

1. [n8n](https://n8n.io/) - Workflow automation platform
2. [Google Cloud Platform](https://console.cloud.google.com/) - For Google Sheets API and OAuth credentials
3. [Apify](https://apify.com/) - Web scraping and automation for YouTube transcripts
4. [Google AI Studio](https://aistudio.google.com/) - Access to Gemini AI model

## Setup Instructions

### Step 1: Set up n8n

1. Create an account at [n8n.io](https://n8n.io/)
2. Create a new workflow (it will be empty initially)
3. Import the system template:
   - Click the 3 dots in the top right corner
   - Choose "Import from file"
   - Select the `youtube-transcript-summariser.json` file from this repository

### Step 2: Set up Google Sheets

1. Create a Google Spreadsheet or use [this template](https://docs.google.com/spreadsheets/d/1y4jzqEyy3FlCriJZoLCfP9XyATunZd56URp14dyrl8Y/edit?usp=sharing) (click "Make a copy")
2. Note the spreadsheet ID from the URL (the long string between /d/ and /edit in the URL)
3. Set up Google OAuth credentials:
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select an existing one
   - Enable the Google Sheets API for your project
   - Create OAuth 2.0 credentials (Client ID and Client Secret)
   - Configure the OAuth consent screen
   - Add authorized redirect URIs for your n8n instance
4. In n8n, configure the Google Sheets node with your credentials:
   - Use the Client ID and Client Secret when creating a new credential
   - Authorize access to your Google account
   - Update the document ID to your spreadsheet

### Step 3: Set up Apify

1. Create an account at [Apify.com](https://apify.com/)
2. Create an Apify access token:
   - Go to [https://console.apify.com/settings/integrations](https://console.apify.com/settings/integrations)
   - Generate a new API token
3. Insert the Apify token inside the n8n HTTP Request node that calls the YouTube transcript scraper

### Step 4: Set up OpenRouter

1. Create an OpenRouter account at [https://openrouter.com/app/apikey](https://openrouter.com/app/apikey)
2. Create an API key for OpenRouter through the same link
3. Insert the OpenRouter API key inside the n8n OpenRouter nodes

## Using the System

1. Open your n8n dashboard
2. Navigate to the imported workflow
3. Test the workflow by entering a YouTube URL when prompted
4. The system will:
   - Extract the transcript from the YouTube video
   - Analyze the content using Gemini AI
   - Generate a summary with actionable insights
   - Store the results in your Google Spreadsheet

## Workflow Outputs

The system generates the following information for each YouTube video:
- General summary of the video content
- Bullet-point summary highlighting key points
- Actionable plan with implementation steps
- Practical examples tailored for SaaS developers and entrepreneurs

## Troubleshooting

Common issues and their solutions:

- **API Connection Errors**: Verify your API tokens are correctly entered and have the necessary permissions
- **Google Authentication Issues**: Make sure your OAuth credentials are properly configured and the redirect URIs match your n8n instance
- **Missing Transcripts**: Some YouTube videos may not have transcripts available or may be in a language not supported by the scraper
- **Workflow Timeout**: For longer videos, you may need to adjust the timeout settings in n8n

## Customization

You can customize the workflow in n8n:
1. Modify the Gemini AI prompt to focus on different aspects or industries
2. Adjust the Google Sheets template to capture different information
3. Add additional processing steps or integrations 