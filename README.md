BoneAppetite — Dog-Friendly Restaurant Locator

A lightweight web app to find dog-friendly restaurants in the Philippines.
Built with HTML + Tailwind, Leaflet.js, and Supabase.
Deployed on GitHub Pages at:
https://crstntaro.github.io/SajaBoysRepo

⸻

Features
	•	Animated hero banner (light/dark aware).
	•	Dark mode toggle with localStorage persistence.
	•	“Use My Location” → automatically pins you & runs search.
	•	Province/Area quick select (e.g. NCR, Cebu, Cavite).
	•	Radius + “Open Now” filter card.
	•	Sidebar results list → click to zoom & popup on the map.
	•	Custom marker.png icon for restaurants.
	•	Responsive and fast (no heavy frameworks).

⸻

Tech Stack
	•	Tailwind CSS (CDN)
	•	Leaflet (maps)
	•	Supabase (database & RPC)
	•	Vanilla JavaScript
	•	GitHub Pages (hosting)

⸻

Project Structure

SajaBoysRepo/
	•	index.html → Landing page with hero + buttons
	•	search.html → Map page with search system
	•	auth.html → Google Sign-In
	•	styles.css → Extra style
	•	headerpic.png → Branding image
	•	marker.png → Custom location marker

⸻

How to Run
	1.	Visit live: https://crstntaro.github.io/SajaBoysRepo
	2.	Or clone locally: git clone https://github.com/crstntaro/SajaBoysRepo.git
	3.	cd SajaBoysRepo
	4.	Start a local server (example: python3 -m http.server 5173)
	5.	Open http://localhost:5173

⸻

How It Works
	•	index.html shows the hero, buttons, and province selector
	•	“Use My Location” → redirects to search.html with lat/lng params
	•	“Open Map (Province)” → search.html with area param
	•	search.html loads the Leaflet map
	•	Reads query params → sets marker & runs Supabase RPC nearby_stores
	•	User marker = blue dot with tooltip
	•	Restaurant markers = marker.png
	•	Sidebar lists results and allows click-to-zoom

⸻

Dark Mode
	•	Preference saved in localStorage
	•	Applies theme before page load
	•	Map tiles swap between OSM (light) and Carto (dark)
