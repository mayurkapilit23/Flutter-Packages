#### animations :

Package Link : https://pub.dev/packages/animations

The `animations` package in Flutter provides **pre-built, beautiful animations** that follow **Material Design** transitions. It simplifies implementing common animation patterns like **fade, shared axis, and container transforms** — without needing to write complex `AnimationController` logic.

## Common Animations Provided

| Animation Type            | Description                                                  |
| ------------------------- | ------------------------------------------------------------ |
| **FadeThroughTransition** | Fade between UI elements (e.g., list to detail view).        |
| **SharedAxisTransition**  | Transition where elements move together along a shared axis (X, Y, or Z). |
| **ContainerTransform**    | Smoothly animates between two UI elements (like cards expanding to detail). |

```yaml
#add dependency to pubspec.yaml
dependencies:
  animations: ^2.0.11 
```

## Use Cases

- Navigation transitions between pages
- Card to detail page animations
- Tab switching with smooth fade or shared axis
- Mimicking Material motion design easily



## Available Widgets

- `OpenContainer`
- `PageTransitionSwitcher`
- `FadeThroughTransition`
- `SharedAxisTransition`
- `FadeScaleTransition`



##  Pro Tips

- Works well with `PageTransitionsTheme` for global routing animations.
- Combine with `Hero` widget for advanced shared animations.
- Ideal for building polished apps without reinventing animation logic.