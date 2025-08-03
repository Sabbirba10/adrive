# ADrive

ADrive is a modern web-based file manager for Cloudflare R2, featuring a serverless backend powered by Cloudflare Pages and Workers. It provides a user-friendly interface for uploading, organizing, and sharing files, with support for large file uploads, thumbnails, and WebDAV access.

## Features

- **Large File Uploads:** Supports chunked uploads for files larger than 100MB.
- **Create Folders:** Organize your files in directories.
- **Search:** Quickly find files by name.
- **Image/Video/PDF Thumbnails:** Preview your media files with generated thumbnails.
- **WebDAV Endpoint:** Access your files using any WebDAV client.
- **Drag and Drop Upload:** Easily upload files by dragging them into the browser.
- **TextPad:** Create and upload text notes directly from the web interface.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [Cloudflare account](https://dash.cloudflare.com/) with R2 enabled

### Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/Sabbirba10/adrive.git
   cd adrive
   ```

2. **Install dependencies:**

   ```sh
   npm install
   ```

3. **Configure Cloudflare R2 and Workers:**

   - Set up your R2 bucket and Workers environment variables as needed.

4. **Start the development server:**

   ```sh
   npm start
   ```

5. **Build for production:**
   ```sh
   npm run build
   ```

## WebDAV Endpoint

You can use any WebDAV client (such as [Cx File Explorer](https://play.google.com/store/apps/details?id=com.cxinventor.file.explorer) or [BD File Manager](https://play.google.com/store/apps/details?id=com.liuzho.file.explorer)) to access your files.

- **Endpoint URL:** `https://<your-domain>/webdav`
- **Username/Password:** Set via environment variables

> **Note:** Standard WebDAV clients may not support large file uploads (≥128MB) due to Cloudflare Workers limitations. Use the web interface for large files.

## Project Structure

- `src/` — Frontend React application
- `functions/webdav/` — Cloudflare Pages Functions (WebDAV API)
- `utils/` — Utility modules
- `public/` — Static assets

## License

[MIT](https://github.com/Sabbirba10/adrive/blob/main/LICENSE)

---

**ADrive** is free and open source. Developed by [Sabbir Bin Abbas](https://github.com/Sabbirba10/).
