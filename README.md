# MSS54 DS2 Tool

Windows 10/11 diagnostic, backup, history, and programming tool for BMW MSS54/MSS54HP DMEs over DS2/K-line.

This public repository is for compiled binary releases of MSS54 DS2 Tool. Source code is not distributed here.

## Download

Download the latest release from the repository's **Releases** page.

Use only official release packages from this repository. Do not run repackaged or modified versions from unknown sources.

## What It Does

MSS54 DS2 Tool can:

- Connect using a COM-port K-line adapter or FTDI D2XX interface.
- Identify MSS54 and MSS54HP DMEs.
- Read DME identity, logistics, AIF, flash-counter, and manufacturer-specific data.
- Read full DME images, data blocks, service blocks, and related backup artifacts.
- Create tracked backups with metadata and history records.
- Validate data/program binaries before writing.
- Correct supported checksums by creating corrected copies.
- Write data block and selected program block regions.
- Restore service block backups.
- Insert AIF records.
- Clear the flash counter using a fresh service block backup and reset plan.
- Keep session logs for review.

## Safety Warning

This tool talks directly to DME memory and programming services.

Read and identify workflows are useful on their own, but write, restore, flash-counter, AIF, erase/rewrite, and fast-entry workflows are inherently high risk. If something goes wrong, you may disable or corrupt the DME and require recovery using BDM or other specialist tooling.

Before using destructive features:

- Use a stable external power supply.
- Use known-good interface hardware.
- Test your cable/interface with read operations first.
- Confirm the DME variant, file, memory layout, and intended action.
- Keep backups.
- Make sure you have a recovery option available.

The app includes validation and safety checks, but they do not make DME programming risk-free.

## Requirements

- Windows 10 or Windows 11.
- A compatible K-line/DS2 interface.
- For COM-port mode: a working serial/VCP driver.
- For FTDI D2XX mode: the matching FTDI D2XX driver/runtime.

## Installation

1. Download the release package.
2. Extract it to a folder you control, such as `Documents\MSS54 DS2 Tool`.
3. Run `Mss54Ds2Tool.App.exe`.

If Windows SmartScreen appears, verify that you downloaded the app from the official release page before continuing.

## Logs And Backups

The app can auto-save session logs to: `Documents\MSS54 DS2 Tool\Logs`

The backup library defaults to: `Documents\MSS54 DS2 Tool\Backups`

Keep these files. They are useful for review, recovery planning, and comparing prior DME state.


