# ResumeForge — Streamlit Cloud deployment copy

This folder contains the deployable Streamlit application source. It intentionally does not include `Resume.csv`, `.env`, local SQLite databases, or model-training files.

## Deploy

1. Create a **new private GitHub repository** for this deployment copy. Do not push the original project repository: it contains a large resume dataset and local-only files in its history.
2. Upload the files and the `assets` folder from this directory to the new repository's root.
3. In Streamlit Community Cloud, choose **Create app**, select the repository, branch, and `app.py` entrypoint, then deploy.
4. In the app's **Settings → Secrets**, add:

   ```toml
   SARVAM_API_KEY = "your-new-Sarvam-key"
   ```

   Keep the key out of GitHub and do not put it in a committed file. The local `.env` is not part of this copy.
5. Restart/reboot the app after saving Secrets.

The app has local resume scoring and manual job-description input. The offline job catalog is disabled in this copy. Saved resume versions are isolated per browser session and are cleared when that session ends; this avoids sharing one visitor's saved resumes with other visitors on a public app.

## Local run

```powershell
python -m pip install -r requirements.txt
streamlit run app.py
```
