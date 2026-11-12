# Oasis Voice Assistant (web)

A browser-based voice assistant. One static file (`index.html`), no server, no build step.

## Features
**Basic:** time, date, jokes, open sites (YouTube, Google, GitHub, Wikipedia), web search.
**Advanced:** weather (OpenWeatherMap), reminders, email drafts (opens your mail app), question answering (Wikipedia), custom commands ("when I say hi, say hello there").

## Run locally
Open `index.html` in Chrome, Edge or Safari. Voice input needs a secure origin, so use GitHub Pages or `python -m http.server` and visit `http://localhost:8000`.

## Put it online with GitHub Pages
1. Create a new GitHub repository and upload `index.html` and `README.md`.
2. Go to **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
3. After a minute your app is live at `https://<your-username>.github.io/<repo-name>/`.

## Weather setup
Get a free key at openweathermap.org, then paste it in **Settings and privacy** in the app. It is stored only in your browser. Do not commit your key to the repository.

## Privacy
- Speech recognition runs through your browser. In Chrome and Edge, audio is sent to the browser vendor's speech service.
- The app has no backend and collects nothing. Your API key, custom commands and settings are saved in this browser's local storage; "Erase saved data" clears them.
- Weather requests go to OpenWeatherMap and "who/what is" answers come from Wikipedia.
- Email never sends from the page; it opens a draft in your own mail app.
- Reminders only fire while the tab stays open.
