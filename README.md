# Flutter Material Color Picker

Material Color picker is a Flutter widget, that can be customizable.

By default, it's Material Colors, but you can define your own colors.

You can also use CircleColor widget to display color in your app.
Example, you can set the color picker in a dialog and display the selected color in a ListTile, for settings.

## How to use it

These examples use a static color for 'selectedColor', but you can use a variable (state)

### Add to your Flutter project

You just need to add `introduction_screen` as a [dependency in your pubspec.yaml file](https://flutter.io/using-packages/).

```yaml
flutter_material_color_picker: ^0.0.3+1
```

### Import

```dart
import 'package:flutter_material_color_picker/flutter_material_color_picker.dart';
```

### Basic

```dart
MaterialColorPicker(
    onColorChange: (Color color) {
        // Handle color changes
    },
    selectedColor: Colors.red
)
```

### Listen main color changes

```dart
MaterialColorPicker(
    onColorChange: (Color color) {
        // Handle color changes
    },
    onMainColorChange: (ColorSwatch color) {
        // Handle main color changes
    },
    selectedColor: Colors.red
)
```

### Custom colors

In this example, custom colors are a list of Material Colors (class who extend of ColorSwatch).
But you can create your own list of ColorSwatch.

```dart
MaterialColorPicker(
    onColorChange: (Color color) {
        // Handle color changes
    },
    selectedColor: Colors.red,
    colors: [
        Colors.red,
        Colors.deepOrange,
        Colors.yellow,
        Colors.lightGreen
    ]
)
```

## Screenshot

### Color selection

There is two step, first choose the main color, and when you press it, you have to choose a shade of the main color.
By default it's all **Material Colors**, but you can define custom colors, a **list of ColorSwatch**.

![Main color selection](https://github.com/Pyozer/color_picker/blob/master/demo/main_color.png?raw=true)

![Shade color selection](https://github.com/Pyozer/color_picker/blob/master/demo/shade_color.png?raw=true)

### Example of usages

You can insert the color picker into a **Dialog**

![Example main color in a dialog](https://github.com/Pyozer/color_picker/blob/master/demo/main_color_dialog.png?raw=true)

![Example shade color in a dialog](https://github.com/Pyozer/color_picker/blob/master/demo/shade_color_dialog.png?raw=true)

### Display color

You can use CircleColor widget, to display the selected color into your settings for example.

![Example of circlecolor widget in ListTile](https://github.com/Pyozer/color_picker/blob/master/demo/example_circle_color.png?raw=true)
