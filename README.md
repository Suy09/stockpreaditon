services:
  - type: web
    name: stock-api
    runtime: python
    buildCommand: "pip install -r requirements.txt"
    startCommand: "gunicorn app:app"
    envVars:
      - key: FLASK_ENV
        value: production
