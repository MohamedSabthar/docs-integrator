---
sidebar_position: 6
title: Configuration Panel
description: Configure projects, services, and functions through a unified configuration view.
slug: /editor/panels/configuration-panel
---

import ThemedImage from '@theme/ThemedImage';
import useBaseUrl from '@docusaurus/useBaseUrl';

# Configuration Panel

The Configuration Panel is the view that opens whenever you select **Configure** in the editor. It groups the settings that apply to the project, service, or function you're working on into a single form, so you can review and update them without editing source code. The panel adapts its content to the level you opened it from.

<ThemedImage
    alt="The HTTP Service Configuration view for the /tasks service, with HTTP Service and the taskListener listener under Attached Listeners on the left, and the Base Path and Service Configuration fields followed by the Configuration for taskListener section (Name, Port, and Host) on the right. Save Changes is at the top right."
    sources={{
        light: useBaseUrl('/img/editor/panels/configuration-panel/service-configuration-v1.0.png'),
        dark: useBaseUrl('/img/editor/panels/configuration-panel/service-configuration-v1.0.png'),
    }}
/>

## Where to open it

The level you open the Configuration Panel from determines which configuration it loads:

- **Project level**: select **Configure** at the top of the project home page, or hover over **Configurations** in the project explorer and select **View Configuration**.
- **Service level**: select **Configure** in the [Service Designer](../designers/service-designer.md) header.
- **Function level**: select **Configure** at the top of a function's flow.

## Configuration levels

The panel exposes configuration at three levels. Each level scopes the settings to the part of the project you opened it from.

### Project-level configurations

Apply to the entire project. The **Configurable Variables** view lists the configurable variables defined in the project, with each variable's type and default value, and the configurable variables of the libraries the project imports. Use this level for values that should be shared across all agents, entry points, and functions in the project and supplied through `Config.toml`.

### Service-level configurations

Apply only to the selected service. The form is split into the service's own settings and the configuration of every listener attached to it. For an HTTP service, this includes:

- **Base Path**: the path the service is exposed on.
- **Service Configuration**: advanced service-level options such as service-level security.
- **Configuration for `<listener>`**: the listener's own settings (for example, **Name**, **Port**, **Host**, **HTTP1 Settings**, **Secure Socket**, and **HTTP Version** for an HTTP listener), one block per attached listener.

The left pane lists the service and its **Attached Listeners** so you can jump straight to the block you want to edit.

### Function-level configurations

Use the same form you saw when you created the function. The form exposes:

- **Name** of the function.
- **Description** of the function.
- **public** checkbox, to make the function visible across the project.
- **Parameters** of the function.
- **Return Type** of the function.

## Saving changes

On the project and service levels, the panel stages your edits until you select **Save Changes** at the top right. **Save Changes** stays disabled until at least one field has been modified, so you can open the panel to inspect a configuration without risk of changing it. On the function level, select **Save** at the bottom of the form.

## What's next

- [Service Designer](../designers/service-designer.md): return to the service designer to manage resources and handlers.
- [Expression Panel](expression-panel.md): use configurable variables in expressions.
