# 🌿 Ayushya

<div align="center">
  
  ![Ayurvedic Wellness](https://img.shields.io/badge/Ayurvedic-Wellness-brightgreen?style=for-the-badge&logo=leaf&logoColor=white)
  ![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
  ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
  ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
  ![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
  ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
  
  *"Ayushya" (आयुष्य) - Life & Longevity through Ancient Wisdom*
  
</div>

## ✨ About the Website

Ayushya is a comprehensive web platform that provides personalized Ayurvedic recommendations based on traditional scriptures. It combines ancient Ayurvedic knowledge with modern AI to deliver remedies tailored to individual users.

## 🔍 How It Works - A Practical Example

Imagine you're experiencing cold symptoms and a headache. Here's how Ayushya helps you:

1. **Visit the Website** - Login with your existing account
  
2. **Your Profile is Ready** - The site already knows your body type (Vata/Pitta/Kapha), constitution, and health baseline from your previously entered profile

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

### 🔄 Website Flow

1. **🔐 Authentication**: User logs in using Google or Facebook account
2. **👤 Basic Profile**: User enters name, gender, age, blood group, height, and weight
3. **🧬 Fixed Profile**: User answers questions about body frame and build, skin type, and hair type
4. **📋 Consultation Profile**: User provides information about current health status including temperature regulation, digestion, sleep patterns, etc.
5. **🩺 Remedy Page**: User describes specific symptoms they're experiencing (e.g., flowing nose, headache, sore eyes)
6. **🧠 AI Processing**: Advanced AI models (Gemini 1.5 Pro/Ultra or GPT-4) process user symptoms along with both fixed and consultation profile data
7. **💫 Personalized Recommendations**: User receives authentic Ayurvedic home remedies based on traditional scriptures:
   - Charaka Samhita
   - Sushruta Samhita
   - Ashtanga Hridaya
   - Other traditional sources
8. **📱 Results Display**: Remedies are presented with references to their traditional sources

## 🛠️ Tech Stack

### 🌐 Frontend
- **Framework**: Next.js 15.3.1
  - Server Components for improved performance
  - App Router for advanced routing capabilities
  - React Server Actions for form handling
  - API Routes for backend integration
- **State Management**: 
  - React Context API
  - Zustand for client-side state
  - React Query for server state
- **UI Design**: 
  - Tailwind CSS for utility-first styling
  - Shadcn UI for accessible component library
  - Framer Motion for fluid animations
  - **Color Palette**: Ayurvedic-inspired natural and vibrant earthy tones:
    - <span style="color:#FFCC33">■</span> Turmeric gold (#FFCC33)
    - <span style="color:#88CC66">■</span> Fresh leaf green (#88CC66)
    - <span style="color:#FF6666">■</span> Hibiscus red (#FF6666)
    - <span style="color:#FFAA33">■</span> Marigold orange (#FFAA33)
    - <span style="color:#66CCFF">■</span> Sky blue (#66CCFF)
    - <span style="color:#FF99CC">■</span> Lotus pink (#FF99CC)
    - <span style="color:#FF5722">■</span> Vibrant saffron (#FF5722)
    - <span style="color:#FFDD44">■</span> Sunlight yellow (#FFDD44)
- **Form Management**:
  - React Hook Form with Zod validation
- **Animation**: 
  - Framer Motion for page transitions and microinteractions
  - Lottie for rich illustrations
- **Dependencies**:
  - `next-intl` for internationalization
  - `contentlayer` for static content management
  - `lucide-react` for beautiful icons
  - `axios` for API communication

### 🖥️ Backend
- **Framework**: Next.js API Routes with Node.js
  - RESTful API endpoints
  - Edge/serverless functions
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
  - AWS Amplify for Next.js hosting and CI/CD
  - Amazon S3 for static assets
  - Amazon CloudFront for content delivery
  - MongoDB Atlas for database
  - Amazon Lambda for serverless functions (optional)

### 📊 Analytics and Monitoring
- **Analytics**: AWS Amplify Analytics and Google Analytics 4
- **Error Monitoring**: Sentry
- **Performance Monitoring**: AWS CloudWatch and Next.js Analytics

### 💳 Payment Integration
- **Payment Gateway**: Stripe and Razorpay
- **Subscription Management**: Stripe Billing

### 📲 Notifications
- **Service**: OneSignal for web push notifications
- **Email**: Resend for transactional emails

## 🚀 Getting Started

### 📋 Prerequisites
- Node.js 18.0.0 or higher
- Yarn or npm
- MongoDB (local or Atlas)
- AWS account
- Stripe/Razorpay merchant account
- Google/OpenAI API keys for AI integration
- Clerk account for authentication

## 📁 Project Structure
```
ayushya/
├── app/                          # Next.js App Router
│   ├── (auth)/                   # Authentication routes
│   │   ├── login/                # Login page
│   │   ├── register/             # Registration page
│   │   └── layout.tsx            # Auth layout
│   ├── (dashboard)/              # Authenticated routes
│   │   ├── profile/              # Profile management
│   │   ├── consultation/         # Consultation pages
│   │   ├── remedies/             # Remedies pages
│   │   └── layout.tsx            # Dashboard layout
│   ├── api/                      # API Routes (Backend)
│   │   ├── auth/                 # Authentication endpoints
│   │   ├── profile/              # Profile endpoints
│   │   ├── consultation/         # Consultation endpoints
│   │   ├── remedies/             # Remedy endpoints
│   │   └── ai/                   # AI integration endpoints
│   ├── globals.css               # Global styles
│   └── layout.tsx                # Root layout
├── components/                   # Reusable components
│   ├── ui/                       # UI components
│   ├── forms/                    # Form components
│   └── shared/                   # Shared components
├── lib/                          # Utility functions
│   ├── api/                      # API client
│   ├── db/                       # Database integration
│   │   ├── models/               # MongoDB schemas
│   │   ├── schemas/              # Zod validation schemas
│   │   └── connect.ts            # Database connection
│   ├── ai/                       # AI integration
│   │   ├── gemini.ts             # Gemini API integration
│   │   └── openai.ts             # OpenAI API integration
│   ├── utils/                    # Helper functions
│   │   ├── format.ts             # Formatting utilities
│   │   ├── validation.ts         # Validation functions
│   │   └── auth.ts               # Authentication utilities
│   └── middleware/               # API middleware
│       ├── auth.ts               # Authentication middleware
│       └── error.ts              # Error handling
├── hooks/                        # Custom React hooks
├── types/                        # TypeScript type definitions
├── public/                       # Static files
│   ├── images/                   # Images
│   └── fonts/                    # Fonts
├── styles/                       # Additional styles
├── middleware.ts                 # Next.js middleware
├── next.config.js                # Next.js configuration
├── tailwind.config.js            # Tailwind CSS configuration
├── amplify.yml                   # AWS Amplify configuration
├── .env.local.example            # Example environment variables
├── tsconfig.json                 # TypeScript configuration
└── package.json                  # Dependencies
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