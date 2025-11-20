# Nail Salon Integrated System — Project Overview & Quick Start

Project summary  
This repository contains a static website collection presenting information for multiple nail salons (individual HTML pages per salon) and a Java Swing sample application demonstrating a small restaurant ordering system. The site is intended for informational/demo purposes; the Java application is a local desktop example for menu, ordering, discounts and order history.

Repository layout (important files)
- index.html — project home page (links to salon pages)  
- page1.html … page12.html — individual salon pages (info, booking rules, price lists, reviews)  
- images/ or images2/ — image assets (ensure file names and paths match exactly)  
- RestaurantOrderingSystem.java — Java Swing sample application (requires JDK 17+)  
- README.md — this file

End-user quick start (view site locally)
- Option A — Open locally: double-click `index.html` to open in your browser.  
  Note: some browsers restrict local resource loading — use a local server if you see broken assets.
- Option B — Run a lightweight HTTP server (recommended):
  - Python 3: `https://jenny-1014.github.io/Nail_Salon_Integrated_System/index.html` → open http://localhost:8000  
  - Node (http-server): `[npx http-server -p 8000](https://jenny-1014.github.io/Nail_Salon_Integrated_System/index.html)` → open http://localhost:8000

Java sample: Restaurant Ordering System (developer)
- Purpose: Demonstrates a desktop ordering workflow (menu categories, add items, quantity, subtotal, discounts, order number, and order history).
- Requirements: JDK 17 or later (the source uses `record` and modern switch expressions).
- Compile & run (command line):
  1. Open a terminal at the project root:  
     `cd "c:\Users\user\Desktop\美甲\Nail_Salon_Integrated_System"`
  2. Compile: `javac RestaurantOrderingSystem.java`
  3. Run: `java RestaurantOrderingSystem`
- In an IDE: import the file into an IntelliJ/Eclipse project and set Project SDK to JDK 17+, then run the `main` method.

Packaging & releasing (maintainer)
- For static site distribution: create a zip of `index.html`, all `page*.html` and the `images/` directories. Example (macOS / Linux):  
  `zip -r release/build-v1.0.0.zip index.html page*.html images/`
- Windows PowerShell example:  
  `New-Item -ItemType Directory -Path release -Force`  
  `Compress-Archive -Path .\index.html, .\page*.html, .\images\* -DestinationPath .\release\build-v1.0.0.zip`
- GitHub Releases: tag the repo and upload the zip, or use `gh release create` to automate.

Important implementation notes
- Paths and case sensitivity: file names and paths must match exactly. Use forward slashes (`/`) in HTML (`images2/12_ej_nail.png`). Linux and many hosting environments are case-sensitive.  
- Filenames: avoid spaces and non-ASCII characters; prefer `snake_case` or `kebab-case`.
- Local data: several salon pages store reviews in browser `localStorage` — clearing browser storage will delete those reviews.

Troubleshooting (common issues)
- Missing images: verify the file exists at the exact path used in HTML and confirm extension and case match.  
- Java compile errors: ensure `java -version` reports JDK 17+. Confirm file name is `RestaurantOrderingSystem.java` and no spaces are in the filename.  
- GUI not responding: close the window or terminate the Java process (e.g., Task Manager on Windows).

Testing recommendations
- Static pages: view each `pageN.html` in a server environment and verify images, links and the "Back to Home" link go to `index.html`.  
- Java sample: exercise adding items, merging same items, applying discounts, and validating order history entries.

Contributing
- Issues and pull requests are welcome. For PRs: describe the change, include testing instructions, and ensure asset paths remain correct.

License & contact
- Add a LICENSE file (recommended: MIT) and include contact information or issue guidelines on the repository page.
