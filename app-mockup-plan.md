# Financial AI App Mockup Plan

## App Concept
An AI-powered financial assistant that monitors banking activity, tracks spending against goals, and sends humorous/roasting notifications to discourage unnecessary purchases.

## Core Features for Mockup
1. **Banking Integration UI** - Display connected accounts and balances
2. **Financial Goals Dashboard** - Show savings goals and progress
3. **Real-time Purchase Detection** - Mock transaction monitoring
4. **AI Roasting Notifications** - Push notifications with witty spending critiques
5. **SMS Integration** - Text message roasts for purchases

## Technical Implementation Plan

### 1. Technology Stack
- **Framework**: Expo with React Native
- **UI Library**: React Native Elements
- **Charts**: react-native-chart-kit or Victory Native
- **State Management**: Context API (simpler for mockup)
- **Animations**: Expo's Animated API
- **Mock Data**: Local state with hardcoded responses

### 2. MVP Mockup Focus (Chat & Graph Pages)
```
├── Main App (Tab Navigation)
│   ├── Graph Page (Financial Overview)
│   │   ├── Cash Flow Visualization
│   │   ├── Goal Lines (Car, Emergency Fund, etc.)
│   │   ├── Daily Savings Progress
│   │   └── Time-to-Goal Projections
│   └── Chat Page (AI Assistant)
│       ├── Message Thread with AI
│       ├── Roasting Responses
│       ├── Financial Advice (with attitude)
│       └── Quick Action Buttons
```

### 3. Detailed Page Specifications

#### Graph Page (Financial Overview)
**Main Chart Features:**
- Line graph showing account balance over time (30-day view)
- Horizontal goal lines with labels:
  - "Dream Car" line at $25,000
  - "Emergency Fund" line at $10,000
  - "Vacation Fund" line at $5,000
- Current balance highlighted with animated dot
- Daily savings goal indicator ($50/day)
- Projection lines showing when goals will be reached

**Visual Elements:**
- Gradient fill under the balance line
- Color-coded goal lines (green for achieved, yellow for close, red for far)
- Time-to-goal badges (e.g., "Car in 18 months at current rate")
- Pull-to-refresh animation
- Smooth transitions when switching time periods

#### Chat Page (AI Roast Assistant)
**Chat Interface:**
- WhatsApp-style message bubbles
- AI avatar with expressions (changes based on message tone)
- Typing indicator with sassy messages ("Calculating how broke you are...")
- Quick reply buttons for common questions

**Sample Conversation Flow:**
```
User: "Can I afford to buy a PS5?"
AI: "Can you afford it? Sure. Should you? That's 10% of your car fund, gaming addict. Your Honda Civic dreams are crying."

User: "I need it for stress relief"
AI: "You know what's stressful? Being 35 and still taking the bus. But hey, at least you'll have 4K graphics to watch your savings account stay at $0."

User: "Fine, what if I skip coffee for a month?"
AI: "NOW we're talking! Skip those overpriced lattes for 2 months and you can get your toy. I'm actually proud of you for once."
```

**Interactive Elements:**
- Shake phone to get a random roast
- Double-tap message for "savage mode" (extra harsh)
- Heart reaction for helpful advice (AI gets confused)

### 4. AI Roasting System (Mockup)
```
Purchase Categories:
- Coffee Shop → "Another $7 latte? Your retirement fund is crying."
- Fast Food → "McDonald's again? Your wallet AND your waistline hate you."
- Online Shopping → "Amazon doesn't need more money, but your savings account does."
- Entertainment → "Netflix AND HBO? Pick a lane, subscription addict."
```

### 5. Visual Design Direction
- **Color Scheme**: 
  - Primary: Deep blue (#1A237E) for trust
  - Accent: Bright red (#F44336) for alerts
  - Success: Green (#4CAF50) for goals
  - Background: Clean whites and light grays
- **Typography**: Modern, clean sans-serif (Inter or SF Pro)
- **Iconography**: Rounded, friendly icons with personality

### 6. Animation Ideas
- Money flying away when overspending
- Celebration confetti when hitting goals
- Shake animation for roasting notifications
- Progress bar fills with liquid animation

### 7. Demo Flow for Ad (Chat & Graph Focus)
1. **Opening Scene**: User on Graph page, sees they're far from car goal
2. **Chat Interaction**: 
   - User: "Why is saving so hard?"
   - AI: "Because you spent $847 on DoorDash last month. Your cooking skills are as empty as your savings account."
3. **Comedy Escalation**:
   - User argues with AI about needing takeout
   - AI responds with increasingly savage roasts
   - User tries to justify purchases
4. **Graph Animation**: Show projection changing as user commits to saving
5. **Resolution**: AI gives reluctant praise when user makes good choice
6. **Tagline**: "Finally, a financial advisor that tells it like it is"

### 8. Development Timeline (Mockup Only)
- **Week 1**: UI/UX wireframes and design system
- **Week 2**: Core screens implementation
- **Week 3**: Animations and transitions
- **Week 4**: Polish and demo recording

### 9. Mock Data Structure
```json
{
  "user": {
    "name": "Demo User",
    "monthlyIncome": 5000,
    "accounts": [
      {
        "type": "Checking",
        "balance": 2340.50,
        "bank": "Mock Bank"
      }
    ]
  },
  "goals": [
    {
      "name": "Emergency Fund",
      "target": 10000,
      "current": 3500,
      "deadline": "2024-12-31"
    }
  ],
  "transactions": [
    {
      "merchant": "Starbucks",
      "amount": 6.75,
      "category": "Coffee",
      "roastMessage": "That's 3 months of Netflix in lattes this week!"
    }
  ]
}
```

### 10. Tools Needed
- React Native development environment
- Figma/Sketch for design mockups
- After Effects for promotional animations
- Sample device frames for presentation

## Next Steps
1. Create detailed wireframes
2. Design high-fidelity mockups
3. Build interactive prototype
4. Record demo video for ad
5. Create marketing materials

## Development Setup for Testing on Physical Devices

### Prerequisites
1. **macOS** (required for iOS development)
2. **Node.js** (v16 or higher)
3. **React Native CLI**
4. **Xcode** (for iOS)
5. **Android Studio** (for Android)

### iOS Development Setup
1. **Install Xcode**
   - Download from Mac App Store
   - Install Xcode Command Line Tools: `xcode-select --install`

2. **Configure iPhone for Development**
   - Connect iPhone via USB
   - Trust computer on iPhone
   - Enable Developer Mode (iOS 16+): Settings → Privacy & Security → Developer Mode
   - Register device in Apple Developer account (free or paid)

3. **Running on iPhone**
   ```bash
   npx react-native run-ios --device
   # Or specify device name:
   npx react-native run-ios --device "John's iPhone"
   ```

### Android Development Setup
1. **Install Android Studio**
   - Download from developer.android.com
   - Install Android SDK (API 31+)
   - Configure ANDROID_HOME environment variable

2. **Enable Developer Mode on Android**
   - Go to Settings → About Phone
   - Tap "Build Number" 7 times
   - Enable USB Debugging in Developer Options

3. **Running on Android**
   ```bash
   # List connected devices
   adb devices
   
   # Run on connected Android device
   npx react-native run-android
   ```

## Expo Go Quick Start Guide

### 1. Project Setup
```bash
# Install Expo CLI globally
npm install -g expo-cli

# Create new Expo project
expo init FinancialRoastApp --template blank

# Navigate to project
cd FinancialRoastApp

# Install required dependencies
expo install react-native-svg
expo install react-native-chart-kit
expo install react-navigation react-native-screens react-native-safe-area-context
expo install @react-navigation/bottom-tabs
expo install react-native-gesture-handler
expo install react-native-reanimated
```

### 2. Download Expo Go App
- **iOS**: Search "Expo Go" in App Store
- **Android**: Search "Expo Go" in Google Play Store

### 3. Start Development
```bash
# Start Expo development server
expo start

# This opens a browser with QR code
# Scan with camera (iOS) or Expo Go app (Android)
```

### 4. File Structure for MVP
```
FinancialRoastApp/
├── App.js (Main navigation setup)
├── screens/
│   ├── GraphScreen.js (Financial overview with chart)
│   └── ChatScreen.js (AI roast conversation)
├── components/
│   ├── FinancialChart.js
│   ├── ChatBubble.js
│   └── GoalLine.js
├── data/
│   └── mockResponses.js (Hardcoded AI responses)
└── assets/
    └── ai-avatar.png
```

### 5. Mock Data Examples

#### Graph Page Data
```javascript
const accountData = {
  currentBalance: 3500,
  dailyData: [
    { day: '1', balance: 2800 },
    { day: '7', balance: 3200 },
    { day: '14', balance: 2900 },
    { day: '21', balance: 3350 },
    { day: '30', balance: 3500 }
  ],
  goals: [
    { name: 'Dream Car', amount: 25000, color: '#FF6B6B' },
    { name: 'Emergency Fund', amount: 10000, color: '#4ECDC4' },
    { name: 'Vacation', amount: 5000, color: '#45B7D1' }
  ],
  dailySavingsGoal: 50,
  projectedDays: {
    car: 430,
    emergency: 130,
    vacation: 30
  }
};
```

#### Chat Response Examples
```javascript
const roastResponses = {
  affordability: [
    "Can you afford it? Technically yes. Should you? That's like asking if you should eat ice cream for breakfast - possible but questionable.",
    "Your bank account says yes, but your future self is already filing a restraining order against current you.",
    "Sure, if you consider ramen a food group for the next 3 months."
  ],
  justification: [
    "Oh, you NEED it? Like you needed those 47 Amazon packages last month?",
    "Interesting definition of 'need'. I bet you also 'need' that gym membership you haven't used since January.",
    "Your needs and wants are more confused than your spending habits."
  ],
  praise: [
    "Wait... did you just make a smart financial decision? I need to sit down.",
    "I'm actually impressed. It's like watching a toddler tie their shoes for the first time.",
    "Look at you being responsible! Your mom would be so proud. Your bank account already is."
  ]
};
```

### Troubleshooting Tips
- **iOS**: If build fails, clean build folder in Xcode
- **Android**: Run `cd android && ./gradlew clean`
- **Both**: Clear Metro cache: `npx react-native start --reset-cache`
- **Network issues**: Ensure devices are on same WiFi network

### Hot Reload
- Shake device to open developer menu
- Enable "Fast Refresh" for instant updates
- No need to rebuild for JS changes

## Notes
- Focus on humor without being offensive
- Ensure notifications feel helpful, not nagging
- Make the roasts customizable in intensity
- Include positive reinforcement for good behavior