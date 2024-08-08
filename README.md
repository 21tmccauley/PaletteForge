# PaletteForge

## Color Picker and Palette Generator: In-depth Walkthrough

### 1. Overall Structure

The site is built using HTML, CSS, and JavaScript, with a modular approach to JavaScript using ES6 modules. The main components are:

- index.html: The main HTML structure
- style.css: All the styling for the application
- main.js: The entry point for JavaScript functionality
- Modules:
  - colorConverter.js: Handles color format conversions
  - colorTheory.js: Implements color theory algorithms
  - colorPicker.js: Manages the color picker functionality
  - paletteGenerator.js: Generates color palettes
  - uiManager.js: Handles UI updates and user interactions

### 2. HTML Structure (index.html)

The HTML is divided into two main sections:
1. Left Column: Contains the color picker, selected colors, and controls
2. Right Column: Displays the generated color palette

Key elements include:
- Color picker container with sliders for Hue, Saturation, and Lightness
- Color preview and hex code display
- "Add Color" button
- Selected colors display area
- Scheme selection buttons
- "Generate Palette" button
- Generated palette display area

### 3. Styling (style.css)

The CSS provides:
- A two-column layout (1/3 left, 2/3 right)
- Styling for the color picker, sliders, buttons, and color displays
- Responsive design elements
- Custom styling for range inputs (sliders)
- Font styling, including the use of Google Fonts (Roboto)

### 4. JavaScript Functionality

#### main.js
- Serves as the entry point
- Imports necessary modules
- Sets up event listeners for main user interactions
- Initializes the ColorPicker class

#### colorConverter.js
- Provides functions to convert between color formats (HSL, HEX, RGB)
- Includes utility functions like `getPerceivedBrightness` and `getContrastColor`

#### colorTheory.js
- Implements color theory algorithms:
  - Complementary colors
  - Split complementary
  - Analogous
  - Triadic
  - Square
  - Tetradic

#### colorPicker.js
- Manages the color picker functionality
- Updates the color display and hex code in real-time as sliders are adjusted
- Provides methods to get the current selected color

#### paletteGenerator.js
- Generates color palettes based on selected colors and chosen color scheme
- Uses color theory algorithms to create harmonious color combinations

#### uiManager.js
- Handles UI updates:
  - Displaying selected colors
  - Updating the generated palette display
  - Managing the current color scheme selection

### 5. User Flow and Data Flow

1. User Interaction with Color Picker:
   - User adjusts HSL sliders
   - ColorPicker class updates color preview and hex code
   - Current color is available for adding to selected colors

2. Adding a Color:
   - User clicks "Add Color" button
   - Current color is added to selectedColors array in uiManager
   - UI is updated to display the new selected color

3. Selecting a Color Scheme:
   - User clicks a scheme button
   - uiManager updates the current scheme display
   - Selected scheme is used when generating the palette

4. Generating a Palette:
   - User clicks "Generate Palette" button
   - paletteGenerator uses selected colors and current scheme to create a palette
   - Generated palette is passed to uiManager to update the display

5. Displaying the Palette:
   - uiManager creates div elements for each color in the palette
   - Colors are displayed with their hex codes
   - Text color is adjusted for readability using getContrastColor

### 6. Key Features and Algorithms

- Real-time HSL to HEX conversion in the color picker
- Color theory algorithms for generating harmonious palettes
- Dynamic text color adjustment for readability on color swatches
- Modular JavaScript structure for maintainability and scalability

### 7. Potential Enhancements

- Save and load palettes
- Export palettes in different formats (CSS, SCSS, JSON)
- Color blindness simulation
- More advanced color theory options (e.g., monochromatic, custom angles)

This walkthrough provides a comprehensive overview of how the different components of the site work together to create a functional and interactive color picker and palette generator.
