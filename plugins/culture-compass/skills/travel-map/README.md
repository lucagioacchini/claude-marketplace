# Travel Map

Part of the **Culture Compass** plugin.

## What it does

Builds a realistic, geographically sensible tourist itinerary for a city or area, with a tour-guide-style explanation for each main stop and a ready-to-use Google Maps route link. On request, it also suggests affordable, well-reviewed local places to eat.

Concretely, it provides:

- A short overview of the destination (context, layout of the main sights, practical difficulties)
- A day-by-day itinerary with time slots, estimated visit durations, travel between stops, and optional alternatives
- An in-depth explanation for each main stop (history, what to look for, significance, documented stories, how to read the place on site) — roughly 120-200 words for main stops, 2-3 lines for minor ones
- A Google Maps directions link (split into several links when the stop limit is exceeded)
- Optionally, a separate "where to eat" section
- Practical closing tips (bookings, accessibility, transport, hours to double-check)

## When it triggers

Use it when the user asks things like "what to see in…", "a N-day itinerary in…", "organise a visit to…", "where to eat in…". It is not meant for flights, hotels, or bookings.

## Reliability rules

- Variable information (opening hours, prices, closures, transport) is checked on the web.
- No invented dates, anecdotes, addresses, prices, ratings, or travel times; uncertain details are omitted or flagged.
- If web search is unavailable, the skill proceeds from general knowledge and states upfront that hours and prices are unverified.

## Food recommendations

Handled by [references/food.md](references/food.md) and only when requested. Defaults: medium-low price range, many positive reviews, authentic local cuisine. Restaurants are kept separate from the itinerary and are not added to the Maps link unless the user asks.

## Inputs

No fixed parameters. The skill extracts from the request: destination, starting point, dates and duration, interests, budget, mobility, dietary needs, and pace. Missing non-essential details are filled with stated assumptions (default: one day, balanced pace); a clarifying question is asked only when it is truly blocking.

## Output

- Responds in Italian unless the user asks otherwise.
- No CSV or other export files unless explicitly requested.

## Example prompts

- "Cosa vedere a Siracusa in un giorno, a piedi, senza ristoranti"
- "Itinerario di due giorni a Bologna, ritmo rilassato, amo l'arte e l'architettura"
- "Organizzami una visita a Matera e dimmi dove mangiare piatti tipici spendendo poco"

## Related

For spoiler-free background on a film, book, or series, see **Opera Context Briefing** in the same plugin.
