# QR & Barcode Reader

A lightweight, single-page web application for scanning QR codes and barcodes directly from a device camera, with no backend or build step required.

## Features

- 📷 Real-time QR code and barcode scanning via device camera
- 🔍 Supports multiple barcode formats (QR Code, EAN-13, and more)
- ⚡ Fast detection at 20 frames per second
- 🛑 Automatically stops scanning after a successful read
- 🌐 Runs entirely in the browser — no installation needed

## Demo

Open `index.html` in a web browser that supports the [MediaDevices API](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices) (e.g., Chrome, Firefox, Edge on a device with a camera).

## Usage

1. Clone or download this repository.
2. Open `index.html` in a modern web browser.
3. Click the **Scannear** button to activate the camera.
4. Point the camera at a QR code or barcode.
5. The decoded value will appear in the text field.

> **Note:** Camera access requires a secure context (`https://` or `localhost`).

## Tech Stack

| Technology | Details |
|---|---|
| HTML5 | Application structure and camera access |
| JavaScript (Vanilla) | Application logic |
| [html5-qrcode](https://github.com/mebjas/html5-qrcode) v2.0.9 | QR/barcode scanning library (loaded via CDN) |

## Project Structure

```
qr-barcode-reader/
├── index.html        # Main application
└── response.json     # Sample scan result
```

## Sample Output

After a successful scan, the decoded result is displayed in the input field and logged to the browser console:

```json
{
  "decodedText": "7758574003035",
  "result": {
    "text": "7758574003035",
    "format": {
      "format": 9,
      "formatName": "EAN_13"
    }
  }
}
```

## Browser Compatibility

Any modern browser that supports the [MediaDevices.getUserMedia()](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia) API:

- Google Chrome 53+
- Mozilla Firefox 36+
- Microsoft Edge 12+
- Safari 11+

## License

This project is open source. See the repository for details.

## Author

**Rafnix Guzmán** — [@rafnixg](https://github.com/rafnixg)
