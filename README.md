# BitCounter

Images related to the application can be found in this repository. The app is currently undergoing approval on the Play Store.


BitCounter is a lightweight clicker/idle game built with Flutter. Players collect a digital resource (bits / crypto-like currency), invest into upgrades and automation, and expand production through systems such as offices and drones. The app combines short active sessions (clicking) with longer idle progression (automations, offline earnings, and persistent upgrades).

## Executive Summary / Report
BitCounter is designed as a compact incremental game focused on satisfying feedback loops and accessible progression. The core loop is: click or tap to earn bits → spend bits on upgrades or automation → gain passive production → unlock features and milestones that increase scaling. The game includes engagement mechanics such as daily quests, achievements, and limited-time rewards to encourage regular return visits. Offline earnings are calculated and credited when players return, enabling reward for time away while keeping progression meaningful.

Key design goals:
- Fast feedback and visible progression on every click.
- Clear upgrade paths and automation that scale well across play sessions.
- Lightweight codebase suitable for mobile deployment and easy iteration.

## Gameplay & Mechanics
- Resource: `bits` — the main currency earned by clicking and automated systems.
- Active income: Direct player clicks/taps that produce immediate bits.
- Upgrades: Permanent or semi-permanent improvements that increase click power or passive income.
- Automation: Systems like drones and daemons that produce bits automatically over time.
- Office & Systems: Mid/late-game structures that unlock advanced multipliers and production synergies.
- Daily Quests & Achievements: Short objectives and milestone rewards to drive retention.
- Offline Earnings: Time-based reward calculation for sessions when the app was closed.
- Micro-rewards: Small ad-reward dialogs or timed bonuses (configurable via `ad_service`).

## Technologies
- Flutter & Dart — single-codebase mobile UI and logic.
- State management: BLoC pattern (project contains `lib/bloc/` for game state/events).
- Android build tooling present under `android/` and Gradle configurations for release signing.
- Optional: Google Mobile Ads integration and related service wrapper in `lib/services/ad_service.dart`.

## Project Structure
- `lib/main.dart` — app entry point and initialization.
- `lib/bloc/` — game logic, events, and state management.
- `lib/core/` — theming, constants, and small utilities (e.g., `big_number`).
- `lib/models/` — data models for drones, upgrades, milestones, etc.
- `lib/screens/` & `lib/widgets/` — UI screens and reusable components.
- `assets/translations/` — English and Turkish localization files.

