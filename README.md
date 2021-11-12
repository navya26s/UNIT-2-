# Adding an 'A' to STEM
>  " I have no hesitation in saying we need to add the letter ‘A’…an education devoid of arts… is an empty, half-brain kind of education." 
Quote by Howard Gardner, an education professor at Harvard University


STEM stands for science, technology, engineering, and mathematics.
STEAM stands for science, technology, engineering, arts and mathematics.

Arts play an integral part in our lives. They offer scope of new discoveries while opening doors to creativity and innovation.  

However, there remain certain soft skills a computer simply cannot replicate in the workplace: teamwork, cooperation, creativity and adaptation to change, to name a few. These changes, as well as the growing emphasis on soft skills across industries and roles, are creating the need for curricula that integrate STEM with the arts. By integrating the arts into STEM, STEAM-focused curricula incorporate the study of the humanities, language arts, dance, drama, music, visual arts, design, new media and more.

When looking at STEM vs. STEAM, the difference lies in the way they approach scientific concepts. STEM focuses explicitly on the hard scientific, technological, engineering or mathematical skills to drive progress or create a new concept. In STEAM curricula, per The Conversation, students leverage both hard and soft skills to solve problems. 


## Art X Science


## Deep Dream Generator
Deep Dream is a program of computer vision that was created by one of Google’s engineers Alex Mordvintsev. This uses a convolutional neural network to find and enhance patterns in images via algorithmic pareidolia, thereby formulating a Dream-like hallucinogenic appearance within deliberately over-processed images.

[reffered website link](https://hackernoon.com/deep-dream-with-tensorflow-a-practical-guide-to-build-your-first-deep-dream-experience-f91df601f479)

### Visualizing the input 
```python
  
  # Define a function to load an image and limit its maximum dimension to 512 pixels.

 def load_img(path_to_img):
   max_dim = 512
   img = tf.io.read_file(path_to_img)
   img = tf.image.decode_image(img, channels=3)
   img = tf.image.convert_image_dtype(img, tf.float32)
   shape = tf.cast(tf.shape(img)[:-1], tf.float32)
   long_dim = max(shape)
   scale = max_dim / long_dim
   new_shape = tf.cast(shape * scale, tf.int32)
   img = tf.image.resize(img, new_shape)
   img = img[tf.newaxis, :]
   return img
   
  # Here we create a simple function to display an image:

def imshow(image, title=None):
  if len(image.shape) > 3:
    image = tf.squeeze(image, axis=0)

  plt.imshow(image)
  if title:
    plt.title(title)
    
# Implementing the image

content_image = load_img(content_path)
style_image = load_img(style_path)

plt.subplot(1, 2, 1)
imshow(content_image, 'Content Image')

plt.subplot(1, 2, 2)
imshow(style_image, 'Style Image')
```
[code extracted from Tensor Flow](https://www.tensorflow.org/tutorials/generative/style_transfer)
