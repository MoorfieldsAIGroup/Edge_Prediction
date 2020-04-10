# edge_prediction

## Usage
### Image Prediction
[Colab][Colab_link] test Page.

[Colab_link]: https://colab.research.google.com/gist/zgy600/e9d433f3fd27d2babda2f01b143e089f/edge_prediction_run_github.ipynb?authuser=1

You will never use anything else than this [website][an_awesome_website_link].

[an_awesome_website_link]: https://stackoverflow.com

You can easily test the output masks on your images via the CLI.

To predict a single image and output the result:
```bash
> python3 label_image.py \
> -m model.tflite \
> -l dict.txt \
> -i test_image.jpeg
```

To predict a multiple images in a folder and output a csv:
```bash
> python3 label_image.py \
> -m model.tflite \
> -l dict.txt \
> -o batch \
> -f data
```

```shell
> python3 label_image.py -h
usage: label_image.py [-h] [-i IMAGE] [-m MODEL_FILE] [-l LABEL_FILE]
                      [--input_mean INPUT_MEAN] [--input_std INPUT_STD]
                      [-f FOLDER] [-o OPTION]

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
  -f FOLDER, --folder FOLDER
                        image folder name
  -o OPTION, --option OPTION
                        single or batch prediction
```

## Reference
1. https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite/examples/python/
