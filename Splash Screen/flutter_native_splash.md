#### flutter_native_splash 

`flutter_native_splash` is a package that **automatically generates native splash screens** for Android, iOS, and web using a single config file.

```yaml
#Add dependency to pubspec.yaml

dev_dependencies:
  flutter_native_splash: 
  
#Then run
flutter pub get
```

```yaml
#Add Configuration in pubspec.yaml

flutter_native_splash:
  color: "#ffffff"  # background color
  image: assets/splash.png  # your splash image
  android: true
  ios: true
```

```cmd
//Run the command in terminal

flutter pub run flutter_native_splash:create
```

