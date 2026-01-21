# Deployment Instructions

1.  **Copy this entire folder** (`Obsidian2Kindle-main`) to the computer where you want to run the plugin.
2.  On that computer, open a terminal inside this folder.
3.  Run the following command to build and start the container with the modifications:

    ```bash
    docker-compose up --build -d
    ```

## Changes Included
-   **Fonts**: `Salonica.ttf` and `Tahu!.ttf` have been removed. The cover now uses `Roboto-Regular.ttf`.
-   **Author**: The `Autor` field from your note's frontmatter is now automatically used as the author name.

## Plugin Configuration (IMPORTANT)

1.  **Plugin Setting**: The Obsidian plugin has a field named **Author**. You **cannot** leave this empty (the plugin will complain).
    -   **Action**: Put **ANYTHING** here. Write "Default", "Me", or "X". It does NOT matter.

2.  **Your Notes ("Autor")**:
    -   Continue using **`Autor:`** (Spanish) in your YAML frontmatter.
    -   Example:
        ```yaml
        ---
        Autor: Gabriel García Márquez
        ---
        ```

3.  **Result**: 
    -   My code on the server will see **`Autor:`** in your note and use that name.
    -   It will **IGNORE** the "Author" setting from the plugin.
