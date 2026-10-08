# TV Media Player – Android Smart TV

Player audio/video pentru Android TV cu:
- Adaugă / Selectează Video / Selectează Audio
- Play, Stop, Shuffle, Repeat
- Optimizat pentru telecomandă (D-pad + butoane media)

## Cum obții APK-ul

### Varianta 1: Android Studio (recomandat)
1. Deschide acest folder în Android Studio
2. Build → Build Bundle(s) / APK(s) → Build APK(s)
3. APK: `app/build/outputs/apk/debug/app-debug.apk`

### Varianta 2: GitHub Actions (cloud, gratuit)
1. Creează un repo pe GitHub
2. Upload întreg folderul proiectului
3. Mergi la tab **Actions** → rulează workflow-ul **Build APK**
4. Descarcă artifact-ul `TVMediaPlayer-debug`

### Varianta 3: Linie de comandă
```bash
# Necesită Android SDK + JDK 17
echo "sdk.dir=/path/to/Android/Sdk" > local.properties
gradle assembleDebug
# sau
./gradlew assembleDebug
```

## Instalare pe TV
```bash
adb connect <IP-ul-TV-ului>
adb install app-debug.apk
```

## Demo HTML
Vezi `TVMediaPlayer_Demo.html` din folderul artifacts pentru o previzualizare în browser.
