# Spin the Lucky Wheel!

A fun, interactive, and customizable lucky wheel game built with HTML, Tailwind CSS, and JavaScript. Spin the wheel to win prizes, enjoy smooth animations, sound effects, and personalize the wheel to your liking!

![Spin the Lucky Wheel Screenshot/GIF](placeholder.gif)
*(Replace `placeholder.gif` with an actual screenshot or GIF of your project)*

## ✨ Features

*   **Interactive Spinning Wheel:** Click the "Spin" button to watch the wheel spin and land on a prize.
*   **Dynamic Wheel Segments:**
    *   Wheel segments are generated dynamically based on configuration.
    *   Uses `conic-gradient` for segment colors.
    *   Text labels are automatically positioned and rotated within segments.
    *   Supports stacked text for very short labels to improve readability.
*   **Weighted Prize Selection:** Prizes can be assigned different probabilities, making some rarer than others.
*   **Customization Panel:**
    *   Easily change the number of prizes (2-16).
    *   Customize the label (name), color, and probability for each prize.
    *   Delete prizes directly from the customization form.
    *   Changes are applied instantly with a smooth visual transition.
*   **Result Popup:** A sleek popup announces the winning prize.
    *   Special "Spin Again" prize logic.
    *   Confetti animation on winning (using `canvas-confetti`).
*   **Prize Board/Legend:** Displays all available prizes and their corresponding colors.
*   **Sound Effects:**
    *   Looping spin sound while the wheel is in motion.
    *   Ticking sound as the wheel spins.
    *   Winning sound effect when a prize is won.
*   **Enhanced Fullscreen Mode:**
    *   Immersive fullscreen experience with a custom animated gradient background.
    *   Smooth content transitions when entering/exiting fullscreen.
*   **Responsive Design:** Adapts well to different screen sizes, from mobile to desktop.
*   **Modern UI/UX:**
    *   Styled with Tailwind CSS for a clean and modern look.
    *   Uses Font Awesome for icons.
    *   Smooth animations for button interactions, popups, and panel transitions.
    *   Visual feedback like button glow and bounce on click.

## 🛠️ Tech Stack

*   **Frontend:** HTML5, CSS3, JavaScript (ES6+)
*   **Styling:** Tailwind CSS
*   **Icons:** Font Awesome
*   **Animations:** CSS Animations, CSS Transitions
*   **Confetti:** `canvas-confetti` library
*   **Audio:** HTML5 `<audio>` element

## 🚀 Getting Started

### Prerequisites

*   A modern web browser (Chrome, Firefox, Edge, Safari).
*   Audio files for sound effects.

### Setup

1.  **Clone the repository (or download the files):**
    ```bash
    git clone https://your-repository-url.git
    cd your-project-directory
    ```
    If you downloaded a ZIP, extract it.

2.  **Place Audio Files:**
    Ensure you have the following audio files in the same directory as `index.html`, or update the `src` attribute in the `<audio>` tags within `index.html`:
    *   `spin-sound.mp3` (for the wheel spinning - set to loop)
    *   `tick-sound.mp3` (for the ticking sound)
    *   `win-sound.mp3` (for when a prize is won)

    *You'll need to provide these sound files yourself as they are not included in the HTML snippet.*

3.  **Open in Browser:**
    Open the `index.html` file in your web browser.

## 🎮 How to Use

1.  **Spin the Wheel:**
    *   Click the large "Spin the Wheel!" button at the bottom of the wheel.
    *   The wheel will spin, accompanied by sound effects, and eventually land on a prize.
2.  **View Result:**
    *   A popup will appear displaying the prize you've won.
    *   If you win "Spin Again", the popup button will prompt you to spin once more.
    *   Otherwise, click "Awesome!" or the close button (X) to dismiss the popup.
3.  **Customize the Wheel:**
    *   Click the **cog icon** (⚙️) in the top-right corner to open the Customization Panel.
    *   **Number of Prizes:** Adjust the slider or input field to set how many prizes you want (2-16).
    *   **Prize Details:** For each prize:
        *   **Name:** Enter the text for the prize.
        *   **Color:** Pick a color using the color picker.
        *   **Probability:** Set a value between 0 and 1. The probabilities will be normalized if they don't add up to 1 (or if all are 0, they'll be distributed evenly).
        *   **Delete Prize:** Click the trash icon (🗑️) next to a prize to remove it (minimum 2 prizes).
    *   Click "Apply Changes" to update the wheel.
4.  **Fullscreen Mode:**
    *   Click the **expand icon** (↔️) in the top-right corner to enter fullscreen mode.
    *   Click the **compress icon** (><) to exit fullscreen mode.
5.  **Prize Board:**
    *   The panel on the right (or below on smaller screens in fullscreen) lists all configured prizes and their colors.

## 🎨 Code Highlights

*   **Wheel Rendering (`initWheel()`):**
    *   Dynamically creates wheel segments using `conic-gradient` for colors.
    *   Positions and rotates text labels using CSS transforms, adjusting text placement based on the number of segments for optimal readability.
    *   Implements a threshold (`STACKED_TEXT_THRESHOLD`) for short labels to display them vertically stacked.
*   **Spin Logic (`spinWheel()`):**
    *   Uses CSS `transform: rotate()` and `transition` for smooth spinning animation.
    *   `getWeightedResult()` function determines the winning segment based on configured probabilities.
    *   Calculates rotation degrees including multiple full spins and a random offset for a more natural feel.
*   **Customization (`populateCustomizationForm()`, `applyCustomizationButton`):**
    *   Dynamically generates input fields for each prize.
    *   Handles adding/removing prizes and updates the form accordingly.
    *   Normalizes probabilities upon applying changes.
    *   Re-initializes the wheel with a brief "settling" spin animation.
*   **Fullscreen Styling:**
    *   Uses `:fullscreen` pseudo-class and JavaScript to apply an enhanced, animated background and adjust layout for an immersive experience.
    *   Includes specific CSS animations (`fullscreenPulseAndShift`, `contentEnterFullscreen`) for fullscreen mode.
*   **Sound Management:**
    *   Uses HTML5 `<audio>` elements with `loop` for the spin sound.
    *   Plays tick sounds at intervals during the spin.
    *   Ensures robust playback by catching potential `play()` promise rejections.

## 🔮 Future Enhancements (Ideas)

*   [ ] Option to save/load wheel configurations (e.g., using LocalStorage).
*   [ ] More advanced animation controls (e.g., spin speed, duration).
*   [ ] Different wheel styles or themes.
*   [ ] "No Prize" or "Try Again" segments with distinct styling.
*   [ ] History of wins.
*   [ ] More complex prize types (e.g., image-based prizes).

## 📄 License

This project is open-source. Feel free to use, modify, and distribute it. If you have a specific license in mind (e.g., MIT), you can add it here.

## 👤 Author

*   Designed by **Sadeepa Lakshan** (as per the footer in the HTML).

---

Enjoy spinning the Lucky Wheel!
