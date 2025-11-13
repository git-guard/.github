# GitGuard

<div align="center">
  <img src="../gitguard-mascot.png" alt="GitGuard Mascot" width="200" />

  <p><strong>Comprehensive GitHub Security Scanning Platform</strong></p>
</div>

---

> Protecting your code, one repository at a time

Welcome to the official GitHub organization for **GitGuard** - a powerful GitHub security scanning platform that helps developers identify vulnerabilities, secrets, and security risks in their repositories.

## What We Build

GitGuard provides enterprise-grade security scanning for GitHub repositories with comprehensive analysis across multiple security dimensions.

### 🔒 Security Scanning Features

- **Vulnerability Detection** - Pattern-based static analysis for common security issues including XSS, SQL injection, command injection, and more
- **Secret Scanning** - Detects hardcoded API keys, tokens, passwords, private keys, and sensitive credentials (Premier tier)
- **Dependency Analysis** - Scans package.json and requirements.txt for known vulnerable dependencies with CVE tracking
- **License Compliance** - Identifies license compatibility issues and compliance risks in your dependencies
- **AI-Powered Analysis** - OpenAI integration for intelligent vulnerability assessment and remediation suggestions (Pro & Premier)
- **Enhanced Security Scoring** - Comprehensive security score calculation based on all findings
- **DDoS Testing** - Simulated DDoS attack testing to evaluate application resilience (Premier tier only)

### 🎯 Subscription Tiers

- **Free** - 5 daily scans, basic vulnerability detection
- **Pro** - 100 daily scans, AI-powered analysis, enhanced scanning, report exports (CSV, JSON, HTML)
- **Premier** - Unlimited scans, secret scanning, DDoS testing, continuous monitoring, webhook notifications, priority support

### 🚀 Key Capabilities

- **Real-time Progress** - Server-Sent Events (SSE) for live scan updates
- **Batch Scanning** - Scan multiple repositories simultaneously
- **GitHub App Integration** - Seamless webhook support for automatic scanning on push/PR events
- **Continuous Monitoring** - Automated cron-based scheduled scanning for your repositories
- **Rate Limit Management** - Intelligent GitHub token rotation to maximize API efficiency
- **GraphQL Optimization** - 90% reduction in GitHub API calls using GraphQL file fetching
- **Report Exports** - Download scan results in CSV, JSON, or HTML formats
- **Scan Sharing** - Share scan results publicly with optional password protection
- **Background Processing** - Asynchronous scanning via AWS SQS queue system
- **False Positive Management** - Mark and track false positives to reduce noise

## Get Started

- **Website:** [gitguard.net](https://gitguard.net)
- **Start Scanning:** Sign in with GitHub and scan your first repository in seconds
- **GitHub App:** Install the GitGuard GitHub App for continuous monitoring
- **Documentation:** Comprehensive guides in our repositories

## Our Repositories

### [app-git-guard](https://github.com/git-guard/app-git-guard)
The main GitGuard application built with Next.js 16, PostgreSQL, and TypeScript. Includes the complete security scanning engine, dashboard, API, and all core features.

## Technology Stack

- **Framework**: Next.js 16 with Turbopack
- **Language**: TypeScript
- **Database**: PostgreSQL with connection pooling
- **Authentication**: NextAuth.js v4 with GitHub OAuth
- **Payments**: Stripe subscription management
- **Email**: Resend for transactional emails
- **AI**: OpenAI API with Groq and Gemini fallbacks
- **Queue**: AWS SQS for background job processing
- **Background Worker**: EC2 t4g.micro instance with systemd service
- **Deployment**: AWS Amplify (web app) + EC2 (worker)
- **UI**: Material-UI (MUI) v6 with Next.js integration

## Architecture Highlights

- **60+ API endpoints** using Next.js App Router with file-based routing
- **Background processing** with dedicated EC2 worker polling SQS queue
- **Real-time updates** via Server-Sent Events for live scan progress
- **Intelligent rate limiting** with automatic GitHub token rotation
- **Security scanning engine** with modular scanner architecture:
  - Core vulnerability scanner
  - Secret scanner
  - Dependency scanner
  - License scanner
  - Enhanced scanner orchestrator
  - Security scoring system
- **Premium features** including DDoS testing simulator and continuous monitoring
- **Webhook delivery system** for scan notifications
- **Report export engine** supporting multiple formats

## For Developers

GitGuard is built with modern web technologies and follows best practices:

```bash
# Clone the repository
git clone https://github.com/git-guard/app-git-guard.git
cd app-git-guard

# Install dependencies
yarn install

# Set up environment variables
cp .env.example .env.local

# Run database migrations
psql $POSTGRES_URL < scripts/supabase-schema.sql

# Start development server
yarn dev
```

Visit the [main repository](https://github.com/git-guard/app-git-guard) for detailed setup instructions, architecture documentation, and contribution guidelines.

## Community & Support

- **GitHub Issues:** Report bugs and request features
- **GitHub Discussions:** Share ideas, ask questions, and get help
- **Documentation:** In-depth guides in individual repositories
- **Website Support:** Contact us through [gitguard.net](https://gitguard.net)

## Contributing

We welcome contributions! See CONTRIBUTING.md in individual repositories for guidelines on:
- Code style and standards
- Development workflow
- Testing requirements
- Pull request process

## Built By

GitGuard is built and maintained by developers who are passionate about security and code quality.

---

Made with security in mind for developers everywhere
