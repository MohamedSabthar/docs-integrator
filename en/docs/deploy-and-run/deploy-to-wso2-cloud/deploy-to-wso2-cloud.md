---
sidebar_position: 0
sidebar_label: Deploy to WSO2 Cloud
title: Deploy to WSO2 Cloud
description: Deploy an agentic integration, or a whole project, from WSO2 Agent Builder to WSO2 Cloud.
keywords: [wso2 agent builder, wso2 cloud, deploy, agentic integration, cloud deployment]
slug: /deploy-and-run/deploy-to-wso2-cloud
---

# Deploy to WSO2 Cloud

You can deploy your agents to WSO2 Cloud directly from WSO2 Agent Builder. WSO2 Cloud is a fully managed platform, so there's no infrastructure to set up. You can deploy a single agentic integration, or every agentic integration in a project at once.

WSO2 Cloud builds your agents from a Git repository. If your project isn't in a remote repository yet, WSO2 Agent Builder walks you through publishing it to GitHub as part of the deployment.

:::info Prerequisites
- A project with at least one agentic integration that has something to run: an [agent](../../develop-and-test/integration-artifacts/ai-integrations/agents/create-an-agent.md) with a trigger, or a [durable agent](../../develop-and-test/integration-artifacts/ai-integrations/agents/gated-tools-or-durable-agentic-workflow.md). Until it has one, **Deploy to WSO2 Cloud** is unavailable and shows "No deployable integration found".
- You're signed in to WSO2 Agent Builder. If you aren't, WSO2 Agent Builder prompts you to sign in when you deploy.
:::

## Deploy an agentic integration

1. Open the agentic integration's overview. To get there, select the agentic integration's name in the sidebar, or select its card on the project overview.
2. Select **Deploy** at the top right. The **Deploy** panel opens.
3. Expand **WSO2 Cloud**, then select **Deploy to WSO2 Cloud**.

    ![The Deploy panel on an agentic integration's overview, with WSO2 Cloud expanded and the Deploy to WSO2 Cloud button highlighted](/img/deploy-and-run/deploy-to-wso2-cloud/01-deploy-panel-v1.0.png)

4. When prompted, select your organization on WSO2 Cloud. Select an existing WSO2 Cloud project, or select **Create New** to create one.

    A new tab opens with the agentic integration to deploy.

5. If your project isn't connected to a remote repository yet, a warning appears. [Publish the project to GitHub](#publish-your-project-to-github), then return to this tab.
6. If WSO2 Cloud can't access your repository, a warning appears. Select **Grant Access**, authorize WSO2 on GitHub in the browser, then return to WSO2 Agent Builder and refresh the tab.
7. Select **Deploy**.

    WSO2 Cloud builds and deploys the agentic integration. When the deployment finishes, select **View project in console** to open it in WSO2 Cloud.

After the first deployment, the **WSO2 Cloud** section of the **Deploy** panel shows that the agentic integration is deployed:

- **Open in Console** opens it in WSO2 Cloud.
- If you have local changes, commit and push them to redeploy. **Open Source Control** takes you there.
- The refresh icon updates the deployment status.

## Deploy a whole project

To deploy every agentic integration in a project at once, start from the project overview.

1. Open the project overview. To get there, select the home icon at the top left of an agentic integration's overview.
2. Select **Deploy** at the top right, then select **Deploy to WSO2 Cloud**.

    ![The project overview's Deploy menu with Deploy to WSO2 Cloud highlighted](/img/deploy-and-run/deploy-to-wso2-cloud/02-project-deploy-menu-v1.0.png)

3. Follow steps 4 to 6 in [Deploy an agentic integration](#deploy-an-agentic-integration). The tab lists every agentic integration in the project, and all of them are selected by default. Clear the ones you don't want to deploy.
4. Select **Deploy All**. When the deployment finishes, select **View project in console**.

## Publish your project to GitHub

WSO2 Cloud deploys from a Git repository. If your project isn't in one yet, publish it from WSO2 Agent Builder:

1. Select **Source Control** in the Activity Bar on the left.
2. Select **Initialize Repository**. This creates a local Git repository in your project folder.
3. Enter a commit message and select **Commit**. When asked whether to stage all your changes, select **Yes**.
4. Select **Publish Branch**. If you aren't signed in to GitHub, WSO2 Agent Builder asks you to authorize access in the browser.
5. Choose a repository name, and choose whether it's public or private. WSO2 Agent Builder creates the repository on GitHub and pushes your project to it.

:::caution Keep secrets out of your repository
Your agentic integration's `Config.toml` can hold secrets, such as the access token for the Default WSO2 Model Provider. Add `Config.toml` to your `.gitignore` before you commit, and set those values in WSO2 Cloud instead.
:::

## Other ways to deploy

The **Deploy** panel also lets you package an agentic integration to run on your own infrastructure:

- **Docker Image**: **Build Image** builds a container image to run on Kubernetes or any container platform.
- **Virtual Machine**: **Build JAR** builds an executable JAR to run on any server with a Java runtime.

On the project overview, the same options are **Build Docker Image** and **Build Executable** in the **Deploy** menu.

## What's next

- <CloudDocsLink to="/manage/integrations">View and manage integrations</CloudDocsLink> — Check build and deployment status, and manage the lifecycle of what you deployed.
- <CloudDocsLink to="/manage/configurations/runtime-configurations">Runtime configurations</CloudDocsLink> — Set configurable values, such as API keys, for each environment.
- <CloudDocsLink to="/manage/configurations/security-configurations">Security configurations</CloudDocsLink> — Secure your agent's endpoints with API key or OAuth2 authentication.
- [Concepts](../../get-started/concepts/concepts.mdx) — Environments, promotion, and configurations.
