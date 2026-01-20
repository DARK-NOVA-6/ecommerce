# ShopHub - E-Commerce Flutter App

A beautiful, modern e-commerce Flutter application built using the FakeStore API. This app showcases advanced UI/UX design, smooth animations, and clean architecture principles.

![Flutter](https://img.shields.io/badge/Flutter-3.10.7-02569B?logo=flutter)
![Provider](https://img.shields.io/badge/State%20Management-Provider-blue)
![Material Design 3](https://img.shields.io/badge/UI-Material%20Design%203-purple)

## 📥 Download & Demo

### 📦 APK File
The ready-to-install APK is included in the repository:
- **Location**: `app-release.apk` (in root directory)
- **Size**: ~20-25 MB (optimized)
- **Ready to install** on any Android device

### 🎥 Video Demo
A complete walkthrough video of the app is included:
- **Location**: `screen_record.webm` (in root directory)
- **Format**: WebM video
- Shows all features in action
- Demonstrates:
  - Product browsing (grid & list view)
  - Search and category filtering
  - Dark mode toggle
  - Smooth animations
  - Add to cart functionality
  - Cart management (quantity changes, swipe to delete)
  - Complete user flow

## 📱 Features

### Core Features
- ✅ **Product Listing Screen**
  - Hero banners with smooth page indicators
  - Categories section with animated chips
  - Grid/List view toggle
  - Real-time search functionality
  - Pull-to-refresh support
  - Shimmer loading effects

- ✅ **Product Details Screen**
  - Hero animation from listing to details
  - Smooth fade and slide animations
  - Category badges
  - Star ratings with reviews count
  - Detailed product description
  - Add to cart functionality

- ✅ **Shopping Cart Screen**
  - Add/remove items with smooth animations
  - Quantity management (increase/decrease)
  - Swipe-to-delete functionality
  - Real-time total calculation
  - Free shipping indicator
  - Empty cart state with call-to-action

### Bonus Features Implemented 🌟
- ✨ **Dark Mode** - Complete dark theme with persistent preference
- ✨ **Smooth Animations** - Hero animations, fade transitions, slide effects
- ✨ **Custom Widgets** - Reusable components for cards, chips, banners
- ✨ **Shimmer Loaders** - Beautiful skeleton loading states
- ✨ **Pixel-Perfect Design** - Modern UI with gradient effects
- ✨ **Badge Indicators** - Cart badge showing item count
- ✨ **Responsive Layouts** - Works on all screen sizes
- ✨ **Cached Images** - Fast image loading with caching

## 🏗️ Architecture

### Project Structure
```
lib/
├── main.dart                 # App entry point with providers
├── models/
│   ├── product.dart         # Product model with JSON serialization
│   └── cart_item.dart       # Cart item model
├── providers/
│   ├── products_provider.dart  # Product state management
│   ├── cart_provider.dart      # Cart state management
│   └── theme_provider.dart     # Theme state management
├── services/
│   └── api_service.dart     # FakeStore API integration
├── screens/
│   ├── home_screen.dart     # Product listing screen
│   ├── product_details_screen.dart  # Product details
│   └── cart_screen.dart     # Shopping cart
├── widgets/
│   ├── hero_banner.dart     # Hero banner carousel
│   ├── product_card.dart    # Product card widget
│   ├── category_chip.dart   # Category filter chip
│   └── shimmer_loading.dart # Loading skeleton
└── theme/
    └── app_theme.dart       # Light & dark theme definitions
```

### State Management
**Provider Pattern** was chosen for its:
- Simplicity and ease of use
- Excellent performance
- Native Flutter integration
- Perfect for this app's complexity level

### Design Patterns Used
1. **Repository Pattern** - API service acts as data layer
2. **MVVM** - Separation of UI and business logic
3. **Singleton** - Single instances of providers
4. **Factory Constructor** - JSON serialization

## 🎨 Design Choices

### Color Scheme
- **Primary**: Indigo (`#6366F1`) 
- **Secondary**: Purple (`#8B5CF6`) 
- **Tertiary**: Pink (`#EC4899`) 

### Animations
1. **Hero Animations** - Product image transitions
2. **Fade Transitions** - Smooth content appearance
3. **Slide Animations** - Card entry effects
4. **Scale Animations** - Badge pulses
5. **Dismissible** - Swipe-to-delete gestures

### UI/UX Highlights
- **Empty States** - Helpful messages with CTAs
- **Error Handling** - Graceful error displays with retry options
- **Loading States** - Shimmer effects instead of spinners
- **Feedback** - Snackbars for user actions
- **Visual Hierarchy** - Clear content organization
- **Touch Targets** - Properly sized interactive elements

## 📦 Dependencies

```yaml
dependencies:
  provider: ^6.1.1              # State management
  http: ^1.2.0                  # API calls
  shimmer: ^3.0.0               # Loading effects
  cached_network_image: ^3.3.1 # Image caching
  smooth_page_indicator: ^1.1.0 # Banner indicators
  shared_preferences: ^2.2.2    # Local storage
  badges: ^3.1.2                # Cart badge
```

## 🚀 Getting Started

### Quick Start (For Testing)

**Just want to try the app?**
1. Download `app-release.apk` from the repository
2. Transfer to your Android device
3. Enable "Install from Unknown Sources" in settings
4. Install and enjoy! 📱

### For Developers

#### Prerequisites
- Flutter SDK 3.10.7 or higher
- Dart SDK
- Android Studio / VS Code
- Android device or emulator

#### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd ecommerce
```

2. **Install dependencies**
```bash
flutter pub get
```

3. **Run the app**
```bash
flutter run
```

4. **Build APK**
```bash
flutter build apk --release
```

The APK will be located at: `build/app/outputs/flutter-apk/app-release.apk`

## 🧪 Testing

### API Endpoints Used
- `GET /products` - Fetch all products
- `GET /products/categories` - Fetch categories
- `GET /products/category/{category}` - Filter by category
- `GET /products/{id}` - Fetch single product

### Features Tested
- ✅ API integration and error handling
- ✅ Cart operations (add, remove, update quantity)
- ✅ Category filtering
- ✅ Search functionality
- ✅ Theme switching
- ✅ State persistence

## 🎯 Technical Highlights

### Performance Optimizations
1. **Cached Network Images** - Reduces data usage and loading times
2. **Lazy Loading** - Efficient list rendering with builders
3. **Selective Rebuilds** - Consumer widgets for targeted updates
