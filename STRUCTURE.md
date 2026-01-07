# Organized Single Collection Structure

This project uses a single Jekyll collection with organized subdirectories where chapters of the same booklet are grouped together.

## Current Structure

```
_booklets/                          # Single collection with organized subdirectories
├── calculus.md                     # Main booklet file
├── calculus/                       # Calculus chapters directory
│   ├── chapter1-limits.md
│   └── chapter2-derivatives.md
├── linear-algebra.md               # Main booklet file
└── linear-algebra/                 # Linear algebra chapters directory
    ├── chapter1-vectors.md
    ├── chapter2-matrices.md
    └── chapter3-transformations.md
```

## Benefits of This Structure

1. **Single collection**: All content is managed through one Jekyll collection
2. **Organized chapters**: Related chapters are grouped in subdirectories
3. **Clear organization**: Easy to find and manage files for each booklet
4. **Maintains simplicity**: Still uses only one Jekyll collection
5. **Visual clarity**: Directory structure matches logical booklet organization

## File Types

### Main Booklet Files
- Located in the root of `_booklets/` directory
- Have a `slug` field in front matter
- Use `booklet` layout (default)
- Listed on the homepage

### Chapter Files  
- Located in subdirectories named after their booklet
- Have `chapter_number` and `booklet` fields in front matter
- Must specify `layout: chapter` in front matter
- Linked from their parent booklet pages

## Adding a New Booklet

1. Create a main booklet file in `_booklets/` (e.g., `physics.md`)
2. Create a subdirectory for chapters (e.g., `_booklets/physics/`)
3. Add chapter files to the booklet's subdirectory
4. Ensure the `slug` in the booklet file matches the `booklet` field in chapter files
5. Set `layout: chapter` for all chapter files

## Key Features

- **Automatic chapter discovery**: Booklet pages automatically find and list their chapters
- **Organized file structure**: Related files are grouped together
- **Jekyll-native**: Uses standard Jekyll collection system efficiently
- **Easy maintenance**: Clear organization makes file management simple