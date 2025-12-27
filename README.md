# SymptomSense

Unified onboarding guide for running the SymptomSense disease prediction experience (Flask API + React UI).

## Requirements
- Python 3.10+ with `pip`
- Node.js 18+ with `npm`
- Windows PowerShell (commands below use PowerShell syntax)

## Backend Setup (Flask)
```
cd "C:\Users\Ameena Tabassum\OneDrive\Desktop\SymptomSence_complete\backend"
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
python app.py
```
- Serves on `http://127.0.0.1:5000`
- `GET /health` confirms resources are loaded

## Frontend Setup (React)
```
cd "C:\Users\Ameena Tabassum\OneDrive\Desktop\SymptomSence_complete\frontend"
npm install
echo REACT_APP_API_URL=http://localhost:5000 > .env   # optional override
npm start
```
- Dev server runs at `http://localhost:3000`
- Proxies API calls to the backend base URL

## Combined Run Instructions
1. Start the backend steps above in one terminal and leave it running.
2. Start the frontend steps in a second terminal.
3. Visit `http://localhost:3000`, enter symptoms, and verify predictions (frontend calls `POST /predict` on the Flask API).

## Troubleshooting
- `react-scripts` missing → rerun `npm install` (listed in `frontend/package.json`).
- Pickle compatibility errors → ensure backend virtualenv uses the versions from `backend/requirements.txt` (scikit-learn `1.2.2`).
- API not reachable → confirm backend terminal shows `Running on http://127.0.0.1:5000` before hitting the UI.

