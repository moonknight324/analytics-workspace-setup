# Analytics Workspace Setup

A standardized, reproducible Python workspace for the data product team. It gives every contributor the same environment, folder layout and secrets handling before any analysis begins.

## Setup

1. Clone the repository:git clone https://github.com/YOUR-USERNAME/analytics-workspace-setup.git
cd analytics-workspace-setup

2. Create the virtual environment:
   - macOS/Linux: `python3 -m venv venv`
   - Windows: `python -m venv venv`
3. Activate it:
   - macOS/Linux: `source venv/bin/activate`
   - Windows (Command Prompt): `venv\Scripts\activate`
   - Windows (PowerShell): `venv\Scripts\Activate.ps1`
4. Install dependencies:

pip install -r requirements.txt

5. Create your environment file:
   - macOS/Linux: `cp .env.example .env`
   - Windows: `copy .env.example .env`

   Then open `.env` and fill in your own values.

## Project Structure

- `data/raw/`: source data exactly as received, never modified.
- `data/processed/`: cleaned data ready for analysis.
- `notebooks/`: Jupyter notebooks for exploration and reporting.
- `scripts/`: repeatable Python scripts and pipeline code.
- `output/`: generated reports, figures and exports.

## Notes

- Required environment variables: `DB_HOST`, `DB_USER`, `DB_PASSWORD`, `API_KEY`.
- Copy `.env.example` to `.env` and fill in your own values. Never commit `.env`.
- After installing a new package, run `pip freeze > requirements.txt` and commit the update.
