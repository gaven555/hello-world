

<h1>Tasks 1 and 2</h1>: 

<b>.Compare Model 1 and Model 2 on the TechTrack dataset using standard object-detection metrics:</b>

In order to compar model 1 and model 2, we need to compare their precision and recall for each of the classes to determine which classes are classified best by each model. To do this, we will compute the precision recall curves. The area under these is an indicator of well the model classifies the object. In the table below, we compute the area under the curve for each class for each precision-recall curve for the two models:

<table style="width:100%">
  <tr>
    <th>Class</th>
    <th> 1</th>
    <th> 2</th>
    <th> 3</th>
    <th> 4</th>
    <th> 5</th>
    <th> 6</th>
    <th> 7</th>
    <th> 8</th>
    <th> 9</th>
    <th> 10</th>
  </tr>
  <tr>
    <td><center>Model 1</td>
    <td><center> 0.1620</td>
    <td><center>0.0535</td>
    <td><center> 0.2039</td>
    <td><center>0.0022</td>
    <td><center>0.0915</td>
    <td><center>0.0057</td>
    <td><center> 0.0539</td>
    <td><center>0.0201</td>
    <td><center>0.0008</td>
    <td><center>0.0804</td>
  </tr>
  <tr>
    <td><center>Model 2</td>
    <td><center>0.1678</td>
    <td><center>0.0507</td>
    <td><center>0.3160</td>
    <td><center>0.0053</td>
    <td><center> 0.1004</td>
    <td><center>0.0037</td>
    <td><center>0.0843</td>
    <td><center>0.0359</td>
    <td><center>0.0080</td>
    <td><center>0.0915</td>
  </tr>
</table>

<br>

<table style="width:100%">
  <tr>
    <th>Class</th>
    <th> 11</th>
    <th> 12</th>
    <th> 13</th>
    <th> 14</th>
    <th> 15</th>
    <th> 16</th>
    <th> 17</th>
    <th> 18</th>
    <th> 19</th>
    <th> 20</th>
  </tr>
  <tr>
    <td><center>Model 1</td>
    <td><center>0.0365 </td>
    <td><center>0.314</td>
    <td><center> 0.0307</td>
    <td><center>0.0244</td>
    <td><center>0.0062</td>
    <td><center>0.1538</td>
    <td><center>0.0868</td>
    <td><center>0.0746</td>
    <td><center>0.0530</td>
    <td><center>0.0025</td>
  </tr>
  <tr>
    <td><center>Model 2</td>
    <td><center>0.0400</td>
    <td><center>0.3466</td>
    <td><center>0.0350</td>
    <td><center>0.0170</td>
    <td><center> 0.0056</td>
    <td><center>0.1805</td>
    <td><center>0.1478</td>
    <td><center>0.0436</td>
    <td><center>0.0445</td>
    <td><center>0.0036</td>
  </tr>
</table>


As seen above for 14 of the classes, model 2 classifies better based on measuring the area under the curve for the individual precision recall curves for each of the classes. The classes that model 2 classifies better are: 1, 3, 4, 5, 7, 8, 9, 10, 11, 12, 13, 16, 17, and 20.

The classes that model 1 classifies better are: 2, 6, 14, 15, 18, and 19

We can also validate these conclusions by looking at the precision recall curves for some of these classes: 

![alt text](PR1.png)

![alt text](PR8.png)

![alt text](PR11.png)


Next we will apply gaussian distortion, vertical flipping, and brightness reduction to see how this affects the detection. Below is an illustration of how these different distortion types were applied: 

Gaussian Noise
![alt text](gaussian_noise.png)

Brightness Reduction 
![alt text](brightness.png)

Vertical Flip
![alt text](vertical_flip.png)

<h1>Tasks 3</h1>: 
<b>.Measure the impact of Gaussian Noise, Vertical Flips, and Brightness adjustments on Model 1’s performance.:</b>

To analyze the affects of these distortions, we will show examples of images that were classified with our model and we will compare its classifications with the ground truths. For each distortion (e.g., flip, brightness reduction, or vertical flip), we will show the unmodified pictures and the modified pictures so that we can see the difference. For the pictures below, the blue boxes represent ground truths while the red boxes represent the model predictions. 


<h2>Gaussian Noise</h2>

Normal Images
<p float="left">
  <img src="/unmodded1.png" width="200" />
  <img src="/unmodded2.png" width="200" /> 
  <img src="/unmodded3.png" width="200" />
  <img src="/unmodded4.png" width="200" />
  <img src="/unmodded5.png" width="200" />
</p>
Images with Gaussian Noise
<p float="left">
  <img src="/dist1.png" width="200" />
  <img src="/dist2.png" width="200" /> 
  <img src="/dist3.png" width="200" />
  <img src="/dist4.png" width="200" />
  <img src="/dist5.png" width="200" />
</p>

<h2>Reduced Brightness</h2>

Normal Images
<p float="left">
  <img src="/unmodded1.png" width="200" />
  <img src="/unmodded2.png" width="200" /> 
  <img src="/unmodded3.png" width="200" />
  <img src="/unmodded4.png" width="200" />
  <img src="/unmodded5.png" width="200" />
</p>
Images with Birghtness Reduced
<p float="left">
  <img src="/brightness1.png" width="200" />
  <img src="/brightness2.png" width="200" /> 
  <img src="/brightness3.png" width="200" />
  <img src="/brightness4.png" width="200" />
  <img src="/brightness5.png" width="200" />
</p>

<h2>Flipped Images</h2>

Normal Images
<p float="left">
  <img src="/unmodded1.png" width="200" />
  <img src="/unmodded2.png" width="200" /> 
  <img src="/unmodded3.png" width="200" />
  <img src="/unmodded4.png" width="200" />
  <img src="/unmodded5.png" width="200" />
</p>
Images that are Flipped
<p float="left">
  <img src="/flip1.png" width="200" />
  <img src="/flip2.png" width="200" /> 
  <img src="/flip3.png" width="200" />
  <img src="/flip4.png" width="200" />
  <img src="/flip5.png" width="200" />
</p>

<b>Analysis</b>

As seen above, all three distortions resulted in a reduction in the number of detections. The distortion that had the greatest impact on our model's ability to detect objects was the vertical flip. Flipping the images reduced the number of detections by over half. The gaussian noise both reduced the number of detections and also resulted in an increase in the number of false positives. Redicing the brightness had a minimal impact on our model's ability to detect objects but did result in a slight reduction in the number of objects detected. 