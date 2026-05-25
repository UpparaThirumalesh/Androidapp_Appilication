# 📱 Koolly App

A location-based Android application designed to help users discover nearby local services such as healthcare, education, household services, and more — especially focusing on small towns and villages where platforms like Google Maps may not show detailed local providers.

---

## 🚀 Features

*   **🔍 Discover Nearby Local Services:** Quickly locate essential providers in your vicinity.
*   **📍 Location-Based Service Filtering:** Automatically filter and view list options tailored to your location.
*   **🗂️ Category-Wise Service Browsing:** Browse services grouped by categories like healthcare, education, utilities, and emergency services.
*   **🗺️ Google Maps Integration:** Seamlessly visualize local service providers on an interactive map.
*   **⚡ Real-Time Data Updates:** Powered by Firebase for immediate data updates and sync.
*   **🧭 Distance-Based Sorting:** Sort providers dynamically with nearest services appearing first.
*   **👤 User Authentication & Profile Management:** Secure sign-in, sign-up, and personal profile options.

---

## 🛠️ Tech Stack

*   **Language:** Android (Java / Kotlin)
*   **UI/UX:** XML (Material Design Components)
*   **Database:** Firebase Realtime Database
*   **Mapping & Location:** Google Maps SDK for Android & Android Location Services (FusedLocationProviderClient)
*   **Core UI Components:** RecyclerView, CardView, Custom Adapters

---

## 📱 App Workflow

1.  **User Authentication:** User logs in or signs up for a secure account.
2.  **Location Acquisition:** App requests and fetches the user's high-precision GPS coordinates.
3.  **Data Fetching:** Loads structured local service provider details from the Firebase Realtime Database.
4.  **Category Selection & Filtering:** Filters loaded services based on active user-selected categories.
5.  **Distance Calculation:** Calculates the geodesic distance between the user's location and each provider's coordinates.
6.  **Sorting & Presentation:** Sorts catalog by distance (nearest first) and renders them in list and comprehensive map views.

---

## 🧠 Core Concept

The core architecture uses real-time latitude and longitude-based calculations to determine proximity. To maximize execution efficiency and minimize CPU overhead, the application parses and filters datasets on category parameters *before* conducting trigonometric distance calculations (such as the Haversine formula) on the local device.

---

## 📸 Screenshots

Add your preview screenshots inside a `screenshots/` directory at the root of your repository to display them here:

| 🏠 Home Screen | 🗺️ Map View |
| :---: | :---: |
| ![Home Screen Layout](screenshots/home_screen.png) | ![Map View Layout](screenshots/map_view.png) |

| 📂 Categories | 👤 Profile Screen |
| :---: | :---: |
| ![Categories Grid](screenshots/categories.png) | ![Profile Screen Layout](screenshots/profile_screen.png) |

---

## 📁 Project Structure

Below is the standard layout of the modular project files:

```text
Coolly-App/
├── app/                  # Main Android application module
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/coolly/
│   │   │   │   ├── activities/    # UI screens (Login, Home, Maps, Profile)
│   │   │   │   ├── adapters/      # RecyclerView binding logic
│   │   │   │   ├── firebase/      # DB reference & authentication configs
│   │   │   │   └── models/        # Data schemas (User, Service, Category)
│   │   │   └── res/               # Layout files (XML), drawables, values
└── screenshots/          # App design visual assets & screenshots
```

---

## ⚡ Key Highlights

*   **Optimized Filtering Pipeline:** Prefilters records prior to distance math, resulting in highly fluid lists even on low-spec mobile devices.
*   **Real-Time Syncing:** Direct and instant binding to Firebase database nodes.
*   **Scalable Architecture:** Clean OOP modeling makes introducing new categories or service types trivial.
*   **Responsive XML Design:** Adapts smoothly across multiple screen sizes, aspect ratios, and pixel densities.

---

## 👨‍💻 Author

**Thirumalesh**
*B.Tech Graduate | Software Developer Enthusiast*
*   **Email:** thiru86420@gmail.com
*   **Skills:** Android SDK, Java/Kotlin UI development, Firebase integrations, Google Location APIs.

---

> 📌 **Note:** This project was developed as part of an internship experience focusing on solving real-world local service discovery problems in underserved geographical areas.

