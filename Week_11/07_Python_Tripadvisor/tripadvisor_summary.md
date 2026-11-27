# Task 7: Tripadvisor spatial analysis

## Data available

- The CSV contains 282 scraped day-trip listings. Its seven fields are scraper order ID, source URL, raw title, raw price, raw ranking/review count, raw duration, and the listing text/description.
- The text can also include details such as whether the price is per adult or per group, cancellation terms, and languages.
- The scraper-order timestamp corresponds to 2024-04-16 11:36 UTC. This is a partial historical snapshot, not the current full Tripadvisor catalogue. The [Tripadvisor day-trips page](https://www.tripadvisor.ch/Attraction_Products-g188045-t11889-zfg11867-o30-Switzerland.html) displayed 602 results when checked on 2026-11-27.

## Main results

- spaCy extracted 485 location mentions from the listing titles, representing 117 distinct place-name strings.
- 230 unique listings contained a price stated per adult; 205 of these had coordinates after geocoding.
- Adult prices ranged from CHF 75 to CHF 1,958, with a mean of CHF 649 and median of CHF 626. The mean above the median reflects a long high-price tail.
- The most frequently mapped destinations were Zürich (71 listings), Luzern (39), Interlaken (25), Basel (20), and Genf (19). A listing can mention more than one destination.
- Ratings were present for only 104 of the 230 per-adult listings. Their mean was 4.88 out of 5, so the high average should not be treated as representative of every listing.
- The extracted maximum-duration value averaged 7.0 hours. This is approximate: the notebook's simple number extraction records “more than 6 hours” as 6.

## What the results suggest

- Day trips are concentrated around major Swiss visitor hubs and Alpine destinations, especially Zürich, Luzern, and Interlaken.
- Prices vary widely, and trip titles often describe several stops, so destination-level counts represent mentions rather than trip origins or full routes.
- Named-entity extraction and place-name geocoding are approximate. Ambiguous names, missing ratings, and the old partial scrape limit how strongly these results can be generalized.
