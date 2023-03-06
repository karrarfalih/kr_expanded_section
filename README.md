# Kr Expanded Section
The kr_expanded_section package provides a widget that can be used to show or hide a child widget with an expanding or collapsing animation. The KrExpandedSection widget takes a child widget and a boolean value to determine whether the child widget should be expanded or collapsed. The widget can be used to create expandable sections in a user interface, such as for displaying additional details or options. The animation duration can also be customized.
## Get Started

To use this package, add `kr_future_builder` as a [dependency in your pubspec.yaml file](https://flutter.dev/docs/development/packages-and-plugins/using-packages).

```yaml
dependencies:
  kr_expanded_section: ^1.0.0
```
Then, import the package:

```dart
import 'package:kr_expanded_section/kr_expanded_section.dart';
```
Or You can install packages from the command line:

```
flutter pub add kr_expanded_section
```

## Usage
Import the package:
```dart
import 'package:kr_expanded_section/kr_expanded_section.dart';
```
Wrap your widget with `KrExpandedSection` and pass the child you want to expand:
```dart
KrExpandedSection(
  expand: true,
  child: Container(
    height: 200,
    width: 200,
    color: Colors.blue,
  ),
)
```

By default, the section is not expanded. To `expand` the section, set `expand` to `true`.

You can also set a function to be called when the section finishes expanding or collapsing by passing it to the `onFinish` parameter:```

```dart
KrExpandedSection(
  expand: true,
  child: Container(
    height: 200,
    width: 200,
    color: Colors.blue,
  ),
  onFinish: () {
    print('Finished expanding/collapsing section!');
  },
)
```
## Example
```dart
import 'package:flutter/material.dart';
import 'package:kr_expanded_section/kr_expanded_section.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Kr Expanded Section Demo',
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Kr Expanded Section Demo'),
        ),
        body: Center(
          child: KrExpandedSection(
            expand: true,
            child: Container(
              height: 200,
              width: 200,
              color: Colors.blue,
            ),
            onFinish: () {
              print('Finished expanding/collapsing section!');
            },
          ),
        ),
      ),
    );
  }
}
```
## License
This package is licensed under the BSD 3-Clause License.