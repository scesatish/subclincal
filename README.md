# Buffalo SCE Thesis App

Mobile-friendly Streamlit app for buffalo subclinical endometritis thesis case logging.

## Features
- New case creation and later reopening by case number
- Flexible reproductive history fields
- Vaginal discharge options: Clear / Translucent / Cloudy
- Estrous cycle interval: Regular / Irregular
- Previous AI count field
- Automatic prediction of induced heat (day 9 and day 10 after treatment)
- Automatic AI windows (48 h and 72 h after predicted induced heat)
- Follow-up entry on the same case
- Photo capture fields for uterine discharge, White Side Test before/after, cytology, and extra images
- Master CSV export
- Case-wise Word report export
- Calendar reminder file (.ics) export
- Internal reminder dashboard with direct case-action links

## Run locally
```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy on Streamlit Community Cloud
1. Upload this folder to a GitHub repository.
2. In Streamlit Community Cloud, create a new app.
3. Select your repository and set the main file to `app.py`.
4. Deploy.

## Notes
- Data is stored in SQLite inside the app folder (`data/buffalo_sce.db`).
- Uploaded images are stored in `data/photos`.
- Generated Word reports and reminder files are stored in `data/exports`.
- For real phone push notifications, connect exported `.ics` reminders to Google Calendar or add external automation later.


## Version 2 upgrades
- Direct Google Calendar add-event links for predicted follow-up dates
- Stronger thesis-style Word report header with university, college, degree line, and thesis title
- .ics reminder file kept as backup for phone/calendar import


## Version 3 upgrades
- Internal reminder to-do list inside the app
- One-tap reminder links that open the exact case in follow-up view
- Query-parameter case routing so reminder links can go straight to the selected case
