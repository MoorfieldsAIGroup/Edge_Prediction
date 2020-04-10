# edge_prediction

## Usage
### Image Prediction
You can easily test the output masks on your images via the CLI.

To predict a single image and output the result:
```bash
> python3 label_image.py \
> --model_file model.tflite \
> --label_file dict.txt \
> --image test_image.jpeg
```

To predict a multiple images in a folder and output a csv:
```bash
> python3 label_image.py \
> --model_file model.tflite \
> --label_file dict.txt \
> --option batch \
> --folder data
```

```shell
> python3 label_image.py -h
usage: label_image.py [-h] [-i IMAGE] [-m MODEL_FILE] [-l LABEL_FILE]
                      [--input_mean INPUT_MEAN] [--input_std INPUT_STD]
                      [--folder FOLDER] [--option OPTION]

optional arguments:
  -h, --help            show this help message and exit
  -i IMAGE, --image IMAGE
                        image to be classified
  -m MODEL_FILE, --model_file MODEL_FILE
                        .tflite model to be executed
  -l LABEL_FILE, --label_file LABEL_FILE
                        name of file containing labels
  --input_mean INPUT_MEAN
                        input_mean
  --input_std INPUT_STD
                        input standard deviation
  --folder FOLDER       image folder
  --option OPTION       single or batch
```

## Reference
1. https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite/examples/python/
