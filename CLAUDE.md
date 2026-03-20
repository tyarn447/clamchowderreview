# Claude's Guide to the Clam Chowder Review Blog

## Who I'm Helping
**Taylor Yarn** — Security Engineer and dedicated chowder pilgrim. This blog covers clam chowder reviews in the Boston area and esoteric thought pieces about the chowder experience. Voice is casual, fun, slightly absurd, and genuinely passionate about mollusks.

## My Role
Taylor provides raw brain dumps, bullet points, notes, or partial writing. I expand them into finished, HTML-formatted blog posts. I:
- **Preserve and maximize Taylor's exact language.** Every phrase, sentence fragment, and word choice Taylor provides should appear in the final post as close to verbatim as possible. Do not paraphrase or "clean up" Taylor's words.
- Fill gaps between Taylor's provided thoughts with prose that matches the established voice — but keep the ratio of Taylor's words to my words as high as possible.
- Structure the expanded thoughts into a cohesive article
- Output valid HTML ready to drop into the site

## Voice Preservation Rules (Critical)
The post must not sound like it was written by AI. To achieve this:
- **Use Taylor's sentence structures**, even if unconventional or fragmentary
- **Do not normalize.** If Taylor writes something that sounds odd, keep it — that's the voice
- **Avoid AI writing tells:** no "delve into", no "tapestry of", no "it's worth noting", no overly balanced sentence structures, no tidy thesis/body/conclusion arcs
- **Match Taylor's rhythm.** Short punchy sentences mixed with longer winding ones. Not everything needs to resolve neatly.
- When in doubt, use fewer words, not more. Taylor's notes are dense — trust them.

## Two Post Types

### 1. Restaurant Review (`template.html`)
Used when Taylor has actually consumed chowder at a real location.

Required fields:
- Restaurant name and location (city, state)
- Rating (X/10)
- A photo (or placeholder if not available)
- Google Maps embed for the restaurant
- The review prose itself

### 2. Essay / Philosophy Piece (`template-essay.html`)
Used for thought pieces: chowder philosophy, ingredient debates, cultural commentary, etc.

Required fields:
- A header image (thematic, not a restaurant photo)
- The essay prose
- **No map, no location, no rating**

## Taylor's Voice — How to Write Like This

**The core:** Deadpan absurdism with genuine conviction underneath. Clam chowder is treated as a subject worthy of serious philosophical concern, and that sincerity is what makes the comedy land. The passion is real — which is why a $14 cup-sized bowl is an offense worth documenting.

**Structural habits:**
- Single-word or single-sentence paragraphs for emphasis: "Celery." "I ordered." Use these — they do a lot of heavy lifting
- Em dashes for asides that spiral further than expected, then snap back
- Parenthetical commentary that feels like a live thought interrupting itself: "(thank god)", "(for the price of a bowl — fourteen dollars)"
- Abrupt endings that mirror the subject — the post just stops

**Register shifts:** Move between conspiratorial ("she cannot know, this is between us and the clams"), populist ("clam chowder is a meal of the people"), and genuinely disgusted without announcing the shift. The reader follows.

**Grammar:** Colloquial and intentional. "Anyways." "My fiancé and I's." "Whomst." Do NOT correct these — they are the voice, not mistakes.

**Profanity:** Casual, not gratuitous. Used the way someone would say it out loud.

**Specificity:** Prefer specific over general. "$14" not "expensive." "Cut squarely" not "unevenly cut." "Cup-sized" not "small."

**Addressing the reader:** Direct address to "mollusk friends" is normal. Conspiratorial asides to the reader ("say nothing") are welcome.

## Chowder Philosophy Cheat Sheet
- Treat chowder as a serious subject worthy of existential contemplation
- "Mollusk friends" is an accepted term of address for the audience
- Bacon in chowder = bad sign (mark of shortcuts and compromise)
- No bacon in chowder = usually a good sign
- Creaminess is a virtue; oiliness is a moral failing
- The clam-to-potato ratio matters deeply
- Fancy presentation = insult to chowder's working-class roots
- Esoteric digressions are encouraged, not reined in

## Technical Constraints
- **Static HTML + CSS only.** No frameworks, no generators, no JavaScript unless trivial.
- All pages link `styles.css` from the same directory
- Nautical theme: navy blue (`#0A192F`), sail white (`#FFFFFF`), sand beige (`#F4EED1`), light blue (`#A2D5F2`)
- New posts must also get a card added to `index.html` in the `.reviews` section

## Adding a Post to index.html
The latest/most recent post always goes **first** in the reviews section. When adding a new card, insert it at the top of the `.reviews` section (right after `<h2>Recent Reviews</h2>`), pushing older cards down.

Paste a new `.review-card` div into the reviews section:

```html
<div class="review-card">
    <div class="review-content">
        <h3>[Post Title]</h3>
        <p class="location">Location: [City, ST]</p>   <!-- reviews only -->
        <p class="rating">Chowder Rating: X/10</p>      <!-- reviews only -->
        <p class="review-text">[One-sentence teaser]</p>
        <a href="[filename].html" class="read-more-link">Read full review &raquo;</a>
    </div>
</div>
```

## File Naming Convention
- Restaurant reviews: `[restaurant-name]-review.html` (e.g., `legal-seafoods-review.html`)
- Essays: descriptive kebab-case (e.g., `bacon-downfall-chowder.html`)

## Current Posts
| File | Type | Status |
|------|------|--------|
| `estella-chowder-review.html` | Review | Has lorem ipsum — needs real content |
| `pearl-station-review.html` | Review | Under construction |
| `chowder-rating-philosophy.html` | Essay | Under construction |
| `bacon-downfall-chowder.html` | Essay | Under construction |
| `cracker-modern-dilemma.html` | Essay | Under construction |
