# خطوات بناء ملف APK لتطبيق كاشير-V1

## الطريقة الأولى: عبر Android Studio (الأكثر استقراراً وتحكماً)
1. فك الضغط عن مجلد المشروع `cashier-apk-project`.
2. افتح المجلد في **Android Studio** وانتظر اكتمال مزامنة Gradle.
3. من القائمة العلوية اختر:
   `Build` -> `Build Bundle(s) / APK(s)` -> `Build APK(s)`.
4. بعد انتهاء البناء ستجد ملف `app-debug.apk` داخل:
   `app/build/outputs/apk/debug/app-debug.apk`.

## الطريقة الثانية: عبر Capacitor CLI (إذا كنت تفضل بيئة Node.js)
1. داخل مجلد `www` يوجد ملف `index.html` الخاص بالتطبيق.
2. ثبّت Capacitor وشغّل:
   ```bash
   npm init -y
   npm install @capacitor/core @capacitor/cli @capacitor/android
   npx cap add android
   npx cap sync android
   cd android && ./gradlew assembleDebug
   ```
