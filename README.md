<img src="https://i.postimg.cc/Qx2m8TkP/ezgif-com-optimize.gif" width="100%" title="Logo">

## Table of contents
- [🦥 Motivation](#motivation)
- [🏃‍♂️ Getting Started](#getting-started)
- [📖 What's inside](#whats-inside)
- [🧙‍♂️ Enhancements](#enhancements)
- [⚠️ Known issues (warnings)](#known-issues-warnings)
- [⭕️ Limitations](#limitations)

##  Motivation
1. I love [React Native](https://reactnative.dev/) 💚
2. I love [Expo](https://expo.io/) 💙
3. I love [React Native Navigation](https://wix.github.io/react-native-navigation) ❤️

So why not put them all together? 😏

Big love and gratitude to all people who are working on React Native, Expo and React Native Navigation!

## Getting Started

1. Clone the repo
```bash
git clone https://github.com/kanzitelli/expo-rnn-starter.git <new-app> && cd <new-app>
```

2. Remove `.git` file (if are not planning to contribute)
```bash
rm -rf .git
```

3. Install packages
```bash
yarn && yarn ios:pods
```

4. Run it!
```bash
yarn ios
yarn android
```

👁‍🗨 If you are planning to use Expo modules, such as preconfigured `expo-updates` and others, or add new ones, what I strongly recommend, then proceed to [Expo Configuration](/EXPO_CONFIGURATION.md) and follow the steps carefully.

🟢 If you would like to rename the app, you can use [react-native-rename-next](https://github.com/mayconmesquita/react-native-rename-next). Don't forget to run `yarn ios:pods` after the process is finished. Also keep in mind that bundle identifier must be valid for both platforms or change it manually.

## What's inside
- [Expo SDK](https://github.com/expo/expo) - universal set of amazing libraries (such as `expo-updates`) which are needed for building sustainable apps
- [React Native Navigation](https://github.com/wix/react-native-navigation) - truly native navigation experience for iOS and Android
- [Reanimated 2](https://github.com/software-mansion/react-native-reanimated) - React Native's Animated library reimplemented
- [MobX](https://github.com/mobxjs/mobx) - simple, scalable state management, with [mobx-persist](https://github.com/pinqy520/mobx-persist) for persisting your stores
### Extra helpful libraries
- [React Native Navigation Hooks](https://github.com/underscopeio/react-native-navigation-hooks) - a set of React hooks for React Native Navigation
- [React Native Vector Icons](https://github.com/oblador/react-native-vector-icons) - customizable icons for React Native. Even though Expo SDK includes `expo-icons` which you can still use, but the reason of adding `react-native-vector-icons` is to get icons as sources before launching tab based app
- [React Native Gesture Handler](https://github.com/kmagiera/react-native-gesture-handler) - native touches and gesture system for React Native
- [React Native Defice Info](https://github.com/react-native-community/react-native-device-info) - device information for React Native iOS and Android
- [Typescript](https://www.typescriptlang.org/) - strict syntactical superset of JavaScript
### Small useful libraries/hooks from me
- `useStyles()` - a hook that takes care of dark mode in your app. Supports toggling modes while you are in app. No dependencies (needs only `react-native`, so could be reusable). It is not a theme provider but could be used as one. It only has two themes light or dark

## Enhancements
There are still some things I would like to add to the starter:
- 🔳 Dark Mode support.
- ⬜️ Localization via [i18next](https://github.com/i18next/i18next/).
- ⬜️ Notifications (remote).

Feel free to open an issue for suggestions.

## Known issues (warnings)
- Expo splash screen. There is some weird behavior using `expo-splash-screen` with `react-native-navigation`. That is why this module has been excluded: [ios](https://github.com/kanzitelli/expo-rnn-starter/blob/master/ios/Podfile#L8) & [android](https://github.com/kanzitelli/expo-rnn-starter/blob/master/android/app/build.gradle#L196).
- Dark Mode in Android. React Native Navigation doesn't toggle navigation and tab bars' background color to dark when dark mode is toggled on. However it does so on iOS. As a workaround, we can subscribe to toggle events and then using `Navigation.mergeOptions` & `Navigation.setDefaultOptions` to change stylings for navigations and tab bars. Anyways, it needs some time to dive into it and come up with better solution.

Feel free to open an issue for any other warning or problems.

## Limitations
- Apps bootstrapped from this starter won't be able to be run on web as Expo apps do. Theoretically, it is possible to create some sort of an adapter between `react-navigation` and `react-native-navigation`. Maybe there will be other issues, but would be cool to have this feature.
- Apps bootstrapped from this starter won't be available through Expo app for iOS and Android as of differences in navigation approach. Theoretically, it is possible to create an app like Expo that will include `react-native-navigation` and somehow download needed bundles. Needs more research.

## License

This project is [MIT licensed](/LICENSE.md)
