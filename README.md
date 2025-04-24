# Unicode Character Cleaner

A simple, client-side web tool to inspect strings for hidden or non-printable Unicode characters (like Zero-Width Spaces, BOM, control characters), visualize them, clean the string based on standard printable characters, and copy the result.

It runs **entirely in your browser** using HTML, CSS, and vanilla JavaScript. No data is ever sent to a server.

## Features

*   **Paste & Analyze:** Paste any text into the input area.
*   **Visual Character Breakdown:** See every character in the string represented visually in the "Character Analysis" section.
    *   Regular printable characters (Letters, Numbers, Punctuation, Symbols) are shown normally.
    *   Standard whitespace (Space, Tab) is shown with distinct symbols (`·`, `⟶`).
    *   Line endings (CR, LF) are shown as symbols and trigger visual line breaks.
    *   Other non-printable characters (control characters, format characters, ZWSP, BOM, etc.) are displayed using their Unicode Hex code (`U+XXXX`).
*   **Detailed Tooltips:** Hover over any character representation in the analysis area to see:
    *   Decimal code point (`&#...;`)
    *   Unicode escape sequence (`\uXXXX`)
    *   Hex code point (`U+XXXX` or `0xXX` for ASCII)
    *   Common names for well-known non-printables (e.g., "Zero Width Space", "BOM").
*   **Character & Byte Counts:** See the total number of characters (correctly handling multi-byte characters) and the UTF-8 byte count for the input string.
*   **Clean Text:** Click the "Clean Text" button to remove characters that are *not* standard printables (`\p{L}\p{M}\p{N}\p{P}\p{S}`) or basic whitespace (Space, Tab, CR, LF). The input box is updated with the cleaned text.
*   **Copy Text:** Click the "Copy Text" button to copy the *current* content of the input text area to your clipboard.
*   **Client-Side Privacy:** Operates 100% within your browser. Your input text is never transmitted anywhere.
*   **Modern Dark Theme:** Easy-on-the-eyes interface.

## How to Use

1.  **Get the File:** Download the `index.html` file from this repository.
2.  **Open:** Open the `index.html` file directly in your preferred web browser (like Chrome, Firefox, Safari, Edge).
3.  **Paste:** Paste the text string you want to analyze into the input text area.
4.  **Analyze:** Click the "Analyze Text" button (or the analysis might update automatically on load/input). The detailed character breakdown will appear below.
5.  **Inspect:** Hover over characters in the "Character Analysis" section to view their details in tooltips.
6.  **Clean (Optional):** Click "Clean Text" to remove hidden/non-printable characters from the input box. The analysis will update automatically.
7.  **Copy (Optional):** Click "Copy Text" to copy the current contents of the input box to your clipboard.
8.  **Clear (Optional):** Click "Clear Input" to empty the text box and the analysis area.

## Technology

*   HTML5
*   CSS3 (including CSS Variables for theming)
*   Vanilla JavaScript (ES6+) - no external libraries or frameworks.

## Privacy Guarantee

This tool is designed with privacy as a priority.
*   **100% Client-Side:** All processing happens within your browser.
*   **No Data Transmission:** The text you enter is **never** sent to any server or external service.
*   **No Storage:** No cookies are used, and no data is stored locally or remotely.

## Running / Deployment

*   **Local Use:** Simply open the `index.html` file in a browser.
*   **Web Deployment:** As this is a single static HTML file, you can host it on any static web hosting service (like GitHub Pages, Netlify, Vercel, AWS S3, Cloudflare Pages, etc.) or serve it from any standard web server. No special backend is required.

## Motivation

This tool was created as a static, client-side alternative to server-based tools for viewing hidden characters, ensuring user privacy and ease of use/deployment. It draws inspiration from similar online utilities while focusing on a pure JavaScript implementation.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](link-to-your-repo/issues) (replace this link).

## License

Distributed under the MIT License. See `LICENSE` file for more information.

