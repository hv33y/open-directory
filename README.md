# Open Directory Finder

A high-efficiency web utility for generating advanced search queries to locate publicly accessible file directories. This tool automates the construction of Google Dorks, specifically targeting server indexes to find direct download links for media, software, and documents.

---

## Project Overview

Open Directory Finder provides a streamlined interface to bypass standard search engine results and isolate "Index of" pages. By utilizing category-specific file extensions and advanced search operators, the application delivers high-precision results for users seeking raw file access without navigating through intermediary landing pages or advertisements.

---

## Search Logic and Google Dorking

The application’s core engine generates standardized query patterns optimized for modern search engine algorithms:

```bash
intitle:"index of" +({extensions}) -inurl:(jsp|pl|php|html|aspx|cgi) "last modified"
```

### Technical Logic Breakdown

- **Index Targeting**: Uses `intitle:"index of"` to filter for server-generated directory listings.
- **Extension Filtering**: Appends targeted file formats (e.g., `.mkv`, `.iso`, `.pdf`) to narrow the scope.
- **Noise Reduction**: Employs `-inurl:` operators to exclude common web scripts (PHP, ASPX, JSP) and SEO-optimized landing pages.
- **Server Verification**: Includes the `"last modified"` string to confirm the result is a standard Apache, Nginx, or IIS directory index.

---

## Key Search Categories

- **Video & Movies**: MKV, MP4, AVI, MOV, WMV, VOB, MPG  
- **Audio & Music**: MP3, FLAC, WAV, OGG, M4A, WMA, AAC  
- **Software & Games**: ISO, EXE, DMG, MSI, APK, BIN, RAR, ZIP, 7Z  
- **Digital Documents**: PDF, EPUB, MOBI, AZW3, DOCX, CBR, CBZ  
- **High-Res Images**: JPG, PNG, GIF, TIFF, SVG, PSD, RAW  

---

## Project Architecture

```text
.
├── .github/workflows/   # CI/CD deployment configurations
├── index.html           # Core search engine logic and UI
└── README.md            # Technical documentation and SEO metadata
```

---

## Technical Specifications

- **Zero-Dependency**: Built with vanilla HTML5, CSS3, and JavaScript  
- **Client-Side Execution**: All query generation happens in the browser to ensure user privacy  
- **Cross-Browser Compatibility**: Fully optimized for Chrome, Firefox, Safari, and Edge  
- **Deployment**: Automated via GitHub Actions for seamless hosting on GitHub Pages  

---

## Usage and Implementation

### Production Environment

Live URL: https://hv33y.github.io/open-directory/

## Contributing

1. Fork the repository  
2. Create a feature branch (`git checkout -b feature/optimization`)  
3. Commit your changes (`git commit -m "Add archive extension support"`)  
4. Push to the branch (`git push origin feature/optimization`)  
5. Open a Pull Request  

---

## Disclaimer

> This utility is intended for educational purposes and for locating publicly available information.  
> Users are responsible for complying with local copyright laws and ensuring they have the legal right to access content discovered through third-party directories.  
> The developer assumes no liability for misuse.

---

## License

Distributed under the MIT License.
