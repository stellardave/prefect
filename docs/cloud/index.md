---
description: Observe and orchestrate your workflow applications with the hosted Prefect Cloud platform.
tags:
    - UI
    - dashboard
    - orchestration
    - Prefect Cloud
    - accounts
    - teams
    - workspaces
    - PaaS
title: Prefect Cloud
search:
  boost: 2
---

# Welcome to Prefect Cloud

Prefect Cloud is a hosted workflow application framework that provides all the capabilities of the open-source Prefect server, plus the following:

!!! cloud-ad "Prefect Cloud features"
    - [User accounts](#user-accounts) &mdash; personal accounts for working in Prefect Cloud.
    - [Workspaces](/cloud/workspaces/) &mdash; isolated environments to organize your flows, deployments, and flow runs.
    - [Automations](/cloud/automations/) &mdash; configure triggers, actions, and notifications in response to real-time monitoring events.
    - [Email notifications](/cloud/automations/) &mdash; send email alerts from Prefect's server based on automation triggers.
    - [Service accounts](/cloud/users/service-accounts/) &mdash; configure API access for running workers or executing flow runs on remote infrastructure.
    - [Custom role-based access controls (RBAC)](/cloud/users/roles/) &mdash; assign users granular permissions to perform certain activities within an account or a workspace.
    - [Single Sign-on (SSO)](/cloud/users/sso/) &mdash; authentication using your identity provider.
    - [Audit Log](/cloud/users/audit-log/) &mdash; a record of user activities to monitor security and compliance.
    - Collaboration &mdash; invite other people to your account.
    - Error summaries  &mdash; (enabled by Marvin AI) distill the error logs of `Failed` and `Crashed` flow runs into actionable information.
    - [Push work pools](/guides/deployment/push-work-pools/) &mdash; run flows on your serverless infrastructure without running a worker.

![Viewing a workspace dashboard in the Prefect Cloud UI](/img/ui/cloud-dashboard.png)

!!! success "Getting Started with Prefect Cloud"
    If you're ready to start with Prefect Cloud, see the [Quickstart](/getting-started/quickstart/) and follow the instructions on the **Cloud** tabs to write and deploy your first Prefect Cloud-monitored flow run.

## User accounts

When you sign up for Prefect Cloud, an account and a user profile are automatically provisioned for you.

Your profile is where you manage your user settings, including:

- Profile, including profile handle and image
- API keys
- Preferences, including timezone and color mode

As an account Admin, you have access to the Account Settings page, which contains settings such as:

- Members
- Workspaces
- Roles

As an account Admin you can create a [workspace](#workspaces) and invite other individuals to your workspace.

Upgrading from a Prefect Cloud Free tier plan to a Pro or Custom tier plan enables additional functionality for adding workspaces, managing teams, and running higher volume workloads.

Workspace Admins for Pro tier plans can set [role-based access controls (RBAC)](#roles-and-custom-permissions), view [Audit Logs](#audit-log), and configure [service accounts](#service-accounts).

Custom plans have [object-level access control lists](/cloud/users/object-access-control-lists/), [custom roles](/cloud/users/roles/), [teams](/cloud/users/teams/), and [single sign-on (SSO)](#single-sign-on-(sso) with [Directory Sync/SCIM provisioning](/cloud/users/sso/#scim-provisioning).

!!! cloud-ad "Prefect Cloud plans for teams of every size"
    See the [Prefect Cloud plans](https://www.prefect.io/pricing/) for details on Pro and Custom account tiers.

## Workspaces

A workspace is an isolated environment within Prefect Cloud for your flows, deployments, and block configuration.
See [Workspaces](/cloud/workspaces/) for more information.

Each workspace keeps track of its own:

- [Flow runs](/concepts/flows/) and task runs executed in an environment that [syncs with the workspace](/cloud/workspaces/)
- [Flows](/concepts/flows/) associated with flow runs and deployments observed by the Prefect Cloud API
- [Deployments](/concepts/deployments/)
- [Work pools](/concepts/work-pools/)
- [Blocks](/concepts/blocks/) and [storage](/concepts/storage/)
- [Events](/cloud/events/)
- [Automations](/concepts/automations/)
- [Incidents](/cloud/incidents/)

![Viewing a workspace dashboard in the Prefect Cloud UI.](/img/ui/cloud-new-workspace.png)

## Events

Prefect Cloud allows you to see your [events](/cloud/events/). Use events to provide information about your workflows, or as [automation](/concepts/automations/) triggers.

![Prefect UI](/img/ui/event-feed.png)

## Automations

Prefect Cloud [automations](/concepts/automations/) provide additional notification capabilities beyond those in a self-hosted open-source Prefect server.
Automations also enable you to create event-driven workflows, toggle resources such as schedules and work pools, and declare incidents.

## Incidents <span class="badge pro"></span> <span class="badge custom"></span>

Prefect Cloud's [incidents](/cloud/incidents/) help teams identify, rectify, and document issues in mission-critical workflows.
Incidents are formal declarations of disruptions to a workspace.
With [automations](/cloud/incidents/#incident-automations), you can pause workspace activity when an incident is created, and resume it when it is resolved.

## Error summaries

Prefect Cloud error summaries, enabled by Marvin AI, distill the error logs of `Failed` and `Crashed` flow runs into actionable information.
To enable Marvin AI features, visit the **Settings** page for your account.

## Service accounts <span class="badge pro"></span> <span class="badge custom"></span>

Service accounts enable you to create Prefect Cloud API keys that are not associated with a user account.
Service accounts are typically used to configure API access for running workers or executing flow runs on remote infrastructure.
See the [service accounts](/cloud/users/service-accounts/) documentation for more information about creating and managing service accounts.

## Roles and custom permissions <span class="badge pro"> </span><span class="badge custom"></span>

Role-based access controls (RBAC) enable you to assign users a role with permissions to perform certain activities within an account or a workspace.
See the [role-based access controls (RBAC)](/cloud/users/roles/) documentation for more information about managing user roles in a Prefect Cloud account.

## Single Sign-on (SSO) <span class="badge pro"></span> <span class="badge custom"></span>

Prefect Cloud's [Pro and Custom plans](https://www.prefect.io/pricing) offer [single sign-on (SSO)](/cloud/users/sso/) authentication integration with your team’s identity provider.
You can set up SSO integration with identity providers that support OIDC and SAML.
Directory Sync and SCIM provisioning are also available with Custom plans.

## Audit log <span class="badge pro"></span> <span class="badge custom"></span>

Prefect Cloud's [Pro and Custom plans](https://www.prefect.io/pricing) offer [Audit Logs](/cloud/users/audit-log/) for compliance and security.
Audit logs provide a chronological record of activities performed by users in an account.

## Prefect Cloud REST API

The [Prefect REST API](/api-ref/rest-api/) communicates data from Prefect clients to Prefect Cloud, or a local Prefect server for orchestration and monitoring.
This API is mainly consumed by Prefect clients like the Prefect Python Client or the Prefect UI.

!!! note "Prefect Cloud REST API interactive documentation"
    Prefect Cloud REST API documentation is available at <a href="https://app.prefect.cloud/api/docs" target="_blank">https://app.prefect.cloud/api/docs</a>.

## Start using Prefect Cloud

To create an account or sign in with an existing Prefect Cloud account, go to [https://app.prefect.cloud/](https://app.prefect.cloud/).

Then follow the steps in the UI to deploy your first Prefect Cloud-monitored flow run. For more details, see the [Prefect Quickstart](/getting-started/quickstart/) and follow the instructions on the **Cloud** tabs.

!!! tip "Get help"
    Meet with a Prefect Product Advocate.
    [Book a Meeting](https://calendly.com/prefect-experts/prefect-product-advocates?utm_campaign=prefect_docs_cloud&utm_content=prefect_docs&utm_medium=docs&utm_source=docs).
