# QR Code Generator

Generate QR codes from text or URLs using a free external API.
https://harshh-2.github.io/QR-Code_Generator/
## Features

- Simple, user-friendly interface
- Generates QR codes instantly
- No dependencies or external libraries
- Input validation for empty entries



## File Structure

├── index.html # HTML markup
├── style.css # Stylesheet
└── function.js # JavaScript logic


## Code Snippet

```js
function generateQRcode() {
  const input = document.getElementById("qrInput").value.trim();
  if (!input) {
    alert("Please enter text or URL to generate QR code");
    return;
  }
  const apiURL = `https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=${encodeURIComponent(input)}`;
  document.getElementById("qrcodeimage").src = apiURL;
}
```
Notes
Uses QRServer API for QR code generation.

Data is sent over HTTPS, but avoid sensitive information.

For privacy-focused applications, consider local QR code libraries.
