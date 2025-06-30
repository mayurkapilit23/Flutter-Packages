### shared_preferences 

This package lets you **store small key-value data locally** on the device, like user login state, settings, or theme mode. It's **persistent even after the app restarts**.

Best for saving simple data like tokens, flags, or preferences.

```dart
shared_preferences:
```

Writing (Saving) Data :

```dart
final prefs = await SharedPreferences.getInstance();

// Save a string
await prefs.setString('username', 'John');

// Save a boolean
await prefs.setBool('isLoggedIn', true);

// Save an int
await prefs.setInt('age', 25);

```

Reading (Getting) Data :

```dart
final prefs = await SharedPreferences.getInstance();

// Get a string
String? username = prefs.getString('username');

// Get a boolean
bool? isLoggedIn = prefs.getBool('isLoggedIn');

// Get an int
int? age = prefs.getInt('age');

```

Deleting Data :

```dart
await prefs.remove('username');
```

Usage :

User Login State - Save whether the user is logged in.

```dart
prefs.setBool('isLoggedIn', true);
```

Storing Tokens or User Info - Store auth tokens, usernames, or email.

```dart
prefs.setString('token', 'abc123');
```

Theme or Language Preference - Remember user's choice.

```dart
prefs.setBool('isDarkMode', true);
prefs.setString('language', 'en');
```

First-Time App Launch - Detect if user is opening app for the first time :

```dart
prefs.setBool('isFirstTime', false);
```

Saving Simple Settings - Toggle sound/music, app settings, etc..

```dart
prefs.setBool('soundOn', true);
```

