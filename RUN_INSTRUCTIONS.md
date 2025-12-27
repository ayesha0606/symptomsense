# SymptomSense Runbook

Step-by-step commands to launch both the Flask backend API and the React frontend UI.

## 1. Backend (Flask)
1. Open **PowerShell**.
2. Change to the backend directory:
   ```
   cd "C:\Users\Ameena Tabassum\OneDrive\Desktop\SymptomSence_complete\backend"
   ```
3. Create and activate a virtual environment:
   ```
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```
4. Upgrade pip (recommended):
   ```
   pip install --upgrade pip
   ```
5. Install backend dependencies:
   ```
   pip install -r requirements.txt
   ```
6. Start the Flask server:
   ```
   python app.py
   ```
7. Leave this terminal open; the API listens on `http://127.0.0.1:5000`. Check `http://127.0.0.1:5000/health` to confirm it is healthy.

## 2. Frontend (React)
1. Open **another PowerShell window**.
2. Change to the frontend directory:
   ```
   cd "C:\Users\Ameena Tabassum\OneDrive\Desktop\SymptomSence_complete\frontend"
   ```
3. Install npm dependencies:
   ```
   npm install
   ```
4. *(Optional)* Point the UI to a custom backend URL (default already targets localhost). To override:
   ```
   echo REACT_APP_API_URL=http://localhost:5000 > .env
   ```
5. Start the development server:
   ```
   npm start
   ```
6. Visit `http://localhost:3000` in a browser; enter symptoms and submit. The UI will call `POST /predict` on the backend you started earlier.

## 3. Shutdown
- Stop the React dev server with `Ctrl+C` in its terminal.
- Stop the Flask server with `Ctrl+C` in its terminal and, if desired, deactivate the virtual environment using `deactivate`.

