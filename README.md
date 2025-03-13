# n8n Automation for Viral Social Media Content Analysis

This repository contains JSON workflow files for automating the analysis of viral social media content using n8n, Airtable, Apify, and Google's Gemini AI.

## Overview

This automation system helps you:

1. Track and analyze specific social media influencers
2. Extract insights from their most successful content
3. Generate content ideas based on viral trends
4. Store all data in an organized Airtable database

## Repository Structure

- **Root directory**: Contains the main workflow JSON files
- **Date-specific folders**: Contain snapshots of the system configuration on specific dates
  - Example: `march-13/` contains the setup from March 13

## Getting Started

For detailed setup instructions, refer to the README.md file in the date-specific folder:
- [March 13 Setup Guide](./march-13/README.md)

## Using the System

Once you have set up the system following the instructions, here's how to use it:

### Running the Workflow

1. Open your n8n dashboard
2. Navigate to the imported workflow
3. Click "Execute Workflow" to start the analysis process
4. The workflow will:
   - Fetch content from specified influencers
   - Analyze engagement metrics
   - Extract key patterns and trends
   - Generate insights using Gemini AI
   - Store all data in your Airtable database

### Managing Influencers

1. Open your Airtable database
2. Add or remove influencers from the tracking table
3. Include relevant information:
   - Username/handle
   - Platform (TikTok, Instagram, etc.)
   - Content niche
   - Any specific tags to track

### Viewing Results

1. Results are automatically stored in your Airtable database
2. You can view:
   - Top-performing content
   - Engagement metrics
   - Content analysis
   - AI-generated insights

### Customization

You can customize the workflow in n8n:
1. Adjust analysis parameters
2. Modify the AI prompts
3. Change the data collection frequency
4. Add additional processing steps

## Troubleshooting

Common issues and their solutions:

- **API Connection Errors**: Verify your API tokens are correctly entered and have the necessary permissions
- **Empty Results**: Check that your influencer data is correctly formatted in Airtable
- **Workflow Timeout**: For larger analyses, you may need to adjust the timeout settings in n8n

## Updating

To update the system:
1. Download the latest JSON file from the repository
2. Import it into your n8n instance
3. Update any API keys if needed 