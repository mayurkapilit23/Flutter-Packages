#### go_router 

`go_router` is a Flutter package for **declarative navigation**. It simplifies navigation, deep linking, and route management using a clean, URL-based approach.

```yaml
#Add dependency in pubspec.yaml
depencdencies:
  go_router:
  
 //Then run
 flutter pub get
```

```dart
//Create your routes using GoRouter

final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      path: '/',
      builder: (context, state) => const HomePage(),
    ),
    GoRoute(
      path: '/about',
      builder: (context, state) => const AboutPage(),
    ),
  ],
);
```

```dart
//Wrap your app with MaterialApp.router

MaterialApp.router(
routerConfig: _router,
)
```

```dart
//Navigate using context.go() or context.push()

context.go('/about'); // Replace current page
context.push('/about'); // Stack new page
```

```dart
//Full Example : 

import 'package:flutter/material.dart';
import 'package:go_router/go_router.dart';

void main() {
  runApp(MyApp());
}

final GoRouter _router = GoRouter(
  routes: [
    GoRoute(
      path: '/',
      builder: (context, state) => const HomePage(),
    ),
    GoRoute(
      path: '/about',
      builder: (context, state) => const AboutPage(),
    ),
  ],
);

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp.router(
      routerConfig: _router,
    );
  }
}

//HomePage
class HomePage extends StatelessWidget {
  const HomePage({super.key});
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            context.go('/about'); // Navigate to /about
          },
          child: Text('Go to About'),
        ),
      ),
    );
  }
}

//AboutPage
class AboutPage extends StatelessWidget {
  const AboutPage({super.key});
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(child: Text('About Page')),
    );
  }
}
```

