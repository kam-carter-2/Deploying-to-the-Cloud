# Deploying-to-the-Cloud

## Cloud Run Deployment & Submission Checklist

1. Ensure Cloud Build API, Cloud Run Admin API, and Container Registry API are enabled.
2. Push `cloudbuild-backend.yaml` and `cloudbuild-frontend.yaml` to repo root.
3. (Option A) Create Cloud Build triggers:
   - Backend trigger: use cloudbuild-backend.yaml
   - Frontend trigger: use cloudbuild-frontend.yaml (update backend URL first)
4. (Option B) Or run `./deploy_cloudrun.sh YOUR_PROJECT_ID` locally after `gcloud auth login`.
5. Get the frontend Cloud Run URL from Cloud Console or via `gcloud run services describe recipe-frontend`.
