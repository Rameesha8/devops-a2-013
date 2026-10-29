# Assignment 2 submission checklist

## Account-side work still required

- [ ] Personalize `index.html` with your name and exact roll number.
- [ ] Select the correct extra section for your roll-number final digit.
- [ ] Create public GitHub repository `devops-a2-ROLL-NUMBER`.
- [ ] Make and push at least five meaningful commits.
- [ ] Use `feature-endpoint` for the extra-section change, open and merge its PR.
- [ ] Build, run, and check the Docker image at `http://localhost:8080`.
- [ ] Push `DOCKERHUB_USERNAME/devops-a2:manual`.
- [ ] Set `DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN` repository secrets.
- [ ] Preserve one failed non-main Actions run and one passed run.
- [ ] Add the webhook and trigger both Push and Pull request events.
- [ ] Add required screenshots and real URLs to `report-template.md`, then export it to PDF.

## Suggested commit sequence

1. `chore: initialize DevOps assignment repository`
2. `feat: add personal portfolio page`
3. `style: add responsive portfolio styling`
4. `build: containerize portfolio with nginx`
5. `ci: add Docker build and publish workflow`
6. `feat: add required portfolio section` (on `feature-endpoint`)
