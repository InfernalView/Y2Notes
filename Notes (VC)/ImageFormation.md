# Image Formation

## Image Formation
**Digital Images** are 2D **sampled** representations of some continuous function.

**Pixels** are sampled digital values, and are the smallest individual element of an image.

**Dimentionality Reduction Machine** is a machine that 'reduces' a 3D world into a 2D image. Like camera imaging.

## Camera Imaging
**Camera Imaging** is a method of capturing 3D objects and environments as a 2D image. Light reflected off an object will be detected and measured by a **Photoreceptive Sensor**; however, when there are too much light received by the sensor, the image will often appear blurry. Blurriness can be reduced by adding a **Barrier** which will block most light rays from reaching the sensor. The barrier contains a gap to allow a small amount of rays to pass through; this gap is called the **Aperture**.

The **Pinhole Camera Model** captures all the light through a singular point; this point is called the **Centre of Projection** or **Optical Centre**. The gap here is still called the **Aperture**, and the image 'formed' on the sensor is called the **Image Plane**; which will be perceive the image as 'inverted' or 'flipped'.

The **Aperture** is, as explained, an important function for camera imaging. Different aperture sizes affect how an image is processed, and to differing degrees of quality. **Large** aperture sizes will let more light through; which makes the image suffer from blurriness, from a lack? of exposure. **Small** aperture sizes will let less light rays through; but may cause **Diffraction** to occur, where the light may blend together and blur the image.

The **Ideal Pinhole** is one where only one ray of light reaches each point on the sensor. This will have its unfovourable effect of darkening the image, and may have heavy diffraction effects.

**Lens** focus light onto a film/sensor, which will reduce an images' blurriness. However, the focus only works at certain distances from the object; and changing the shape of the lens will also change this distances. Most good cameras adapted this to allow for varying foci, by all the lens to be changed.

## Image Noise
**Image Noise** is unwanted variations in pixel values that degrade the visual quality of an image. Which is normally caused by: imperfect sensors, environmental factors, low light conditions, and etc.

There are four different types of image noises:
* **Thermal Noise**, or **Additive Gaussian Noise**, occurs due to random flunctuations of electrons when the photo sensor is amplified. This noise is highly related to ISO level.
* **Shot Noise**, or **Poisson Noise**, occurs due to photons randomly hitting the sensor, which will have the effect of some parts of the sensor having a higher signal strength from more photons that hit it. This is a directly proportional effect, and it is highly related to photoiode.
* **Replacement Noise**, or **Salt&Pepper Noise**, where some pixels on an image may appear overly dark or bright, which are called 'Dead pixel' and 'Hot pixel' respectively. (I dunno how is problem)
* **Speckle Noise**. Subjective and Objective speckles, which commonly occur in medical images and radar. (Idk cause)

**Signal-to-Noise Ratio** refers to the level (degree?) of a desired signal compares to the level of background noise. This is expressed in decibels (*db*), and it is calculated by this formula.

$$SNR = \frac{P_{signal}}{P_{noise}}$$

There are many ways for **Image Enhancement**:
* Image Denoise
* Image Deblurring
* Super-resolution
* Dehazing
* Deraining
* Prob more...
