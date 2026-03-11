# Warehouse Inventory Manager

A Rust-based inventory management system modelling a distribution warehouse, built as a university project.

[demo.webm](https://github.com/user-attachments/assets/c53a729d-be61-4ace-878e-e28e8680b475)

## Description 
Implements a prototypical in-memory database with indexed lookups, structural constraints, pluggable allocation strategies, and a composable filter pipeline for item ingestion.

## Features
- Multi-dimensional spatial layout (rows → shelves → zones)
- O(log n) item lookups by ID and name via indexed data structures
- Typed item quality variants with category-specific constraints (fragile, oversized, normal)
- Swappable allocation strategies (closest-first, round-robin)
- Trait-based filter system for warehouse admission rules

# Running the project

`cargo test` to run unit tests which validate the manager, allocators, and filters.

`cargo run` to run the TUI. 
It was implemented with the `dialoguer` and `console` crates.
In multi-select prompts, use the space bar to `select` and hit `enter` to commit.
