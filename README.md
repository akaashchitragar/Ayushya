# 🌿 Ayushya

<div align="center">
  
  ![Ayurvedic Wellness](https://img.shields.io/badge/Ayurvedic-Wellness-brightgreen?style=for-the-badge&logo=leaf&logoColor=white)
  ![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
  ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
  ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
  ![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
  ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
  
  *"Ayushya" (आयुष्य) - Life & Longevity through Ancient Wisdom*
  
</div>

## ✨ About the App

Ayushya is an Android mobile application that provides personalized Ayurvedic recommendations based on traditional scriptures. It combines ancient Ayurvedic knowledge with modern AI to deliver remedies tailored to individual users.

## 🔍 How It Works - A Practical Example

Imagine you're experiencing cold symptoms and a headache. Here's how Ayushya helps you:

1. **Open the App** - Login with your existing account
  
2. **Your Profile is Ready** - The app already knows your body type (Vata/Pitta/Kapha), constitution, and health baseline from your previously entered profile

3. **Describe Your Symptoms** - Simply type or speak: "I have a cold with runny nose and a throbbing headache since yesterday"

4. **Behind the Scenes** - The AI analyzes:
   - Your symptoms (cold, runny nose, headache)
   - Your body constitution (from your profile)
   - Your health history and preferences
   - Traditional Ayurvedic texts for matching conditions

5. **Personalized Results** - Within seconds, you receive personalized home remedies:

   ```
   🌿 RECOMMENDED HOME REMEDIES FOR YOUR COLD & HEADACHE:

   1. Ginger-Tulsi Tea
      • Boil 1 cup water with 1-inch fresh ginger
      • Add 5-7 fresh tulsi (holy basil) leaves
      • Steep for 5 minutes, strain and add honey to taste
      • Drink warm 2-3 times daily
   
   2. Steam Inhalation with Ajwain
      • Boil water in a pot
      • Add 1 tsp carom seeds (ajwain)
      • Inhale the steam for 5-10 minutes
      • Cover head with towel for better effect
   
   3. Turmeric Milk
      • Heat 1 cup milk with ¼ tsp turmeric powder
      • Add pinch of black pepper and ½ tsp ghee
      • Drink before bedtime
   
   SOURCE: Charaka Samhita, Sutrasthana 5:62-65
   ```

6. **Save for Later** - Save these remedies to your profile for future reference or share with family

This personalized approach considers your unique constitution rather than providing generic remedies, making the treatment more effective according to Ayurvedic principles.

### 🎯 Key Features

- **📊 Profile Management**: Captures detailed Ayurvedic constitution in two parts:
  - **📝 Fixed Profile** (entered once): Body frame and build, skin type, and hair type
  - **🔄 Consultation Profile** (answered per remedy): Temperature regulation, appetite and digestion, sleep patterns, mental and emotional tendencies, digestive health, stress response, and current health conditions
- **💊 Remedy Consultation**: Provides personalized remedies based on symptoms the User inputs, individual constitution, and references to classical Ayurvedic texts like Charaka Samhita, Sushruta Samhita, and Ashtanga Hridaya.
- **🌐 Multilingual Support**: Access content in multiple languages, especially those spoken in regions where Ayurveda is popular.

### 🔄 App Flow

1. **🔐 Authentication**: User logs in using Google or Facebook account
2. **👤 Basic Profile**: User enters name, gender, age, blood group, height, and weight
3. **🧬 Fixed Profile**: User answers questions about body frame and build, skin type, and hair type
4. **📋 Consultation Profile**: User provides information about current health status including temperature regulation, digestion, sleep patterns, etc.
5. **🩺 Remedy Screen**: User describes specific symptoms they're experiencing (e.g., flowing nose, headache, sore eyes)
6. **🧠 AI Processing**: Advanced AI models (Gemini 1.5 Pro/Ultra or GPT-4) process user symptoms along with both fixed and consultation profile data
7. **💫 Personalized Recommendations**: User receives authentic Ayurvedic home remedies based on traditional scriptures:
   - Charaka Samhita
   - Sushruta Samhita
   - Ashtanga Hridaya
   - Other traditional sources
8. **📱 Results Display**: Remedies are presented with references to their traditional sources

## 🛠️ Tech Stack

### 📱 Frontend
- **Framework**: React Native with Expo (Latest stable release)
- **State Management**: 
  - React Context API
  - Redux or Zustand
  - React Hooks
- **UI Design**: 
  - React Native Paper for Material Design implementation
  - Material Design 3 principles with adaptive layouts
  - Theming system for Ayurvedic color palette
  - **Color Palette**: Ayurvedic-inspired natural and vibrant earthy tones:
    - <span style="color:#FFCC33">■</span> Turmeric gold (#FFCC33)
    - <span style="color:#88CC66">■</span> Fresh leaf green (#88CC66)
    - <span style="color:#FF6666">■</span> Hibiscus red (#FF6666)
    - <span style="color:#FFAA33">■</span> Marigold orange (#FFAA33)
    - <span style="color:#66CCFF">■</span> Sky blue (#66CCFF)
    - <span style="color:#FF99CC">■</span> Lotus pink (#FF99CC)
    - <span style="color:#FF5722">■</span> Vibrant saffron (#FF5722)
    - <span style="color:#FFDD44">■</span> Sunlight yellow (#FFDD44)
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

### 🖥️ Backend
- **Framework**: Node.js with Express.js
  - RESTful API endpoints
  - Middleware-based architecture
  - TypeScript for type safety
- **Database**: MongoDB with Mongoose
  - Document-based data model for flexible Ayurvedic profiles
  - Scalable for growing user base
- **Authentication**: 
  - Clerk Authentication
  - JWT token verification
  - Social login (Google, Facebook)
- **Storage**: AWS S3 for user data and assets
- **API Documentation**: 
  - Swagger/OpenAPI
  - Express OpenAPI validation

### 🧠 AI/ML
- **Primary AI Model**: Gemini 1.5 Pro/Ultra
- **Alternative AI Model**: GPT-4/GPT-4o
- **Integration**: 
  - `@google/generative-ai` package for Gemini
  - `openai` package for GPT models
  - Background job processing with Bull queue

### ☁️ Hosting
- **Cloud Provider**: AWS
- **Services**:
  - AWS Amplify for hosting (if web support is added)
  - Amazon S3 for static assets
  - Amazon CloudFront for content delivery

### 📊 Analytics and Monitoring
- **Analytics**: Firebase Analytics
- **Error Monitoring**: Sentry
- **Performance Monitoring**: Firebase Performance

### 💳 Payment Integration
- **Payment Gateway**: Razorpay
- **In-App Purchases**: 
  - React Native In-App Purchase for Android
  - Google Play Billing Library

### 📲 Push Notifications
- **Service**: OneSignal
- **Local Notifications**: expo-notifications

## 🚀 Getting Started

### 📋 Prerequisites
- Node.js 18.0.0 or higher
- Yarn or npm
- Expo CLI (`npm install -g expo-cli`)
- MongoDB (local or Atlas)
- AWS account
- Razorpay merchant account
- Google/OpenAI API keys for AI integration
- Clerk account for authentication

### 💻 Installation
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
yarn install
# or
npm install

# Start the development servers
# Terminal 1 - Frontend
cd frontend
expo start

# Terminal 2 - Backend
cd backend
npm run dev
```

### 📦 Building for Production
```bash
# Build for Android
expo build:android

# Generate optimized native code (with EAS)
eas build --platform android

# Preview with development builds
eas build --profile development --platform android
```

### ⚙️ Environment Setup
Create a `.env` file in the frontend directory with the following variables:
```
REACT_APP_CLERK_PUBLISHABLE_KEY=pk_test_*****
REACT_APP_API_URL=http://localhost:4000/api
REACT_APP_GOOGLE_AI_API_KEY=AIzaSyD5xr3CEnK7grZ16_aJmpLh7bfUOVwipuY
```

Create a `.env` file in the backend directory with the following variables:
```
PORT=4000
NODE_ENV=development
MONGODB_URI=mongodb://localhost:27017/ayushya
CLERK_SECRET_KEY=sk_test_*****
GOOGLE_AI_API_KEY=AIzaSyD5xr3CEnK7grZ16_aJmpLh7bfUOVwipuY
OPENAI_API_KEY=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
AWS_ACCESS_KEY_ID=your-aws-access-key
AWS_SECRET_ACCESS_KEY=your-aws-secret-key
AWS_STORAGE_BUCKET_NAME=ayushya-storage
```

## 📁 Project Structure
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
│   └── tsconfig.json             # TypeScript configuration
├── backend/
│   ├── src/
│   │   ├── config/               # Configuration files
│   │   │   ├── database.js       # MongoDB connection
│   │   │   └── env.js            # Environment variables
│   │   ├── controllers/          # Request handlers
│   │   │   ├── profileController.js  # User profile handlers
│   │   │   ├── consultationController.js  # Consultation handlers
│   │   │   └── remedyController.js  # Remedy handlers
│   │   ├── middleware/           # Express middleware
│   │   │   ├── auth.js           # Authentication middleware
│   │   │   └── errorHandler.js   # Error handling
│   │   ├── models/               # MongoDB schemas
│   │   │   ├── User.js           # User model
│   │   │   ├── Profile.js        # Profile model
│   │   │   └── Remedy.js         # Remedy model
│   │   ├── routes/               # API routes
│   │   │   ├── profileRoutes.js  # Profile endpoints
│   │   │   ├── consultationRoutes.js  # Consultation endpoints
│   │   │   └── remedyRoutes.js   # Remedy endpoints
│   │   ├── services/             # Business logic
│   │   │   ├── geminiService.js  # Gemini API integration
│   │   │   └── openaiService.js  # OpenAI API integration
│   │   ├── utils/                # Helper functions
│   │   │   └── asyncHandler.js   # Async error handling
│   │   └── app.js                # Express app setup
│   ├── package.json              # Dependencies
│   └── tsconfig.json             # TypeScript configuration
└── README.md                     # Project documentation
```

## 👥 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)

## 📞 Contact
For any inquiries, please reach out to [akash@webart4u.com](mailto:akash@webart4u.com).

---

<div align="center">
  <img src="https://img.shields.io/badge/Made%20with%20%E2%9D%A4%EF%B8%8F%20for-Ayurvedic%20Wellness-orange" alt="Made with love for Ayurvedic Wellness" />
</div>