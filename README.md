# Mobile Wireframe with CSS Grid

## Project Overview

This project demonstrates the implementation of a mobile wireframe layout using CSS Grid. The layout is designed to showcase a typical mobile application structure with various sections including header, navigation, content areas, and footer.

## Technologies Used

- **HTML5**: For the structural markup of the page
- **CSS3**: For styling the layout
- **CSS Grid**: For creating the responsive grid-based layout

## Project Structure

The project consists of the following files:

- `index.html`: Contains the HTML structure of the wireframe
- `css/style.css`: Contains the CSS styling including the grid layout
- `css/reset.css`: Provides a CSS reset to ensure consistent styling across browsers
- `mobile-wireframe.png`: The reference wireframe image that guided the implementation

## Implementation Details

### HTML Structure

The HTML structure is organized into semantic sections:

```html
<header>HEADER</header>
<aside class="top-aside">ASIDE</aside>
<main>
    <div class="column">COLUMN</div>
    <div class="column">COLUMN</div>
    <div class="column">COLUMN</div>
</main>
<aside class="bottom-aside">ASIDE</aside>
<footer>FOOTER</footer>
```

### CSS Grid Implementation

The layout uses CSS Grid at two levels:

1. **Body-level Grid**: The overall page layout is controlled by a grid applied to the body element:

    ```css
    body {
        display: grid;
        grid-template-rows: auto auto auto auto auto;
        gap: 2px;
    }

    ```

2. **Main Content Grid**: The main content area uses a nested grid to arrange the columns:

    ```css
    main {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: repeat(3, auto);
        gap: 10px;
    }
    ```

### Styling Features

- **Color Scheme**: Each section has a distinct color for visual clarity
  - Header: Purple (#c93b8e)
  - Aside sections: Blue (#2980b9)
  - Main content area: Green (#2ecc71)
  - Columns: Pink (#e91e63)
  - Footer: Orange (#e67e22)

- **Typography**: Large, bold, centered text for clear visibility
- **Responsive Design**: The layout is designed for mobile devices with a max-width of 400px
- **Content Centering**: Flexbox is used within each grid cell to center content both horizontally and vertically

## Mobile-First Approach

This project follows a mobile-first approach, focusing on creating an optimal experience for mobile devices before considering larger screens. The wireframe is specifically designed for mobile viewing with appropriate spacing and sizing.
