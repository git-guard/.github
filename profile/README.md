# GitGuard

<div align="center">
  <img src="../gitguard-mascot.png" alt="GitGuard Mascot" width="200" />

  <p><strong>Comprehensive GitHub Security Scanning Platform</strong></p>
</div>

---

> Protecting your code, one repository at a time

Welcome to the official GitHub organization for **GitGuard** - a powerful GitHub security scanning platform that helps developers identify vulnerabilities, secrets, and security risks in their repositories.

## What We Build

GitGuard provides enterprise-grade security scanning for GitHub repositories:

- **Vulnerability Detection** - Pattern-based static analysis for common security issues
- **Secret Scanning** - Detects hardcoded API keys, tokens, and passwords
- **Dependency Analysis** - Scans package.json/requirements.txt for vulnerable dependencies
- **License Compliance** - Checks license compatibility and compliance
- **AI-Powered Analysis** - OpenAI integration for intelligent vulnerability assessment
- **Continuous Monitoring** - Automated scanning with webhook integration

## Subscription Tiers

- **Free** - 5 daily scans, basic scanning features
- **Pro** - 100 daily scans, AI-powered scanning, report exports
- **Premier** - Unlimited scans, DDoS testing, continuous monitoring, webhook notifications

## Key Features

- Real-time scan progress with Server-Sent Events (SSE)
- Batch scanning for multiple repositories
- GitHub App integration with webhook support
- Rate limit management with intelligent token rotation
- GraphQL-based file fetching (90% reduction in API calls)
- Export reports (CSV, JSON, HTML)
- Scan sharing with optional password protection

## Get Started

- **Try it free:** [gitguard.io](https://gitguard.io) *(or your actual domain)*
- **Documentation:** Check out our repositories for detailed guides
- **GitHub App:** Install the GitGuard GitHub App for continuous monitoring

## Our Repositories

### [app-git-guard](https://github.com/yourusername/app-git-guard)
The main GitGuard application built with Next.js 14, PostgreSQL, and TypeScript. Includes the security scanning engine, dashboard, and all core features.

## Technology Stack

- **Framework**: Next.js 16 with Turbopack
- **Language**: TypeScript
- **Database**: PostgreSQL
- **Authentication**: NextAuth.js
- **Payments**: Stripe
- **AI**: OpenAI API (with Groq and Gemini fallbacks)
- **Queue**: AWS SQS
- **Deployment**: AWS Amplify (web) + EC2 (worker)

## For Developers

GitGuard is built with modern web technologies and best practices:

```bash
# Clone the repository
git clone https://github.com/yourusername/app-git-guard.git

# Install dependencies
yarn install

# Set up environment variables
cp .env.example .env.local

# Start development server
yarn dev
```

Visit the [main repository](https://github.com/yourusername/app-git-guard) for detailed setup instructions.

## Architecture Highlights

- **60+ API endpoints** using Next.js App Router
- **Background processing** with EC2 worker and AWS SQS
- **Real-time updates** via Server-Sent Events
- **Rate limit management** with intelligent GitHub token rotation
- **Premium features** including DDoS testing and continuous monitoring

## Community

- **GitHub Issues:** Report bugs and request features
- **Discussions:** Share ideas and get help
- **Contributing:** See CONTRIBUTING.md in individual repositories

## Built By

GitGuard is built and maintained by developers who care about security.

---

Made with security in mind for developers everywhere
