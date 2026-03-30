# HDR Web Prospect Scout — Brief

**Goal:** Find Hailey, ID area small/medium businesses that are viable candidates for a new or redesigned website, which could be sold by Hailey Device Repair.

**Target geography:** Hailey, ID and surrounding Wood River Valley (Ketchum, Sun Valley, Bellevue, Carey)

---

## Your Task Each Run

1. **Pick a discovery method** (rotate through these):
   - Google Maps search: `site:maps.google.com` or use web_search for `[business type] Hailey Idaho`
   - Yelp: `web_fetch https://www.yelp.com/search?find_desc=[category]&find_loc=Hailey+ID`
   - Yellow Pages: `web_fetch https://www.yellowpages.com/hailey-id/[category]`
   - Google search: `[type] Hailey ID site:yelp.com` or just `[type] Hailey Idaho`
   - Local directories: visitsunvalley.com, haileyidaho.gov business listings
   - Search for businesses in these categories (rotate): restaurants, salons, spas, contractors, plumbers, electricians, landscapers, auto repair, gyms, yoga studios, real estate agents, law offices, dental offices, veterinarians, retail shops, bakeries, breweries, hotels/lodges, tour operators, ski shops

2. **Find at least 1 new business** not already in prospects.md

3. **Evaluate the website** (if they have one):
   - Fetch the homepage with `web_fetch [url]`
   - Score it 1-10 on: Design quality, Mobile-friendliness signals, Content clarity, SEO basics (title/meta present)
   - Flag as **OUTDATED** if: looks pre-2018, heavy use of Flash-era patterns, poor mobile signals, Wix/Weebly/GoDaddy builder tells, no SSL, generic template with placeholder content
   - Flag as **NO WEBSITE** if you can't find any website for them

4. **Rate viability** as a web design prospect (1-10):
   - 10 = perfect: established business, outdated/no site, serves local consumers, clear budget signals
   - High scores: restaurants, salons, contractors, tourist-facing businesses, professional services
   - Lower scores: already has a great modern site, national chain, or likely closed

5. **Append to `/tmp/File-transfer/hdr-prospects/prospects.md`** using the format below

6. **Commit and push:**
   ```
   cd /tmp/File-transfer && git add hdr-prospects/prospects.md && git commit -m "prospects: [business name]" && git push
   ```

7. Reply `DONE: [business name] — viability [score]/10`

---

## Output Format (append to prospects.md)

```
---
## [Business Name]
- **Location:** [City, ID]
- **Category:** [e.g. Restaurant, Salon, Contractor]
- **Website:** [URL or NONE]
- **Website Status:** [OUTDATED | BASIC | DECENT | MODERN | NO WEBSITE]
- **Website Score:** [1-10 or N/A]
- **Viability Score:** [1-10]
- **Why:** [2-3 sentences. What makes them a good/bad prospect? What would a new site do for them?]
- **Contact Signal:** [Phone / address / social found]
- **Scouted:** [YYYY-MM-DD]
---
```

## Scoring Guide

**Viability 9-10:** Established local business, clearly outdated or no website, consumer-facing, serves tourists or locals with money (Wood River Valley = affluent area)

**Viability 7-8:** Good business, mediocre website, would clearly benefit from upgrade

**Viability 5-6:** Has a decent site already, or business type less likely to invest

**Viability 1-4:** National chain, already modern, likely closed, or not a real prospect

## Notes
- Skip businesses already in prospects.md (check the last 10 entries)
- Skip national chains (Subway, McDonald's, etc.)
- The Wood River Valley is an affluent ski resort area — businesses here often have money to spend
- A new site from HDR would typically be $500-1500 for a small business
- Focus on businesses that are clearly local and owner-operated
