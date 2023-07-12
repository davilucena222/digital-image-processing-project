# Digital Image Processing Project
<p>
  The goal of this project was to develop algorithms that treat and modify images from their pixels, by increasing brightness, luminance, and intensity. Each image used in this project had changes that will be demonstrated and discussed throughout this description.
</p>

# Techonologies
<ul>
  <li>Python</li>
  <li>Google Colab</li>
  <li>numpy</li>
  <li>os</li>
  <li>matplotlib</li>
  <li>Image Filter</li>
  <li>ImageOps</li>
  <li>ImageEnhance</li>
</ul>

# Topics covered and used
<p>
  This project involved saturation control through gray levels (HSB/HSV), RGB image conversions to YIQ based on the matrix formula, negative X and Y of the images absorbing the colors that would be emitted in the bands, the correlation of images with masks (mean, median, Sobel among others).
The objectives in relation to the conversions were to insert and control the luminance (Y) of the image with additional chrominance (I and Q) logos that in turn do not have a direct visualization. In the environment of negating the images, techniques were used to invert the values (based on their neighborhood) of a certain band so that in a given pixel there was a predominance of the same band, so in negative Y we obtained results in which black became white and the white became black. In the image correlation, neighborhoods with extension by zero (offset), and the interpolation of the pivot in the mask were taken into account, with the purpose of smoothing images, extracting noise (salt-and-pepper), and detecting edges with convolutional masks. And as the last point to be treated, the control of hue and saturation of an image was implemented, on the other hand, formulas of angle of color quadrants, chroma, and "value" (brightness -> brightness) were used that form the HSB or also known HSV.
</p>

# Materials and methods
<p>
  In this project, we made use of libraries and tools throughout the development of each question to convert values and fill arrays with their already converted values. In the construction of algorithms such as correlation, conversion from RGB to YIQ mean, median, and Sobel filters were developed with the help of libraries such as numpy, matplotlib, and os. These libraries assisted in converting certain types of data to other types and basic operations also to achieve this goal. In addition, it was necessary to capture each converted data to be displayed correctly as an image, to accomplish this feat it was necessary to use some image libraries to help build a new image model, filter image data, merge data from an image with another and finally display it already changed with its modified data. However, for that, it was necessary to use some libraries from the PIL library, such as the Image library performs basic operations on images such as copying, the ImageFilter library, ImageEnhance which modifies image properties and finally the ImageOps library which modifies the size of images. an image expands the image and also modifies its properties.
  
Throughout this work we apply concepts such as the conversion of RGB images to YIQ, we also apply the concept of inverting colors in images in each band of R, G, or B, and we also use the concept of correlation to perform the operation between the defined mask and the image, we apply filters such as the mean, median, and Sobel in order to carry out tests and verify how the image would behave given the application of each filter. In addition, we apply basic color concepts between images such as adding colors and subtracting colors to identify gray levels. Finally, we applied the concept of HSB together with the saturation control and the conversion of images to RGB, in the application of these concepts it was possible to modify the hue of the image, perform the normalization of values between 0 and 1, calculate the value of the most predominant, separating the RGB bands to apply operations to each one of them, defining the sector of the angles in which the colors would be present based on the concept of quadrants and gradient to carry out the saturation control precisely at the time of the conversion and its operations.
</p>

# Theory and application of image and filter methods with results

<p>We've applied some concepts evolving filter images and conversion methods in the images used on the project, some of them are:</p>

<ul>
  <li>RGB-YIQ-RGB Conversion</li>  
</ul>

 ![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/7999910a-bba9-4f78-924a-ebca0251dc64)

<ul>
  <li>Negative in RGB (band by band) and in the Y band, followed by conversion to RGB</li>  
</ul>

![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/67df51f9-0711-4858-9550-bf0a73e5a468)

<ul>
  <li>Correlation m x n over R, G, and B, with offset, filter, and pivot defined in a separate file (txt)</li>  
</ul>

![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/31d7447a-852b-4146-8103-03769f812e2f)

<ul>
  <li>MEDIAN FILTER</li>  
</ul>

![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/129049f9-5765-4863-9b91-fea0e3173c74)

<ul>
  <li>HSB</li>  
</ul>

![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/bb9a4f9c-64f4-4fd4-9612-1215ba1afa84)

![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/dba0655e-3c54-4de6-ba41-ce91287d41c9)

<ul>
  <li>Changing values in hue, saturation, and brightness</li>
</ul>

![image](https://github.com/davilucena222/projeto-processamento-digital-de-imagens/assets/56702492/e21e03e2-86f3-4782-a650-c21fe905f8a1)

# Results description

<p>
After applying the concepts previously discussed in each question, it was possible to reach each established objective.
In the first application, we obtain the RGB image converted to YIQ with its color properties modified for each of the 3 bands, in addition, we separate the image in the YIQ band, in the RGB band, and also in the Y band to carry out comparisons and understand which modifications were carried out after the entire conversion process.
  
In the second application, we apply the negative to the input image and configure the algorithm to be dynamic, and apply the negative in the R, G, or B band, then the image is converted to YIQ and then to RGB, with this we apply the negative and obtain the expected result, where there was a white color, it started to receive a black color, and where there was a black color, it started to receive a white color and where the three RGB components were present, it started to receive the secondary colors, considering that the negative in a component can cause the occurrence of another color with the possible mixtures.

As for the third application, as a result, we get some behaviors related to the image after performing the operations between the image itself and a mask. In this question, we applied some filters such as the average one, where it was possible to perceive blurring in the image, but also occurrences of blurring in the shape of boxes, since the average filter itself causes such an occurrence, we used the horizontal Sobel filter and as a result, the image demonstrated quite explicitly the presence of vertical edges in his composition when applied the vertical Sobel filter more horizontal edges were detected in the image and the distinction from one edge to another was quite noticeable.
  
In the fourth application, the median filter was used and as a result of the output image we had an image with a more natural blur compared to the blur that the average filter causes in an image, in addition, the colors of the image were closer and the contour was larger, as a consequence the noise of the image is also reduced the image is cleaner, but it is more blurred because the larger the mask the greater the blurring of the output image.
  
Finally, in the fifth application, we had an image with some behaviors due to the saturation control in the HSB system. First, we separated the image in each HSB band to observe and understand its behavior, in the HUE band we obtained a darker image due to variations in its hue, that is, its R, G, and B components, in the SATURATION or SATURATION band we had an image with variations of light gray and dark gray tones due to RGB color variation, be it a light variation or dark variation of the image at each point and in the BRIGHTNESS or BRIGHTNESS band the result was an image with some brightness variations lighter and darker depending on the region of the image itself and taking into account its hue. Then we converted the image to RGB by applying the saturation control and from that moment on the image and its properties started to behave in some ways when the hue, saturation, or brightness are changed, because when changing the saturation for example the hue with smaller values is increased, the luminance as a consequence is also increased, the occurrence of color variations are noticeable depending on the change in hue, saturation and brightness.
</p>

# Google Colab of the project with more information 

<p>If you want to have more deep information about this project and applications, please access the Google Colab in this link.</p>

<ul>
  <li>
    <a href="https://colab.research.google.com/drive/1FMIcZYK6cK6JDnE1XkLUATfBNuH6eucb?usp=sharing">
      Google Colab of the project
    </a>
  </li>
</ul>


# Developers:
<a href="https://www.linkedin.com/in/davi-luiz-a54645195/" target="_blank">
  <img align="center" alt="davi-linkedin" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" style="max-width:100%;">
  Davi José Lucena Luiz
</a>



<a href="https://www.linkedin.com/in/fabricio-dev/" target="_blank">
  <img align="center" alt="davi-linkedin" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" style="max-width:100%;">
  Carlos Fabrício da Silva Pontes
</a>

<a href="https://www.linkedin.com/in/abraão-homualdo-8300b8203/" target="_blank">
  <img align="center" alt="davi-linkedin" height="60" width="80" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" style="max-width:100%;">
  Abrãao Homualdo Alves Moreira
</a>
