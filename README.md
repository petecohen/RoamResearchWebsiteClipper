# RoamResearchWebsiteClipper
Roam Research Quick Capture Bookmarklet

This bookmarklet allows you to quickly capture selected text from any webpage and format it for easy pasting into Roam Research, complete with source attribution.

## How to Use

1. **Create a Bookmark:**
   - Bookmark any page in your browser (the actual page doesn't matter).

2. **Edit the Bookmark:**
   - Right-click on the newly created bookmark.
   - Select "Edit" or "Properties" (depending on your browser).

3. **Replace the URL:**
   - In the URL or address field, paste the following code:
     ```javascript
     javascript:(function(){     let text = window.getSelection().toString() || "";     let formattedText = `__${text.trim()}__ - via ${document.title} ${location.href}`;     prompt("Press CTRL+C or CMD+C, then escape and paste into Roam.", formattedText); })()
     ```

4. **Name Your Bookmark:**
   - Change the name to something meaningful like "Roam Capture" or "To Roam".

5. **Position for Easy Access:**
   - Move the bookmark to your bookmarks bar for quick access.

## Using the Bookmarklet

1. Navigate to any webpage and select the text you want to capture.
2. Click your newly created bookmarklet.
3. A prompt will appear with the formatted text. Press CTRL+C (Windows) or CMD+C (Mac) to copy.
4. Press Escape to close the prompt.
5. Paste the copied text into your Roam Research graph.

## What It Does

- Captures selected text from the current webpage.
- Formats the text with double underscores for Roam's bold formatting.
- Adds attribution including the page title and URL.
- Presents the formatted text in a copy-friendly prompt.

## Note

- If no text is selected, the bookmarklet will still run, allowing you to manually enter text in Roam with the current page's attribution.
- The double underscore format (`__text__`) creates bold text in Roam Research.

## Compatibility

Works with most modern browsers that support JavaScript's `window.getSelection()` method.

## License

[MIT License](LICENSE)

---

Modified by Pete Cohen. I built on the work of some else (sorry, I can't remember who!) and iterated on it with Claude Sonnet 3.5
