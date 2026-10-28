# 🎬 Video Idea Generator

A small Streamlit app. Type a video title or topic and Claude gives you 10 different video ideas, each with a title, hook, short description and format. You can download the results as a text file.

## Files

| File | Purpose |
|------|---------|
| `app.py` | The Streamlit app |
| `requirements.txt` | Python packages |
| `README.md` | This file |

## Run locally

1. Install Python 3.10 or newer.
2. Install the packages:
   ```
   pip install -r requirements.txt
   ```
3. Set your Anthropic API key (get one at https://console.anthropic.com):
   - Mac/Linux: `export ANTHROPIC_API_KEY="your-key"`
   - Windows (PowerShell): `$env:ANTHROPIC_API_KEY="your-key"`
   - Or skip this and paste the key into the app's sidebar.
4. Start the app:
   ```
   streamlit run app.py
   ```

## Deploy on Streamlit Community Cloud

1. Upload `app.py`, `requirements.txt` and `README.md` to a GitHub repository.
2. Go to https://share.streamlit.io, click **Create app**, pick the repository, branch `main` and main file `app.py`.
3. Open **Advanced settings → Secrets** and add:
   ```
   ANTHROPIC_API_KEY = "your-key"
   ```
4. Click **Deploy**.

Never upload your API key to GitHub. Keep it only in Streamlit Secrets.

## Models

The sidebar lets you choose between:
- `claude-sonnet-5-5` (better quality)
- `claude-haiku-5-5` (faster and cheaper)

To change the options, edit the `MODELS` dictionary at the top of `app.py`.
