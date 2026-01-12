# Wazuh-MCP-Threat-Hunting-Demo
Demo of using MCP server for Wazuh to perform AI-assisted threat hunting.
# Wazuh MCP Threat Hunting Demo

## Project Overview (專案簡介)
This project demonstrates how to use the **Wazuh MCP Server** to integrate Wazuh logs with an LLM Agent. By using natural language via chat interfaces, we can perform threat hunting and query security alerts without manually navigating the Wazuh dashboard.

- **Tools Used:** Wazuh, MCP Server, [Mention your LLM tool, e.g., LangChain/Claude Desktop/OpenAI]
- **Target:** Detect Nmap scanning activity via Chat.

## Architecture (架構)
1. **Wazuh Manager:** Collects security logs and alerts.
2. **MCP Server:** Bridges the LLM with the Wazuh API.
3. **User Client:** Interacts with the system using natural language queries.

## Threat Hunting Demo (功能展示)

### Scenario: Detecting Network Scanning
I performed an Nmap scan against the Wazuh agent. Instead of checking the dashboard, I asked the AI Agent to identify threats.

#### 1. The Query (對話查詢)
Checking if any scanning activity was detected from a specific IP.

![Chat Screenshot](chat_screenshot.png)
*(Upload your chat screenshot and name it chat_screenshot.png)*

> **Observation:** The Agent successfully queried the Wazuh API and returned the specific alert regarding "ET SCAN Nmap".

#### 2. Verification in Wazuh (Wazuh 後台驗證)
Verifying the data in the Wazuh Dashboard.

![Wazuh Dashboard](wazuh_dashboard.png)
*(Upload your wazuh dashboard screenshot and name it wazuh_dashboard.png)*

## Conclusion
Using MCP protocol allows for rapid incident triage. The AI agent can effectively filter noise and present relevant security alerts from Wazuh.

## References
- [mcp-server-wazuh GitHub](https://github.com/gbrigandi/mcp-server-wazuh)
