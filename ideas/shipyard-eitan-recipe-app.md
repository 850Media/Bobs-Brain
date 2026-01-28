# Shipyard Contest: Eitan Bernath Recipe App

**Contest:** RevenueCat Shipyard
**Creator:** Eitan Bernath (@eitan) - 3M+ followers
**Brief:** Recipe organizer with smart grocery lists
**Deadline:** February 12, 2026 11:45pm ET
**Prize:** $20,000 + exposure

---

## App Concept

**Name Ideas:**
- CookBook AI
- RecipeBox
- MealMate
- PrepPal
- GrocerEats

**One-liner:** Save recipes from anywhere, AI organizes ingredients, smart grocery list builds itself.

---

## Core Features (MVP)

### 1. Recipe Import
- Paste URL → AI extracts recipe
- Take photo of recipe → AI reads it (OCR + AI)
- Manual entry
- Save from social media links (Instagram, TikTok, YouTube)

### 2. Recipe Organization
- Collections/folders (Breakfast, Dinner, Quick Meals, etc.)
- Tags (vegetarian, under 30 min, etc.)
- Search
- Favorites

### 3. Smart Grocery List
- Tap recipes → ingredients auto-add to list
- AI combines duplicates ("2 recipes need onions" → "Onions (2)")
- Group by store aisle (Produce, Dairy, Meat, etc.)
- Check off while shopping
- Share list

### 4. Meal Planning (Nice to have)
- Weekly calendar view
- Drag recipes to days
- Auto-generate grocery list from week's meals

---

## RevenueCat Monetization

**Freemium Model:**

| Tier | Price | Features |
|------|-------|----------|
| **Free** | $0 | 10 recipes, basic grocery list |
| **Premium** | $4.99/mo or $29.99/yr | Unlimited recipes, AI import, meal planning, aisle sorting |

**Paywall triggers:**
- Import more than 10 recipes
- Use AI photo import
- Access meal planning
- Share grocery lists

---

## Tech Stack (Vibecode)

- **Mobile:** React Native (cross-platform)
- **Backend:** Supabase
- **AI:** OpenAI for recipe extraction
- **Monetization:** RevenueCat SDK
- **Auth:** Email or Apple/Google sign-in

---

## Screens

### Onboarding
1. Welcome + value prop
2. Sign up (email or social)
3. Paywall preview (show premium features)

### Main App
1. **Home** - Recent recipes, quick actions
2. **Recipes** - Grid/list of saved recipes
3. **Recipe Detail** - Ingredients, instructions, add to list button
4. **Add Recipe** - URL input, photo capture, manual
5. **Grocery List** - Smart list, grouped by aisle
6. **Meal Plan** - Weekly calendar (Premium)
7. **Settings** - Account, subscription, preferences

---

## AI Features

### URL Import
```
Input: https://example.com/chicken-parm-recipe
Output: {
  title: "Chicken Parmesan",
  servings: 4,
  prepTime: "15 min",
  cookTime: "30 min",
  ingredients: [...],
  instructions: [...],
  image: "..."
}
```

### Photo Import
- User takes photo of recipe card/cookbook page
- OCR extracts text
- AI structures into recipe format

### Smart Grocery Combining
- "1 cup diced onion" + "1/2 onion, sliced" → "Onions (1.5)"
- Groups by category automatically

---

## Vibe Coding Prompt

```
Build a recipe organizer mobile app with smart grocery lists.

Core features:
1. Save recipes by pasting a URL - AI extracts title, ingredients, instructions
2. Organize recipes into collections with tags and search
3. Smart grocery list - tap recipes to add ingredients, AI combines duplicates and groups by store aisle
4. Meal planning calendar (premium feature)

Two tiers:
- Free: 10 recipes, basic list
- Premium ($4.99/mo): Unlimited recipes, AI import, meal planning

Tech: React Native, Supabase, OpenAI for recipe extraction, RevenueCat for subscriptions.

Make it beautiful - this is for a celebrity chef's audience. Clean, modern, food-focused design.
```

---

## Differentiators (What Makes You Win)

1. **AI-powered import** - Paste URL, get structured recipe instantly
2. **Smart grocery combining** - Not just a list, actual intelligence
3. **Beautiful design** - Eitan's audience cares about aesthetics
4. **Dead simple UX** - No learning curve

---

## Demo Video Outline (< 3 min)

0:00 - Hook: "Never lose a recipe again"
0:15 - Problem: Screenshots, bookmarks, lost recipes
0:30 - Solution: Show URL import → instant recipe
0:45 - Organize: Collections, tags, search
1:00 - Smart grocery list: Add recipes, see combined list
1:30 - Meal planning: Weekly view
1:45 - Premium features + pricing
2:00 - Built for Eitan's community
2:15 - Call to action

---

## Timeline

| Day | Task |
|-----|------|
| 1-2 | Vibe code MVP |
| 3-4 | Polish UI, test |
| 5 | RevenueCat integration |
| 6 | TestFlight build |
| 7 | Demo video |
| 8+ | Buffer for fixes |

---

*Spec by Bob 🛠️ — 2026-01-28*
