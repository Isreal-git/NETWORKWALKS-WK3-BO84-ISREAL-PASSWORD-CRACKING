#  Week 3: Password Cracking Methodologies (JTR & Networkwalks)

##  Overview
This repository documents my completion of **Week 3 Project Modules (W3-PM1 & W3-PM2)** for my Cybersecurity & Ethical Hacking training. 

The objective of these labs was to recover the password of an encrypted PDF file (`My Locked PDF1.pdf`). To demonstrate versatility and a deeper understanding of password recovery, I successfully cracked the file using **two different methodologies**:
1. **Offline Cracking:** Using John the Ripper (JTR) and its GUI, Johnny, on Windows.
2. **Online Web-Based Cracking:** Using the Networkwalks Hash Calculator and Password Cracker.

##  Tools Used
*   **John the Ripper (JTR) & Johnny GUI** - Command-line and graphical interface for offline password cracking.
*   **Networkwalks Hash Calculator & Password Cracker** - Web-based tools for hash extraction and cracking.
*   **OnlineHashCrack PDF Extractor** - Web-based hash extractor used for the JTR module.
*   **Windows OS** - Lab environment.

---

##  Module 1: Password Cracking with JTR (W3-PM1)

###  Lab Walkthrough
1.  **Installation & Setup:** Downloaded and extracted the official John the Ripper Windows package. Installed the Johnny GUI and pointed it to the `john.exe` executable in the `run` directory.
2.  **Hash Extraction:** Uploaded `My Locked PDF1.pdf` to the OnlineHashCrack tool to extract the `$pdf$` hash.
3.  **Cracking the Password:** Saved the hash to `hash1.txt`, loaded it into Johnny, and successfully ran the attack to recover the password.
4.  **Verification:** Opened the PDF using the cracked password.

###  Troubleshooting (The Learning Curve)
During the Windows setup, I encountered the error: `The code execution cannot proceed because cygwin1.dll was not found`. 
*   **The Fix:** I realized Johnny was initially pointed to the unextracted `.zip` folder rather than the actual `john.exe` application. By properly extracting the archive and ensuring all `.dll` files (including `cygwin1.dll`) were in the same `run` directory, the tool executed flawlessly. This taught me valuable lessons in environment management and DLL dependencies.

---

##  Module 2: Password Cracking with Networkwalks Tools (W3-PM2)

###  Lab Walkthrough
1.  **Hash Extraction:** Used the web-based **Networkwalks Hash Calculator** to upload `My Locked PDF1.pdf` and extract the password hash.
2.  **Cracking the Password:** Copied the complete `$pdf$` hash and pasted it into the **Networkwalks Password Cracker** web tool.
3.  **Verification:** The tool successfully recovered the 3-character plaintext password in seconds. I verified this by opening the locked PDF.

---

##  Key Takeaways
*   **Methodology Comparison:** Learned how to approach the same problem from both an offline tool perspective (JTR) and a web-based accessible perspective (Networkwalks).
*   **Hashing vs. Encryption:** Reinforced the concept that hashing is a one-way function. We don't "decrypt" a hash; we crack it by guessing passwords, hashing the guesses, and comparing the outputs.
*   **Password Complexity:** The rapid cracking of a 3-character password perfectly illustrates why simple passwords are extremely vulnerable to modern brute-force and dictionary attacks.

---
*Disclaimer: These labs were completed in a controlled, educational environment for ethical hacking and cybersecurity training purposes only.*

<br>

## ✍️ AUTHOR
**👤 Author:** ALABI ISREAL   
**Role:** Cybersecurity Intern B084  
**LinkedIn:** www.linkedin.com/in/alabi-isreal-bab9b8432

### 📌 Project Information
*   **Program Name:** Cybersecurity program at Networkwalks
*   **Week:** 03
*   **Repository:** GitHub
