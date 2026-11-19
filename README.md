<h1 align="center">Mona Gallery</h1>

<p align="center">
  <a href="#introduction">Introduction</a> •
  <a href="#prerequisites">Prerequisites</a> •
  <a href="#mona-gallery">Mona Gallery</a> •  
  <a href="#license">License</a> •
  <a href="#maintainers">Maintainers</a> •
  <a href="#support">Support</a> •
  <a href="#learning-resources">Learning Resources</a> •

</p>

## :octocat: Agenda

### Day 1

- [ ] What is GitHub Advanced Security?
- [ ] GitHub Advanced Security Licensing
- [ ] GHAS Enablement
- [ ] How does it work?
  - [ ] Dependancy Graph, Dependabot, Dependency Review
  - [ ] Secret Scanning
  - [ ] Code Scanning and CodeQL Default Setup
  - [ ] Code Scanning Autofix

Instructions for the hands-on exercises: [Developer Exercises - Day 1](exercises/developer-exercises-day1.md)

### Day 2

- [ ] How does it work?
  - [ ] CodeQL Advanced Setup
  - [ ] CodeQL Workflow optimization
  - [ ] Customizing CodeQL Configuration
  - [ ] Security Overview
  - [ ] Security Campaings
- [ ] Integrations - GHAS API and Webhooks
  - [ ] 3rd party tool integration
  - [ ] Secret Scanning alerts in PR
- [ ] Troubleshooting GHAS

Instructions for the hands-on exercises: [Developer Exercises - Day 2](exercises/developer-exercises-day2.md)

### Introduction

This repository contains the source code for the delibrately vulnerable `Mona Gallery` web application used for security training purposes.

### Prerequisites

If you want to run the `Mona Gallery` application, you will require Docker. You can run the application with a simple `docker compose up` command. For more information on ports and services see the [docker compose file](./docker-compose.yaml).

There are two users you can use to log into the app via OIDC integration. For details see [passwords file](./passwords.txt).

### Mona Gallery

The Mona Gallery is a delibrately vulnerable web application consisting of several prevalent vulnerability types, such as SQL injection, XSS, and deserialization, among others. The application's codebase is diverse, utilizing multiple technologies, including Go, Python, Javascript, and Java. A architecture diagram can be found below.  We will use this application's codebase for this workshop.

![mona-gallery](./repo-utils/images/app-demo.gif)

#### Architecture Diagram

The application's frontend is built with Vue.js 3 and Bootstrap 5, while authorization is managed through the Zitadel OIDC service implemented in Go. Middleware functions are handled in Python. The API is developed in Go, and Blob storage is implemented with MinIO, written in Java. Furthermore, the API layer is also implemented in Go, and the database relies on SQL Lite. Each of these services is encapsulated in its respective Docker container, resulting in a total of five images. To run the application, you can utilize Docker Compose.  

![image](./repo-utils/images/architecture-diagram.png)

## License

This project is licensed under the terms of the MIT open source license. Please refer to [MIT](./LICENSE.txt) for the full terms.

## Maintainers

See the [CODEOWNERS](./.github/CODEOWNERS) for the list of maintainers.

## Support

The support process is outlined in the [SUPPORT.md](./SUPPORT.md)

### Learning Resources

- [GitHub Advanced Security Learning Path - Microsoft Learn](https://learn.microsoft.com/en-us/collections/rqymc6yw8q5rey)
- [Docs - GitHub Advanced Security](https://docs.github.com/en/enterprise-cloud@latest/get-started/learning-about-github/about-github-advanced-security)
- [About code scanning](https://docs.github.com/en/github/finding-security-vulnerabilities-and-errors-in-your-code/about-code-scanning)
- [About Dependabot Alerts](https://docs.github.com/en/free-pro-team@latest/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies)
- [About secret scanning](https://docs.github.com/en/github/administering-a-repository/about-secret-scanning)
- [Events that trigger workflows](https://docs.github.com/en/free-pro-team@latest/actions/reference/events-that-trigger-workflows)
- [Configuring the CodeQL workflow for compiled languages](
https://docs.github.com/en/free-pro-team@latest/github/finding-security-vulnerabilities-and-errors-in-your-code/configuring-the-codeql-workflow-for-compiled-languages)
- [Configuring code scanning](https://docs.github.com/en/free-pro-team@latest/github/finding-security-vulnerabilities-and-errors-in-your-code/configuring-code-scanning)
- [Configuring notifications for Dependabot alerts](https://docs.github.com/en/free-pro-team@latest/github/managing-security-vulnerabilities/configuring-notifications-for-vulnerable-dependencies#configuring-notifications-for-dependabot-alerts)
- [Customizing dependency updates](https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/customizing-dependency-updates)
- [Dependabot rules](https://docs.github.com/en/enterprise-cloud@latest/code-security/dependabot/dependabot-auto-triage-rules/about-dependabot-auto-triage-rules)
- [Dependency Review](https://docs.github.com/en/enterprise-cloud@latest/code-security/supply-chain-security/understanding-your-software-supply-chain/about-dependency-review)
- [Configuration options for the dependabot.yml file](https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/configuration-options-for-dependency-updates)
- [Filter pattern cheat sheet](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions#filter-pattern-cheat-sheet)
- [Running additional queries](
https://docs.github.com/en/free-pro-team@latest/github/finding-security-vulnerabilities-and-errors-in-your-code/configuring-code-scanning#running-additional-queries)
- [Troubleshooting the CodeQL workflow](https://docs.github.com/en/free-pro-team@latest/github/finding-security-vulnerabilities-and-errors-in-your-code/troubleshooting-the-codeql-workflow)
- [Code Scanning Autofix](https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/responsible-use-autofix-code-scanning)
- [Security Overview](https://docs.github.com/en/enterprise-cloud@latest/code-security/security-overview/about-security-overview)
- [Security Campaings](https://docs.github.com/en/enterprise-cloud@latest/code-security/securing-your-organization/fixing-security-alerts-at-scale/creating-tracking-security-campaigns)
- [Code scanning API](https://docs.github.com/en/free-pro-team@latest/rest/reference/code-scanning)
- [Secret scanning API](https://docs.github.com/en/rest/reference/secret-scanning)
- [GraphQL API](https://docs.github.com/en/free-pro-team@latest/graphql)
  - [RepositoryVulnerabilityAlert](https://docs.github.com/en/free-pro-team@latest/graphql/reference/objects#repositoryvulnerabilityalert)
- [REST API](https://docs.github.com/en/free-pro-team@latest/rest)
