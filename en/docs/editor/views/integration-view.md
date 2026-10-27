---
sidebar_position: 2
title: Integration View
description: Work with the Integration view to build and manage individual integrations.
keywords: [wso2 agent builder, editor, integration view, design canvas, deployment]
slug: /editor/views/integration-view
---

import ThemedImage from '@theme/ThemedImage';
import useBaseUrl from '@docusaurus/useBaseUrl';

# Integration View

The Integration view is the primary development interface in WSO2 Agent Builder. Use it to build, test, and deploy a single integration. It combines a project explorer, a visual design canvas, and deployment options in one unified workspace.

<ThemedImage
    alt="Integration view overview"
    sources={{
        light: useBaseUrl('/img/editor/views/integration-view/overview-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/integration-view/overview-v5.1.png'),
    }}
/>

## Design canvas

The design canvas is the central area of the Integration view. It opens on the **Agent Overview**, which shows the agents and workflows in your integration and the triggers that start them. Select an agent card to open that agent's own canvas, where you can add a trigger, memory, and tools, and see the model provider the agent uses.

<ThemedImage
    alt="Design canvas"
    sources={{
        light: useBaseUrl('/img/editor/views/integration-view/design-canvas-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/integration-view/design-canvas-v5.1.png'),
    }}
/>

### Service diagram

The service diagram renders your integration as an interactive graph. Each node represents a component:

- **Entry points** appear as the primary nodes on the left.
- **Listeners** connect to the entry points they serve.
- **External connections** appear on the right, showing which services your integration calls.
- **Lines** between nodes indicate data flow and dependencies.

Click any node to open that component in the visual designer. Right-click a node or click its three-dot menu (**⋮**) to access context actions such as **Edit** and **Delete**.

### Zoom and navigation controls

Use the controls in the bottom-left corner of the canvas to adjust the view:

- **+**: zoom in.
- **−**: zoom out.
- **Fit to screen**: automatically adjusts the zoom level to show all nodes.

You can also scroll to zoom and drag to pan across the canvas.

### Build with Copilot

Describe what you want in natural language, and [WSO2 Agent Builder Copilot](../copilot/copilot.md) generates the agent for you.

- **New integration**: The canvas shows the Copilot composer, which asks **What should your agent do?** Describe what you want your agent to do and send it, or pick one of the examples under **Examples**. To build it yourself instead, select **Add an agent manually** or **Add an MCP Server manually**.

  <ThemedImage
      alt="The Copilot composer on the overview of a new integration."
      sources={{
          light: useBaseUrl('/img/editor/copilot/copilot-composer.png'),
          dark: useBaseUrl('/img/editor/copilot/copilot-composer.png'),
      }}
  />

- **Integration with agents**: Select the Copilot orb in the bottom-right corner of the canvas. Select it once for a quick chat, or double-click it to open the full Copilot panel.

  <ThemedImage
      alt="The WSO2 Agent Builder Copilot orb on the integration overview."
      sources={{
          light: useBaseUrl('/img/editor/copilot/copilot-orb.png'),
          dark: useBaseUrl('/img/editor/copilot/copilot-orb.png'),
      }}
  />

### Add agents and MCP servers

Use the buttons at the top right of the **Agent Overview** to add to your integration:

- **+ Add Agent**: adds an AI agent.
- **+ Add MCP**: adds an MCP server.

On a new integration, the Copilot composer offers the same options as **Add an agent manually** and **Add an MCP Server manually**. See [Build with Copilot](#build-with-copilot).

## Toolbar

The toolbar sits at the top of the Integration view and provides quick access to common actions for configuring, running, and deploying your integration.

<ThemedImage
    alt="Toolbar"
    sources={{
        light: useBaseUrl('/img/editor/views/integration-view/toolbar-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/integration-view/toolbar-v5.1.png'),
    }}
/>

| Action | Description |
|---|---|
| **Undo** / **Redo** | Reverses or reapplies recent changes. Works across both the visual designer and the code editor. |
| **Configure** | Opens the configuration panel, equivalent to adding a configuration from the project explorer. |
| **Tracing** | Shows whether tracing is on for the integration (for example, **Tracing: Off**). Select it to turn tracing on or off. |
| **Run** | Builds and runs your integration locally. WSO2 Agent Builder compiles the Ballerina code, starts the services, and displays the output in the terminal panel. |
| **Deploy** | Shows or hides the deployment options panel on the right side of the view. |

## Deployment options panel

Select **Deploy** in the toolbar to open the deployment options panel on the right side of the view. The panel provides shortcuts to deploy the integration to different environments. Select **Deploy** again to close it.

<ThemedImage
    alt="Deployment button in the toolbar"
    sources={{
        light: useBaseUrl('/img/editor/views/integration-view/deployment-button-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/integration-view/deployment-button-v5.1.png'),
    }}
/>

<ThemedImage
    alt="Deployment options"
    sources={{
        light: useBaseUrl('/img/editor/views/integration-view/deployment-options-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/integration-view/deployment-options-v5.1.png'),
    }}
/>

| Option | Target |
|---|---|
| [**WSO2 Cloud**](../../deploy-and-run/deploy-to-wso2-cloud/deploy-to-wso2-cloud.md) | Fully managed cloud platform for hosting and running integrations. Select **Deploy to WSO2 Cloud** to start. |
| [**Docker Image**](product://integrator/deploy-and-run/self-hosted/containerized-deployment) | Build Docker images and deploy integrations to Docker, Kubernetes, or OpenShift. |
| [**Virtual Machine**](product://integrator/deploy-and-run/self-hosted/vm-deployment) | Deploy integrations as standalone JAR files on virtual machines. |

The panel also includes an **Integration Control Plane** section for monitoring and managing running integrations from a centralized dashboard. Select **Enable ICP Monitoring** to activate the [Integration Control Plane (ICP)](../integration-control-plane.md) for this integration, or expand **Publish to Local ICP** to push the integration to a local ICP instance.

## What's next

- [Flow Canvas](../canvases/flow-canvas/flow-canvas.md) — Build logic using the visual designer.
- [Integration artifacts](../../develop-and-test/integration-artifacts/integration-artifacts.md) — Learn about artifact types and their configuration.
- [Deploy to WSO2 Cloud](../../deploy-and-run/deploy-to-wso2-cloud/deploy-to-wso2-cloud.md) — Deploy your integration to the cloud.
