🔧 Chunk Content Structure
Each chunk contains multiple conversations in readable format:
=== Conversation Title (Date) ===### 🔧 Chunk Content Structure

Each chunk contains multiple conversations in readable format:
=== Conversation Title (Date) ===### 🔧 Chunk Content Structure
Each chunk contains multiple conversations in this format:
=== Conversation Title (Date) ===### 🔧 Chunk Content Structure

Each chunk contains multiple conversations in this format:
=== Conversation Title (Date) ===### 🔧 Chunk Content Structure
Each chunk contains multiple conversations in this format:
=== Conversation Title (Date) ===# ChatWeaver Text Extractor - User Manual
## Complete Guide to Secure AI Conversation Processing

**Version 2.0 - Secure Edition**  
**By Sentinel AI Systems**

---

## Table of Contents

1. [What is the Text Extractor?](#what-is-the-text-extractor)
2. [Key Features & Security](#key-features--security)
3. [Prerequisites](#prerequisites)
4. [Getting Started](#getting-started)
5. [Step-by-Step Usage Guide](#step-by-step-usage-guide)
6. [Upload Destinations Explained](#upload-destinations-explained)
7. [Chunking Strategies](#chunking-strategies)
8. [Security & Privacy](#security--privacy)
9. [Troubleshooting](#troubleshooting)
10. [Best Practices](#best-practices)
11. [FAQ](#faq)

---

## What is the Text Extractor?

The **ChatWeaver Text Extractor** is a secure, web-based tool designed to convert AI conversation exports into properly formatted text chunks for RememberAPI integration.

### Primary Purpose:
- **Converts complex JSON exports** into readable conversation text
- **Creates optimized chunks** for efficient API usage (5-20 pieces instead of thousands)
- **Provides multiple upload destinations** (Knowledge Bank, Core Memory, or Both)
- **Processes data locally** for maximum security and privacy

### Key Innovation:
Unlike basic file uploaders, this tool solves the specific problem of OpenAI's complex JSON structure that causes silent upload failures in RememberAPI.

---

## Key Features & Security

### 🔐 Security First Design
- **Local processing** - Your data never leaves your browser during extraction
- **No stored credentials** - Enter your own API keys each session
- **Direct transmission** - Credentials go straight to RememberAPI
- **Clear privacy notices** - Full transparency about data handling

### 🚀 Intelligent Processing
- **Smart JSON parsing** of OpenAI's nested structure
- **Optimized chunking** - Large chunks instead of thousands of tiny pieces
- **Multiple destinations** - Choose Knowledge Bank, Core Memory, or both
- **Progress tracking** with pause/resume capability

### 🎯 User Experience
- **Step-by-step guidance** throughout the process
- **Real-time file analysis** with detailed statistics
- **Input validation** and helpful error messages
- **Professional interface** with clear status updates

---

## Prerequisites

### Required Accounts:
1. **RememberAPI account** - Active subscription
2. **Knowledge Bank add-on** - For Knowledge Bank uploads ($15-45/month)
3. **API access** - Valid API key from RememberAPI dashboard

### System Requirements:
- **Modern web browser** (Chrome, Firefox, Edge, Safari)
- **JavaScript enabled** - Required for processing
- **Internet connection** - For uploads to RememberAPI
- **Local storage** - For conversation files (1-50MB typical)

### Supported File Types:
- **OpenAI exports** - conversations.json from ChatGPT data export
- **Claude exports** - Similar JSON structure from Anthropic
- **Compatible formats** - Other AI platforms with similar structure

---

## Getting Started

### Step 1: Obtain Conversation Export

#### **For OpenAI/ChatGPT:**
1. Log into your OpenAI account
2. Go to Settings → Data Controls
3. Click "Export Data"
4. Wait for email with download link
5. Download and extract `conversations.json`

#### **For Claude/Anthropic:**
1. Check available export options in account settings
2. Request conversation history export
3. Download the JSON file when ready

### Step 2: Set Up RememberAPI

#### **Get Your API Key:**
1. Log into RememberAPI.com
2. Navigate to Dashboard → API Keys
3. Generate new key or copy existing one
4. Keep this secure - you'll enter it in the tool

#### **Verify Service Access:**
1. Confirm Knowledge Bank add-on is active (if using)
2. Check your current API quota and usage
3. Review your subscription limits

### Step 3: Access the Tool
1. Download the HTML file from the GitHub repository
2. Save to a convenient location (Desktop, Documents)
3. Double-click to open in your web browser
4. Verify JavaScript is enabled

---

## Step-by-Step Usage Guide

### Phase 1: File Analysis
1. **Select File**: Click "Select your conversations.json file"
2. **Navigate**: Browse to your downloaded export file
3. **Analyze**: Tool automatically analyzes and displays:
   - Total conversations found
   - Message count across all conversations
   - Estimated word count for processing
   - File size and structure information
   - Preview of chunking options

### Phase 2: Configure Processing
1. **Choose Chunking Strategy**:
   - **10 Large Chunks** (Recommended) - ~4K conversations each
   - **5 Massive Chunks** - Fewer API calls, larger content
   - **20 Medium Chunks** - More granular organization
   - **Custom** - Specify 1-50 chunks exactly

2. **Timestamp Settings**:
   - **Include timestamps** - Adds conversation dates to text
   - **Content only** - Just message text without dates

### Phase 3: Text Extraction
1. **Start Processing**: Click "🔧 Extract & Process Text"
2. **Monitor Progress**: Watch real-time processing updates
3. **Review Results**: Examine the summary showing:
   - Number of chunks successfully created
   - Total conversations and words processed
   - Exact API call count for upload

### Phase 4: Upload Configuration
1. **Enter Credentials**:
   - **API Key** - Your RememberAPI key (starts with 'sk-')
   - **User ID** - Consistent identifier (name, email, etc.)

2. **Select Destination**:
   - **Knowledge Bank** - Document storage (Recommended)
   - **Core Memory** - Personal context (Limited to 50 conversations)
   - **Both Systems** - Maximum coverage (High API usage)

3. **Content Settings**:
   - **Title** - Descriptive name for your content
   - **Tags** - Keywords for organization (comma-separated)

### Phase 5: Upload Process
1. **Initiate Upload**: Click "📤 Upload to RememberAPI"
2. **Confirm Action**: Review and confirm the upload parameters
3. **Monitor Progress**: Track real-time upload status
4. **Manage Process**: Use pause button if needed to stop
5. **Review Results**: Check final success/error summary

### Phase 6: Verification
1. **Check Dashboard**: Log into RememberAPI to verify uploads
2. **Test Retrieval**: Use API or dashboard to query your content
3. **Validate Content**: Ensure conversations are searchable and accessible

---

## Upload Destinations Explained

### 🗃️ Knowledge Bank (Recommended)

#### **What it does:**
- Stores conversation chunks as searchable documents
- Uses RememberAPI's SliceDiceChunk engine for processing
- Creates knowledge entries accessible via `/v1/knowledge/get`
- Optimized for large-scale content storage

#### **Best for:**
- Complete conversation archives
- Searchable knowledge bases
- Reference material storage
- Long-term content preservation

#### **API Usage:** 1 call per chunk (typically 5-20 calls)
#### **Requirements:** Knowledge Bank add-on subscription
#### **Processing Time:** Fast, efficient bulk uploads

### 🧠 Core Memory (Personal Context)

#### **What it does:**
- Processes individual conversations for personalized AI context
- Creates memory entries through `/v1/remember` endpoint
- Focuses on user preferences and important interactions
- Limited to 50 conversations to prevent API overuse

#### **Best for:**
- Personal AI customization
- Key conversation highlights
- User preference storage
- Important context preservation

#### **API Usage:** 1+ calls per conversation (potentially 100+ calls)
#### **Limitations:** 50 conversation maximum for safety
#### **Processing Time:** Slower due to individual processing

### 🔄 Both Systems (Maximum Coverage)

#### **What it does:**
- Uploads all chunks to Knowledge Bank first
- Then processes limited conversations for Core Memory
- Provides comprehensive coverage of both storage types

#### **Best for:**
- Users who want maximum functionality
- Small to medium datasets (under 1K conversations)
- Accounts with high API quotas

#### **API Usage:** Knowledge Bank calls + Core Memory calls (highest usage)
#### **Considerations:** Monitor quotas carefully, extended processing time

---

## Chunking Strategies

### 🎯 Strategy Comparison

| Strategy | Chunks | Conversations/Chunk | API Calls | Best For |
|----------|--------|-------------------|-----------|----------|
| **5 Massive** | 5 | ~8,000 each | 5 calls | Minimal API usage |
| **10 Large** | 10 | ~4,000 each | 10 calls | **Recommended** |
| **20 Medium** | 20 | ~2,000 each | 20 calls | Granular retrieval |
| **Custom** | Your choice | Variable | Variable | Specific needs |

### 💡 Choosing the Right Strategy

#### **For Large Archives (10K+ conversations):**
- **Use 5 or 10 chunks** - Minimizes API costs
- **Larger context** per chunk for better retrieval
- **Most efficient** for bulk storage

#### **For Medium Archives (1K-10K conversations):**
- **Use 10 or 20 chunks** - Good balance
- **Reasonable API usage** with good organization
- **Optimal for most users**

#### **For Small Archives (<1K conversations):**
- **Use 20 chunks or custom** - More granular control
- **API usage less of a concern** with smaller datasets

### 🔧 Chunk Content Structure

Each chunk contains multiple conversations in this format:
=== Conversation Title (Date) ===# ChatWeaver Text Extractor - User Manual
Complete Guide to Secure AI Conversation Processing
Version 2.0 - Secure Edition
By Sentinel AI Systems

Table of Contents

What is the Text Extractor?
Key Features & Security
Prerequisites
Getting Started
Step-by-Step Usage Guide
Upload Destinations Explained
Chunking Strategies
Security & Privacy
Troubleshooting
Best Practices
FAQ


What is the Text Extractor?
The ChatWeaver Text Extractor is a secure, web-based tool designed to convert AI conversation exports into properly formatted text chunks for RememberAPI integration.
Primary Purpose:

Converts complex JSON exports into readable conversation text
Creates optimized chunks for efficient API usage (5-20 pieces instead of thousands)
Provides multiple upload destinations (Knowledge Bank, Core Memory, or Both)
Processes data locally for maximum security and privacy

Key Innovation:
Unlike basic file uploaders, this tool solves the specific problem of OpenAI's complex JSON structure that causes silent upload failures in RememberAPI.

Key Features & Security
🔐 Security First Design

Local processing - Your data never leaves your browser during extraction
No stored credentials - Enter your own API keys each session
Direct transmission - Credentials go straight to RememberAPI
Clear privacy notices - Full transparency about data handling

🚀 Intelligent Processing

Smart JSON parsing of OpenAI's nested structure
Optimized chunking - Large chunks instead of thousands of tiny pieces
Multiple destinations - Choose Knowledge Bank, Core Memory, or both
Progress tracking with pause/resume capability

🎯 User Experience

Step-by-step guidance throughout the process
Real-time file analysis with detailed statistics
Input validation and helpful error messages
Professional interface with clear status updates


Prerequisites
Required Accounts:

RememberAPI account - Active subscription
Knowledge Bank add-on - For Knowledge Bank uploads ($15-45/month)
API access - Valid API key from RememberAPI dashboard

System Requirements:

Modern web browser (Chrome, Firefox, Edge, Safari)
JavaScript enabled - Required for processing
Internet connection - For uploads to RememberAPI
Local storage - For conversation files (1-50MB typical)

Supported File Types:

OpenAI exports - conversations.json from ChatGPT data export
Claude exports - Similar JSON structure from Anthropic
Compatible formats - Other AI platforms with similar structure


Getting Started
Step 1: Obtain Conversation Export
For OpenAI/ChatGPT:

Log into your OpenAI account
Go to Settings → Data Controls
Click "Export Data"
Wait for email with download link
Download and extract conversations.json

For Claude/Anthropic:

Check available export options in account settings
Request conversation history export
Download the JSON file when ready

Step 2: Set Up RememberAPI
Get Your API Key:

Log into RememberAPI.com
Navigate to Dashboard → API Keys
Generate new key or copy existing one
Keep this secure - you'll enter it in the tool

Verify Service Access:

Confirm Knowledge Bank add-on is active (if using)
Check your current API quota and usage
Review your subscription limits

Step 3: Access the Tool

Download the HTML file from the GitHub repository
Save to a convenient location (Desktop, Documents)
Double-click to open in your web browser
Verify JavaScript is enabled


Step-by-Step Usage Guide
Phase 1: File Analysis

Select File: Click "Select your conversations.json file"
Navigate: Browse to your downloaded export file
Analyze: Tool automatically analyzes and displays:

Total conversations found
Message count across all conversations
Estimated word count for processing
File size and structure information
Preview of chunking options



Phase 2: Configure Processing

Choose Chunking Strategy:

10 Large Chunks (Recommended) - ~4K conversations each
5 Massive Chunks - Fewer API calls, larger content
20 Medium Chunks - More granular organization
Custom - Specify 1-50 chunks exactly


Timestamp Settings:

Include timestamps - Adds conversation dates to text
Content only - Just message text without dates



Phase 3: Text Extraction

Start Processing: Click "🔧 Extract & Process Text"
Monitor Progress: Watch real-time processing updates
Review Results: Examine the summary showing:

Number of chunks successfully created
Total conversations and words processed
Exact API call count for upload



Phase 4: Upload Configuration

Enter Credentials:

API Key - Your RememberAPI key (starts with 'sk-')
User ID - Consistent identifier (name, email, etc.)


Select Destination:

Knowledge Bank - Document storage (Recommended)
Core Memory - Personal context (Limited to 50 conversations)
Both Systems - Maximum coverage (High API usage)


Content Settings:

Title - Descriptive name for your content
Tags - Keywords for organization (comma-separated)



Phase 5: Upload Process

Initiate Upload: Click "📤 Upload to RememberAPI"
Confirm Action: Review and confirm the upload parameters
Monitor Progress: Track real-time upload status
Manage Process: Use pause button if needed to stop
Review Results: Check final success/error summary

Phase 6: Verification

Check Dashboard: Log into RememberAPI to verify uploads
Test Retrieval: Use API or dashboard to query your content
Validate Content: Ensure conversations are searchable and accessible


Upload Destinations Explained
🗃️ Knowledge Bank (Recommended)
What it does:

Stores conversation chunks as searchable documents
Uses RememberAPI's SliceDiceChunk engine for processing
Creates knowledge entries accessible via /v1/knowledge/get
Optimized for large-scale content storage

Best for:

Complete conversation archives
Searchable knowledge bases
Reference material storage
Long-term content preservation

API Usage: 1 call per chunk (typically 5-20 calls)
Requirements: Knowledge Bank add-on subscription
Processing Time: Fast, efficient bulk uploads
🧠 Core Memory (Personal Context)
What it does:

Processes individual conversations for personalized AI context
Creates memory entries through `/v1/
