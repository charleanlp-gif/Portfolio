# ScannerMe

**Mobile QR and barcode scanning app with local storage and CSV export**

**Status:** ✅ Completed MVP  
**Platform:** Android  
**Current milestone:** Standalone APK build completed successfully

## What it does

ScannerMe is a mobile scanning app built to capture QR codes and barcodes quickly, save them locally on the device, keep a scan history, and export the captured data to CSV.

The MVP is designed to work **offline first**. Scanned codes are stored in a local SQLite database instead of depending on a cloud service, which keeps the app useful even without an internet connection.

## Why I built it

I wanted a simple scanning workflow that I could control myself instead of relying on a paid scanning app for an occasional stock-taking task.

The goal was to build the smallest useful version first: scan codes, save them reliably, review the history, and export the results.

## Current working features

- QR code scanning
- Barcode scanning
- Local SQLite storage
- Persistent scan history
- Continuous scanning mode
- Duplicate scans allowed intentionally
- Clear visual scan-success feedback
- Three-second scan cooldown between saved scans
- Session scan counter
- CSV export
- Selectable CSV fields before export
- Saved-scan count in Settings
- Clear scan history tool
- Standalone Android APK build

## CSV export

The user can choose which fields to include before exporting.

Available fields include:

- Code Value
- Code Type
- Date
- Time
- Created At

Duplicate scans are exported as separate rows, which keeps the app suitable for workflows where repeated scans may represent quantity, repeated checks, attendance, or audit events.

## Technology stack

- Expo
- React Native
- TypeScript
- Expo Router
- Expo Camera
- Expo SQLite
- Expo File System
- Expo Sharing
- EAS Build

## How the app is structured

The current MVP contains separate screens for:

- Home
- Scan
- History
- Export CSV
- Settings

The app stores scan data locally first and treats export or future cloud services as optional layers rather than making the core scanner depend on them.

## Development approach

I built ScannerMe in small, testable phases:

1. Create the Expo app shell
2. Add the main screens
3. Add QR and barcode scanning
4. Add local SQLite storage
5. Add persistent scan history
6. Add CSV export
7. Add settings and testing tools
8. Improve the continuous scanning workflow
9. Add selectable CSV fields
10. Build a standalone Android APK

Each phase was tested before moving to the next one.

## Current status

The first working standalone milestone is complete.

The app can run through Expo during development and has also been built successfully as an installable Android APK for testing outside Expo Go.

## Screenshots

Screenshots of the mobile app will be added here.

## Planned future expansion

Possible future improvements include:

- Manual code entry for damaged or unreadable labels
- Named scan sessions
- Export file-name options
- Duplicate-count summaries
- Product and item records
- Stock-in and stock-out modes
- Quantity tracking
- Excel export
- Cloud sync
- User accounts and admin tools

These are planned extensions and are **not presented as completed features of the current MVP**.

## What this project demonstrates

ScannerMe gave me hands-on experience with mobile development, camera permissions, local databases, file export, Android builds, debugging device connectivity, and designing a project so that a small useful MVP can later expand without rebuilding everything from scratch.
