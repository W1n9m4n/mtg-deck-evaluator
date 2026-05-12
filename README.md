# mtg-deck-evaluator

MTG Deck Evaluator – Evaluation Rules

The app evaluates normal 60-card Magic: The Gathering decks for Standard and Legacy.

Input format:
- One card per line.
- Quantity first, then card name.
- Optional set code, collector number, and foil marker are ignored.
- Example:
  4 Lightning Strike (DMU) 137
  1 The Modern Age (NEO) 66
  Sideboard
  3 Torch the Tower

Card resolution:
- Card names are resolved through Scryfall.
- Double-faced cards are supported by front-face name.
- Fuzzy lookup is used if exact lookup fails.
- Unresolved cards are listed separately.

Legality checks:
- Main deck must have at least 60 cards.
- Sideboard may have up to 15 cards.
- Non-basic cards may appear up to 4 times.
- Basic lands may appear any number of times.
- Standard and Legacy legality are checked separately.
- Legal does not mean strong.

Detected archetypes:
- Aggro
- Control
- Tempo
- Ramp
- Midrange
- Rogue / Synergy

Archetype detection uses:
- Creature count
- Low mana value count
- Interaction count
- Draw/selection count
- High mana value count
- Land count

Card roles:
- Threats: creatures and creature-like win conditions
- Interaction: removal, discard, counterspells, damage
- Draw: draw, scry, surveil, selection
- Ramp: mana generation, treasures, land search

Displayed infographics:
- Main deck count
- Land count
- Average mana value
- Detected archetype
- Mana curve
- Mana color demand
- Card type breakdown
- Deck composition

Structural Score:
Each format receives a separate score out of 100.

Categories:
- Deckplan / Archetype: 15
- Mana Base: 20
- Curve / Tempo: 15
- Functional Density: 15
- Consistency: 15
- Card Quality: 10
- Sideboard: 10

Standard rating:
- 83–100: Meta-near
- 71–82: Competitive
- 56–70: FNM-ready
- 41–55: Playable
- 0–40: Casual

Legacy rating:
- 85–100: Legacy Competitive
- 70–84: Legacy Rogue
- 50–69: Legacy casual / low
- 0–49: Legacy weak

Meta Benchmark:
Each format also receives a separate benchmark score.

Standard Meta Benchmark: 20 points
- Archetype Fit
- Core Structure
- Curve Match
- Mana Match
- Sideboard

Legacy Meta Benchmark: 20 points
- Archetype Fit
- Legacy Efficiency
- Mana Quality
- Interaction
- Sideboard Hate
- Speed

Important limitation:
The Meta Benchmark is heuristic only.
It does not currently compare against live tournament data from MTGGoldfish, MTGDecks, Untapped.gg, or MTGA Zone.

Final report includes:
- Legality
- Structural Score
- Rating label
- Meta Benchmark
- Detailed score lines
- Problems and warnings
