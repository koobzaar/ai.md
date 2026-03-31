# **Gemini Transcript Exporter (LLM Optimized)**

A Userscript designed to export full Google Gemini conversations into a highly structured, strict Markdown format specifically engineered for ingestion by other Large Language Models (LLMs). 

## **Features**

* **LLM-Optimized Syntax:** Uses strict boundaries (::USER\_MESSAGE::, ::MODEL\_REASONING::, ::MODEL\_RESPONSE::) instead of standard Markdown headers to prevent parsing collisions.  
* **System Directive Injection:** Automatically prepends a system prompt to the exported document, instructing the consuming LLM on how to parse the file.  
* **Reasoning Extraction:** Automatically expands and extracts Gemini's internal "thought process" or reasoning blocks, keeping them distinct from the final response.  
* **Native UI Integration:** Injects a seamless, non-intrusive pull-out drawer on the right side of the screen that matches Gemini's native typography and color scheme (Google Sans, Material Design).  
* **Deep-Scroll Loading:** Bypasses Angular's lazy-loading by programmatically scrolling to the top of the chat history and waiting for all conversation blocks to render before exporting.  
* **Collision-Free Filenames:** Generates precise, timestamped filenames (e.g., Conversation\_Title\_2023-10-27\_14-30-00.md) to prevent overwriting when exporting a progressing conversation multiple times.

## **Installation**

1. Install a Userscript manager extension for your browser (e.g., [Tampermonkey](https://www.tampermonkey.net/) or [Violentmonkey](https://violentmonkey.github.io/)).  
2. Create a new script in your extension.  
3. Copy the contents of [gemini-transcript-exporter.user.js](https://www.google.com/search?q=https://github.com/koobzaar/gemini.md/blob/main/gemini-transcript-exporter.user.js) and paste it into the editor.  
4. Save and enable the script.

## **Usage**

1. Open a conversation in [Google Gemini](https://gemini.google.com/).  
2. Look to the middle-right edge of your screen for a small ◀ tab.  
3. Hover over the tab to slide out the **"Export .md"** button.  
4. Click the button. The script will briefly display "Loading...", scroll through your history to ensure all messages are loaded, expand any reasoning panels, and then download your .md file.
