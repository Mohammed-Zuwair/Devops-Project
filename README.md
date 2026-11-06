
# DeployGuard
### A Quality-Gated CI/CD Pipeline with Automated Failure Detection and Recovery

## Project Overview
DeployGuard is a CI/CD automation project built using GitHub Actions. It validates website files, scans for exposed secrets, controls deployment through a safety gate, deploys the website to GitHub Pages, checks website health, and supports recovery to a previously working version.

## Objectives
- Automate website validation.
- Detect exposed secrets before deployment.
- Prevent deployment when validation fails.
- Automate production deployment.
- Verify website availability after deployment.
- Restore a known-good version through manual recovery.

## Technologies Used
- Git and GitHub
- GitHub Actions
- GitHub Pages
- YAML
- HTML and CSS
- Gitleaks
- Linux Shell Commands

## CI/CD Pipeline
1. Source code is pushed to GitHub.
2. Validation checks verify required files and HTML structure.
3. Gitleaks scans for exposed secrets.
4. Deployment safety gate authorizes the next stage only if validation succeeds.
5. Website is deployed to GitHub Pages.
6. Health check verifies the live website response.
7. Recovery workflow can manually restore a selected known-good commit.

## Failure Handling
If validation fails, dependent deployment jobs are skipped. This prevents an invalid version from being deployed.

The recovery workflow accepts a known-good commit SHA and redeploys that version. Recovery is manually triggered.

## Project Workflows
- `.github/workflows/deploy.yml` — Main CI/CD pipeline.
- `.github/workflows/recovery.yml` — Manual recovery workflow.

## Live Website
https://mohammed-zuwair.github.io/Devops-Project/

## Repository
https://github.com/Mohammed-Zuwair/Devops-Project

## Testing Performed
- Required file validation.
- HTML structure validation.
- CSS connection validation.
- Secret scanning.
- Deployment gate verification.
- Successful production deployment.
- Post-deployment health check.
- Simulated validation failure.
- Manual recovery deployment.

## Conclusion
DeployGuard demonstrates how quality checks, security scanning, controlled deployment, health monitoring, and recovery mechanisms can improve the reliability of a CI/CD pipeline.
