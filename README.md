# Digital Clock Application

This is a simple Digital Clock application that displays the current time in a 12-hour format with an AM/PM suffix. The clock updates every second, showing hours, minutes, and seconds. The background is a full-screen image that complements the clock's appearance, and the clock itself has a stylish font with a backdrop blur effect for better visibility.

## Features
- **Real-Time Clock**: Displays the current time in a 12-hour format (HH:MM:SS AM/PM).
- **Auto Update**: The time updates every second to keep it accurate.
- **Customizable Styling**: The clock has a large font size with a shadow effect, and the background is a customizable image.
- **Responsive Layout**: The clock is centered on the screen and adjusts to different screen sizes.

## Structure

### HTML (`index.html`)
- The HTML file creates the basic structure of the digital clock:
  - A `div` container (`clock-container`) that holds the clock display.
  - A `div` inside the container (`clock`) where the time will be displayed.

### JavaScript (`script.js`)
- **Clock Functionality**: The script defines an `updateClock` function that:
  - Retrieves the current time using JavaScript's `Date` object.
  - Converts the time to a 12-hour format with a `AM/PM` suffix.
  - Formats hours, minutes, and seconds to always display two digits (e.g., 08:05:09).
  - Updates the clock's text content every second using `setInterval`.
  
### CSS (`style.css`)
- **Background Image**: The background is a full-screen image (`Halifax.jpeg`) that is centered and scaled to cover the entire page.
- **Clock Styling**: The clock is styled with a large font size, bold weight, and white color for high visibility against the background. It also includes a subtle blur effect (`backdrop-filter: blur(3px)`) and semi-transparent background color to enhance readability.
- **Centering the Clock**: The clock is placed at the center of the screen using Flexbox for both horizontal and vertical alignment.

## How it Works
1. **Display Time**: When the page loads, the clock shows `00:00:00 AM` by default.
2. **Update Time**: The `updateClock` function is invoked once initially to display the current time and then updates every second using `setInterval`.
3. **12-Hour Format**: The time is displayed in a 12-hour format with an AM/PM suffix. The `getHours()` method is used to get the hour in 24-hour format, which is then converted to 12-hour format.
4. **Styling**: The clock is displayed with a large font and shadow for emphasis. The background image is applied to the entire body, and the clock container is styled to be centered vertically and horizontally.

## Code Explanation

### HTML
- The `clock-container` div holds the `clock` div, where the time is displayed.
- The script tag links to the external JavaScript file (`script.js`), which contains the logic for updating the clock.

### JavaScript
- **`updateClock()`**:
  - The `new Date()` method gets the current time.
  - The time is formatted into a 12-hour clock with the `AM/PM` suffix, and the time string is updated in the `clock` div.
- **`setInterval()`**:
  - Calls the `updateClock` function every 1000 milliseconds (1 second) to keep the time updated.

### CSS
- **Background**: A custom background image is set to cover the whole page using the `background-image` property.
- **Clock Styling**: The clock is given a large font size, bold text, and shadow to ensure it stands out against the background. A `backdrop-filter` property applies a slight blur effect to the clock's background, ensuring the time is readable even on a visually complex background.

## How to Use
1. Open the `index.html` file in your browser.
2. The clock will automatically start displaying the current time in a 12-hour format with the `AM/PM` suffix.
3. The clock will update every second to show the current time.
