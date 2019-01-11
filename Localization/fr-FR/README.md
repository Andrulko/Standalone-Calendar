# Abc

Def. Translation.

### Readme

Einige Menschen haben nicht die open-source-Kalender von AOSP und sind gezwungen, verwenden Sie entweder die proprietären Google-Kalender aus Google Play oder versendet verkrüppelt Kalender von z.B. Samsung.

Ich machte ein repository zu bauen, der AOSP-Kalender ohne die Notwendigkeit für die Errichtung der gesamten Android-OS. Es hat eine andere Paket-name um zu verhindern, dass Konflikte mit “com.android.Kalender".

### Build instructions

    git submodule init
    git submodule update
    
    gradle build
    

### Wie das geschah

- see `build.gradle` and the modifications to `AndroidManifest.xml`
- `fix_strings_and_import.py` was created to fix a build problem and rename imports of R.java
- get time zone data from http://www.iana.org/time-zones write `backward` and `zone.tab` to assets and to assets of https://github.com/dschuermann/standalone-calendar-timezonepicker
- comment out code in https://github.com/dschuermann/standalone-calendar-frameworks-ex