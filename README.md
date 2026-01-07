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

```
python3 -m venv venv
source venv/bin/activate
```
2. Install MCP Audit locally
```
pip install -e .
```
3. Run MCP scan
```
mcp-audit scan
```

Optional verbose scan:

```
mcp-audit scan --verbose
```
## Results
The scan checked the following locations:

Claude Desktop configuration

Cursor configuration

VS Code (Continue extension)

Windsurf

Zed

Project-level MCP configs

## Result:
No unintended or background MCP configurations were found.

This confirms that the local environment only contains MCPs that were intentionally enabled for controlled use cases (e.g., Playwright demo automation).

## Key Takeaways

MCP Audit helps detect hidden or unintended MCP servers

Not all MCP usage is a security risk — context and intent matter

Running local audits is a simple but powerful security hygiene practice

MCP security should be part of developer and QA awareness, not just security teams

## Next Steps

Test against a demo repository with known MCP configurations

Integrate MCP audit checks into CI pipelines

Expand audits to team-wide environments

## References

MCP Security Fundamentals

MCP Audit Tool

---

## notes/findings.md 

## Findings Summary

- No hidden MCP servers detected
- All MCP usage was intentional and scoped
- Playwright-based MCP usage did not expose system-level risks
- MCP Audit is effective for awareness and early detection, not runtime enforcement

## My Achievements:
- No hidden MCP servers detected
- All MCP usage was intentional and scoped
- Playwright-based MCP usage did not expose system-level risks
- MCP Audit is effective for awareness and early detection, not runtime enforcement

### I intentionally used MCP for Playwright demo automation 
and then ran an MCP security audit to ensure there were no unintended or background MCP servers in my environment. 
This helped validate secure and transparent MCP usage


