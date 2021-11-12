# Adding an 'A' to STEM
>  " I have no hesitation in saying we need to add the letter ‘A’…an education devoid of arts… is an empty, half-brain kind of education." 
 by Howard Gardner, an education professor at Harvard University


STEM stands for science, technology, engineering, and mathematics.

While, STEAM stands for science, technology, engineering, **arts** and mathematics.

![image](https://github.com/navya26s/UNIT-2-/blob/main/steam.png)

Arts play an integral part in our lives. They offer scope of new discoveries while opening doors to creativity and innovation.  

However, there remain certain soft skills a computer simply cannot replicate in the workplace: teamwork, cooperation, creativity and adaptation to change, to name a few. These changes, as well as the growing emphasis on soft skills across industries and roles, are creating the need for curricula that integrate STEM with the arts. By integrating the arts into STEM, STEAM-focused curricula incorporate the study of the humanities, language arts, dance, drama, music, visual arts, design, new media and more.

When looking at STEM vs. STEAM, the difference lies in the way they approach scientific concepts. STEM focuses explicitly on the hard scientific, technological, engineering or mathematical skills to drive progress or create a new concept. In STEAM curricula, per The Conversation, students leverage both hard and soft skills to solve problems. 

[reffered website link](https://www.ucf.edu/online/engineering/news/comparing-stem-vs-steam-why-the-arts-make-a-difference/)


## Art X Science

STEAM takes STEM one step further by emphasizing the arts, taking inspiration from the field and applying its concepts in cross-discipline learning that supports creativity in science, mathematics and more. STEAM focuses on teaching students to form connections between a variety of subjects in order to get the most out of learning about any subject, from robotics and coding to reading and music. In a world where many arts programs are at risk in favor of STEM education, STEAM seeks to keep these subjects closely intertwined. 

[reffered website link](https://sphero.com/blogs/news/stem-vs-steam)

In a subject like Arts we time and again see concepts of other subjects, like mathematics.  Van Gogh made the ‘Starry Night’, a painting that combines artistic aesthetic appeal and dynamic brushwork combined with the application of mathematical concepts like the turbulent flow, angular perspectives and geometric proportions. This contributed in making it a better artwork as it added more value to the theme of conflict and chaos that he was trying to bring out through the artwork with the use of the spirals in the sky.

Artists, for many centuries have used this combination in order to achieve brilliance in their field of work. Leonardo da Vinci’s Last Supper is an example of visual balance and geometric symmetry  creating a sense of appeal. Artistic knowledge is something that is not fully objective and independent, yet needs a combination of several things put together in order to drive it to success giving rise to a deeper knowledge. 

Even in modern day, we have found a combination of design and computer science- one such example can be seen in a neural generato called **Deep Dream Generato**

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

### Application of Deep Dream Generator
#### Use of an Arduino

I implemented the knowledge and experiences of making a simple LED circuit using an 'Arduino' and photgraphed the lit up LED. 
I created this using a resister, jumper wires, a LED, a bread board and an UNO. Then, I uploaded my images on the Deep Dream Generator and experimented with several presets to see the final outcomes.
![image](https://github.com/navya26s/UNIT-2-/blob/main/Untitled_Artwork%2036.png)

