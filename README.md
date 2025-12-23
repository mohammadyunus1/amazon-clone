# Amazon Clone – CI/CD on AWS

Live demo: http://amazon-clone-frontend-yunus.s3-website.eu-north-1.amazonaws.com  

## Overview
Full stack Amazon‑style storefront deployed through a fully automated CI/CD pipeline on AWS. Source is hosted on GitHub, built with AWS CodeBuild, and deployed to an S3 static website bucket via AWS CodePipeline.

## Tech Stack
- Frontend: HTML, CSS, JavaScript (in `frontend/`)
- Cloud: Amazon S3 (static website hosting)
- CI/CD: AWS CodePipeline, AWS CodeBuild (`buildspec.yml`)
- SCM: Git & GitHub

## Architecture
1. Push code to the `main` branch of this GitHub repository.
2. AWS CodePipeline detects the change and pulls the latest source.
3. AWS CodeBuild runs `buildspec.yml` to build the frontend artifact.
4. Deploy stage uploads the built files to the S3 website bucket `amazon-clone-frontend-yunus`.
5. S3 serves the site publicly via its static website endpoint (link above).

## Features
- End‑to‑end automated deployment (no manual S3 uploads).
- IAM roles and S3 bucket policies configured for secure `PutObject` access from CodePipeline/CodeBuild.
- Easy to extend with CloudFront and a custom domain for production.

## Screenshots
<img width="1366" height="643" alt="image" src="https://github.com/user-attachments/assets/8045eb00-b462-46af-9597-803c0bc3eb4c" />
<img width="1366" height="681" alt="image" src="https://github.com/user-attachments/assets/1e51994c-e5e7-415b-90f9-59e0f769cd46" />


