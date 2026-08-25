````markdown
# Task 1: Gitea Local Setup & Understanding

## Interview Explanation

The main goal of Task 1 was to understand the Gitea project structure, set up the required development environment, build Gitea from source, and run it locally without using Docker.

First, the official Gitea repository was forked to my GitHub account and cloned locally. The fork was configured as the `origin` remote and the official Gitea repository was added as `upstream`. A separate `gitea-task-1` branch was created for the work.

After cloning the project, the development documentation was reviewed to identify the required tools and versions. The environment was configured using MSYS2 UCRT64. The required tools were verified as:

- Go 1.27.0
- Node.js 24.15.0
- npm 11.12.1
- pnpm 11.22.0
- GNU Make 4.4.1

Some tools were initially available in Git Bash but not in the MSYS2 UCRT64 terminal, so the PATH configuration was adjusted and the tools were verified again.

The project dependencies were then installed and Gitea was built from source using:

```bash
make build
````

After the build completed successfully, Gitea was started locally using:

```bash
./gitea web
```

The application started successfully on:

```text
http://localhost:3000
```

The browser was then used to verify that the Gitea Initial Configuration page was loading correctly.

## Gitea Initial Configuration

The first screenshot shows the Initial Configuration page with the database and general configuration sections. This confirmed that the locally built Gitea application was running correctly and ready for initial configuration.

![Gitea Initial Configuration](./screenshots/task-1/01-initial-configuration.png)

The next screenshot shows the general server settings, including the local Gitea Base URL, log path, and optional settings.

![Gitea Server Configuration](./screenshots/task-1/02-server-configuration.png)

The final screenshot shows the repository root path, Git LFS path, running user, server domain, SSH port, and Gitea HTTP port. The application was configured for local development using `localhost` and port `3000`.

![Gitea Local Paths and Ports](./screenshots/task-1/03-local-paths-and-ports.png)

Docker was not used for this setup. The Gitea source repository's existing Docker-related files were left unchanged because they are part of the project source; the application itself was built and run directly from the local source.

## Git and PR Workflow

The work was kept on the `gitea-task-1` branch. After completing the task, the Task 1 documentation was added to the repository, committed, and pushed to my fork.

The pull request will be created from:

```text
Gilakarabhavish/gitea-project1
gitea-task-1
```

to:

```text
go-gitea/gitea
main
```

## Result

Gitea was successfully built from source and verified locally at `http://localhost:3000`. The development environment, project structure, Git workflow, and local Gitea setup were successfully understood and documented.

## Status

Task 1 completed successfully.

```
```
