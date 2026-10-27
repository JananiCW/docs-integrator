---
sidebar_position: 1
title: Project View
description: Manage projects with multiple integrations and libraries in WSO2 Agent Builder.
keywords: [wso2 agent builder, editor, project view, integrations, libraries]
slug: /editor/views/project-view
---

import ThemedImage from '@theme/ThemedImage';
import useBaseUrl from '@docusaurus/useBaseUrl';

# Project View

The Project view is the top-level view in WSO2 Agent Builder. It appears when you open a project that contains multiple integrations or libraries, giving you an overview of everything in the project, deployment options, and project-level actions in one place.

<ThemedImage
    alt="Project view overview"
    sources={{
        light: useBaseUrl('/img/editor/views/project-view/overview-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/project-view/overview-v5.1.png'),
    }}
/>

## Project overview canvas

The project overview canvas is the central area of the Project view. It displays the project name as a heading and provides a unified dashboard for managing all integrations and libraries in the project.

<ThemedImage
    alt="Project overview canvas"
    sources={{
        light: useBaseUrl('/img/editor/views/project-view/project-overview-canvas-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/project-view/project-overview-canvas-v5.1.png'),
    }}
/>

### Integrations and libraries

The **Agentic Integrations & Libraries** section displays a card grid showing each integration and library in the project. Each card shows:

- The name (for example, `AIAgent` or `Commons`).
- The agents it contains, such as `Wso2AgentAssistant`. A library card also shows a `Library` badge, followed by any agent definitions it provides, such as `CustomerSupportAgent`.

Click any card to navigate to the [Integration view](integration-view.md) or [Library view](library-view.md), where you can build and manage its artifacts.

### Add integration or library

Click the **+ Add** button at the top of the canvas to add a new integration or library to the project. Select the type, provide a name and configuration, and the new entry appears in the card grid and project explorer.

## Deployment options panel

The deployment options panel appears on the right side of an integration's overview when you select **Deploy**. It groups the ways to deploy the integration under **Deploy**, and the ways to monitor and manage it after deployment under **Management**.

<ThemedImage
    alt="Deployment options"
    sources={{
        light: useBaseUrl('/img/editor/views/project-view/deployment-options-v5.1.png'),
        dark: useBaseUrl('/img/editor/views/project-view/deployment-options-v5.1.png'),
    }}
/>

| Option | Target |
|---|---|
| [**Deploy to WSO2 Cloud**](../../deploy-and-run/deploy-to-wso2-cloud/deploy-to-wso2-cloud.md) | Fully managed cloud platform for hosting and running integrations. |
| [**Deploy with Docker**](product://integrator/deploy-and-run/self-hosted/containerized-deployment) | Build Docker images and deploy integrations to Docker, Kubernetes, or OpenShift. |
| [**Deploy on a VM**](product://integrator/deploy-and-run/self-hosted/vm-deployment) | Deploy integrations as standalone JAR files on virtual machines. |
| [**Integration Control Plane (ICP)**](product://integrator/icp) | Monitor and manage running integrations from a centralized dashboard. |

At the project level, click **Enable ICP for all integrations** to activate ICP monitoring for every integration in the project at once.




## What's next

- [Integration view](integration-view.md) — The primary development interface for individual integrations.
- [Library view](library-view.md) — Build and manage reusable libraries.
