# Woven Record Media

A comprehensive video content creation and publishing platform that transforms raw uploads into multi-platform optimized content through automated processing, transcoding, and AI-powered analysis.

## 🎬 Active Repositories

### Core Video Processing Platform
- **[oneup-pipeline](https://github.com/woven-record-media/oneup-pipeline)** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
  - Production-ready AWS video processing pipeline for transcoding, transcription, and metadata creation
  - Transforms raw uploads into multi-platform optimized content (YouTube, Instagram, TikTok, Facebook)
  - Features: Content safety screening, automated transcoding, speech-to-text, AI analysis

### Backend Infrastructure  
- **[oneup-backend](https://github.com/woven-record-media/oneup-backend)** ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
  - High-performance Cloudflare Workers backend with Durable Objects
  - Provides infrastructure for OneUp Portal (excluding video processing pipeline)
  - Features: Social media OAuth, user management, file uploads

### Frontend Applications
- **[oneup-web-assets](https://github.com/woven-record-media/oneup-web-assets)** ![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=vue.js&logoColor=white)
  - Vue.js frontend web assets for OneUp platform
  - Creator-focused user interfaces for content management and publishing

### Web Presence
- **[the-woven-record](https://github.com/woven-record-media/the-woven-record)** ![HTML](https://img.shields.io/badge/HTML-E34F26?style=flat&logo=html5&logoColor=white)
  - Homepage for The Woven Record news site

## 🏗️ Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Video Processing** | Python + AWS | Pipeline for transcoding, transcription, AI analysis |
| **Backend API** | TypeScript + Cloudflare Workers | High-performance serverless backend with Durable Objects |
| **Frontend** | Vue.js | Creator-focused web applications |
| **Infrastructure** | Terraform + AWS/Cloudflare | Infrastructure as Code |

## 🔄 Developer Workflow

Our development process is optimized for working with Claude AI and follows a structured approach:

### Context Management
- Use `/clear` in Claude to start fresh between tasks or GitHub issues
- Reference documents with `@` symbol to add relevant context
- Focus on one task at a time to maintain accuracy

### Required Documents
Create and maintain these key documents in each repository:

- **`CLAUDE.md`** - Instructions for Claude on authentication, workflows, and restrictions
- **`ARCHITECTURE.md`** - System architecture, data flow diagrams, and component descriptions  
- **`spec/*.md`** - Detailed specifications for individual system components
- **`README.md`** - Human-readable documentation for setup and deployment

### Planning Workflow
1. **Create GitHub Issue** - Describe use case, desired outcome, and implementation approach
2. **Planning Mode** - Work with Claude to develop detailed implementation plan
3. **Save Plan** - Document plan in the GitHub issue
4. **Track Progress** - Update issues as work progresses

### GitHub Workflow
1. **Branch Protection** - Never edit files directly on main branch
2. **Issue → Plan → Branch** - Create new branch for each planned task
3. **Commits** - Have Claude handle commits with descriptive messages
4. **Pull Request** - Create as draft, get Copilot review, get `/security-review` address findings (write agents for this in the future)
5. **Documentation Updates** - Update ARCHITECTURE.md including diagrams, spec files, and README as needed
6. **Merge** - Merge to main after testing and documentation updates

### Best Practices
- **One Task Focus** - Complete one GitHub issue/task before starting another
- **Document Everything** - Keep design documents current with implementation
- **Test Before Deploy** - Validate all changes before merging
- **Review Process** - Use Copilot for PR reviews and address all findings

## 🚀 Getting Started

### For Video Processing (oneup-pipeline)
```bash
# Set up AWS credentials and environment
export AWS_PROFILE=your-profile
export STAGE=dev

# Use CLI tools for testing pipeline components
cd content_safety_screening/cli && python safety_screening_cli.py --interactive
cd transcoding && python transcoding_cli.py --interactive
```

### For Backend Development (oneup-backend)
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Deploy to Cloudflare Workers
npm run deploy
```

### Prerequisites
- **AWS CLI** - Configured with appropriate credentials
- **wrangler** - For Cloudflare deployments
- **Node.js** - For TypeScript/Vue.js development
- **Python** - For video processing pipeline
- **Terraform** - For infrastructure management

## 🎯 System Overview

The Woven Record Media platform processes content through several stages:

1. **Upload** → Content creators upload raw videos through web interface
2. **Safety Screening** → AI-powered content safety analysis with COPPA compliance
3. **Transcoding** → Multi-platform video optimization (YouTube, Instagram, TikTok)
4. **Transcription** → Speech-to-text conversion for accessibility and searchability
5. **AI Analysis** → Automated metadata generation and content optimization
6. **Publishing** → Multi-platform distribution with platform-specific formatting

---

## 📦 Archived Repositories

The following repositories are archived and no longer under active development:

- **oneup-portal** (Python) - Pipeline users portal (archived)
- **reach-everywhere-videos** (TypeScript) - Lovable portal landing page prototype (archived)
- **woven-record-media-web** (HTML) - Web assets for Woven Record Media (archived)
- **file-upload-frontend** (Python) - File upload webpage code (archived)
