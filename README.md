# MAD Vacations — Website

## Two versions included

- **mad-vacations-website.html** — single self-contained file, all images embedded. Open it anywhere or upload this one file to any host. Recommended.
- **mad-vacations-website.zip** — the same site with a separate `assets/` folder (index.html + assets must stay together), for hosts where you prefer smaller pages.

## Availability calendar — one-time Google setting (no API key needed)

The site is already pointed at your calendar (**madvacationsuk@gmail.com**). It reads the calendar's public free/busy feed, so the only thing you must do is make that feed public:

1. Open calendar.google.com on a computer → ⚙ Settings.
2. Click your calendar in the left sidebar → **Access permissions for events**.
3. Tick **"Make available to public"** and set the dropdown to **"See only free/busy (hide details)"**.

Within a short while (Google caches the public feed, so allow up to a few hours for brand-new changes to appear) the website will show live availability. Your exact rules are built in: within 6:00 AM–11:30 PM, more than 10 booked hours = **Booked**, anything less = **Partially booked**, none = **Available**. Overlapping bookings are merged so hours aren't double-counted, and only event times are ever read — never titles, guests or notes.

Notes:
- The public feed is fetched through a free read-only relay (allorigins/corsproxy) because browsers can't read Google's feed directly. If you ever want to remove that dependency, create a free Google API key (console.cloud.google.com → enable "Google Calendar API" → Credentials → API key) and paste it into `GOOGLE_API_KEY` in the file — the site then switches to the official API automatically.
- Repeating events: use normal one-off bookings in this calendar (rental bookings usually are). Recurring series are only counted on their first occurrence via the public feed; with an API key they're expanded fully.

## Enquiry form — one-time activation

The form emails **madvacationsuk@gmail.com** via the free FormSubmit service. The first time anyone presses "Send enquiry", FormSubmit sends an activation link to that inbox — click it once and every future enquiry (name, email, phone, dates, pick-up/drop-off) arrives automatically.

## Reviews

Search the file for **"EDIT ME"** and replace the three sample testimonial cards with genuine quotes from your real Google/Turo reviews, and paste your real Google review link and Turo listing URL into the two buttons.

## WhatsApp

QR code, floating chat bubble and all booking buttons already point to **+44 7405 295569** with a pre-filled greeting.
