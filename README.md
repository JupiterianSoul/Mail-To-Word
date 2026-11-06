# Mail to Word

A small web app that exports Gmail conversations to Word. Sign in with Google, search by email address, pick the threads you want and download them as Word, TXT or JSON.

## Stack

- FastAPI and Jinja2 templates
- Gmail API through the Google client libraries
- python-docx for the Word export

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
```

Fill in `.env` with an OAuth client ID and secret from the Google Cloud console, and set `SECRET_KEY` to a random string. Then start the server:

```bash
uvicorn app.main:app --reload
```

The app is served on http://127.0.0.1:8000.

## Status

The page and the app skeleton are in place. The Gmail sign-in and export routes are still to be written.

## License

See `LICENSE`.
