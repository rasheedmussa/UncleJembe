# Uncle Jembe — Full App Build Prompt

Use this document as the single source of truth for generating or extending the **Uncle Jembe** Android app and related assets.

**Project author:** Rashid Mussa  
**Package:** `com.rashidmussa.unclejembe`  
**App name:** Uncle Jembe  
**Primary language:** Swahili  
**Secondary language:** English  

---

## Purpose

Create an open-source, **offline-first** Android agriculture assistant for Tanzanian farmers. The app helps farmers choose crops and seeds for their region, understand planting seasons, recognize and manage plant diseases, and get practical farming advice using **local data** and **rule-based AI-style** recommendations (no mandatory internet).

---

## Technical Requirements (Android)

**Build**

- Gradle
- Android Gradle Plugin **8.5.2**

**SDK**

- `compileSdk` 34  
- `targetSdk` 34  
- `minSdk` 24  
- **Java 17**

**Libraries**

- AndroidX AppCompat  
- Material Components  
- RecyclerView  
- ViewPager2  
- ConstraintLayout  
- AndroidX Biometric  
- AndroidX Security Crypto  
- OkHttp  
- Gson  
- Media3 ExoPlayer  

**Architecture / UX**

- Native Android, **Java**  
- Offline-first, clean architecture  
- Modern Material Design, mobile-friendly for rural users  
- Swahili-first UI with English support  

---

## Suggested App Package Layout (modules / packages)

```text
app/
 ├── dashboard/
 ├── crop_recommendation/
 ├── seed_recommendation/
 ├── disease_library/
 ├── ai_assistant/
 ├── farming_calendar/
 ├── videos/
 ├── farmer_profile/
 ├── offline_database/
 └── settings/
```

---

## Feature Specifications

### 1. Splash Screen

- Show Uncle Jembe logo  
- Short tagline: **“Msaidizi wa Kilimo Tanzania”**  
- Navigate to onboarding or dashboard (based on first-run state)  

### 2. Onboarding (ViewPager2)

Screens:

- Know what to plant in your area  
- Get seed recommendations  
- Learn about crop diseases  
- Use farming advice offline  

### 3. Farmer Profile Setup

Collect: name, region, district, farm size, main crop interest, soil type, farming experience.  
Store locally and securely with **AndroidX Security Crypto**.

### 4. Dashboard

Cards for:

- Crop Recommendation  
- Seed Recommendation  
- Plant Diseases  
- Farming Calendar  
- AI Farming Assistant  
- Learning Videos  
- Farmer Profile  
- Settings  

### 5. Crop Recommendation

User selects: region, district, soil type, season.  
Recommendations from **offline JSON**. Each crop card: crop name, best planting season, suitable soil, water requirement, expected harvest period, common risks, practical advice.

### 6. Seed Recommendation

User selects crop and location.  
Recommendations consider: region, climate, rainfall, crop, soil type.  
Seed card: seed name, crop type, suitable region, maturity period, drought tolerance, disease resistance, planting advice.

### 7. Plant Disease Library

Searchable offline library (RecyclerView + detail).  
Fields: disease name, crop affected, symptoms, cause, prevention, treatment, common regions, severity.

### 8. Offline AI Farming Assistant

Chat UI; **no internet required** for core answers.  
Rule-based logic over local JSON (keywords, region, crop, disease, season, soil).  
Swahili-first replies; suggest consulting an agricultural officer for serious cases.  
Example intents: planting advice by region, seed choice, disease symptoms, crop timing, low-rainfall crops.

### 9. Farming Calendar

By region and crop: planting months, fertilizer, weeding, pest control, harvest.

### 10. Learning Videos (Media3 ExoPlayer)

List videos, play **local** assets offline, optional **remote** URLs when online. Metadata in local JSON.

### 11. Offline Data (assets + Gson)

Suggested JSON files under `assets/`:

- `regions.json`  
- `crops.json`  
- `seeds.json`  
- `diseases.json`  
- `farming_calendar.json`  
- `ai_rules.json`  
- `videos.json`  

### 12. Optional Online Sync (OkHttp)

When network is available, optionally check for updated farming data. **App must remain fully functional** with bundled data when offline.

### 13. Settings

- Language: Swahili / English  
- Data update  
- About Uncle Jembe  
- Open-source / contribution info  
- Privacy policy  

### 14. Security

AndroidX Security Crypto for profile and sensitive preferences.

### 15. UI Design

Agriculture-inspired palette: green, earth brown, white, soft yellow; large readable text; simple icons; cards; farmer-friendly navigation; performant on low-end devices.

### 16. Open Source / About Copy

Include text that Uncle Jembe is an open-source project by Rashid Mussa to support Tanzanian farmers, and that developers, experts, universities, NGOs, and contributors are welcome.

### 17. Required Deliverables (when scaffolding the Android app)

- Complete Android project structure  
- Gradle files  
- Java source  
- XML layouts  
- Sample asset JSON  
- `README.md`  
- `LICENSE`  
- Clean package naming  
- Sensible comments  
- Offline-first architecture  

**Important:** Internet must **not** be mandatory for recommendations, disease library, AI assistant, or farming calendar.

---

### 18. Landing Page Website

Create a **modern, responsive** marketing site for Uncle Jembe.

**Purpose:** Introduce the app, explain benefits to farmers, attract contributors, and provide download / learn-more entry points.

**Style:** Agriculture-tech; green, white, earth brown, soft yellow; clean SaaS layout; **mobile-first**; Swahili-first copy; professional yet farmer-friendly; subtle modern motion where appropriate.

**Sections**

1. **Hero** — Title: *Uncle Jembe — Msaidizi wa Kilimo Tanzania*. Subtitle about crops, seeds, diseases, offline. Buttons: **Pakua App**, **Changia Open Source** (placeholders OK).  
2. **Problem** — Lack of accurate info, wrong seeds, late disease detection, rural connectivity, slow expert advice.  
3. **Solution** — Regional crop recs, seed advice, disease library, calendar, AI assistant, offline-first.  
4. **Features** — Cards: Crop / Seed / Diseases / Offline AI / Calendar / Videos / Profile / Offline data.  
5. **How it works** — (1) Chagua mkoa na wilaya (2) Taarifa za shamba (3) Mazao na mbegu (4) AI maswali (5) Magonjwa na kinga.  
6. **Open source** — Title: *Mradi wa Wazi kwa Kilimo Bora Tanzania*; body welcoming contributors; button **View on GitHub** (placeholder URL).  
7. **App preview** — Mockup cards for Dashboard, Crops, AI, Diseases, Calendar.  
8. **Target users** — Smallholders, students, extension officers, NGOs, universities/researchers, impact-minded developers.  
9. **CTA** — *Tujenge Kilimo Bora kwa Teknolojia*; buttons Pakua App / Contribute on GitHub.  
10. **Footer** — Uncle Jembe, Created by Rashid Mussa, open-source agriculture project, GitHub, contact, privacy, license.

**Technical**

- Clean HTML/CSS/JS **or** React if the repo already uses it.  
- Responsive, SEO-friendly, fast.  
- Meta title: `Uncle Jembe - Offline AI Farming Assistant for Tanzania`  
- Meta description: open-source offline agriculture app; crops, seeds, seasons, diseases; localized data.  
- Open Graph tags for title, description, type, url.  
- Placeholder links for app store / APK and GitHub.  
- Suggested domain reference: `unclejembe.co.tz`  

**Repository layout:** Implement under `landing/` at repo root (see that folder).

---

## Sample Offline Data Shape (example)

```json
{
  "region": "Iringa",
  "district": "Iringa Urban",
  "recommended_crops": [
    {
      "crop_name": "Maize",
      "planting_season": "November to January",
      "recommended_seed": "Hybrid maize suitable for highland areas",
      "soil_type": "Loamy soil",
      "common_diseases": ["Maize streak virus", "Fall armyworm"],
      "advice": "Plant early during the rainy season and use certified seeds."
    }
  ]
}
```

---

## Roadmap (reference)

- **v1.0:** Offline crop/seed/disease, profile, calendar, Sw/En, basic local AI.  
- **v2.0:** Camera disease hints, weather-aware recs, offline videos, expert contributions, data updates.  
- **v3.0:** Marketplace, community, voice AI, extension portal, regional analytics.  

---

## Disclaimer (app + site)

Uncle Jembe provides guidance for education and support. Farmers should consult local agricultural officers or certified experts before major decisions.
