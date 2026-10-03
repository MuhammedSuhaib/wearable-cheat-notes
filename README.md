# Wearable Cheat Notes

MVP tool that splits text into 130-character chunks for smartband push notifications.

<img width="1080" height="1350" alt="wearable-cheat-notes" src="https://github.com/user-attachments/assets/6ed7d794-a8c3-48ec-9ce1-36df33a22b48" />
 
**1,945 unique viewers** on a repo I forgot about. 😱  

Last year I open-sourced this as a game. Analytics later showed it was used to bypass exams. 😅  

Requires a two-person setup (sender + receiver on smartband). Not fully automated.

**Live demo:** https://push-notifcation-splitter.streamlit.app/

## How it works
1. Sender pastes answers + short label (e.g. `Q1`)
2. App splits text into ≤130-char chunks
3. Chunks appear numbered: `[Q1/1]`, `[Q1/2]`, …
4. Sender transmits them → receiver gets silent push notifications on the smartband

## Files
- `index.py` — Streamlit splitter
- `index.html` — smartband UI mock
- `wearable-cheat-notes.png` — analytics screenshot

## Run locally

### With uv (recommended)
```bash
uv run streamlit run index.py
```

### Classic way
```bash
pip install streamlit
streamlit run index.py
```

## Message formatting tips
- `#` headings · `##` subheadings · `*` bullets  
- `[s1/1]` section IDs · `<br>` line breaks · `^` powers · `/` division
