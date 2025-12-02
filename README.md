[README.md](https://github.com/user-attachments/files/23871584/README.md)# bemindwell
BeMindWell - A comprehensive mental health and wellness app for iOS, Android, and Web
[Uploading README.m# BeMindWell - Mental Health & Wellness App

<p align="center">
  <img src="https://d64gsuwffb70l.cloudfront.net/6896d60c4a42e05f0c804a92_1758808797233_e01de7bf.webp" alt="BeMindWell Logo" width="200"/>
</p>

<p align="center">
  <strong>Your Comprehensive Mental Health Companion</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#quick-start">Quick Start</a> •
  <a href="#github-repository">GitHub</a> •
  <a href="#launch-instructions">Launch</a> •
  <a href="#documentation">Documentation</a>
</p>

> **🚀 READY TO LAUNCH?** See [QUICK-LAUNCH-SUMMARY.md](QUICK-LAUNCH-SUMMARY.md) for a fast-track guide!


## 🌟 Overview

BeMindWell is a comprehensive mental health and wellness application designed to support individuals on their journey to better mental health. Built with React Native and Expo, it offers a wide range of features including mood tracking, meditation exercises, medication reminders, therapist finder, and more.

## ✨ Features

### Free Features (Offline Access)
- 📊 **Mood Tracking** - Track your emotional state offline
- 🧘 **Meditation Exercises** - Guided meditation available offline
- 🆘 **Crisis Resources** - Emergency contacts and resources
- 📱 **Emergency Contacts** - Quick access to help

### Premium Features ($9.99/month or $99.99/year)
- 💊 **Medication Tracker** - Never miss a dose with smart reminders
- 🏥 **Find Facilities** - Search Sydney mental health facilities (Brisbane Waters #1 rated)
- 📈 **SUDs Tracker** - Subjective Units of Distress Scale monitoring
- 🌸 **Daily Affirmations** - Positive mindset building
- 🌬️ **Breathing Exercises** - Stress relief techniques
- 👥 **Group Sync** - Connect with support groups
- 📋 **Wellness Plans** - Personalized mental health action plans
- 📊 **Health Tracking** - Monitor sleep and wellness metrics
- 👤 **User Profile** - Personalized settings and progress
- 🎯 **Daily Activities** - Structured wellness routines

### Technical Features
- 🔐 **Secure Authentication** - Multi-tenant secure login with Supabase
- 🔒 **Row Level Security** - Complete data isolation with tenant-based RLS
- 💾 **Offline Storage** - Local data persistence for critical features
- 📱 **Cross-Platform** - iOS, Android, and Web support
- 🎨 **Modern UI/UX** - Beautiful, intuitive interface
- ♿ **Accessibility** - WCAG compliant design
- 💳 **PayPal Integration** - Secure subscription payments

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn
- Expo CLI
- Supabase account
- PayPal Business account (for payments)

### Installation

```bash
# Clone the repository from GitHub
git clone https://github.com/YOUR_USERNAME/bemindwell.git
cd bemindwell

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your Supabase credentials

# Start the development server
npm start
```

### Running on Different Platforms

```bash
# iOS Simulator
npm run ios

# Android Emulator
npm run android

# Web Browser
npm run web
```

## 🌐 GitHub Repository

**Repository URL**: `https://github.com/YOUR_USERNAME/bemindwell`

For detailed GitHub setup instructions, see [GITHUB-SETUP-GUIDE.md](GITHUB-SETUP-GUIDE.md)

## 🚀 Launch Instructions

For complete step-by-step launch instructions for all platforms, see [LAUNCH-GUIDE.md](LAUNCH-GUIDE.md)

### Quick Launch Overview:
- **Website**: Deploy to Vercel/Netlify (15 minutes)
- **iOS App Store**: Submit via EAS (24-48 hour review)
- **Google Play Store**: Submit via EAS (3-7 day review)


## 📋 Pre-Publishing Checklist


**IMPORTANT**: Before publishing, complete ALL items in [PRE-PUBLISH-CHECKLIST.md](PRE-PUBLISH-CHECKLIST.md)

Key items:
- ✅ Environment variables configured
- ✅ Supabase database setup complete
- ✅ App assets created (icon, splash screen, etc.)
- ✅ Legal documents reviewed and customized
- ✅ Payment integration tested
- ✅ App store accounts created
- ✅ Build configuration verified

## 📱 Building for Production

### Build for App Stores

```bash
# Install EAS CLI
npm install -g eas-cli

# Login to Expo
eas login

# Configure EAS
eas build:configure

# Build for iOS
eas build --platform ios --profile production

# Build for Android
eas build --platform android --profile production

# Submit to stores
eas submit --platform ios
eas submit --platform android
```

For detailed build instructions, see [BUILD-AND-DEPLOY-GUIDE.md](BUILD-AND-DEPLOY-GUIDE.md)

## 🗄️ Database Setup

BeMindWell uses Supabase with Row Level Security for data protection:

1. Create a Supabase project at https://supabase.com
2. Run `supabase-setup.sql` in SQL editor
3. Run `supabase-settings-setup.sql` for settings
4. Run `subscription-changes-rls-policies.sql` for security
5. Run `database-security-functions.sql` for admin functions
6. Enable Row Level Security on all tables
7. Configure authentication providers

See [supabase-project-setup.md](supabase-project-setup.md) for detailed instructions.

## 🔐 Security Features

- **Multi-tenant Architecture** - Complete data isolation between organizations
- **Row Level Security** - Database-level access control
- **Encrypted Storage** - Sensitive data encryption at rest
- **Secure Authentication** - JWT-based auth with Supabase
- **HIPAA Considerations** - Built with healthcare compliance in mind
- **Premium Feature Gating** - Secure subscription verification

## 💳 Subscription Model

- **Free Tier**: Offline features (mood tracking, meditation, crisis resources)
- **Premium Monthly**: $9.99/month - All features unlocked
- **Premium Yearly**: $99.99/year - Best value (2 months free)

Payment processing via PayPal with secure webhook integration.

## 🏥 Sydney Mental Health Facilities

BeMindWell includes comprehensive listings of Sydney mental health facilities:
- **Brisbane Waters Private Hospital** - #1 Rated (5.0 stars)
- Nepean Mental Health Centre
- Cumberland Hospital
- Safe Haven Campbelltown
- South Western Sydney Primary Health Network
- Penrith Medicare Mental Health Centre

Premium users can search and filter facilities by name, location, and type.

## 📦 Project Structure

```
bemindwell/
├── app/                    # Main application screens
│   ├── index.tsx          # Entry point with feature gating
│   ├── _layout.tsx        # Layout configuration
│   └── lib/               # Libraries and utilities
├── components/            # Reusable React components
│   ├── AuthScreen.tsx    # Authentication
│   ├── Dashboard.tsx     # Main dashboard
│   ├── PremiumFeaturesTab.tsx  # Subscription management
│   └── ...               # All other components
├── assets/               # Images and static assets
├── data/                 # Static data files
├── .env                  # Environment variables (create from .env.example)
├── app.config.js         # Expo configuration
├── eas.json             # EAS build configuration
├── package.json          # Dependencies and scripts
├── PRE-PUBLISH-CHECKLIST.md  # Publishing checklist
└── BUILD-AND-DEPLOY-GUIDE.md  # Deployment instructions
```

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🆘 Support

- Pre-Publish Checklist: [PRE-PUBLISH-CHECKLIST.md](PRE-PUBLISH-CHECKLIST.md)
- Build Guide: [BUILD-AND-DEPLOY-GUIDE.md](BUILD-AND-DEPLOY-GUIDE.md)
- Database Setup: [supabase-project-setup.md](supabase-project-setup.md)
- Issues: GitHub Issues
- Email: support@bemindwell.com

## 📚 Additional Documentation

- [Privacy Policy](PRIVACY-POLICY.md)
- [Terms of Service](TERMS-OF-SERVICE.md)
- [User Agreement](USER-AGREEMENT.md)
- [App Store Descriptions](APP-STORE-DESCRIPTIONS.md)
- [Marketing Guide](MARKETING-IMPLEMENTATION-GUIDE.md)
- [SEO Optimization](SEO-OPTIMIZATION.md)

## 🙏 Acknowledgments

- Built with [React Native](https://reactnative.dev/) and [Expo](https://expo.dev/)
- Database powered by [Supabase](https://supabase.com/)
- Icons from [@expo/vector-icons](https://icons.expo.fyi/)
- Payments via [PayPal](https://www.paypal.com/)

## 📊 Status

- ✅ Core Features Complete
- ✅ Database Security Implemented
- ✅ Multi-tenant Support
- ✅ Offline Mode
- ✅ Premium Subscription System
- ✅ PayPal Integration
- ✅ Feature Gating Implemented
- ✅ Sydney Facilities Database
- ✅ Production Ready

## 🚀 Ready to Publish?

1. Complete [PRE-PUBLISH-CHECKLIST.md](PRE-PUBLISH-CHECKLIST.md)
2. Test thoroughly on iOS and Android
3. Review all legal documents
4. Set up payment processing
5. Create app store assets
6. Build with EAS
7. Submit to App Store and Google Play

---

<p align="center">
  Made with care for mental health awareness
</p>
d…]()
