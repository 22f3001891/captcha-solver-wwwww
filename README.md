# Image OCR Demo (for your own images)

Overview
- This single‑page web app loads an image from a URL parameter or local file and extracts visible text using Tesseract.js (on‑device OCR in your browser).
- It includes optional preprocessing (thresholding, invert, light sharpen) to improve recognition on high‑contrast, simple images.
- Ethical use only: This tool is intended for accessibility, QA, and processing images you own or have permission to analyze. Do not use it to defeat third‑party anti‑bot challenges or violate any terms of service.

License
- MIT License (see full text below).

Setup
- No build steps required.
- Files:
  - index.html (app)
  - README.md (this document)

Run locally:
- Simply open index.html in a modern browser (Chrome, Edge, Firefox, Safari).
- The app will auto‑load a synthetic sample image on first load.

Usage
1. Load an image:
   - Query parameter:
     - Append ?url=https://your-domain.com/path/to/image.png to the page URL, e.g.:
       - file:///.../index.html?url=https://example.com/sample.png
   - Paste an image URL into the input box and press “Load”.
   - Click “Choose File” or drag and drop a local image.
   - “Use Sample” inserts a synthetic, high‑contrast test image.

2. Preprocess (optional):
   - Enable “Preprocess (threshold)”. Adjust the threshold slider; optionally toggle Invert and Sharpen.
   - If the image is cross‑origin without CORS, the browser will prevent pixel access; preprocessing will be disabled and a note will appear.

3. Solve:
   - Click “Solve” to run OCR. Progress and status are displayed during recognition.
   - Click “Copy” to copy the recognized text.

Notes and tips:
- Cross‑origin images: For best results with remote URLs, serve images with CORS headers (Access-Control-Allow-Origin: *) to enable preprocessing. Otherwise, use local files or same‑origin URLs.
- Language: The default language is English (eng). This page is kept minimal; for advanced scenarios you could extend it to load other languages supported by Tesseract.js.
- Accessibility: This can aid reading text from images for users and automated testing of your own systems.

Security and ethics
- Do not use this tool to bypass anti‑bot systems, account protections, or other safeguards on services you do not own.
- Ensure you have rights to process any image you load.

Full MIT License
Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.