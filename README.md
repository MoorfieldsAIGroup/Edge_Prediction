# edge_prediction

## Usage
### Image Prediction
You can easily test the output masks on your images via the CLI.
To predict a single image and output the result:
```
python3 label_image.py \
--model_file model.tflite \
--label_file dict.txt \
--image test_image.jpeg
```
To predict a multiple images in a folder and output a csv:
```
python3 label_image.py \
--model_file model.tflite \
--label_file dict.txt \
--option batch \
--folder data
```

## Reference
1. https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite/examples/python/
