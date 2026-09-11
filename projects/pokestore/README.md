# Pokéstore

**Status:** In development — functional inventory, sales and AI artwork search prototype

Pokéstore is a local Pokémon card inventory and sales-management application built to solve a practical collecting problem: existing tools made it difficult to manage owned stock, estimate selling value, organise resale inventory and search cards by what actually appears in the artwork.

The project combines inventory management, market pricing, sales tracking and an experimental semantic artwork search system.

## The problem

Card collectors often need more than a normal card database.

For this project, the main pain points were:

- keeping physical sale stock organised
- tracking quantities, conditions, variants and languages
- comparing market value with intended selling prices
- calculating potential revenue and markup
- recording sales without manually adjusting stock afterwards
- finding cards for themed binders or collections by visual content in the artwork rather than only by Pokémon name, set or printed text

Pokéstore was built around those workflows instead of treating the collection as a simple list of card names.

## Current working features

### Dashboard

The dashboard provides a live overview of the current sale inventory, including:

- potential sales revenue
- current market value
- potential markup amount
- actual sales revenue
- cards on hand
- active listings
- units sold
- missing live-price checks
- inventory snapshot in National Pokédex order
- price refresh controls
- CSV export

### Inventory management

The master inventory currently supports:

- National Pokédex ordering
- card name and rarity information
- set and card number
- finish / variant
- condition
- language
- quantity on hand
- market value in ZAR
- suggested selling price
- manual selling price override
- active selling price
- total stock value
- live-price status
- inventory search
- row editing
- automatic quantity merging
- automatic stock reduction when sales are recorded

### Add Stock workflow

Cards can be searched by name, collection set or both.

After choosing the correct artwork, the user can select the exact physical version owned and record:

- variant / finish
- condition
- quantity
- language

Different variants can carry different market prices before the card is added to inventory.

### Sales tracking

Pokéstore includes a sales workflow for recording completed sales.

Current fields include:

- inventory card
- quantity sold
- sale date
- optional actual price per unit
- sales channel
- notes

When a sale is recorded, stock is reduced automatically and the transaction can appear in the recent-sales history.

### Pricing and data settings

The application currently supports:

- configurable markup over market price
- USD to ZAR conversion
- EUR to ZAR conversion
- price refresh tracking
- card catalogue data from TCGdex
- CSV export

## AI Artwork Search

One of Pokéstore's main experimental features is semantic artwork search.

Instead of only searching card names or printed text, the system is designed to search the visual meaning of the card illustration.

Example searches include:

- fish-like
- Poké Ball
- underwater
- forest
- food
- moon / night
- multiple Pokémon
- natural-language concepts such as `water`

A local vision-language model analyses card images and stores their visual embeddings / fingerprints locally. Later searches are converted into the same embedding space and compared against the saved artwork index.

This means the search is intended to find cards because of what appears in the artwork, even when that visual concept is not part of the card name.

### Current AI status

The semantic artwork search is working as a prototype, but the full catalogue has not yet been indexed.

At the latest documented test:

- physical card catalogue: **19,508 cards**
- AI-indexed artworks: **242**

Because only a portion of the catalogue has been indexed so far, semantic search results are still limited by the size of the local AI index.

The indexing system itself is functional and can continue processing more catalogue artwork over time.

## Local-first design

Pokéstore keeps its working data and AI artwork index on the local computer.

This project intentionally explores a local-first workflow so that inventory and artwork-search data do not need to depend on a permanent cloud service for everyday use.

## Current status

Pokéstore is a **functional prototype under active development**.

The inventory, pricing, stock-entry, sales and semantic-search foundations are working. The project is not being presented as a finished commercial product, and the AI catalogue is still being progressively indexed and refined.

## Screenshots

Screenshots will be added here as the portfolio version is prepared.

Planned showcase screens:

1. Dashboard
2. Master inventory
3. Semantic Artwork Search with visual results
4. Add card to inventory workflow
5. Settings / pricing and AI-search explanation

## Why this project matters

Pokéstore started from a real collecting and resale workflow rather than a tutorial exercise.

The project combines:

- practical inventory management
- business-style pricing logic
- local data handling
- external card catalogue data
- currency conversion
- stock and sales workflow design
- semantic search
- local AI indexing
- interface design for a specialised user need

The long-term aim is to make it easier to manage a physical card collection while also enabling artwork-based discovery that traditional card filters cannot provide.

---

Pokémon and related names/images are trademarks of their respective owners. This is an independent personal software project and is not affiliated with or endorsed by The Pokémon Company, Nintendo, Game Freak or Creatures Inc.
