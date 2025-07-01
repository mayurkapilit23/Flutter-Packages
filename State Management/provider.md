#### provider :

In Flutter, **Provider** is a **state management package** that allows you to manage and share data across your app in an efficient and scalable way.

**Provider** helps you **store data in one place** and **access or update it from anywhere in the app** without passing it manually down the widget tree.

**Why Use Provider?**

- Avoids `setState()` everywhere
- Shares data across widgets efficiently
- Clean architecture and testable code
- Built on top of InheritedWidget (Flutter’s built-in way to share data)

```yaml
#add dependency to pubspec.yaml
dependencies:
  provider: 
```

```dart
//Create a model class with ChangeNotifier- The class holds your state and logic

import 'package:flutter/material.dart';

class CounterProvider with ChangeNotifier {
  int _count = 0;

  int get count => _count;

  void increment() {
    _count++;
    notifyListeners(); // Notifies listeners to rebuild
  }
}
```

```dart
//Wrap your app with ChangeNotifierProvider - Usually in main.dart

import 'package:flutter/material.dart';
import 'package:provider/provider.dart';
import 'counter_provider.dart'; // Your provider file
import 'my_app.dart'; // Your main widget

void main() {
  runApp(
    ChangeNotifierProvider(
      create: (context) => CounterProvider(),
      child: MyApp(),
    ),
  );
}
```

```dart
//User the provider in your widgets - use any one of the following 

//[1] Provider.of<YourProvider>(context)

final counter = Provider.of<CounterProvider>(context);
Text('Count: ${counter.count}')

//[2] Consumer<YourProvider>()
    
Consumer<CounterProvider>(
  builder: (context, counter, child) {
    return Text('Count: ${counter.count}');
  },
)
//[3] context.watch<T>() or context.read<T>()

// For UI updates
int count = context.watch<CounterProvider>().count;

// For calling functions only
context.read<CounterProvider>().increment(); 
```

