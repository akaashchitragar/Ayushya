# Ayushya

*"Ayushya" (आयुष्य) - Life & Longevity through Ancient Wisdom*

## About the App

Ayushya is a cross-platform mobile application that provides personalized Ayurvedic recommendations based on traditional scriptures. It combines ancient Ayurvedic knowledge with modern AI to deliver remedies tailored to individual users.

### Key Features

- **Profile Management**: Captures detailed Ayurvedic constitution in two parts:
  - **Fixed Profile** (entered once): Body frame and build, skin type, and hair type
  - **Consultation Profile** (answered per remedy): Temperature regulation, appetite and digestion, sleep patterns, mental and emotional tendencies, digestive health, stress response, and current health conditions
- **Remedy Consultation**: Provides personalized remedies based on symptoms the User inputs, individual constitution, and references to classical Ayurvedic texts like Charaka Samhita, Sushruta Samhita, and Ashtanga Hridaya.
- **Multilingual Support**: Access content in multiple languages, especially those spoken in regions where Ayurveda is popular.

### App Flow

1. **Authentication**: User logs in using Google or Facebook account
2. **Basic Profile**: User enters name, gender, age, blood group, height, and weight
3. **Fixed Profile**: User answers questions about body frame and build, skin type, and hair type
4. **Consultation Profile**: User provides information about current health status including temperature regulation, digestion, sleep patterns, etc.
5. **Remedy Screen**: User describes specific symptoms they're experiencing (e.g., flowing nose, headache, sore eyes)
6. **AI Processing**: Advanced AI models (Gemini 1.5 Pro/Ultra or GPT-4) process user symptoms along with both fixed and consultation profile data
7. **Personalized Recommendations**: User receives authentic Ayurvedic home remedies based on traditional scriptures:
   - Charaka Samhita
   - Sushruta Samhita
   - Ashtanga Hridaya
   - Other traditional sources
8. **Results Display**: Remedies are presented with references to their traditional sources

## Tech Stack

### Frontend
- **Framework**: Flutter 3.19+ (Latest stable release)
- **State Management**: 
  - Riverpod 2.0+
  - Flutter Hooks
- **UI Design**: 
  - Material 3 (Material You) design system
  - Adaptive and responsive layouts
  - Dynamic theming with color extraction
  - **Color Palette**: Ayurvedic-inspired natural and earthy tones:
    - Turmeric gold (#E4A11B)
    - Neem green (#728C69)
    - Terracotta (#C97C5D)
    - Sandalwood (#B49A67)
    - Ashwagandha root (#8D6E63)
    - Aloe Vera (#A6BB8D)
    - Deep herbal brown (#5D4037)
    - Vibrant saffron (#FF5722)
- **Animation**: 
  - Lottie for rich animations
  - Flutter animations for micro-interactions
- **Dependencies**:
  - `flutter_localizations` for internationalization
  - `flutter_svg` for vector graphics
  - `shared_preferences` for local storage
  - `http`/`dio` for API communication

### Backend
- **Backend as a Service**: Supabase (Latest version)
- **Database**: Supabase (PostgreSQL)
- **Authentication**: 
  - Supabase Auth
  - Social login (Google, Facebook)
- **Storage**: Supabase Storage for user data and assets

### AI/ML
- **Primary AI Model**: Gemini 1.5 Pro/Ultra
- **Alternative AI Model**: GPT-4/GPT-4o
- **Integration**: 
  - Google AI SDK for Flutter
  - OpenAI API via REST

### Hosting
- **Cloud Provider**: AWS
- **Services**:
  - AWS Amplify for hosting (if web support is added)
  - Amazon S3 for static assets
  - Amazon CloudFront for content delivery

### Analytics and Monitoring
- **Analytics**: Firebase Analytics
- **Error Monitoring**: Sentry
- **Performance Monitoring**: Firebase Performance

### Payment Integration
- **Payment Gateway**: Razorpay
- **In-App Purchases**: 
  - Google Play Billing
  - Apple In-App Purchase

### Push Notifications
- **Service**: Firebase Cloud Messaging (FCM)
- **Local Notifications**: flutter_local_notifications

## Getting Started

### Prerequisites
- Flutter SDK 3.19.0 or higher
- Dart SDK 3.2.0 or higher
- Supabase account
- Firebase project
- AWS account
- Razorpay merchant account
- Google/OpenAI API keys for AI integration

### Installation
```bash
# Clone the repository
git clone https://github.com/akaashchitragar/ayushya.git

# Navigate to the project directory
cd ayushya

# Install dependencies
flutter pub get

# Run the app
flutter run
```

### Building APK
```bash
# Build a release APK
flutter build apk

# The APK will be available at:
# build/app/outputs/flutter-apk/app-release.apk

# Build a debug APK
flutter build apk --debug

# Build split APKs by architecture (smaller size)
flutter build apk --split-per-abi

# Install directly to a connected device
flutter install
```

### Environment Setup
Create a `.env` file in the root directory with the following variables:
```
SUPABASE_URL=https://izfnriaczcaplztpjqvj.supabase.co
SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Iml6Zm5yaWFjemNhcGx6dHBqcXZqIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDYxMDY5MjIsImV4cCI6MjA2MTY4MjkyMn0.0NdDQ0pgtmsex_qsO5r4OtejN4HFhHSAX2WWtbG06qM
GOOGLE_AI_API_KEY=AIzaSyD5xr3CEnK7grZ16_aJmpLh7bfUOVwipuY
OPENAI_API_KEY=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
```

## Project Structure
```
ayushya/
├── lib/
│   ├── components/           # Reusable UI components
│   ├── models/               # Data models and state
│   ├── screens/              # App screens
│   │   ├── auth/             # Authentication screens
│   │   ├── profile/          # Profile management screens
│   │   ├── consultation/     # Consultation screens
│   │   └── remedies/         # Remedy display screens
│   ├── services/             # API and backend services
│   │   ├── ai_service.dart   # AI integration
│   │   ├── auth_service.dart # Authentication
│   │   └── database.dart     # Database operations
│   ├── utils/                # Utility functions and constants
│   │   ├── theme.dart        # App theming
│   │   └── constants.dart    # App constants
│   └── main.dart             # App entry point
├── assets/                   # Static assets
│   ├── images/               # Images and illustrations
│   ├── fonts/                # Custom fonts
│   ├── animations/           # Lottie animations
│   └── translations/         # Localization files
├── android/                  # Android-specific code
├── ios/                      # iOS-specific code
├── test/                     # Test cases
└── pubspec.yaml              # Dependencies
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For any inquiries, please reach out to [akash@webart4u.com](mailto:akash@webart4u.com).
