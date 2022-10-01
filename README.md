# Image-Captioning-on-Flickr-8k

Image captioning refers to the task of generating the caption that describes the visual description of the image accurately.
## Dataset
Dataset used for this task is: Flickr 8K. It contains roughly 8000 images which can be used. There are 5 caption provided associated with each image. Other Dataset also exists for same task such as: Flickr 30k, MS COCO etc. but they're too big of dataset to run on the local computer.

## Model
Currently I have trained two models:- 

A) **Simple Encoder-Decoder Type Model.**

For First Model architecture is fairly simple. It contains two "Encoder" Modules, One for Image & other for Text. They helps the Image & Generated Text to encode in some "middle" state(Vectors). This "middle" state will be converted to an output(next word in the Sentence) by the decoder module.

![download](https://user-images.githubusercontent.com/56585873/193397631-77799415-ca62-49da-9425-021376bc6719.png)

LSTM module is used to convert the Input Sequence into middle state in form of a Vector. While InceptionV3/VGG is used to convert the Input Image into the vector, which will be further passed into Dense to convert the Image into middle state. Both the Text and Image input, after conversion into middle state, is passed into a Decoder which is a nothing but a Feed Forward Neural Network.


B) **Enocder-Decoder Model with Self Attention Module**
