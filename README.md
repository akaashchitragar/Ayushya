# Ayushya

*"Ayushya" (आयुष्य) - Life & Longevity through Ancient Wisdom*

## About the App

Ayushya is an Android mobile application that provides personalized Ayurvedic recommendations based on traditional scriptures. It combines ancient Ayurvedic knowledge with modern AI to deliver remedies tailored to individual users.

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
- **Framework**: React Native with Expo (Latest stable release)
- **State Management**: 
  - React Context API
  - Redux or Zustand
  - React Hooks
- **UI Design**: 
  - React Native Paper or UI Kitten for Material Design
  - Adaptive layouts for different Android screen sizes
  - Material Design 3 principles
  - **Color Palette**: Ayurvedic-inspired natural and vibrant earthy tones:
    - Turmeric gold (#FFCC33)
    - Fresh leaf green (#88CC66)
    - Hibiscus red (#FF6666)
    - Marigold orange (#FFAA33)
    - Sky blue (#66CCFF)
    - Lotus pink (#FF99CC)
    - Vibrant saffron (#FF5722)
    - Sunlight yellow (#FFDD44)
- **Navigation**:
  - React Navigation for screen transitions
- **Animation**: 
  - Lottie for rich animations
  - React Native Reanimated for micro-interactions
- **Dependencies**:
  - `i18next` for internationalization
  - `react-native-svg` for vector graphics
  - `@react-native-async-storage/async-storage` for local storage
  - `axios` for API communication

### Backend
- **Framework**: Django (Latest stable release)
  - Django REST Framework for RESTful API
  - Django ORM for database operations
- **Database**: PostgreSQL
- **Authentication**: 
  - Clerk Authentication
  - JWT token verification
  - Social login (Google, Facebook, Apple)
- **Storage**: AWS S3 for user data and assets
- **API Documentation**: 
  - Swagger/OpenAPI
  - DRF Spectacular

### AI/ML
- **Primary AI Model**: Gemini 1.5 Pro/Ultra
- **Alternative AI Model**: GPT-4/GPT-4o
- **Integration**: 
  - `google-generativeai` Python package for Gemini
  - `openai` Python package for GPT models
  - Asynchronous processing with Celery

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
  - React Native In-App Purchase for Android
  - Google Play Billing Library

### Push Notifications
- **Service**: OneSignal
- **Local Notifications**: expo-notifications

## Getting Started

### Prerequisites
- Node.js 16.0.0 or higher
- Yarn or npm
- Expo CLI (`npm install -g expo-cli`)
- Python 3.10 or higher
- Django 4.2 or higher
- PostgreSQL
- Firebase project
- AWS account
- Razorpay merchant account
- Google/OpenAI API keys for AI integration
- Clerk account for authentication

### Installation
```bash
# Clone the repository
git clone https://github.com/akaashchitragar/ayushya.git

# Navigate to the project directory
cd ayushya

# Frontend setup
cd frontend
yarn install
# or
npm install

# Backend setup
cd ../backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate

# Start the development servers
# Terminal 1 - Frontend
cd frontend
expo start

# Terminal 2 - Backend
cd backend
python manage.py runserver
```

### Building for Production
```bash
# Build for Android
expo build:android

# Generate optimized native code (with EAS)
eas build --platform android

# Preview with development builds
eas build --profile development --platform android
```

### Environment Setup
Create a `.env` file in the frontend directory with the following variables:
```
REACT_APP_CLERK_PUBLISHABLE_KEY=pk_test_*****
REACT_APP_API_URL=http://localhost:8000/api
REACT_APP_GOOGLE_AI_API_KEY=AIzaSyD5xr3CEnK7grZ16_aJmpLh7bfUOVwipuY
```

Create a `.env` file in the backend directory with the following variables:
```
SECRET_KEY=your-django-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=postgres://user:password@localhost:5432/ayushya
CLERK_SECRET_KEY=sk_test_*****
GOOGLE_AI_API_KEY=AIzaSyD5xr3CEnK7grZ16_aJmpLh7bfUOVwipuY
OPENAI_API_KEY=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
AWS_ACCESS_KEY_ID=your-aws-access-key
AWS_SECRET_ACCESS_KEY=your-aws-secret-key
AWS_STORAGE_BUCKET_NAME=ayushya-storage
```

## Project Structure
```
ayushya/
├── frontend/
│   ├── src/
│   │   ├── components/           # Reusable UI components
│   │   ├── models/               # TypeScript interfaces and data models
│   │   ├── screens/              # App screens
│   │   │   ├── auth/             # Authentication screens
│   │   │   ├── profile/          # Profile management screens
│   │   │   ├── consultation/     # Consultation screens
│   │   │   └── remedies/         # Remedy display screens
│   │   ├── services/             # API and backend services
│   │   │   ├── aiService.js      # AI integration
│   │   │   ├── authService.js    # Authentication
│   │   │   └── api.js            # API calls
│   │   ├── utils/                # Utility functions and constants
│   │   │   ├── theme.js          # App theming
│   │   │   └── constants.js      # App constants
│   │   └── App.js                # App entry point
│   ├── assets/                   # Static assets
│   │   ├── images/               # Images and illustrations
│   │   ├── fonts/                # Custom fonts
│   │   ├── animations/           # Lottie animations
│   │   └── translations/         # Localization files
│   ├── android/                  # Android-specific code
│   ├── app.json                  # Expo configuration
│   ├── babel.config.js           # Babel configuration
│   ├── metro.config.js           # Metro bundler configuration
│   ├── eas.json                  # EAS Build configuration
│   ├── package.json              # Dependencies
│   └── tsconfig.json             # TypeScript configuration (if using TypeScript)
├── backend/
│   ├── ayushya/                  # Django project directory
│   │   ├── settings.py           # Django settings
│   │   ├── urls.py               # URL routing
│   │   └── wsgi.py               # WSGI configuration
│   ├── api/                      # Django app for API
│   │   ├── models.py             # Database models
│   │   ├── serializers.py        # DRF serializers
│   │   ├── views.py              # API views
│   │   └── urls.py               # API URL routing
│   ├── authentication/           # Django app for Clerk auth
│   │   ├── middleware.py         # JWT verification
│   │   └── utils.py              # Auth utilities
│   ├── ai/                       # Django app for AI integration
│   │   ├── gemini_service.py     # Gemini API integration
│   │   ├── openai_service.py     # OpenAI API integration
│   │   └── views.py              # AI API endpoints
│   ├── manage.py                 # Django management script
│   └── requirements.txt          # Python dependencies
└── README.md                     # Project documentation
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For any inquiries, please reach out to [akash@webart4u.com](mailto:akash@webart4u.com).