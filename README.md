## 🎉 RxPad Prescriber v1.3.0 — First Public Freeware Release

**RxPad** is an offline-first Windows desktop app for small clinics to compose prescriptions, keep patient history, and print tidy PDFs.

**Freeware notice:** RxPad Prescriber is **freeware**. No one is authorized to charge you for the software. Distribution is intentionally restricted by per-device activation to ensure it reaches intended users—please contact me for activation (details below).

---

### ✨ Highlights
- **Offline-first:** Works fully offline after activation.
- **Clean PDFs:** Professional Rx printouts using ReportLab.
- **Local data:** Per-user SQLite database; no admin rights required.
- **Automatic backups:** On open and exit.
- **Simple UI:** Fast, clinic-friendly workflow.

> ⚠️ **Backup disclaimer:** RxPad makes local automatic backups, but **this is not a guarantee** against data loss. Disk or OS failures can still cause issues. You are responsible for keeping copies in safe locations. A future version will add optional cloud backup targets (OneDrive/Google Drive).

---

### 🔐 Activation (freeware, restricted distribution)
1. Install and run RxPad; open **License** from the top bar.
2. **Copy your HWID**.
3. **Contact me** via the in-app **Report a bug / Contact** option (or the contact info in this release) to request activation for your device.
4. You’ll receive a **`license.jwt`** file. Import it on the License page → status shows **Activated**.

*Token format: Ed25519 (alg=EdDSA); claims include `iss="rxpad-licenser"`, `aud="rxpad"`, `sub=HWID`, `exp=<timestamp>`.*

---

### 🆕 What’s new in v1.3.0
- **Token-only activation:** Removed legacy GitHub-based activation. The app verifies a signed token **entirely offline**.
- **PDF viewer flow:** New “Open” (viewer page) and direct **PDF** links from patient history.
- **Patient history fix:** Quick history panel now loads reliably with correct links.
- **UI polish:** Composer button styles scoped; bug modal buttons consistent.
- **Cleanup:** Removed redundant imports and old code paths.

---

### 🖥️ System requirements
- Windows 10/11 (x64)
- Internet only for **install time** if WebView2 runtime isn’t present (installer will fetch the Evergreen bootstrapper). App usage is **offline** post-activation.

---

### 📦 Install & update
- Run the setup EXE.
- No admin rights needed (per-user install).
- To update, just run the newer installer—your data and token remain in.

**Uninstall:** Use Windows “Apps & features”. User data persists at .

---

### 🔏 Privacy & security
- **No telemetry.** No background network calls after activation.
- License verification is **fully offline** with the embedded Ed25519 public key.
- Only the **public key** ships with the app; private keys never leave the licenser machine.

---

### 🐞 Support & feedback
- Use **Help → Report a bug** from inside the app (includes helpful context).
- Or contact: **<add your preferred contact here>**.

If you find this useful and would like to support development, you can **donate**:  
**<add UPI / PayPal / BuyMeACoffee link here>**

---

### ⚖️ Legal
This software is **freeware**. It is provided “**as is**” without warranties of any kind. By using it, you agree you are responsible for your data and backups. See `FREEWARE_LICENSE.txt` in the release for full details.
