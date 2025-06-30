### cached_network_image :

This Flutter package is used to **load images from the internet and cache them locally**, so they load faster the next time.

Perfect for profile pictures, galleries, or any remote image.

**Features :**

- Automatic image caching
- Placeholder and error widget support

```yaml
cached_network_image :
```

```dart
CachedNetworkImage(
  imageUrl: 'https://example.com/image.jpg',
  placeholder: (context, url) => CircularProgressIndicator(),
  errorWidget: (context, url, error) => Icon(Icons.error),
)
```

