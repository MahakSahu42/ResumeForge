# ResumeForge
it is a private repository for my project resumeforge

## Deploy on Streamlit Community Cloud

This app uses local resume scoring, manual job descriptions, and optional Sarvam AI insights. The offline job catalog is disabled. Saved resume versions are isolated per browser session and cleared when the session ends.

The deployment intentionally excludes `Resume.csv`, `.env`, and local SQLite databases. In Streamlit Community Cloud, add your key under **App settings → Secrets**:

```toml
SARVAM_API_KEY = "your-new-Sarvam-key"
```

Keep secrets out of GitHub. Deploy `app.py` from the repository root. See `README_DEPLOY.md` for detailed setup.
