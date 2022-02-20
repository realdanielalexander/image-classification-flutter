# Flutter Image Classification

This app classifies images based on any TFLite image classification model.
A sample model has been provided to classify cats vs. dogs.

## Instructions to use on your tflite model

1. Clone repository
2. Change the model in assets/tflite/[name].tflite
3. Change the txt file in assets to represent your classes (see example below).
4. Add both the .tflite and .txt to pubspec.yaml under assets:
5. You're good to go!

## model.txt

```
Cat
Dog
```
