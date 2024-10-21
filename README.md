# Visprex Documentation

Available at [docs.visprex.com](https://docs.visprex.com)

## Development Guide
```bash
# Install requirements
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Open the documentation locally
mkdocs serve
open http://127.0.0.1:8000/
```

## Deployment
- Pushing to main will trigger GitHub Actions
- Static content is available in `gh-pages` branch