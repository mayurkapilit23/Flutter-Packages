**Dotted Border**

**dotted_border** lets you draw **dashed or dotted borders** around any widget in Flutter. Useful for highlighting cards, inputs, or sections visually.


```yaml
#add dependency to pubspec.yaml
dependencies:
  dotted_border: 

#package url: https://pub.dev/packages/dotted_border
```

```dart
//implementation
DottedBorder(
        color: Colors.blue,
        strokeWidth: 2,
        dashPattern: [6, 3],
        borderType: BorderType.RRect,
        radius: Radius.circular(12),
        child: Padding(
          padding: EdgeInsets.all(16.0),
          child: Text('Dotted Border Box'),
        ),
      )
```