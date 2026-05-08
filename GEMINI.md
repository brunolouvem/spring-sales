# Spring Sales Project Overview

This project is a clean, modern, and responsive web-based product catalog designed for a "Spring Sale". It features a grid of items for sale with image carousels, detailed descriptions, and a lightbox for image inspection.

## Architecture & Technology Stack

- **Frontend:** Vanilla HTML5, CSS3, and JavaScript (ES6+).
- **Styling:** Modern CSS utilizing CSS Variables, Grid, Flexbox, and responsive design techniques (`clamp()`, `aspect-ratio`, media queries).
- **Data Management:** The catalog data is managed in `catalog.js` as a simple JavaScript array of objects.
- **Interactivity:**
    - **Image Carousels:** Each product card supports multiple images with navigation buttons and dots.
    - **Lightbox:** A full-screen image preview mode.
    - **Read More:** Expandable descriptions for longer text content.
    - **Reservation System:** Supports marking items as "Reserved" via a boolean flag in the data, which triggers a visual overlay and price strikethrough.

## Project Structure

- `index.html`: Main structure, core application logic, and **Open Graph (OG) tags** for social media previews.
- `catalog.js`: Data store containing the list of items for sale.
- `style.css`: All styling rules, including theme tokens and responsive layouts.
- `assets/images/`: Directory containing product images.

## Social Media Previews (OG Tags)

The `index.html` file includes Open Graph and Twitter meta tags to ensure that sharing the link on platforms like WhatsApp, Slack, or X (Twitter) displays a professional preview.
- **Project Domain:** `https://brunolouvem.github.io/spring-sales/`
- **Featured Image:** Canon EOS250D (using an absolute URL for maximum compatibility).

## Development Workflow

### Building and Running
- **Running:** This is a static web project. You can run it by opening `index.html` directly in any modern web browser or using a simple local development server (e.g., `npx serve .` or Live Server in VS Code).
- **Building:** No build step is required.

### Adding New Items
To add or update items in the catalog:
1.  Add the product images to `assets/images/`.
2.  Update the `items` array in `catalog.js` with a new object following this structure:
    ```javascript
    {
      name: "Product Name",
      description: "Short or long description (supports HTML for links).",
      price: 100,
      currency: "€",
      images: [
        "assets/images/image1.jpeg",
        "assets/images/image2.jpeg"
      ],
      storeUrl: "https://external-link.com",
      storeName: "amazon.de",
      reserved: false, // Optional: set to true to show as reserved
      sold: false      // Optional: set to true to show as sold
    }
    ```

### Testing
- **Visual Validation:** Manually verify the layout and interactivity (carousels, lightbox, responsive behavior) across different screen sizes.
- **Accessibility:** Ensure images have `alt` tags and interactive elements remain keyboard-accessible.

## Design Conventions
- **Theming:** Use CSS variables defined in `:root` for colors and spacing to maintain consistency.
- **Grid Layout:** The main catalog uses a CSS Grid `auto-fill` pattern to automatically adjust the number of columns based on screen width.
- **Images:** Product images should ideally follow a consistent aspect ratio (currently 3:4) for the best visual alignment in the grid.
best visual alignment in the grid.
