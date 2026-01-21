# 📂 Google Drive Asset Automator

**A Python-based automation engine for batch file retrieval and recursive folder traversal via Google Drive API.**

## 📖 Overview
This script was developed to solve a massive logistical bottleneck within the **Aum.Music** project. Upon reaching the **100th playlist milestone**, I needed to create a celebratory collage featuring the cover art from every previous release. 

## ⚖️ The Challenge
Managing assets for 100+ individual playlists manually was no longer feasible:
* **Complex Structure:** Each playlist had its own folder containing multiple file types: raw assets, WIP edits, metadata (CSV/Text), and the final publish-ready cover.
* **Volume:** Navigating 100+ nested folders on Google Drive to manually identify and download the correct "final" version of each image would have taken several hours of error-prone work.
* **Selection Logic:** The script needed to intelligently distinguish between different versions of images within the same folder.

## 💡 The Solution
I built a Python automation engine that leverages the **Google Drive API** to do the heavy lifting:
1.  **Service Account Integration:** Implements secure, non-interactive authentication for automated cloud access.
2.  **Recursive Traversal:** Automatically crawls through the entire directory tree.
3.  **Smart Versioning Logic:** Identifies and selects the most recently updated image relevant to each playlist, ensuring only the "Final" version is retrieved.
4.  **Local Sync:** Streamlines the download process directly to a predefined local directory on a personal computer.

## 🚀 Results
* **Efficiency:** The script identified, filtered, and saved **95 out of 100** target images in **under 30 minutes**.
* **Accuracy:** Eliminated human error in version selection and file naming.
* **Scalability:** The logic is now modular and can handle the next milestone (900+ playlists) with zero extra effort.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **API:** Google Drive API (v3).
* **Libraries:** `google-api-python-client`, `google-auth`.
* **Authentication:** OAuth 2.0 Service Account flow.

## ⚙️ Usage
1.  **Prerequisites:** Python 3 and a Google Cloud Project with Drive API enabled.
2.  **Setup:** Place your service account `key.json` in the root directory.
3.  **Configure:** Set `KEY_PATH` and `DOWNLOAD_PATH` within `scratch_drive.py`.
4.  **Run:**
    ```bash
    python scratch_drive.py
    ```

## ⚠️ Disclaimer
*This utility was designed for internal asset management and workflow optimization. Ensure your service account has the necessary permissions for the target directories.*

---
*Created by Chagai Yechiel*
