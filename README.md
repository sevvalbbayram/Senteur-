# Senteur AI

> A data-driven niche perfume recommendation engine that helps you 
> find your signature scent.

## Overview

Senteur AI is an interactive R Shiny web application that provides 
personalized niche perfume recommendations based on your favorite 
perfumes, preferred notes, or the vibe you're going for.

The fragrance industry has a digital gap: online shopping eliminates 
the physical testing experience, yet physical testing is unreliable 
and time-consuming. Niche perfume houses — especially common in France 
and the Middle East — often have no physical retail presence 
internationally despite shipping worldwide. Senteur AI bridges this 
gap with data-driven recommendations.

## Features

- **Find Similar Perfumes** — Select a perfume and get the top 3 
  most similar ones based on TF-IDF cosine similarity of descriptions
- **Find by Notes** — Input one or more notes (e.g. "vanilla, 
  sandalwood") and get the best matches
- **Find by Vibe** — Choose a mood (Clean Girl, Warm & Cozy, 
  Tropical, Romantic, Sexy & Bold, Fresh, Sweet & Yummy, Skin Scent, 
  Androgynous, Nutty) and get curated recommendations

## Dataset

- 84,144 perfumes scraped from Fragrantica with notes, ratings, 
  descriptions, and reviews
- Subset to 2,191 high-quality niche perfumes (rated 3.7 or above) 
  for recommendation quality
- 4,936 unique notes, of which 258 (5%) appear only once

## Methods

| Technique | Purpose |
|-----------|---------|
| TF-IDF | Vectorize perfume descriptions |
| Cosine similarity | Rank perfume-to-perfume and note-to-perfume matches |
| Association rules | Discover note co-occurrence patterns (e.g. jasmine + musk + patchouli → rose, lift 4.28) |
| N-gram NLP (n=2) | Extract vibe descriptors and review patterns |
| Word clouds | Visualize description vs. review language differences |

## Key Findings

- "Blind buy" was the most common bigram in reviews — confirming 
  the market need for informed recommendations
- Musk appears in ~38% of all perfumes as a base note foundation
- Sweetness is the most common vibe descriptor, driven by the 
  rise of gourmand perfumes in niche perfumery
- Descriptions are objective (notes, gender, parfumer); reviews are 
  subjective ("love," "longevity," "wear")

## Tech Stack

- R — data analysis and application
- Shiny — interactive web application
- tidyverse — data manipulation
- tm / tidytext — NLP and text mining
- arules — association rules
- proxy — cosine similarity
- wordcloud — visualization

---

Copyright (c) 2025 Sevval Begum Bayram. All rights reserved.
