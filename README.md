# Uncle Jembe

**Uncle Jembe** is an open-source Android agriculture assistant built to help Tanzanian farmers make better farming decisions using offline agricultural data and AI-powered recommendations.

The app helps farmers understand what crops to plant, which seeds to use, common plant diseases in their area, planting seasons, and practical farming guidance based on Tanzanian regions.

## Author

Created by **Rashid Mussa**  
Founder of Tembo Labs & TalkNa
Tanzania

## Vision

To improve agriculture in Tanzania by giving farmers simple, accessible, offline-first digital tools that help them make smarter farming decisions.

## Mission

Uncle Jembe aims to support farmers with localized agricultural knowledge, crop recommendations, seed guidance, plant disease information, and AI-based farming advice that works even without internet access.

## Why Uncle Jembe?

Many smallholder farmers in Tanzania face challenges such as:

- Limited access to agricultural experts
- Poor seed selection
- Lack of localized farming information
- Plant diseases and pests
- Unpredictable weather patterns
- Low internet access in rural areas

Uncle Jembe is designed to solve these challenges through an offline-first mobile application.

## Key Features

### 1. Location-Based Crop Recommendation

Farmers can select their region, district, or farming zone and get recommended crops suitable for that area.

Examples:

- Iringa: Maize, beans, sunflower, potatoes
- Mbeya: Rice, maize, potatoes, bananas
- Dodoma: Sunflower, sorghum, millet, grapes
- Morogoro: Rice, maize, sesame, vegetables

### 2. Seed Recommendation

The app suggests suitable seed varieties based on:

- Region
- Climate zone
- Rainfall pattern
- Soil type
- Crop type
- Planting season

### 3. Offline AI Farming Assistant

Uncle Jembe includes an offline AI-style assistant that helps farmers ask questions such as:

- What should I plant in Iringa this season?
- Which maize seed is good for Dodoma?
- Why are my tomato leaves turning yellow?
- How can I prevent maize disease?
- When should I plant sunflower?

The assistant uses locally stored agricultural knowledge.

### 4. Plant Disease Library

Farmers can browse common crop diseases, symptoms, causes, prevention methods, and treatment guidance.

Information includes:

- Disease name
- Affected crop
- Symptoms
- Causes
- Prevention
- Recommended action
- Region where disease is common

### 5. Offline Knowledge Base

All core farming information is stored locally so the app works without internet.

Offline data may include:

- Crop data
- Seed varieties
- Regional farming recommendations
- Disease information
- Farming calendars
- Pest management guides
- Soil and climate notes

### 6. Farming Calendar

The app provides planting and harvesting guidance based on Tanzanian agricultural seasons.

### 7. Educational Videos

The app supports farming tutorial videos using Media3 ExoPlayer. Videos can be bundled offline or downloaded when internet is available.

### 8. Secure Farmer Profile

Farmers can create a local profile with:

- Name
- Region
- District
- Farm size
- Preferred crops
- Soil type
- Farming experience

Sensitive data is stored securely using AndroidX Security Crypto.

## Open Source Purpose

Uncle Jembe is open-source because agriculture is a community challenge.

We welcome contributions from:

- Android developers
- AI developers
- Agricultural experts
- Agronomists
- Universities
- NGOs
- Government agriculture officers
- Data contributors
- UX/UI designers
- Translators

## Tech Stack

### Android

- Java 17
- Gradle
- Android Gradle Plugin 8.5.2
- compileSdk 34
- targetSdk 34
- minSdk 24

### Libraries

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

## Project Goals

- Build a simple offline-first farming assistant
- Provide localized Tanzanian agricultural information
- Help farmers choose the right crops and seeds
- Reduce crop losses caused by disease and poor planning
- Create an open-source knowledge platform for agriculture in Tanzania

## Suggested App Modules

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

## Sample Offline Data Structure

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

## AI Assistant Concept

The offline AI assistant should use local JSON data and rule-based intelligence first.

Example logic:

```text
If user location = Dodoma
And rainfall = low
Recommend drought-resistant crops such as sunflower, sorghum, millet, and groundnuts.
```

Future versions may support:

- On-device AI model
- Image-based plant disease detection
- Voice assistant in Swahili
- SMS-based farming advice
- Integration with weather APIs
- Marketplace for seeds and farm inputs

## Roadmap

### Version 1.0

- Offline crop recommendation
- Seed recommendation
- Disease library
- Farmer profile
- Farming calendar
- Swahili and English support
- Basic AI assistant using local data

### Version 2.0

- Plant disease detection using camera
- Weather-based recommendations
- Offline video lessons
- Expert contribution dashboard
- Data update system

### Version 3.0

- Marketplace for seeds and inputs
- Farmer community forum
- AI voice assistant
- Extension officer portal
- Regional agriculture analytics

## Contribution Guidelines

We welcome contributions.

You can contribute by:

- Adding crop data
- Adding seed varieties
- Improving disease information
- Fixing bugs
- Improving UI/UX
- Translating content
- Adding farming calendars
- Improving offline AI logic

## Landing Page

A responsive marketing site lives in [`landing/`](landing/). Open `landing/index.html` in a browser or host the `landing` folder on any static host.

## Full Build Prompt

For a single consolidated specification (Android app **and** landing page, items 1–18), see [`docs/APP_BUILD_PROMPT.md`](docs/APP_BUILD_PROMPT.md).

## License

This project is released under the [MIT License](LICENSE).

## Disclaimer

Uncle Jembe provides agricultural guidance for educational and support purposes. Farmers should also consult local agricultural officers or certified experts before making major farming decisions.

## Contact

For collaboration, contribution, or partnership:

**Rashid Mussa**  
Tanzania  
Founder, TalkNa
