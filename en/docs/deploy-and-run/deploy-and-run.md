---
sidebar_position: 0
sidebar_label: Overview
title: Deploy and Run
description: Learn about the ways to deploy agents built in WSO2 Agent Builder, from WSO2 Cloud to your own infrastructure, and how to run them once they're live.
keywords: [wso2 agent builder, deployment, wso2 cloud, docker, virtual machine, integration control plane]
slug: /deploy-and-run
hide_table_of_contents: true
wide_layout: true
---

# Deploy and Run

Once your agent works in WSO2 Agent Builder, this section covers how to ship it and how to run it in production.

You deploy from the **Deploy** panel on an agentic integration's overview, or from the **Deploy** menu on the project overview.

## Deploy

Choose where your agents run. Where you deploy also decides how you [manage](../manage/manage.md) and [observe](../observe/observe.md) them.

<PaletteGrid>

<PaletteCard icon="agents" href="/deploy-and-run/deploy-to-agent-manager">
  <h3 class="palette-card-title">Deploy to WSO2 Agent Manager</h3>
  <ul class="palette-card-list">
    <li>Run and manage your organization's agents in one place</li>
    <li>Connect to your Agent Manager instance</li>
    <li>Builds from your GitHub repository</li>
  </ul>
</PaletteCard>

<PaletteCard icon="cloud" href="/deploy-and-run/deploy-to-wso2-cloud">
  <h3 class="palette-card-title">Deploy to WSO2 Cloud</h3>
  <ul class="palette-card-list">
    <li>Fully managed, with no infrastructure to set up</li>
    <li>Deploy one agentic integration or a whole project</li>
    <li>Builds from your Git repository</li>
  </ul>
</PaletteCard>

<PaletteCard icon="server">
  <h3 class="palette-card-title">Self-Hosted Deployment</h3>
  <p class="palette-card-desc">Package an agentic integration to run on infrastructure you manage.</p>
  <ul class="palette-card-list">
    <li><strong>Docker Image</strong>: a container image for Kubernetes or any container platform</li>
    <li><strong>Virtual Machine</strong>: an executable JAR for any server with a Java runtime</li>
  </ul>
</PaletteCard>

</PaletteGrid>

## Run in production

<PaletteGrid>

<PaletteCard icon="tools" href="/get-started/concepts">
  <h3 class="palette-card-title">Configurations and Secrets</h3>
  <ul class="palette-card-list">
    <li>Keep API keys and tokens out of your code</li>
    <li>Set values per environment</li>
  </ul>
</PaletteCard>

<PaletteCard icon="manage-observe" href="/manage">
  <h3 class="palette-card-title">Manage</h3>
  <ul class="palette-card-list">
    <li>Configuration and lifecycle of deployed agents</li>
    <li>Integration Control Plane</li>
  </ul>
</PaletteCard>

<PaletteCard icon="metrics" href="/observe">
  <h3 class="palette-card-title">Observe</h3>
  <ul class="palette-card-list">
    <li>Logs, metrics, and traces</li>
  </ul>
</PaletteCard>

</PaletteGrid>

## What's next

- [Deploy to WSO2 Agent Manager](deploy-to-agent-manager/deploy-to-agent-manager.md) — Deploy your agent to your Agent Manager instance.
- [Deploy to WSO2 Cloud](deploy-to-wso2-cloud/deploy-to-wso2-cloud.md) — Deploy your agent to the fully managed WSO2 Cloud.
- [Concepts](../get-started/concepts/concepts.mdx) — Deployment options, environments, and promotion.
