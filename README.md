# 🍸 Cocktail Recommender

A curated cocktail recommendation engine powered by the OpenAI API and a meticulously researched dataset of **141 of Kevin Ryan's favorite drinks** — each with complete recipes, acceptable ingredient substitutions, aliases for fuzzy matching, and origin.

---

## ✨ Features

- **Complete Dataset**  
  - 141 cocktails with:
    - Name and aliases
    - Full specifications in ounces (oz)
    - Garnish instructions
    - Method (shake, stir, build, blend, etc.)
    - Acceptable ingredient substitutions
    - origin or attribution for every recipe
    - Tagging for style/ genre (tiki, classic, modern, etc...)

- **OpenAI API Integration**  
  - Provide a list of ingredients you have on hand, and the system recommends cocktails you can make (or nearly make).
  - Provide a taste or a flavor you are in the mood for...
  - Provide a genre you are interested in... 
  - Offers smart substitutions (e.g., Triple Sec ↔ Dry Curaçao).

- **Historical Context**  
  - Origins sourced from respected cocktail history references within Kevin Ryan's home library:
    - *Sasha Petraske’s “Regarding Cocktails” (and cocktails from Milk and Honey)*
    - *Death & Co cocktails*,
    - *Maksym Pazuniak's Rogue Cocktails*, *Beta Cocktails* and cocktails from Cure in New Orleans,
    - *Smuggler’s Cove by Martin Cate*
    - *Beachbum Berry’s tiki research*
    - *Savoy Cocktail Book*
    - and other important literature!!!

---

## 📂 Dataset Structure

The file [`recipes.json`](recipes.json) is a JSON array of cocktail objects.  
Each object looks like:

```json
{
  "name": "Sazerac",
  "aliases": ["New Orleans Sazerac"],
  "spec_oz": [
    { "ingredient": "Rye Whiskey", "amount_oz": 2.0 },
    { "ingredient": "Sugar Cube", "amount_oz": 0.25 },
    { "ingredient": "Peychaud's Bitters", "amount_oz": 0.125 }
  ],
  "garnish": "Lemon peel",
  "method": "Stir",
  "substitutions": [
    { "ingredient": "Rye Whiskey", "possible_subs": ["Bourbon"] }
  ],
  "tags": ["classic", "whiskey", "New Orleans"],
  "origin": "The Sazerac House, New Orleans"
}
