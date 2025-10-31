# Mobile App Setup with Expo Router

## Project Information
- **Repository**: prodev-mobile-setup
- **Directory**: prodev-mobile-app-0x00
- **Author**: Njiru-ux
- **Date**: October 30, 2025

## Objective
Set up a mobile application using the Expo Router template, document the scaffolding process, and understand the file structure of a React Native application using Expo.

## Steps Followed for Scaffolding

### 1. Project Initialization
Navigated to the project directory and initialized a new Expo project using the latest Expo Router template:

```bash
cd prodev-mobile-setup/prodev-mobile-app-0x00
npx create-expo-app@latest .
```

This command created a new Expo project with the following structure:
- `/app` - Main application directory with routing
- `/components` - Reusable React components
- `/constants` - Application constants (colors, themes, etc.)
- `/hooks` - Custom React hooks
- `/assets` - Images and other static assets
- `/scripts` - Build and utility scripts

### 2. Home Screen Modification
Modified the home screen to display custom text:

**File**: `app/(tabs)/index.tsx`
**Line 21**: Changed from `Welcome!` to `First App Created`

```typescript
<ThemedText type="title">First App Created</ThemedText>
```

### 3. Running the Application
Started the Expo development server:

```bash
npx expo start
```

This command:
- Generates a QR code for testing on physical devices
- Starts the Metro bundler
- Enables hot reloading for development
- Provides options for iOS, Android, and web testing

**Testing Methods**:
- **iOS**: Scan QR code with Camera app
- **Android**: Scan QR code with Expo Go app
- **Web**: Press 'w' in terminal

## Reset Project Observations

### Command Executed
```bash
npm run reset-project
```

### What Happened
The reset command performed the following actions:

1. **Moved existing files to `/app-example` directory**:
   - `/components` → `/app-example/components`
   - `/hooks` → `/app-example/hooks`
   - `/constants` → `/app-example/constants`
   - `/scripts` → `/app-example/scripts`
   - `/app` → `/app-example/app` (including our "First App Created" modification)

2. **Created a fresh minimal `/app` directory** with:
   - `app/index.tsx` - New minimal home screen
   - `app/_layout.tsx` - Basic layout configuration

3. **Purpose of Reset**:
   - Preserves the original template and modifications in `/app-example`
   - Provides a clean slate in `/app` for starting fresh
   - Allows developers to reference the original template while building custom features
   - Useful for learning by comparing the full template vs. minimal setup

### File Structure After Reset

```
prodev-mobile-app-0x00/
├── app/                          # Fresh minimal app directory
│   ├── index.tsx                 # New home screen
│   └── _layout.tsx               # Basic layout
├── app-example/                  # Original template (preserved)
│   ├── app/
│   │   └── (tabs)/
│   │       └── index.tsx         # Contains "First App Created"
│   ├── components/
│   ├── constants/
│   │   └── Colors.tsx
│   ├── hooks/
│   └── scripts/
├── assets/
├── node_modules/
├── package.json
├── tsconfig.json
└── README.md                     # This file
```

## Key Learnings

1. **Expo Router Template**: Provides a full-featured starting point with navigation, theming, and best practices
2. **File-based Routing**: The `/app` directory structure automatically creates routes
3. **Reset Command**: Useful for getting a minimal setup while preserving the original template
4. **Development Workflow**: Hot reloading and cross-platform testing make development efficient
5. **TypeScript Integration**: The template includes TypeScript configuration for type safety

## Next Steps
1. Continue development in the fresh `/app` directory
2. Reference `/app-example` for component examples and patterns
3. Delete `/app-example` when no longer needed for reference
4. Build custom features using the minimal setup

## Resources
- [Expo Documentation](https://docs.expo.dev/)
- [Expo Router Documentation](https://docs.expo.dev/router/introduction/)
- [React Native Documentation](https://reactnative.dev/)