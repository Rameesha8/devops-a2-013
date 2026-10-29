# Assignment 2 Report

## Submission links

- GitHub repository: `PASTE_PUBLIC_GITHUB_REPOSITORY_URL`
- Docker Hub repository: `PASTE_DOCKER_HUB_REPOSITORY_URL`
- Successful workflow run: `PASTE_SUCCESSFUL_RUN_URL`
- Failed workflow run: `PASTE_FAILED_RUN_URL`

## Project overview

This project is a personal portfolio written with plain HTML and CSS. It is packaged as an Nginx Docker image so the same page can run consistently on any machine with Docker. GitHub Actions checks the page on each push and pull request, then builds and publishes the `latest` image tag only from the `main` branch.

## Evidence screenshots

Insert the following screenshots before exporting this report to PDF:

1. Git commit history showing at least five meaningful commits.
2. Merged `feature-endpoint` pull request.
3. Docker Hub tags page showing `manual` and `latest`.
4. One failed Actions run and one successful Actions run.
5. The portfolio running from the container at `http://localhost:8080`, with the address bar visible.

## Webhook observations

| Event | `X-GitHub-Event` header | `ref` field (push only) | Observation |
| --- | --- | --- | --- |
| Ping | `ping` | Not applicable | GitHub sent a test delivery after the webhook was created. |
| Push | `push` | `refs/heads/main` | Replace with the actual ref and delivery observation from webhook.site. |
| Pull request opened | `pull_request` | Not applicable | Replace with the actual action and observation from webhook.site. |

A webhook sends HTTP event notifications to the external URL chosen in repository settings. The GitHub Actions workflow runs jobs inside GitHub's automation service; here it validates the page, builds the image, and pushes to Docker Hub only for `main`.

## Problem and solution

Replace this paragraph with a real issue you encountered. Include the exact error message and explain the concrete action that solved it. Example: Docker reported `port is already allocated`; I stopped the earlier container with `docker rm -f devops-a2-page` and started the container again on port 8080.
