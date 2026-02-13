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

### Advanced Security Tools (New)

- **CVSS 3.1 Scoring** - Industry-standard vulnerability scoring with base, temporal, and environmental metrics (Pro/Premier)
- **API Security Scanner** - Analyzes OpenAPI/Swagger and GraphQL schemas for security misconfigurations (Premier)
- **Vulnerability Validation** - Confidence scoring (0-100%) with false positive detection and proof-of-concept generation (Pro/Premier)
- **Compliance Reporting** - Generate compliance reports mapped to industry frameworks:
  - OWASP Top 10 (Web Application Security)
  - PCI-DSS 4.0 (Payment Card Industry)
  - SOC 2 (Service Organization Controls)
  - HIPAA (Healthcare)
  - CIS Controls (Security Best Practices)

### 🎯 Subscription Tiers

- **Free** - 5 scans per day, basic vulnerability detection (50+ patterns)
- **Pro** - 100 scans per day, everything in Free plus AI-powered analysis, enhanced scanning, report exports (CSV, JSON, HTML)
- **Premier** - Unlimited scans, all features enabled by default (AI analysis, dependency scanning, secret detection), DDoS testing, continuous monitoring, webhook notifications, priority support

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
The main GitGuard web application built with Next.js 16, PostgreSQL, and TypeScript. Includes the complete security scanning engine, dashboard, API, and all core features. Accessible at [gitguard.net](https://gitguard.net).

### [gitguard-cli](https://github.com/git-guard/gitguard-cli)
Command-line security scanner for developers. Scan your code locally before deployment with support for 50+ vulnerability patterns across 12+ programming languages.

**Key Features:**
- **Smart Preference Syncing** - Automatically uses your web app settings (AI, dependencies, secrets)
- **Browser-based Authentication** - Secure OAuth flow with long-lived tokens
- **Override Flags** - Force-enable or disable features per scan (`--ai`, `--no-ai`, etc.)
- **GitIgnore Support** - Respects `.gitignore` patterns to avoid uploading excluded files
- **CI/CD Ready** - Exit codes for pipeline integration, JSON output support
- **Cross-platform** - Works on macOS, Linux, Windows

**New CLI Options:**
- `--cvss` - Enable CVSS 3.1 vulnerability scoring
- `--api-security` - Scan API specifications for security issues
- `--validate` - Enable vulnerability validation with confidence scoring
- `--compliance <framework>` - Generate compliance report (owasp, pci-dss, soc2, hipaa, cis, all)

**Installation:**
```bash
npm install -g @gitguard/cli
gitguard login
gitguard scan
```

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

GitGuard is built with modern web technologies and follows best practices. If you're interested in contributing or learning more about our architecture, please reach out to us at support@gitguard.net.

### Quick Start with CLI

```bash
# Install the CLI
npm install -g @gitguard/cli

# Authenticate
gitguard login

# Scan your project
gitguard scan

# Check your account
gitguard whoami
```

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
