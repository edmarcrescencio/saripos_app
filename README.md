# SariPOS Official Website & Documentation Portal

Official website, documentation hub, and APK release center for **SariPOS** — the 100% offline-first Point of Sale (POS) and inventory management application architected specifically for Philippine neighbourhood retail (*sari-sari stores*).

---

## 🌟 Real Application Workflows Documented

The website directly reflects the authentic application workflows from the official SariPOS application:

1. **Initial Setup & Security (`/docs/initial-setup-and-security`)**
   - Onboarding & Store Profile Setup (Store Name, Owner Name, Contact Number, Receipt Header).
   - Owner security profiles hashed with individual cryptographic salts.
   - Returning user unlocks via 6-digit PIN or Device Biometrics (Fingerprint / Face Unlock).

2. **POS Checkout & Multi-Payment Modes (`/docs/checkout-and-payment-methods`)**
   - 3-Way checkout:
     - **Cash Payment:** Quick-pay tender buttons with automatic change (*sukli*) calculation.
     - **E-Wallet (GCash / Maya):** Reference number entry and verified screenshot validation.
     - **Utang / Credit:** Direct customer ledger assignment with credit limit checks.
   - Post-sale actions: Automatic ESC/POS thermal printing or instant receipt dispatch via native cellular SMS.

3. **Supermarket Continuous Barcode Scanning (`/docs/continuous-barcode-scanning`)**
   - Low-latency continuous camera scanning sheet.
   - Amplified hardware-level audio-boosted beep confirmation for every scan.
   - Scan debouncing with configurable cooldown to prevent accidental duplicate additions.
   - Manual barcode input modal for worn or damaged manufacturer tags.

4. **E-Wallet Cash In / Cash Out & OCR Receipt Scanner (`/docs/ewallet-cash-in-cash-out-ocr`)**
   - Neighborhood cash hub operations.
   - On-device Google ML Kit OCR text recognition verifying provider branding, transaction dates, amounts, and reference numbers to prevent customer fraud.

5. **Utang (Store Credit) & Suki Directory (`/docs/managing-customers-and-utang`)**
   - Itemized credit balances, partial repayment (*hulugan*) tracking.
   - Native SIM-direct SMS payment reminders sent over cellular carrier with zero third-party gateway fees.
   - Configurable credit limits per suki customer.

6. **Suki Loyalty Points & Reward Tiers (`/docs/suki-loyalty-rewards`)**
   - Configurable points per ₱100 spend.
   - Progression across Bronze, Silver, and Gold badges.
   - One-tap point redemption as cart discounts.

7. **Product Catalog & On-Device AI Background Removal (`/docs/adding-and-editing-products`)**
   - Embedded local ONNX neural network model (`birefnet-general-epoch_244.onnx`) executing 100% offline.
   - Strips messy store backgrounds from shelf photos, producing clean transparent PNGs.
   - Inventory movement ledger (Stock-In deliveries, damaged goods write-offs, and household personal use).

8. **Offline Thermal Receipt Printing (`/docs/configuring-supported-printers`)**
   - Bluetooth and direct USB OTG ESC/POS thermal printing (58mm and 80mm rolls).
   - Standardized Philippine receipt header (Store Name, Owner Name, Contact Number, Timestamp).
   - Android print spooler fallback for WiFi/Mopria printers.

9. **Cash Drawer Shifts & Closing Reconciliation (`/docs/cash-drawer-shifts-and-closing`)**
   - Opening float change fund (*panukli*) tracking.
   - Mid-shift cash payouts with mandatory reason codes.
   - Closing shift reconciliation formula: `Expected Cash = Float + Cash Sales + Utang Collected - Payouts`, highlighting overages and shortages.

10. **Uninstall-Proof Backups & Persistent Storage (`/docs/creating-and-restoring-backups`)**
    - Product images stored in persistent device storage (`SariPOS/uploaded/images`) surviving app uninstallation.
    - Export encrypted `.saripos` archives containing full SQLite tables and images saved to `Download/SariPOS`.
    - Automated weekly rolling auto-backups.

11. **Android 13–15 Restricted Settings Guide (`/docs/common-troubleshooting-guide`)**
    - Step-by-step walkthrough for enabling restricted SMS permissions on sideloaded APKs on Android 13, 14, and 15+.

---

## 👵 Accessibility & Senior-Friendly Design

- **Text Size Zoomer (`Laki ng Sulat`):** One-tap switch between `Normal`, `Malaki A+` (18px default), and `Extra A++` (20px).
- **Taglish & English Language Switcher:** Plain, respectful, everyday Filipino store language (*Iwas Mali sa Sukli*, *Wala Nang Away sa Utang*, *100% Libre*).
- **High-Contrast Touch Targets:** 72px primary buttons with large icons and clear subheadings.
- **Side-by-Side Comparison:** *"Lumang Kwaderno (Notebook)"* vs. *"SariPOS sa Cellphone"*.

---
