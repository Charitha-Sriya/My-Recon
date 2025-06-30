# MyRecon
My Recon tools help gather domain info like IP addresses, DNS records, and HTTP headers. Traceroute shows network paths. crt.sh finds subdomains via SSL data. Google search reveals indexed pages. Together, these tools map a target's online footprint for security analysis.
# 🔍 MyRecon – Web-Based Reconnaissance Toolkit

MyRecon is a lightweight web-based recon tool designed for quick domain reconnaissance using common Linux utilities. It helps ethical hackers and researchers gather valuable information like IP addresses, DNS records, subdomains, HTTP headers, and more — all from a simple web interface.

---

## 📸 Screenshots

### Home Interface
![Home Page](![image](https://github.com/user-attachments/assets/69832d34-28f7-4575-92a3-cec5482e16e6))
### Sample Report
![Report Page](https://user-images.githubusercontent.com/YOUR_USERNAME/REPORT_IMAGE.png)

---

## ⚙️ Features

- 🌍 IP address resolution
- 🧭 Traceroute path mapping
- 📡 WHOIS information extraction
- 🌐 DNS record enumeration
- 📝 HTTP header inspection
- 🔐 Subdomain discovery via crt.sh
- 🔍 Google dork-style title fetch (limited)

---

## 📁 Project Structure

```
MyRecon/
├── index.html      # User input form
├── run.php         # Executes recon and returns HTML report
├── recon.sh        # Bash script performing recon tasks
└── recon-<domain>/ # Folder where report is saved
```

---

## 🚀 How to Use

1. 🖥️ **Install Prerequisites:**
   Ensure the following tools are available on your Linux system:
   ```
   dig, whois, curl, traceroute
   ```

2. 🧪 **Run Locally (e.g., with XAMPP or Apache+PHP):**
   - Copy files into your server's `htdocs/` folder
   - Access `http://localhost/MyRecon/` in your browser

3. 📬 **Enter a domain name** in the input field and click “Run Recon”

4. 📄 **View report** generated in `recon-<domain>/report.html`

---

## 🛠 Tools Used in Recon

| Task                  | Tool     | Description |
|-----------------------|----------|-------------|
| IP Lookup             | `dig`    | Resolves domain to IP address |
| WHOIS Information     | `whois`  | Shows domain ownership & registrar |
| DNS Records           | `dig`    | Retrieves MX, NS, TXT records etc. |
| Traceroute            | `traceroute` | Maps network hops to server |
| HTTP Headers          | `curl -I`| Shows server info, security headers |
| Subdomain Discovery   | `crt.sh` | Extracts from SSL cert logs |
| Google Dorking        | `curl`   | Fetches indexed titles from Google (limited) |

---

## 🛡️ Disclaimer

This tool is for **educational and ethical purposes only**. Use it on domains you own or have permission to test.

---

## 👨‍💻 Author

- [Charitha-Sriya]([https://github.com/Charitha-Sriya])
- Feel free to star ⭐ the repo if you find it helpful!

---

## 📄 License

MIT License – Use freely, modify responsibly.
