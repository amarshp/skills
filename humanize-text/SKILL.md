---
name: humanize-text
description: Rewrites AI-generated text to evade AI detectors by maximizing perplexity and burstiness. Use this skill whenever the user wants to make text sound more human, bypass AI detection tools (QuillBot, GPTZero, Turnitin, etc.), humanize a passage, make writing less robotic, or when they say things like "rewrite this to pass AI detection", "make this sound human", "humanize this", or "this got flagged as AI". Always trigger this skill when the user shares a passage and asks for it to sound less AI-generated, even if they don't mention a specific detector.
---

# Humanize Text Skill

Rewrites AI-generated text to maximize perplexity and burstiness so it evades AI detectors.

## Core Concepts

AI detectors flag text using two metrics:

- **Perplexity**: How predictable the word choice is. AI picks the most statistically probable next word, making it very predictable. Humans choose with more randomness.
- **Burstiness**: Variation in sentence length and structure. AI writes like a metronome — uniform lengths, uniform rhythm. Humans mix short punchy fragments with long winding sentences.

Your job is to break both patterns.

---

## Rewriting Rules

### 1. Destroy the Metronome Rhythm (Burstiness)
Aggressively vary sentence length. Mix 3-6 word fragments with long multi-clause sentences. Never let three consecutive sentences be the same approximate length.

**Before:** "AI models are trained on massive datasets. They excel at recognizing complex patterns. This makes them useful across diverse industries."

**After:** "Trained on massive datasets, AI models are genuinely good at pattern recognition. Across every industry, really."

### 2. Strip AI Signpost Transitions
Replace rigid logical connectors with casual or implicit ones.

| Remove | Replace with |
|--------|-------------|
| Furthermore, Moreover | Plus, On top of that |
| In conclusion, In summary | The bottom line is, Look, Ultimately |
| Consequently, Therefore | So, Which means |
| It is important to note that | Note that, Crucially |
| Additionally | Also, And |

### 3. Kill Passive Voice
Change passive constructions to active, punchy ones.

**Before:** "The data was analyzed by the team."
**After:** "We tore through the data."

### 4. Inject Human Imperfections
- Use contractions: don't, it's, we're, you'll
- Add parenthetical asides that feel like afterthoughts (like this one)
- Use fragments for emphasis. Deliberately.
- Throw in a rhetorical question where it fits naturally
- First-person framing: "In my experience", "The reality is", "Here's the thing"

### 5. Banned Word List
Never use: delve, tapestry, landscape, testament, game-changer, paramount, hurdle, multi-faceted, groundbreaking, robust, leverage (as a verb), utilize, cutting-edge, seamless, streamline

### 6. Vary Paragraph Length
Don't let every paragraph be 3-4 sentences. Mix one-liners with longer blocks. A single sentence standing alone carries weight.

---

## Output Format

- Rewrite the full passage applying all rules above
- Do not explain the changes unless the user asks
- Do not add preamble like "Here is the rewritten version:"
- Just output the rewritten text, ready to copy-paste
- Match the approximate length and topic of the original

---

## Quick Self-Check Before Outputting

1. Are there 3+ consecutive sentences of similar length? Break them.
2. Are there any signpost transitions? Replace them.
3. Is any voice passive? Flip it.
4. Are there contractions? There should be.
5. Is there at least one fragment or aside? Add one.
6. Are any banned words present? Remove them.
