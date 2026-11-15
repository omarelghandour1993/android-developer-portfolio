# Swapply

![Android](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)
![React](https://img.shields.io/badge/React-19-20232A?logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-007ACC?logo=typescript&logoColor=white)
![Capacitor](https://img.shields.io/badge/Capacitor-7-119EFF?logo=capacitor&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?logo=supabase&logoColor=white)

## Overview

**Swapply is an Android-focused product exchange application for Egypt.** It helps people exchange personal items directly instead of buying and selling them. An optional, mutually agreed cash difference can be included to balance an exchange; Swapply does not process payments.

The project combines a React and TypeScript application with Capacitor for Android, Supabase for authentication and backend data, and Cloudflare R2 for product-image storage.

## Implemented product capabilities

The private project documentation and source structure identify the following implemented application areas:

- **Accounts and profiles:** Supabase authentication, session/profile context, email-confirmation callback handling, account deletion support and profile management.
- **Marketplace:** product feed, category browsing, search, filters, pagination, product details, listing creation, editing and deletion.
- **Exchange workflow:** create and manage swap offers, accept or decline offers, reserve listings during an active exchange, and mark exchanges as completed.
- **Messaging:** private conversations associated with offers, realtime message delivery and read-state handling.
- **Favourites:** save products and view a dedicated favourites list.
- **Notifications:** realtime offer updates, in-app badges and toasts, Android local notifications, and Firebase Cloud Messaging integration for closed-app delivery.
- **Trust and moderation:** report listings, block members, unblock members, and administrative tools for reports, listings and member status.
- **Dashboard:** listing, offer, completed-exchange and favourite counts.
- **Appearance:** retro 1980s/1990s arcade-inspired interface, light/dark themes and device-persisted theme preference.
- **Media handling:** camera/gallery selection, image resizing and WebP compression before upload.

Feature presence in source code is not the same as independent production certification. Live service availability depends on the relevant Supabase, Cloudflare and Firebase configuration and deployment.

## Screenshots

Add genuine captures from the running Swapply application to `screenshots/`. Suggested filenames:

| Screen | Suggested file |
|---|---|
| App icon | `app-icon.png` |
| Splash screen | `splash-screen.png` |
| Sign in | `login-screen.png` |
| Registration | `registration-screen.png` |
| Marketplace home | `home-screen.png` |
| Search and filters | `search-screen.png` |
| Product details | `product-details.png` |
| Create/edit listing | `add-product.png` |
| Swap offer | `swap-offer.png` |
| Offer inbox | `offers-screen.png` |
| Conversation | `chat-screen.png` |
| Dashboard | `dashboard.png` |
| Profile / settings | `profile-screen.png` |
| Admin tools | `admin-dashboard.png` |

Only add image links after the corresponding real screenshot files have been committed. Do not present mockups as actual application captures.

## Demonstration video

Place real recordings in `demo-video/` and link them here when available.

Recommended 60–90 second walkthrough:
1. Open the app and browse available items.
2. Search or filter listings.
3. Open a product and submit a swap offer.
4. Show the offer and conversation flow.
5. Demonstrate notifications and the user dashboard.

## Technology stack

| Technology | Role in the project |
|---|---|
| React 19 | Component-based application UI |
| TypeScript | Typed application code |
| Vite 6 | Frontend development and production build |
| Capacitor 7 | Android packaging and native plugin bridge |
| Supabase | Authentication, Postgres database, Row Level Security, Realtime and Edge Functions |
| Cloudflare R2 | Object storage for compressed product images, accessed through presigned uploads |
| Firebase Cloud Messaging | Push delivery integration for closed-app notifications |
| Android / Gradle | Native Android project and release build |

The Android app uses Capacitor plugins for app lifecycle/deep links, camera, local notifications, push notifications and status bar integration.

## Architecture

See [architecture.md](./architecture.md) for the component overview, backend responsibilities, data flow and security boundaries.

## Development contribution and workflow

The project repository documents work across:

- Product concept and requirements: an exchange-first platform with optional cash balancing, not a conventional sales marketplace.
- React and TypeScript frontend implementation, routing, reusable components and application screens.
- Supabase authentication, profile/session handling, database integration and Row Level Security-backed access.
- Product discovery, listing management and the swap-offer lifecycle.
- Private realtime conversations and notification flows.
- Capacitor Android integration, native plugin setup, deep-link handling and Android build preparation.
- Image processing and secure upload flow using short-lived presigned URLs.
- Moderation, favourites, dashboard and administrative workflows.
- Testing, debugging, database migrations and release preparation.

This portfolio describes the documented project implementation. It does not claim third-party audit, production-scale performance testing, or independently verified Play Store publication.

## Build overview

The documented local workflow uses Node.js 20+, Android Studio/Android SDK and Git.

```powershell
npm install
npm run build
npx cap sync android
npx cap open android
```

The native Android project can then be built and tested through Android Studio or Gradle. A working build requires locally supplied configuration such as the appropriate Firebase client configuration and signing setup.

## Download

No public release APK is included in this portfolio at this time.

When a distributable release is ready, place the APK in `download/` and update this section with:
- Exact filename and version
- Release date
- SHA-256 checksum
- Compatibility notes

Never commit signing keystores, passwords, private environment files, service-account credentials or backend secrets.

## Project links

- [Architecture](./architecture.md)
- [Verified feature inventory](./features.md)
- [Development process](./development-process.md)
- [Screenshots folder](./screenshots/)
- [Demo video folder](./demo-video/)
- [Download folder](./download/)

**Source code:** The application source repository is private. This public portfolio intentionally contains project documentation and approved presentation assets only.
