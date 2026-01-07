# mcp-security-audit-demo
This project demonstrates a practical security audit of Model Context Protocol (MCP) usage in a local development environment.  The goal is to identify whether any MCP servers are present, understand where they are configured, and assess potential security risks — especially in environments using AI-assisted development tools.
# MCP Security Audit – Local Environment Demo

## Overview

This project demonstrates a practical security audit of Model Context Protocol (MCP) usage in a local development environment.

The goal is to identify whether any MCP servers are present, understand where they are configured, and assess potential security risks — especially in environments using AI-assisted development tools.

This demo was inspired by the MCP Security Fundamentals and MCP Audit tooling.

---

## Why This Matters

As MCP adoption grows across AI tools and developer environments, teams often ask:

- What MCP servers are already running on our machines?
- Are these MCPs intentional or accidental?
- Do any MCPs introduce security risks such as:
  - Tool poisoning
  - Prompt injection
  - API security gaps
  - Tool confusion
  - Supply chain attacks

This project focuses on answering those questions through hands-on auditing.

---

## Tools Used

- **MCP Audit CLI**
- Python 3 (virtual environment)
- Local macOS development environment

---

## Setup & Execution

### 1. Create and activate a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```
2. Install MCP Audit locally
```
pip install -e .
```
3. Run MCP scan
```
mcp-audit scan ```

Optional verbose scan:

```
mcp-audit scan --verbose
```
Results
The scan checked the following locations:

Claude Desktop configuration

Cursor configuration

VS Code (Continue extension)

Windsurf

Zed

Project-level MCP configs

Result:
No unintended or background MCP configurations were found.

This confirms that the local environment only contains MCPs that were intentionally enabled for controlled use cases (e.g., Playwright demo automation).

