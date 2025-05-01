# Ayushya

![Ayushya Logo](assets/logo.png)

*"Ayushya" (आयुष्य) - Life & Longevity through Ancient Wisdom*

## About the App

Ayushya is a cross-platform mobile application that provides personalized Ayurvedic recommendations based on traditional scriptures. It combines ancient Ayurvedic knowledge with modern AI to deliver remedies tailored to individual users.

### Key Features

- **Profile Management**: Captures detailed Ayurvedic constitution, including body type, skin and hair type, sleep patterns, digestive health, and more.
- **Remedy Consultation**: Provides personalized remedies based on symptoms, individual constitution, and references to classical Ayurvedic texts like Charaka Samhita, Sushruta Samhita, and Ashtanga Hridaya.
- **Symptom Tracking**: Monitor symptoms over time and track the effectiveness of remedies with visual charts and graphs.
- **Multilingual Support**: Access content in multiple languages, especially those spoken in regions where Ayurveda is popular.
- **AI-Powered Chatbot**: Get instant consultations and answers to health queries.

## Tech Stack

### Frontend
- **Framework**: Flutter
- **UI Design**: Material Design

### Backend
- **Backend as a Service**: Supabase
- **Database**: Supabase (PostgreSQL)
- **Authentication**: Supabase Auth

### AI/ML
- **Primary AI Model**: Gemini 1.5 Ultra
- **Alternative AI Model**: ChatGPT

### Hosting
- **Cloud Provider**: AWS
- **Services**:
  - AWS Amplify for hosting (if web support is added)
  - Amazon S3 for static assets
  - Amazon CloudFront for content delivery

### Analytics and Monitoring
- **Analytics**: Firebase Analytics
- **Error Monitoring**: Sentry

### Payment Integration
- **Payment Gateway**: Razorpay

### Push Notifications
- **Service**: Firebase Cloud Messaging (FCM)

## Getting Started

### Prerequisites
- Flutter SDK
- Supabase account
- Firebase project
- AWS account
- Razorpay merchant account

### Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/ayushya.git

# Navigate to the project directory
cd ayushya

# Install dependencies
flutter pub get

# Run the app
flutter run
```

## Project Structure
```
ayushya/
├── lib/
│   ├── components/
│   ├── models/
│   ├── screens/
│   ├── services/
│   ├── utils/
│   └── main.dart
├── assets/
├── android/
├── ios/
├── test/
└── pubspec.yaml
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For any inquiries, please reach out to [akash@webart4u.com](mailto:akash@webart4u.com). 