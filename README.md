# 🥗 Food Nutrition Analyzer — Flutter App

AI-powered food nutrition analyzer for diabetes patients.

## 📱 Features

- ✅ **Image Upload** — Camera + Gallery
- ✅ **AI Food Detection** — Google ML Kit Image Labeling
- ✅ **Nutrition Analysis** — Sugar, Carbs, Protein, Fat, Calories, Fiber
- ✅ **Diabetes Check** — Safe/Unsafe for diabetic patients
- ✅ **Blood Sugar Impact** — Glucose & Insulin level indicators
- ✅ **Health Suggestions** — Personalized tips
- ✅ **Voice Assistant** — Ask questions, get spoken answers
- ✅ **Daily History** — Track all scanned foods
- ✅ **Daily Goals** — Calorie & Sugar tracking
- ✅ **User Profiles** — Diabetes-aware recommendations
- ✅ **Local Food Database** — Works offline for common foods

---

## 🚀 Quick Setup

### Step 1 — Install Flutter
```
https://flutter.dev/docs/get-started/install
```

### Step 2 — Get Dependencies
```bash
cd food_nutrition_analyzer
flutter pub get
```

### Step 3 — Run the App
```bash
flutter run
```

---

## 🔑 API Setup (Optional — App works offline too)

### Nutritionix API (Nutrition Data)
1. Register at https://www.nutritionix.com/business/api
2. Get your App ID and App Key
3. Open `lib/services/nutrition_api_service.dart`
4. Replace these values:
   ```dart
   static const String _appId = 'YOUR_NUTRITIONIX_APP_ID';
   static const String _appKey = 'YOUR_NUTRITIONIX_APP_KEY';
   ```

### Firebase (Optional — for cloud history)
1. Go to https://console.firebase.google.com
2. Create new project
3. Add Android/iOS app
4. Download `google-services.json` → place in `android/app/`
5. Uncomment Firebase init in `lib/main.dart`

---

## 📦 Flutter Packages Used

| Package | Purpose |
|---------|---------|
| `image_picker` | Camera & Gallery photo selection |
| `http` | API calls to Nutritionix |
| `firebase_core` | Firebase initialization |
| `firebase_auth` | User authentication |
| `cloud_firestore` | Cloud database for history |
| `google_mlkit_image_labeling` | AI food detection |
| `speech_to_text` | Voice input |
| `flutter_tts` | Voice output (text-to-speech) |
| `provider` | State management |
| `fl_chart` | Nutrition charts |
| `shared_preferences` | Local storage |

---

## 📂 Project Structure

```
lib/
├── main.dart                    # App entry point
├── models/
│   └── food_nutrition.dart      # Data model + local DB
├── screens/
│   ├── splash_screen.dart       # App splash
│   ├── login_screen.dart        # Login
│   ├── signup_screen.dart       # Registration
│   ├── home_screen.dart         # Main screen + scan
│   ├── result_screen.dart       # Nutrition results
│   ├── history_screen.dart      # Scan history
│   └── profile_screen.dart      # User profile
├── services/
│   ├── nutrition_provider.dart  # State management
│   ├── auth_provider.dart       # Auth state
│   ├── nutrition_api_service.dart # Nutritionix API
│   ├── food_detection_service.dart # ML Kit detection
│   └── voice_assistant_service.dart # Voice features
└── utils/
    └── app_theme.dart           # Colors & theme
```

---

## 📱 Screens

| Screen | Description |
|--------|-------------|
| Splash | App logo animation |
| Login | Email/password login |
| Signup | Register with diabetes profile |
| Home | Upload/camera button + quick search |
| Result | Full nutrition details + diabetes alert |
| History | Past scanned foods with swipe-to-delete |
| Profile | User info, daily goals, settings |

---

## 🤖 AI Tech Stack

- **Image Detection**: Google ML Kit Image Labeling
- **Nutrition Data**: Nutritionix API + Local offline database
- **Voice Input**: speech_to_text package
- **Voice Output**: flutter_tts package

---

## 🏥 Diabetes Features

- Every food shows ✅ or ⚠️ for diabetic suitability
- Glucose impact: Low / Medium / High
- Insulin effect: Low / Medium / High
- Personalized notes for diabetic patients
- Daily sugar tracking with goal alerts

---

## 🎓 FYP Project Info

- **Category**: AI • ML • Healthcare • Mobile • Computer Vision
- **Degree**: BSCS (Bachelor of Computer Science)
- **Technologies**: Flutter, Firebase, Google ML Kit, Nutritionix API
- **Version**: 1.0.0

---

## 🔮 Future Features

- [ ] Urdu language support
- [ ] Diet plan generator
- [ ] Sugar alert system
- [ ] BMI calculator
- [ ] Water reminder notifications
- [ ] Barcode scanner
- [ ] Meal planner

---

## 📞 Common Issues

**Q: App crashes on startup?**
A: Run `flutter pub get` and make sure you have Flutter 3.0+

**Q: Food not detected correctly?**
A: Enable Google ML Kit by uncommenting code in `food_detection_service.dart`

**Q: Nutrition data not loading?**
A: Add your Nutritionix API keys or the app will use local offline database

**Q: Firebase errors?**
A: Either add `google-services.json` or keep Firebase commented out in `main.dart`
