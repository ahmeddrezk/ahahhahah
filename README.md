# NOMA — Smart Accessories Store

<p align="center">
  <strong>A mobile app for premium smart accessories shopping</strong><br/>
  Graduation Project — Flutter Training · NTI Round 5
</p>

<p align="center">
  <img alt="Flutter" src="https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white"/>
  <img alt="Dart" src="https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white"/>
  <img alt="NTI" src="https://img.shields.io/badge/NTI-Round%205-294A3A?style=flat"/>
  <img alt="Platform" src="https://img.shields.io/badge/Platform-iOS%20%7C%20Android-7B827A?style=flat"/>
</p>

---

## Overview

**NOMA** is an e-commerce mobile app focused on smart and premium accessories (watches, bags, jewelry, belts, and more). It delivers a complete shopping experience — from first launch to product management — with a calm visual identity inspired by earthy tones (deep green + warm cream).

| Item | Details |
|------|---------|
| **App Name** | NOMA |
| **Tagline** | Smart Accessories Store |
| **Platform** | Flutter (iOS & Android) |
| **Project Type** | Graduation Project — Flutter Training |
| **Organization** | NTI (National Telecommunication Institute) |
| **Intake** | Round 5 |
| **Design** | [Figma — NTI Final Project](https://www.figma.com/design/1adCRVoFF08Qz5uaDZbz4Q/NTI-Final-Project) |

---

## Project Idea

NOMA aims to build a complete mobile shopping experience that mirrors a real accessories store, with a focus on:

- A smooth, clear user experience from the first launch
- A full purchase journey (browse → details → cart → order)
- Product content management (add / edit / delete) for seller or admin roles
- Consistent UI aligned with a unified design system (colors, typography, components)

---

## Key Features

### 1) App Launch & Introduction
- Splash screen with brand identity
- Onboarding across 3 screens:
  - Discover Accessories
  - Shop With Confidence
  - Join the Community
- Skip option to go straight to login

### 2) Authentication & Account
- Sign in (Email + Password)
- Create a new account
- Email Verification
- Forgot Password + Reset Password
- Social login (Google / Apple) as designed
- Change password from settings
- Delete account

### 3) Browse & Shop
- Home with banners, promotions, and featured products
- Browse by Categories: Watches, Bags, Jewelry, Belts…
- Category Products listing
- Search with results or No Results Found state
- Product Details: price, description, ratings, color/options
- Write a Review
- My Cart with Empty Cart state

### 4) Profile & Settings
- My Profile
- Settings (e.g. theme and currency as per design)
- Privacy Policy
- About Us
- Contact Us

### 5) Product Management (Seller / Admin)
- Add Product
- Manage Products
- Delete Confirmation

### 6) System States
- Error screen with retry messaging
- Empty states (Empty Cart / No Results)

---

## User Journey / Workflow

```text
┌─────────────┐
│   Splash    │
└──────┬──────┘
       ▼
┌──────────────────────────┐
│  Onboarding (3 screens)  │── Skip ──┐
└────────────┬─────────────┘          │
             ▼                        ▼
      ┌────────────┐           ┌────────────┐
      │   Login    │◄─────────►│  Register  │
      └──────┬─────┘           └──────┬─────┘
             │                        │
             │   Forgot Password      │
             │         ▼              │
             │   Reset Password       │
             │         ▼              │
             │  Email Verification    │
             ▼                        ▼
      ┌─────────────────────────────────┐
      │              Home               │
      └──┬──────────┬──────────┬────────┘
         │          │          │
         ▼          ▼          ▼
   Categories    Search     Profile
         │          │          │
         ▼          ▼          ▼
   Category     Results    Settings /
   Products                About / Contact
         │
         ▼
   Product Details ──► Write Review
         │
         ▼
      My Cart
         │
         ▼
   (Checkout flow)
```

### New User Path
1. Opens the app → Splash  
2. Views Onboarding and learns what NOMA offers  
3. Creates an account or signs in  
4. Verifies email if required  
5. Lands on Home and starts browsing  

### Purchase Path
1. Picks a category or searches for a product  
2. Opens Product Details to review price, description, and ratings  
3. Adds to cart and adjusts quantity  
4. Completes the order from the cart  

### Content Management Path
1. Opens product management / admin area  
2. Adds a new product or edits an existing one  
3. Deletes a product with confirmation before removal  

---

## Screens (from Design)

| Group | Screens |
|-------|---------|
| **Onboarding** | Splash · Discover · Shop With Confidence · Join the Community |
| **Auth** | Login · Create Account · Email Verification · Forgot Password · Reset Password |
| **Shopping** | Home · Categories · Category Products · Search Results · Product Details · Write a Review · My Cart · Empty Cart |
| **Account** | My Profile · Settings · Change Password · Privacy Policy · About Us · Contact Us |
| **Admin** | Add Product · Manage Products · Delete Confirmation |
| **System** | No Results Found · Error |

---

## Design System

| Role | Color | Hex |
|------|-------|-----|
| Primary | Deep green | `#294A3A` |
| Text Primary | Near-black green | `#1E2521` |
| Text Secondary / Hint | Sage gray | `#7B827A` |
| Background | Cream | `#F6F2EA` / `#F7F4EC` |
| Surface | Warm off-white | `#FFFCF7` |
| Border | Soft beige | `#E8DDCB` |
| Accent | Terracotta | `#B9785B` |
| Error / Destructive | Red | `#DC2626` |

Colors live in `lib/app_colors.dart`, and text styles in `lib/app_styles.dart`.

---

## Tech Stack

- **Flutter** — single codebase for iOS and Android  
- **Dart** — app language  
- **Material Design** — UI component foundation  
- Project structure:
  - `lib/screens/` — screens
  - `lib/widgets/` — shared widgets
  - `lib/app_colors.dart` — app colors
  - `lib/app_styles.dart` — typography styles

> The stack will expand later (State Management / API / Local Storage) based on the implementation plan.

---

## Project Structure

```text
nti_project/
├── lib/
│   ├── main.dart
│   ├── app_colors.dart
│   ├── app_styles.dart
│   ├── screens/
│   │   └── splash_screen.dart
│   └── widgets/
├── android/
├── ios/
├── test/
├── pubspec.yaml
└── README.md
```

---

## Getting Started

### Requirements
- Flutter SDK (compatible with Dart `^3.12.2`)
- Android Studio / Xcode depending on platform
- Emulator or physical device

### Steps

```bash
# Clone the repository
git clone <repository-url>
cd nti_project

# Install dependencies
flutter pub get

# Run the app
flutter run
```

Check your environment:

```bash
flutter doctor
```

---

## Roadmap

- [x] Project setup and visual identity  
- [x] Splash screen  
- [ ] Onboarding screens  
- [ ] Authentication screens  
- [ ] Home + Categories + Product Details  
- [ ] Cart & Wishlist  
- [ ] Profile & Settings  
- [ ] Product management (CRUD)  
- [ ] API / Backend integration  
- [ ] Testing and performance polish  

---

## Team

Graduation project for **Flutter Training — NTI Round 5**.

| Name | Role | Contact |
|------|------|---------|
| <!-- Member name --> | <!-- e.g. Flutter Developer / UI · Team Lead --> | <!-- GitHub / LinkedIn / Email --> |
| <!-- Member name --> | <!-- Role --> | <!-- Link --> |
| <!-- Member name --> | <!-- Role --> | <!-- Link --> |
| <!-- Member name --> | <!-- Role --> | <!-- Link --> |

> Update this table with real team names, roles, and contact links before submission.

---

## About the Program

This is the **final graduation project** for the **Flutter** training track at:

**NTI — National Telecommunication Institute**  
**Round 5**

The program aims to help trainees build a complete mobile app with Flutter — from design to implementation — covering UI, code organization, and a full user journey inside a real product.

---

## License

Educational / graduation project — not intended for commercial release unless approved by the team and the training organization.

---

<p align="center">
  <strong>NOMA</strong> · Smart Accessories Store<br/>
  Made with Flutter · NTI Round 5 Graduation Project
</p>
