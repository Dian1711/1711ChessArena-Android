# 1711 Chess Arena — Android

A separate Android app for **1711 Chess Arena**. The Telegram Mini App repository and its backend are intentionally left untouched.

## Project goals

- Match the Telegram version's main menu and feature set: VS Bot, Random Match, Private Room, Friends, Profile, game clock, and match results.
- Use Android-specific Guest and Google sign-in, not Telegram identity.
- Keep Android player data and multiplayer services separate from Telegram.
- Build a debug APK with GitHub Actions, without requiring a local command line.

## Current status

This repository is being initialized. The first milestone is a reproducible Android build and app shell. Authentication, database schema, chess gameplay, and online matchmaking must be implemented and tested before the app is considered playable.

## Build APK

1. Open the **Actions** tab.
2. Select **Build Android APK**.
3. Run the workflow using **Run workflow** (or push a commit).
4. Download the `1711-chess-arena-debug-apk` artifact when the workflow succeeds.

## Safety boundaries

- Do not reuse or modify the Telegram app's source, Supabase project, database, or credentials in this repository.
- Never commit service-role keys, OAuth client secrets, or private credentials.
- Google sign-in requires a separately configured Android OAuth client and backend configuration.
