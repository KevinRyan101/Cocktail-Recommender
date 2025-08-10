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
    - Origin or attribution for every recipe
    - Tagging for style/ genre (tiki, classic, modern, etc...)

- **OpenAI API Integration**  
  - Provide a list of ingredients you have on hand... 
  - Provide a taste or a flavor you are in the mood for...
  - Provide a genre you are interested in...
  - Provide an origin location or creator...
  - *and the system recommends cocktails you can make!!!* 
  - (Also offers smart substitutions e.g., Triple Sec ↔ Dry Curaçao).

- **Historical Context**  
  - Origins sourced from respected cocktail history references within Kevin Ryan's home library:
    - Sasha Petraske’s *“Regarding Cocktails”* (and cocktails from Milk and Honey on the Lower East Side),
    - Maksym Pazuniak's *"Rogue Cocktails"*, *"Beta Cocktails"* (and cocktails from Cure in New Orleans),
    - Death & Co cocktails,
    - *"Smuggler’s Cove"* by Martin and Rebecca Cate,
    - Beachbum Berry’s tiki research,
    - *Savoy Cocktail Book*
    - and other important literature!!!

---

## 💡 Example Uses
**Home Bartender’s Tool –** Know exactly what you can make with your current inventory of bottles.

**Party Planning Tool –** Find drinks that match the theme or desired flavors of your party.

**Bar Menu Generator –** Auto-generate seasonal menus with cocktail descriptions.

**Cocktail Education –** Learn how to mix good drinks.

**Substitution Advisor –** Find the best alternative when you’re missing an ingredient.

---

## 📂 Dataset Structure

The file [`recipes.json`](recipes.json) is a JSON array of cocktail objects.  
Each object looks like:

```json
{
 "name": "Eeyore's Requiem",
  "aliases": ["Eeyore’s", "Eeyore Requiem", "Eeyores Requiem"],
  "spec_oz": [
    { "ingredient": "Campari", "amount_oz": 1.5 },
    { "ingredient": "Blanc Vermouth", "amount_oz": 1.0 },
    { "ingredient": "Gin", "amount_oz": 0.5 },
    { "ingredient": "Cynar", "amount_oz": 0.25 },
    { "ingredient": "Fernet-Branca", "amount_oz": 0.25 },
    { "ingredient": "Orange Bitters", "amount_oz": 0.02 }
  ],
  "garnish": "Orange peel twist",
  "method": "Stir; serve up",
  "substitutions": [
    { "ingredient": "Campari", "possible_subs": ["Cappelletti", "Luxardo Bitter", "Gancia Bitter"] },
    { "ingredient": "Blanc Vermouth", "possible_subs": ["Lillet Blanc", "Cocchi Americano", "Half Sweet/ Half Dry"] },
    { "ingredient": "Cynar", "possible_subs": ["Cardamaro", "Amaro Montenegro"] }
  ],
  "tags": ["bitter", "amaro-forward", "modern-classic"],
  "origin": "Toby Maloney, The Violet Hour (Chicago, 2008)"
}
