# DevOps Assignment 2 - Personal Portfolio

A plain HTML and CSS portfolio packaged with Nginx and checked, built, and published by GitHub Actions.

## Before publishing

1. Replace `YOUR NAME` and `YOUR-ROLL-NUMBER` in `index.html`.
2. Keep exactly one extra section based on the final roll-number digit:
   - `0-3`: Skills (already included)
   - `4-6`: Labs, with Git, GitHub, Docker, and Actions plus one line each
   - `7-9`: Contact, with your email address and GitHub profile link
3. Create public repository `devops-a2-YOUR-ROLL-NUMBER` and push this project.
4. In GitHub repository secrets, add `DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN` (a Docker Hub access token, never a password).

## Run locally

```powershell
docker build -t YOUR_DOCKERHUB_USERNAME/devops-a2:manual .
docker run -d -p 8080:80 --name devops-a2-page YOUR_DOCKERHUB_USERNAME/devops-a2:manual
```

Open http://localhost:8080. To stop and remove the container:

```powershell
docker rm -f devops-a2-page
```

## Docker Hub manual image

```powershell
docker login
docker push YOUR_DOCKERHUB_USERNAME/devops-a2:manual
```

## Required Git history

Make at least five meaningful commits. Create `feature-endpoint`, add the required extra section there, push it, open a pull request, then merge it into `main`. Keep one intentionally failed workflow run on a non-main branch and one successful run.

## Webhook

Create a webhook at `https://webhook.site`, then in GitHub select Settings > Webhooks > Add webhook. Use its unique URL, `application/json`, and choose the Push and Pull requests events. Record the observed requests in the report template.
