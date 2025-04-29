# Mobile and Desktop Wireframe with CSS Grid

## Project Overview

This project demonstrates the implementation of responsive wireframe layouts using CSS Grid. The layouts are designed to showcase both mobile and desktop application structures with various sections including header, navigation, content areas, and footer.

## Technologies Used

- **HTML5**: For the structural markup of the page
- **CSS3**: For styling the layout
- **CSS Grid**: For creating the responsive grid-based layout
- **Media Queries**: For implementing responsive design between mobile and desktop views

## Project Structure

The project consists of the following files:

- `index.html`: Contains the HTML structure of the wireframe
- `css/style.css`: Contains the CSS styling including the grid layout
- `css/reset.css`: Provides a CSS reset to ensure consistent styling across browsers
- `mobile-wireframe.png`: The reference wireframe image for mobile implementation
- `desktop-wireframe.png`: The reference wireframe image for desktop implementation

## Implementation Details

### HTML Structure

The HTML structure is organized into semantic sections:

```html
<header>HEADER</header>
<aside class="top-aside">ASIDE</aside>
<main class="main-content">
    <article>ARTICLE</article>
    <div class="column-container">
        <div class="column">COLUMN</div>
        <div class="column">COLUMN</div>
        <div class="column">COLUMN</div>
    </div>
</main>
<aside class="bottom-aside">ASIDE</aside>
<footer>FOOTER</footer>
```

### CSS Grid Implementation

#### Mobile Layout

The mobile layout uses CSS Grid with a vertical stacking approach:

```css
body {
    display: grid;
    grid-template-rows: auto auto auto auto auto;
    gap: 2px;
}

main {
    display: grid;
    grid-template-rows: auto 1fr auto;
    gap: 10px;
}
```

#### Desktop Layout

The desktop layout uses a more complex grid structure with named grid areas:

```css
@media screen and (min-width: 768px) {
    body {
        display: grid;
        grid-template-rows: auto 1fr auto;
        grid-template-columns: 1fr 2fr 1fr;
        grid-template-areas:
            "header header header"
            "left-aside main right-aside"
            "footer footer footer";
        gap: 10px;
    }

    main {
        grid-area: main;
        display: grid;
        grid-template-rows: 1fr auto auto;
    }

    main .column-container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 10px;
    }
}
```

### Styling Features

- **Color Scheme**: Each section has a distinct color for visual clarity
  - Header: Purple (#c93b8e)
  - Left Aside: Blue (#2980b9)
  - Right Aside: Light Blue (#3498db)
  - Main content area: Green (#2ecc71)
  - Columns: Pink (#e91e63)
  - Footer: Orange (#e67e22)

- **Typography**: Bold, centered text for clear visibility
- **Responsive Design**: The layout adapts between mobile and desktop views
- **Content Centering**: Grid layout is used to center content both horizontally and vertically

## Responsive Design Approach

This project follows a mobile-first approach, with the base styles designed for mobile devices. Media queries are then used to adapt the layout for larger screens:

### Mobile View (Default)

- Vertical stacking of all elements
- Single column layout
- Optimized for narrow screens

### Desktop View (min-width: 768px)

- Three-column layout in the main section
- Sidebar elements positioned on either side of the main content
- "ARTICLE" text positioned just above the columns
- Full-width header and footer

## Implementation Highlights

1. **Named Grid Areas**: The desktop layout uses named grid areas for intuitive placement of elements
2. **Nested Grids**: The main content area uses a nested grid to arrange the article text and columns
3. **Responsive Spacing**: Gap sizes and padding adjust between mobile and desktop views
4. **Flexible Sizing**: The use of fractional units (fr) ensures the layout adapts to different screen sizes
