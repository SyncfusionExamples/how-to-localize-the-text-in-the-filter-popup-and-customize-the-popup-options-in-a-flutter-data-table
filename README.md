# How to localize the Text in the filter popup menu and customize the popup menu options in a Flutter DataTable (SfDataGrid)?

In this article, we will guide you through the process of localizing the text in the filter popup menu of a [Flutter DataGrid](https://www.syncfusion.com/flutter-widgets/flutter-datagrid) and customizing the available options.

## STEP 1:
You need to add the following package in the dependencies of pubspec.yaml.

```dart
syncfusion_localizations: ^21.2.5
flutter_localizations:
    sdk: flutter

```

## STEP 2:
Import the following library into the flutter application:

```dart
import 'package:flutter_localizations/flutter_localizations.dart';
import 'package:syncfusion_localizations/syncfusion_localizations.dart';
 
```

## STEP 3:
Ensure that the [localizationsDelegates](https://api.flutter.dev/flutter/material/MaterialApp/localizationsDelegates.html) property in the [MaterialApp](https://api.flutter.dev/flutter/material/MaterialApp-class.html) widget contains the required localizations. Declare the supported locales in the [supportedLocales](https://api.flutter.dev/flutter/material/MaterialApp/supportedLocales.html) property and assign the desired locale to the [locale](https://api.flutter.dev/flutter/dart-ui/Locale-class.html) property.

 ```dart
class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      localizationsDelegates: const [
        GlobalMaterialLocalizations.delegate,
        GlobalWidgetsLocalizations.delegate,
        SfGlobalLocalizations.delegate
      ],
      supportedLocales: const [
        Locale('zh'),
        Locale('ar'),
        Locale('ja'),
      ],
      locale: const Locale('ar'),
      title: 'Syncfusion DataGrid Demo',
      theme: ThemeData(primarySwatch: Colors.blue),
      home: MyHomePage(),
    );
  }
}

 ```