# medium-show-and-tell-caption-generator
Code to run inference on a Show And Tell Model. This model is trained to generate captions given an image.

A tutorial for the code can be found here: https://medium.freecodecamp.org/building-an-image-caption-generator-with-deep-learning-in-tensorflow-a142722e9b1f


# execute code for google colab

### clone repository

```
!git clone https://github.com/birkanatici/caption_generator app
```

### download model
```
!python3 app/bin/download_model.py --model-dir app/etc
```

### download test image
```
!curl https://www.cat-world.com.au/wp-content/uploads/2009/07/kitten-drinking-milk.jpg --output app/imgs/test.jpg
```

### generate caption 
```
!python3 app/medium_show_and_tell_caption_generator/inference.py --model_path "app/etc/show-and-tell.pb" --input_files "app/imgs/test.jpg" --vocab_file "app/etc/word_counts.txt"
```
