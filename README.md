# ImageDetectTF
<p>This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API. 
## Steps
<br />
<b>Step 1.</b> Clone this repository
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv tfod
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfodj
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook 1. Image Collection.ipynb</a> - ensure you change the kernel to the virtual environment as shown below
<br/>
![Screenshot 1](https://github.com/radeon2525/ImageDetectTF/assets/122255661/3c816160-70c1-436e-9a77-9a595bdfd572)
![Screenshot 2](https://github.com/radeon2525/ImageDetectTF/assets/122255661/804d2af9-eea1-4988-81dd-092c3171822b)

[Screenshot 3](https://github.com/radeon2525/ImageDetectTF/assets/122255661/526301de-a872-49bf-ada6-ebb89d720c24)
![Screenshot 4](https://github.com/radeon2525/ImageDetectTF/assets/122255661/09321900-9fbd-445c-b6a2-a7a6f8834596)



<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\TFODCourse\Tensorflow\workspace\images\train<br />
\TFODCourse\Tensorflow\workspace\images\test
<br></br>
<b>Step 7.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<br></br>
<b>Step 8.</b> Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<br />
<b>Step 9.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 8. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
