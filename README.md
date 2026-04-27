<p align="center">
  <pre>
  ████████╗██╗██╗  ██╗    ██╗   ██╗███████╗███████╗██████╗ 
  ╚══██╔══╝██║██║ ██╔╝    ██║   ██║██╔════╝██╔════╝██╔══██╗
     ██║   ██║█████╔╝     ██║   ██║███████╗█████╗  ██████╔╝
     ██║   ██║██╔═██╗     ██║   ██║╚════██║██╔══╝  ██╔══██╗
     ██║   ██║██║  ██╗    ╚██████╔╝███████║███████╗██║  ██║
     ╚═╝   ╚═╝╚═╝  ╚═╝     ╚═════╝ ╚══════╝╚══════╝╚═╝  ╚═╝
  </pre>
</p>

<h1 align="center">🎯 TikTok User Scraper<br><sub>High‑speed multi‑threaded username collector</sub></h1>

<p align="center">
  <strong>Scrape TikTok usernames with >500 followers by performing random keyword searches. 80 parallel threads. Saves results to file.</strong><br>
  <em>Educational project – demonstrates threading, API interaction, and data extraction.</em>
</p>

<p align="center">
  <a href="https://github.com/Ali-Haidar-Sy/Tiktok-User-Scraper/stargazers"><img src="https://img.shields.io/github/stars/Ali-Haidar-Sy/Tiktok-User-Scraper?style=for-the-badge&color=yellow"></a>
  <a href="https://github.com/Ali-Haidar-Sy/Tiktok-User-Scraper/blob/main/LICENSE"><img src="https://img.shields.io/github/license/Ali-Haidar-Sy/Tiktok-User-Scraper?style=for-the-badge&color=blue"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white"></a>
  <a href="https://t.me/P33_9"><img src="https://img.shields.io/badge/Telegram-@P33_9-2CA5E0?style=for-the-badge&logo=telegram"></a>
  <a href="https://www.instagram.com/_ungn"><img src="https://img.shields.io/badge/Instagram-@_ungn-E4405F?style=for-the-badge&logo=instagram"></a>
  <a href="https://github.com/Ali-Haidar-Sy"><img src="https://img.shields.io/badge/GitHub-Ali--Haidar--Sy-181717?style=for-the-badge&logo=github"></a>
</p>

---

## 🔍 What is TikTok User Scraper?

A multi‑threaded Python script that:

- Generates random search queries from multiple character sets (Arabic, Latin, Japanese, Cyrillic…).
- Sends those queries to TikTok’s internal API (`/api/search/user/full/`) **80 threads in parallel**.
- Extracts every returned user’s `unique_id` and `follower_count`.
- Filters and saves only usernames with **more than 500 followers** to `S1.txt`.
- Designed for educational and research purposes only.

---

## ⚡ Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/Ali-Haidar-Sy/Tiktok-User-Scraper.git
cd Tiktok-User-Scraper

# 2. Install the required external libraries
pip install requests user_agent

# 3. Run the scraper
python tiktok_scraper.py
The script runs forever until you stop it (Ctrl+C).
Collected usernames will be appended in real time to S1.txt.

📦 Dependencies
Module	Purpose
requests	HTTP client
user_agent	Random user‑agent generation to avoid fingerprinting
threading, uuid, random	Built‑in – used for concurrency, identifiers, and data randomisation
🧠 How It Works (Technical Flow)
Threaded S1() function – started 80 times.

Each thread:

Picks a random character pool (Arabic, English, Japanese…).

Builds a random keyword (4‑8 characters).

Creates a new TikTok session with a fresh ttwid, device_id, and cookies.

Calls GET /api/search/user/full/ with the keyword and necessary headers/params.

Extracts the user_list from the JSON response.

Checks follower_count > 500 → saves unique_id to S1.txt and prints to console.

The loop continues indefinitely – you control when to stop.

🖥️ Example Output
text
1 : user_example_1 : 3200
2 : another_profile : 12000
3 : cool_tiktoker : 950
...
All saved to S1.txt
⚠️ Ethical & Legal Notice
This tool interacts with TikTok’s internal (non‑public) APIs without authorisation.

Do not use it for spam, harassment, doxxing, or any illegal activity.

Do not violate TikTok’s Terms of Service.

This script is provided strictly for educational purposes – to learn threading, HTTP requests, and data parsing.

The author assumes zero liability for any misuse or damage caused by this software.

If you are unsure whether your use case is lawful, do not run this tool.

🛡️ Disclaimer
text
This project is not affiliated with TikTok, ByteDance, or any related entities.
All trademarks belong to their respective owners.
🤝 Contributing
Bug reports, feature requests, and pull requests are welcome!
Please open an Issue first to discuss any major changes.

📞 Connect With Me
Platform	Handle
GitHub	Ali-Haidar-Sy
Telegram	@P33_9
Instagram	@_ungn
<p align="center"> <strong>🎯 If this scraper helped you, give it a ⭐!</strong> </p> ```
