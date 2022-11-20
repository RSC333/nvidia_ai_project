# NumberClassifier
 
The goal of this project is to be able to identify the digits 0-9 using ai. This can be used as the basis for a text recognition model and expandded to include all symbols and letters. 

## The Algorithm

This project was trained on the Jetson Nano. It uses the imagenet and resnet-18 models which were re-trained using a dataset of images handwritten numbers from 0-9. When it is run, it uses the imagenet.py file with the retrained resnet18.onnx file in order to determine what digit was written on the input file.

## Running this project

1. Download model and image files onto Jetson Nano
2. Navigate to jetson-inference/python/training/classification
3. Set Net and Dataset variables
`NET=models/chars`
`DATASET=data/chars`
4. Run `imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/7/img008-045.png test.png` to process image, replacing image directory with chosen image. 
5. Check test.png to see results

[View a video explanation here](video link)
