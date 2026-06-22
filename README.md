# Release Information

- **Version**: 1.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: Analysis and Investigation

- **Verified with Models**: Fortinet FortiAI (AI model Large)

# Investigation Summarization Agent

Generates investigation summaries with final verdict, key findings, and recommended next steps based on gathered evidence and investigation results.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

**Required MCP Servers**: NA

<!-- > [!Note]
>
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.
>  -->

### Prerequisites

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
>
> FortiAI solution pack and Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.0`.
> 


## Input Parameters

The input must be provided as a JSON object.

| Parameter    | Description                                                                               |
|--------------|-------------------------------------------------------------------------------------------|
| `logs`       | Array of investigation logs containing question evaluations, findings, and step outcomes. |
| `hypotheses` | Array of investigation hypotheses requiring validation and evidence correlation.          |

## Response

The output is returned as a JSON object.

| Parameter            | Description                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------|
| `key_findings`       | Array of significant discoveries and critical evidence identified during investigation.       |
| `hypothesis_details` | Detailed analysis and validation status of investigation hypotheses with supporting evidence. |
| `verdict`            | Final determination of alert validity and threat classification.                              |
| `next_steps`         | Recommended actions and follow-up investigations based on investigation results.              |


