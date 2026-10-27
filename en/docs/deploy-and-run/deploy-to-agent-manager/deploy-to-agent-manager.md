---
sidebar_position: 0
sidebar_label: Deploy to WSO2 Agent Manager
title: Deploy to WSO2 Agent Manager
description: Deploy an agentic integration from WSO2 Agent Builder to WSO2 Agent Manager.
keywords: [wso2 agent builder, wso2 agent manager, deploy, agentic integration]
slug: /deploy-and-run/deploy-to-agent-manager
---

# Deploy to WSO2 Agent Manager

You can deploy your agents to WSO2 Agent Manager directly from WSO2 Agent Builder. WSO2 Agent Manager runs and manages the agents in your organization, and collects their traces.

:::info Prerequisites
- An agentic integration with an [agent](../../develop-and-test/integration-artifacts/ai-integrations/agents/create-an-agent.md).
- Access to a WSO2 Agent Manager instance, and its console URL.
- Your project in a GitHub repository. WSO2 Agent Manager builds agents from GitHub only. To publish your project, see [Deploy to WSO2 Cloud](../deploy-to-wso2-cloud/deploy-to-wso2-cloud.md#deploy-an-agentic-integration), step 3.
:::

## Deploy an agentic integration

1. In WSO2 Agent Builder, open the agentic integration's overview. To get there, select the agentic integration's name in the sidebar.
2. Select **Deploy** at the top right. In the **Deploy** panel, expand **WSO2 Agent Manager** and select **Connect to Agent Manager**.

    ![The Deploy panel on an agentic integration's overview, with WSO2 Agent Manager expanded and the Connect to Agent Manager button highlighted](/img/deploy-and-run/deploy-to-agent-manager/01-deploy-panel-v1.0.png)

3. Enter your Agent Manager console URL and press **Enter**.

    ![The Connect to Agent Manager prompt asking for the Agent Manager Console URL](/img/deploy-and-run/deploy-to-agent-manager/02-console-url-v1.0.png)

    WSO2 Agent Builder opens your browser so you can sign in to Agent Manager.

{/* TODO: Verify the remaining steps against a running Agent Manager instance and add screenshots: sign in, select the organization, select or create a project ("Select Agent Manager Project (1/2)"), name the agent ("Agent Name (2/2)"), the "Create Agent in Agent Manager" form, and "Open in Agent Manager". */}

## What's next

- [Deploy to WSO2 Cloud](../deploy-to-wso2-cloud/deploy-to-wso2-cloud.md) — Deploy to the fully managed WSO2 Cloud instead.
- [Concepts](../../get-started/concepts/concepts.mdx) — Environments, promotion, and configurations.
