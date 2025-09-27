````markdown
# 🎁 Hedieaty – Gift Registry & Event Companion

Hedieaty is a **Flutter application** for planning celebrations, curating wish lists, and coordinating gift pledges with friends.  
It integrates **Firebase Authentication, Cloud Firestore, Storage, and Messaging** for a seamless experience across platforms.

---

## 📑 Table of Contents
- [✨ Features](#-features)
- [🏗️ Architecture Overview](#️-architecture-overview)
- [🛠️ Tech Stack](#️-tech-stack)
- [🚀 Getting Started](#-getting-started)
- [⚙️ Firebase Configuration](#️-firebase-configuration)
- [▶️ Running the App](#️-running-the-app)
- [🧪 Testing](#-testing)
- [📂 Project Structure](#-project-structure)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [💡 Alternate Title Suggestion](#-alternate-title-suggestion)

---

## ✨ Features
- 🔑 **Authentication & Onboarding** – Email/password login, device FCM token registration.  
- 🏠 **Home Dashboard & Friend Discovery** – Pull-to-refresh, inline search, Firestore-powered friend list.  
- 👥 **Friend Request Workflow** – Username-based requests, duplicate checks, approval/rejection flows.  
- 🎉 **Event Planning & Wish Lists** – Categorize celebrations, add logistics, and request gifts.  
- 🎁 **Gift Catalog Management** – Add/edit/delete gifts, guests pledge items with validation.  
- 🔔 **Collaborative Gift Tracking** – Friends pledge gifts and trigger push notifications.  
- 📊 **Pledged Gifts Dashboard** – View and manage all pledged items in one place.  
- 👤 **Profile & Preferences** – Update username, toggle notifications, manage account.  
- 🗂️ **Typed Data Models** – Firestore entities encapsulated in models for consistency.  
- 🧭 **Bottom Navigation & Routing** – Central `MaterialApp` with indexed navigation stack.  

---

## 🏗️ Architecture Overview
- Standard **Flutter lib/** layout with clear separation between **screens, widgets, and models**.  
- **Firebase initialization** occurs before `runApp`.  
- **StreamBuilder** manages auth state → splash, login, or main app.  
- **Firestore models** ensure type safety and maintainability.  
- **Push notifications** via FCM + Firestore token lookups when pledges change.  

---

## 🛠️ Tech Stack
| Layer          | Technology |
|----------------|------------|
| Framework      | Flutter 3.5+ (Material Design) |
| Backend        | Firebase Core, Auth, Firestore, Storage, Messaging |
| Utilities      | intl (dates), image_picker (avatars), assets/images/gift.png |

---

## 🚀 Getting Started
1. **Install prerequisites**  
   - Flutter (≥ 3.5)  
   - Firebase CLI / flutterfire  

2. **Clone and install packages**  
   ```bash
   flutter pub get
````

3. **Configure Firebase**

   * Run:

     ```bash
     flutterfire configure
     ```
   * Place `google-services.json` (Android) and `GoogleService-Info.plist` (iOS) in the correct folders.

4. **Seed Firestore & Auth**

   * Create users and collections (`users`, `events`, `gifts`) for testing.

---

## ⚙️ Firebase Configuration

* The generated **`DefaultFirebaseOptions`** targets **Android + iOS**.
* Other platforms → `UnsupportedError`.
* Run `flutterfire configure` after creating your Firebase project to regenerate config.

---

## ▶️ Running the App

Run on a simulator or device:

```bash
flutter run
```

`main.dart` ensures Firebase initializes before building the shared App widget.

---

## 🧪 Testing

* **Widget Tests** → `test/widget_test.dart` (replace default counter test).
* **Integration Tests** → `integration_test/login_test.dart` covers login → event → pledge flow.

  ```bash
  flutter test integration_test
  ```

---

## 📂 Project Structure

```
lib/                → Core app code (routing, tabs, models, screens, widgets)
assets/images/      → Static images (gift illustrations, branding)
integration_test/   → End-to-end Firebase integration tests
test/               → Widget test harness
```

---

## 🤝 Contributing

1. Fork & create a feature branch.
2. Keep Firebase credentials **out of version control**.
3. Add unit/integration tests for new features.
4. Run `flutter analyze` & test suites before PR.

---

## 📜 License

Specify here (e.g., MIT, Apache 2.0).

---

## 💡 Alternate Title Suggestion

**GiftCircle – Collaborative Wish List Manager**

> Highlights the app’s shared gift planning & friend-driven pledges.

---

## ⚠️ Testing Status

🚧 *Tests not run – read-only QA review*

```

---

Would you like me to also add **badges** (like Flutter version, Firebase, License, etc.) at the top of the README for extra polish, like the ones you see in popular repos?
```
