# Windows Privilege Escalation Techniques

## Disclaimer
**This repository is for educational and research purposes only.** Unauthorized use of these techniques on systems without explicit permission is illegal and unethical. Always test security measures in controlled environments, such as personal labs or legal penetration testing engagements.

---

## Table of Contents
- [Introduction](#introduction)
- [Bypassing UAC](#bypassing-uac)
- [Brute Force Attacks](#brute-force-attacks)
- [Fake UAC Prompt](#fake-uac-prompt)
- [Executable UAC Bypass](#executable-uac-bypass)

---

## Introduction
This guide explores different privilege escalation techniques that can be used for security research, penetration testing, and ethical hacking. **Do not use these methods on unauthorized systems.**

---

## Bypassing UAC
User Account Control (UAC) is a Windows security feature designed to prevent unauthorized system changes. However, security researchers analyze UAC bypass techniques to identify potential vulnerabilities and improve system defenses. Below are some research-based techniques for ethical security testing.

### 1. Brute Force Attacks
Brute force attacks involve systematically trying multiple username-password combinations to gain access to an account. These attacks demonstrate the importance of strong passwords and proper authentication mechanisms.

#### Steps:
1. Run the `userbruteforce.bat` script.
2. Press `1` and select the target account.
3. Press `2` and enter the target's username.
4. Provide a password list (default: `passlist.txt`).
5. Wait for the script to attempt authentication.

**Note:** If the script stops unexpectedly, it may be due to special characters (`! > < | ^`) in the password being tested. Remove that attempt from the password file and restart. Always perform testing in authorized environments.

---

### 2. Fake UAC Prompt
A fake UAC prompt can be used to demonstrate how attackers can deceive users into providing administrator credentials. Security professionals study these techniques to improve user awareness and design countermeasures against phishing attempts.

#### Steps:
1. Close any open Command Prompt windows.
2. Run `main.vbs`.
3. Hide the folder to prevent detection.
4. Request administrator input for testing purposes.
5. If credentials are entered, access is granted.
6. **If you want to terminate this action, run the `Repair.dll` file.**

**Warning:** This method is strictly for ethical research and security awareness training. Never use it for unauthorized access.

---

### 3. Executable UAC Bypass
Some Windows installers have the UAC shield icon, indicating they require elevated privileges. Security researchers analyze these installers to identify potential privilege escalation opportunities and develop defensive strategies.

#### Steps:
1. Download a legitimate installer with the UAC shield logo.
2. Drag the installer onto `bypass.bat`.
3. The script will attempt to execute the process with elevated privileges.
4. If antivirus software blocks `bypass.bat`, use `newbypass.bat` instead.

**Note:** Many modern antivirus programs detect and block such techniques. Ethical hackers and security researchers should focus on understanding and mitigating these threats.

---

## Ethical Considerations
These techniques should only be used in legally authorized penetration tests or personal lab environments. Misuse of these methods could result in legal consequences.

For ethical hacking certifications and legal testing environments, consider:
- **TryHackMe** ([https://tryhackme.com](https://tryhackme.com))
- **Hack The Box** ([https://www.hackthebox.com](https://www.hackthebox.com))
- **Offensive Security Certified Professional (OSCP)**

---

## License
This project is intended for ethical research and education only. By using this repository, you agree to use these techniques responsibly.

