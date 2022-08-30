# War in the Air - Notebook

The project is created using <strong>Sentinel-5P Level 2</strong> https://aws.amazon.com/marketplace/pp/prodview-ndthuqa4tzx4s Imagery from the <strong>Amazon Sustainability Data Initiative</strong> which is free to use for the public.
<br />
The Project aims to create a dataset for the study of the effects of War, particularly the contribution of War efforts towards Carbon Monoxide Emission on Earth. The <strong>Sentinel-5P Level 2</strong> imagery has information on the amount of CO found in the Troposphere at a given time. 

## Dataset Structure

The Data set is split into <strong>Pre-War</strong> period (1 Feb - 23 Feb 2022), <strong>Refugee Crisis Peak</strong> period (Feb 24 - Mar 23 2022), <strong>Mid-War</strong> period (May 1 - May 23 2022) and <strong>Post-War</strong> period (Aug 1 - Aug 26). The periods were selected to view a time based view of the levels of CO in the Troposphere and find any information on how the War in Ukraine has contributed towards CO emissions compared to the rest of the world. This is still subject to actual CO Emission increment on a regular basis, but with a microscopic look at the contribution from the War in Ukraine. 

The Code to compile fresh data or use current dataset can be found at https://github.com/williammabotjadev/war-in-the-air

# Usage

To Use the current dataset, you just need to upload the folders <strong>pre_images</strong>, <strong>post_images</strong>, <strong>immi_images</strong> and <strong>mid_images</strong> into sub-directories of a local folder called 'images', or any name as <strong>pre</strong>, <strong>post</strong>, <strong>immi</strong> and <strong>mid</strong> respectively. 

<h5>S3 Options are also available for the Current Image Dataset</h5>

<strong>The Bucket Addresses for Each Class</strong>

<strong>immi class</strong>
s3://war-in-the-air/images/immi/


<strong>pre class</strong>
s3://war-in-the-air/images/pre/


<strong>mid class</strong>
s3://war-in-the-air/images/mid/


<strong>post class</strong>
s3://war-in-the-air/images/post/

<strong>Download Example</strong>

<code>mkdir pre</code>
<br />
<br />
<code>cd pre</code>
<br />
<br />
<code>aws s3 sync --no-sign-request s3://war-in-the-air/images/pre .</code> 
<br />
<br />
The Model can be tweaked to any Activation Algorithm of your Choice but it uses RELU as a default. You may also expand on the Training of the Model with a different Epoch amount, the default is 3. 

The Study aims to go deeper into analyzing the data, that has been converted from Tif to PNG through the Code at https://github.com/williammabotjadev/war-in-the-air. 
