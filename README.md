# Demo Company Go Monorepo

Since I am unable to attend the presentations, I’ve prepared a summary of my own hackathon project: exploring Backstage and generating code-first documentation.

## What is Backstage?
Backstage is an open-source developer portal created by Spotify that helps engineering teams manage their software infrastructure more efficiently. It provides a unified interface for discovering, documenting, and operating services, APIs, and libraries across a company. With built-in support for software catalogs, documentation and more. Backstage enables a “single pane of glass” experience for developers to streamline workflows and improve visibility into their systems.

## How does it work?

### Catalog
In Backstage, you can register various entities such as users, teams, projects, systems, and components. These entities can depend on one another, and Backstage builds a relationship graph from these links. This graph helps developers easily navigate the ecosystem, understand ownership, and visualize dependencies across the platform — making it simpler to manage complex architectures and responsibilities.

In our case, for example, Backstage can be extremely helpful for project managers by providing a clear overview of which services are located in which repositories — whether they are written in PHP, Go, or Python. This visibility makes it easier to track ownership, organize cross-team collaboration, and understand the tech stack distribution across the organization.

### Docs
Backstage also allows you to register documentation for individual components. With a simple annotation like `backstage.io/techdocs-ref: dir:.,` Backstage knows to automatically sync and monitor the documentation located within the component's directory. This enables teams to maintain code-first, decentralized documentation that is then centralized and searchable within the developer portal. As a result, everyone in the organization benefits from consistent, always-up-to-date docs — all in one place.

### Extensibility & Integrations
Backstage is highly extensible and can be used effectively even within private GitHub organizations. It supports a wide range of authentication providers (such as GitHub, GitLab, Google, Okta), and its flexible plugin architecture allows teams to integrate with tools like CI/CD pipelines, Kubernetes, monitoring dashboards, and more.

This means you can tailor Backstage to your organization’s ecosystem — whether that means showing deployment status from your CI, surfacing logs from your observability tools, or managing services running in your Kubernetes cluster — all within a unified interface.

## Live Demo

For the demo, I used a custom-built monorepo, which can be viewed at the following GitHub URL:
👉 https://github.com/kazmerdome/demo-company-go-monorepo

This project showcases the structure of a Go monorepository where various tools, services, and domain layers are maintained by different teams. To keep things simple, I created the following example teams for the demo:

- engineering-team
- product-team
- design-team
- monetization-team
- data-science-team

Each top-level directory in the repo represents a subservice. Every subservice contains a catalog-info.yaml file, which provides Backstage with the necessary metadata and information about that component. This file is also where service dependencies are declared.

📄 Example:
[cohort-worker catalog-info.yaml](https://github.com/kazmerdome/demo-company-go-monorepo/blob/main/cmd/cohort-worker/catalog-info.yaml)

Additionally, each subservice includes a /docs folder. The contents of this folder are automatically synced with Backstage, allowing centralized and searchable documentation to be generated for each component without any manual steps.

This repository is also registered in Backstage as a System entity under the name go-platform. Naturally, if we have other repositories, each of them can be registered under a different system name. This enables clear visibility across systems, allowing teams to understand how services are grouped and how they relate to one another — broken down per service, per system.

This logical separation is especially useful in large-scale environments, where multiple platforms or domains are managed independently but still need to interoperate.

### Run the demo

You can try the demo locally by following these two simple steps:

Step 1:
Run the Docker container:
```bash
docker run -it -p 7007:7007 kazmerdome/demo-backstage:latest
```

Step 2:
Open your browser and navigate to:
`http://localhost:7007`

This will launch the Backstage developer portal, preloaded with the demo catalog and synced documentation.

After that, you can start browsing the portal — I recommend checking out the Home and Docs sections in the sidebar.

If you have any questions, feel free to reach out!
