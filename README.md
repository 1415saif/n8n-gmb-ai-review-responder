# n8n-gmb-ai-review-responder
AI-powered Google Business Profile review responder built with n8n. Automatically detects new reviews, generates personalized and SEO-optimized replies using LLMs, posts the response on GMB, and logs all activity into Google Sheets.
Overview

This repository contains an automated workflow built in n8n that manages Google Business Profile (GMB) reviews. The system detects new reviews, analyzes them using an AI model, generates a personalized and professional reply, posts the response directly on Google Business Profile, and logs all review details into Google Sheets for record-keeping.

This workflow is designed for businesses looking to improve customer communication, maintain consistent brand tone, and streamline review management.

Features
Automated Review Detection

The workflow starts with the Google Business Profile Trigger, which monitors and captures new incoming reviews as soon as they are posted.

AI-Powered Reply Generation

A custom prompt and an OpenRouter LLM model are used to:

Analyze star ratings and review sentiment

Generate professional, polite, SEO-friendly responses

Personalize replies using the reviewer’s name

Create structured responses even when the reviewer only leaves a star rating

Dynamic Review Reply Posting

The workflow automatically posts the generated response back to the GMB profile using the Google Business Profile Reply node.

Activity Logging

Every processed review and AI-generated reply is appended to a Google Sheet for tracking and audit purposes.

Fully Automated Flow

No manual intervention needed after setup. The workflow handles all steps:

Detect review

Extract required fields

Generate AI response

Post reply

Log data

Workflow Structure

Google Business Profile Trigger
Detects new reviews and passes raw data to the next node.

Needed Fields Node
Extracts specific fields such as reviewer name, star rating, review text, and time.

Basic LLM Chain with OpenRouter Model
Processes review details through a crafted prompt to generate a human-quality response.

Wait Node
Ensures proper timing between generation and posting.

Reply to Review
Posts the generated reply directly to GMB.

Append Row in Google Sheets
Logs all relevant review and reply details for tracking and reporting.

Requirements

n8n account or self-hosted setup

Google Business Profile API access

Google Cloud Project with appropriate permissions

OpenRouter API key

Google Sheets API credentials

Setup Instructions

Clone this repository or import the workflow into your n8n instance.

Configure the Google Business Profile credentials in n8n.

Add your OpenRouter API key in the AI model node.

Connect Google Sheets with service account credentials.

Update your sheet structure with matching fields.

Activate the workflow and test using a sample review.
