# Research Buddy - Web Highlighter & Note Exporter

A lightweight Google Chrome Extension built with Manifest V3 that allows users to highlight important text on web pages, save highlights locally, and export collected notes as Markdown or TXT files.

Research Buddy is designed for students, researchers, developers, and anyone who frequently collects useful information while browsing the web.

Built for the Web Design & Development Lab Mini-Hackathon.

## Features

* Highlight selected text directly on any webpage.
* Save highlights locally using Chrome Storage.
* Automatically restore saved highlights when revisiting a page.
* View highlights for the currently active browser tab.
* Display saved snippets with timestamps.
* Delete individual highlights.
* Clear all highlights from the current page.
* Export saved highlights as TXT files.
* Export saved highlights as Markdown files.
* Include page title, source URL, timestamps, and saved snippets in exported notes.
* Works without external frameworks or heavy dependencies.

## How It Works

Research Buddy uses Chrome Extension APIs to capture selected text from webpages and store it locally.

When a user selects text, the extension creates a visual highlight and saves the selected content along with information about the webpage. When the page is opened again, previously saved highlights can be restored.

The popup provides access to the highlights collected from the active browser tab and allows users to manage or export their notes.

## Technical Architecture

| Component      | File             | Description                                                                            |
| -------------- | ---------------- | -------------------------------------------------------------------------------------- |
| Manifest       | `manifest.json`  | Manifest V3 configuration, permissions, content scripts, and service worker settings.  |
| Service Worker | `background.js`  | Handles extension lifecycle events, storage initialization, and message communication. |
| Content Script | `content.js`     | Detects selected text, applies highlights, and restores saved highlights.              |
| Styles         | `styles.css`     | Provides styling for highlighted content injected into webpages.                       |
| Popup UI       | `popup.html`     | Provides the extension's popup interface.                                              |
| Popup Script   | `popup.js`       | Handles active-tab communication, snippet rendering, deletion, and note exporting.     |
| Test Page      | `test_page.html` | Provides a local webpage for testing the extension.                                    |

## Technologies Used

* HTML5
* CSS3
* Vanilla JavaScript
* Chrome Extension APIs
* Chrome Storage API
* Manifest V3

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/ZainAliT/research-buddy.git
```

### 2. Open Chrome Extensions

Open the following page in Google Chrome:

```text
chrome://extensions/
```

### 3. Enable Developer Mode

Enable the Developer mode option from the top-right corner.

### 4. Load the Extension

Click **Load unpacked** and select the project directory:

```text
Research_Buddy_Chrome_Extension_V3
```

The extension will now be available in Chrome.

### Local File Testing

If you want to test the extension with a local HTML file such as `test_page.html`, open the extension details in `chrome://extensions/` and enable:

**Allow access to file URLs**

## How to Use

### Highlight Text

Open any webpage and select the text you want to save. Research Buddy will highlight the selected text and store it locally.

### View Saved Highlights

Click the Research Buddy extension from the Chrome toolbar to open the popup and view the highlights associated with the current webpage.

### Export Notes

The popup provides options to export saved highlights in two formats:

* TXT for a simple text-based document.
* Markdown for structured notes that can be used with applications such as Notion, Obsidian, or GitHub.

### Manage Highlights

Individual snippets can be deleted from the popup. You can also clear all saved highlights associated with the current webpage.

## Project Structure

```text
Research_Buddy_Chrome_Extension_V3/
├── manifest.json
├── background.js
├── content.js
├── styles.css
├── popup.html
├── popup.js
├── test_page.html
├── icons/
└── README.md
```

## Exported Notes

The Markdown export contains information such as:

* Page title
* Source URL
* Export date
* Total number of highlights
* Saved snippets
* Individual snippet timestamps

This makes the exported notes useful for research documentation, study material, technical references, and personal knowledge management.

## Privacy

Research Buddy is designed to keep saved highlights locally within the browser using Chrome's local storage capabilities. The extension does not require an external backend or database to store highlighted notes.

## Purpose

The project demonstrates practical Chrome Extension development using Manifest V3, browser APIs, DOM manipulation, local storage, message passing, and client-side file generation.

## Author

**Sultan Zaib**

Web Design & Development Lab Mini-Hackathon

## License

This project is developed for educational and learning purposes.
