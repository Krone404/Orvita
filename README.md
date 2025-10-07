# Orvita
Orvita is the ultimate alarm app that syncs with your calendar groups, making waking up easier than ever. Say hello to hassle-free mornings and never miss an important event again with Orvita's seamless integration. Simplify your life and stay organized with Orvita.

┌───────────────────────────────────────────────────────────┐
│                      User Interface                       │
│     React Native (TypeScript + React Components)           │
│   ──────────────────────────────────────────────────────   │
│   • Home / Alarm / Settings Screens                        │
│   • Navigation (React Navigation)                          │
│   • Calendar View (e.g. react-native-calendars)            │
│   • Theming & Animations (Reanimated, Lottie, etc.)        │
└───────────────────────────────────────────────────────────┘
                     │
                     │  (JS–Native Bridge)
                     ▼
┌───────────────────────────────────────────────────────────┐
│                   Shared Logic Layer                      │
│   • Alarm Manager (JS logic to add/edit/remove alarms)     │
│   • State Management (Redux / Zustand / Context API)       │
│   • Local Storage (AsyncStorage / MMKV / SQLite)           │
│   • API Requests (e.g. to Google Calendar or backend)      │
└───────────────────────────────────────────────────────────┘
                     │
                     │  Calls Native APIs via NativeModules
                     ▼
┌───────────────────────────────────────────────────────────┐
│                Native Bridge & Modules                    │
│   (Written in Kotlin for Android, Swift for iOS)           │
│   • AlarmModule → schedules alarms                         │
│   • BackgroundModule → runs code while app closed          │
│   • CalendarModule → integrates with OS calendar            │
│   • NotificationModule → shows notifications                │
└───────────────────────────────────────────────────────────┘
                     │
        ┌────────────┴─────────────────────┐
        ▼                                  ▼
┌────────────────────────┐     ┌────────────────────────┐
│   Android Native Side   │     │     iOS Native Side     │
│  (Java/Kotlin + Gradle) │     │  (Swift/Obj-C + Xcode) │
│ ─────────────────────── │     │ ─────────────────────── │
│ • AlarmManager / WorkMgr│     │ • UNUserNotificationCtr │
│ • Foreground Services   │     │ • BGTaskScheduler       │
│ • Power Optimization    │     │ • Background Fetch API  │
│ • Firebase Integration  │     │ • iCloud / Apple APIs   │
└────────────────────────┘     └────────────────────────┘
                     │
                     ▼
┌───────────────────────────────────────────────────────────┐
│                  OS & Hardware Layer                      │
│   • Android / iOS System APIs                             │
│   • Alarm Scheduling, Notifications, Calendar Access      │
│   • Battery & Permissions Management                      │
└───────────────────────────────────────────────────────────┘
