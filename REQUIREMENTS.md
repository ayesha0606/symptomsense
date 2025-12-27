# SymptomSense Requirements

Single reference for all dependencies needed to run both the backend (Flask) and frontend (React) applications.

## Backend (Python)
Install via pip inside your virtual environment:
```
pip install Flask==3.0.0
pip install flask-cors==4.0.0
pip install numpy>=1.26.0,<2.2.0
pip install scikit-learn==1.2.2
pip install joblib>=1.2.0
```
These match `backend/requirements.txt`.

## Frontend (Node.js)
Install via npm in `frontend/`:
```
npm install axios@^1.5.0
npm install react@^18.2.0
npm install react-dom@^18.2.0
npm install react-router-dom@^6.14.1
npm install react-scripts@5.0.1
```
These match `frontend/package.json`.

