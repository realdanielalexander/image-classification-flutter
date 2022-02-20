# Flutter Image Classification

This app classifies images based on any TFLite image classification model.
A sample model has been provided to classify cats vs. dogs.

![Alt text](sample.jpg?raw=true 'Sample')

## Instructions to use on your tflite model

1. Clone repository
2. Modify the model in assets/tflite/[name].tflite
3. Modify the class names in assets/tflite/[name].txt represent your classes (see example below).
4. Modify both [name].tflite and [name].txt to pubspec.yaml under assets (see example below).
5. Change the loadModel function in lib/main.dart to load your [name].tflite and [name].yaml (see example below).
6. Run Flutter app. The tflite package uses v1 embeddings so we need to pass in --ignore-deprecation

```
flutter run --ignore-deprecation
```

## cats_dogs.txt

```
Cat
Dog
```

## pubspec.yaml

```
assets {
    - assets/tflite/[name].tflite
    - assets/tflite/[name].txt
}
```

## lib/main.dart

```
String res = await Tflite.loadModel(
    model: "assets/tflite/[name].tflite",
    labels: "assets/tflite/[name].txt",
) ?? '';
```
