<h2>TensorFlow-FlexUNet-Image-Segmentation-Knee-X-Ray-Two-Classes-Edge-Detection (2026/10/02)</h2>
Sarah T. Arai<br>
Software Laboratory antillia.com<br><br>
This is the first experiment in Image Segmentation for <b>Knee X-Ray Two Classes (Grades) Edge Detection</b>
 based on
our <a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">TensorFlowFlexUNet Model</a>
 (<b>TensorFlow Flexible UNet Image Segmentation Model for Multiclass</b>) and a upscaled PNG
 <a href="https://drive.google.com/file/d/1kM-yjagZmrLFj0ugcPeMT0fHGqiPlWZJ/view?usp=sharing">
Augmented-Knee-X-Ray-Two-Classes-ImageMask-Dataset.zip</a> with colorized masks 
(<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>), 
which was derived by us from the following two datasets: 
<br><br>
<b>Dataset 1:</b>
X-Ray images in <b>MedicalExpert-I</b> of
<a href="https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images">
<b>Digital Knee X-ray Images</b>
</a> 
<br>
<b>Dataset 2:</b>
Edge_Detection masks in <b>MedicalExpert-I</b> of 
<a href="https://www.kaggle.com/datasets/shuvokumarbasakbd/knee-x-ray-digital-colorized-images">
<b>Knee X-ray Digital Colorized Images</b>
</a> 
<br>
<br>
In this experiment, we aggregated the data originally categorized into four classes 
(Doubtful, Mild, Moderate, and Severe) into two classes (<b>Doubtful_or_Mild</b> and <b>Moderate_or_Severe</b>) 
for simplicity.
<br><br> 
<hr>
<b>Actual Image Segmentation for Knee X-Ray Images</b><br>
As shown below, the inferred masks resemble the ground-truth masks. <br>
<br>
<b>class_color_map = {Doubtful_or_Mild: green, Moderate_or_Severe: dark_red)} </b><br><br>
<table>
<tr>
<th width="320" height="auto">Input: image</th>
<th width="320" height="auto">Mask (ground_truth)</th>
<th width="320" height="auto">Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/hflip_DoubtfulG1 (355)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/hflip_DoubtfulG1 (355)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/hflip_DoubtfulG1 (355)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/ModerateG3 (2)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/ModerateG3 (2)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/ModerateG3 (2)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/vflip_SevereG4 (197)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/vflip_SevereG4 (197)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/vflip_SevereG4 (197)_5.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1. Dataset Citation</h3>
The dataset used here was derived from the following two datasets on the Kaggle website.
<br><br>
<b>Dataset 1: </b>
X-Ray gray scale images in <b>MedicalExpert-I</b> of
<a href="https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images">
<b>Digital Knee X-ray Images</b>
</a> by Orvile
<br>
<b>Dataset 2: </b>
Edge_Detection masks in <b>MedicalExpert-I</b> of 
<a href="https://www.kaggle.com/datasets/shuvokumarbasakbd/knee-x-ray-digital-colorized-images">
<b>Knee X-ray Digital Colorized Images</b>
</a> by Medi Hunter - 4004.
<br><br>
The following explanation (excerpt) was taken from the first website above.
For more information of the second dataset, please refer to 
<a href="https://www.kaggle.com/datasets/shuvokumarbasakbd/knee-x-ray-digital-colorized-images">
<b>Knee X-ray Digital Colorized Images</b>
</a><br><br>
<b>About Dataset</b><br>
<b>Digital Knee X-Ray Images</b><br>
<b>A Carefully Curated Dataset for Knee Osteoarthritis Grading</b><br>
Welcome to this comprehensive dataset featuring 1,650 high-quality digital X-ray images of knee joints,
 sourced from top hospitals and diagnostic centers. <br>
 Each image is meticulously annotated by medical experts using the Kellgren and Lawrence (K&L) grading system,
  the gold standard for assessing knee osteoarthritis severity. Perfect for data scientists, researchers,
   and innovators, this dataset is ideal for advancing machine learning, pattern recognition, 
and medical image analysis—think automated osteoarthritis detection systems and beyond!
<br><br>
<b>Why This Dataset Matters</b><br>
Knee osteoarthritis (OA) impacts millions globally, and accurate diagnosis is key to effective treatment. <br>
The Kellgren and Lawrence system helps radiologists evaluate OA severity through radiographic features.<br>
 This dataset provides a robust, labeled collection of knee X-rays to drive the development of <br>
 automated diagnostic tools, merging medicine and technology for better health outcomes.
<br><br>
<b>What’s Inside</b><br>
Digital Knee X-Rays: 1,650 grayscale, 8-bit images captured using a PROTEC PRS 500E X-ray machine.<br>
Expert Annotations: Each image is labeled by two medical experts with its K&L grade, likely in filenames 
or a metadata file.<br>
Cartilage Insights: Includes a novel approach to extract cartilage regions of interest (ROIs) based on pixel density—ROI details may be included (check the files!).
<br><br>
<b>License</b><br>
<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>
<br>
<br>
<h3>
2. Knee-X-Ray ImageMask Dataset
</h3>
<h3>2.1 Download ImageMask Dataset</h3>
 If you would like to train this Knee-X-Ray Segmentation model,
 please download the dataset from Google Drive  
 <a href="https://drive.google.com/file/d/1kM-yjagZmrLFj0ugcPeMT0fHGqiPlWZJ/view?usp=sharing">
Augmented-Knee-X-Ray-Two-Classes-ImageMask-Dataset.zip</a>. 
Expand the downloaded ImageMaskDataset and put it under the <b>./dataset</b> folder.
<br>
<pre>
./dataset
└─Knee-X-Ray-Two-Classes
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
         ├─images
         └─masks
</pre>
<br>
<b>Knee-X-Ray-Two-Classes Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/Knee-X-Ray-Two-Classes_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images in the training and valid datasets is large enough to use for the
 training set of our segmentation model.
<br>
<h3>2.2 Derivation of ImageMask Dataset</h3>
The folder structure of our <b>MedicalExpert-I</b> derived from the original dataet is as follows.
<br>
<pre>
./Knee X-ray Images
 └─MedicalExpert-I
    │
    ├─1Doubtful
    │   ├─Edges
    │   └─Image
    │    
    ├─2Mild
    │   ├─Edges
    │   └─Images
    │
    ├─3Moderate
    │   ├─Edges
    │   └─Images
    │
    └─4Severe
         ├─Edge
         └─Images 
</pre>
It consits of the four grades, Doubtful,Mild, Moderate and Severe data.
<ul>
<li>
<b>Images:</b>Knee X-Ray gray scale images taken from <b>Dataset 1</b>.
</li>
<li>
<b>Edges: </b>Edge masks images taken from Edge_Detection subset in <b>Dataset 2</b>.
</ul>
<br>
<b>Step 1</b><br>
We generated a 2x enlarged Image and Edge Mask master dataset with colorized masks 
<b>(Doubtful_or_Mild: green, Moderate_or_Severe: dark_red) </b>
from the images in <b>Images</b> and the corresponding 
masks in <b>Edges</b>.<br>
<br>
<b>Step 2</b><br>
To address the limited size of the master, we generated our own 
Augmented ImageMaskDataset from the master by using a simple horizontal and vertical image flipping tools.
<br>
<h3>2.3 Train Sample Images and Masks</h3>
<b>Train_sample_images</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_sample_masks</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/train_masks_sample.png" width="1024" height="auto">
<br>

<h3>
3. Train TensorFlowFlexUNet Model
</h3>
 We trained the Knee-X-Ray TensorFlowFlexUNet model using the following
<a href="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
This runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters=16 </b> and large <b>base_kernels=(11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large <b>num_layers=8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
; You may specify your own UNet class derived from our TensorFlowFlexModel
model         = "TensorFlowFlexUNet"
generator     =  False
image_width    = 512
image_height   = 512
image_channels = 3
num_classes    = 3
base_filters   = 16
base_kernels   = (11,11)
num_layers     = 8
dropout_rate   = 0.04
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_focal_dice_loss" and <a href="./src/dice_coef_multiclass.py">"dice_coef_hybrid"</a>,
and weight parameters <b>hybrid_alpha</b> and <b>hybrid_beta</b> for <b>dice_coef_hybrid</b> function. 
<pre>
[model]
loss           = "categorical_focal_dice_loss"
metrics        = ["dice_coef_hybrid"]
; Experimental two weight parameters to calculate "dice_coef_hybrid" metric.
hybrid_alpha   = 1.7
hybrid_beta    = 0.3
</pre>
<b>Dataset class</b><br>
Specifed <a href="./src/ImageCategorizedMaskDataset.py">ImageCategorizedMaskDataset</a> class.<br>
<pre>
[dataset]
class_name    = "ImageCategorizedMaskDataset"
</pre>
<br>
<b>Learning rate reducer callback</b><br>
Enabled the learning_rate_reducer callback and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with the patience parameter.
<pre>
[train]
patience      = 10
</pre>
<b>RGB Color map</b><br>
Specified RGB color map dict for Knee-X-Ray 1+2 classes.<br>
<pre>
[mask]
mask_datatyoe    = "categorized"
mask_file_format = ".png"
;Knee-X-Ray RGB color map dict for 1+2 classes.
rgb_map = {(0,0,0):0,(0,255,0):1,(180,20,20):2}
</pre>

<b>Epoch change inference callback</b><br>
Enabled <a href="./src/EpochChangeInferencer.py">epoch_change_infer callback</a></b>.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
num_infer_images         = 6
</pre>

By using this callback, on every epoch change, the inference procedure can be called
 for 6 images in the <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> 
<br> 
As shown below, early in the model training, the predicted masks from our UNet segmentation model showed 
discouraging results.
 However, as training progressed through the epochs, the predictions gradually improved. 
 <br> 
<br>
<b>Epoch_change_inference output at starting (epoch 1, 2, 3, 4)</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (epoch 18, 19, 20, 21)</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at ending (epoch 38, 39, 40, 41)</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>
<br>
In this experiment, the training process was stopped at epoch 41 by EarlyStoppingCallback.<br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/train_console_output_at_epoch41.png" width="1024" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/eval/train_metrics.png" width="520" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>
4. Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes</b> folder,
and run the following bat file to evaluate the TensorFlowUNet model for Knee-X-Ray.<br>
<pre>
>./2.evaluate.bat
</pre>
This runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetEvaluator.py ./train_eval_infer_aug.config
</pre>

Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/evaluate_console_output_at_epoch41.png" width="1024" height="auto">
<br><br>Image-Segmentation-Knee-X-Ray

<a href="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_focal_dice_loss) on this Knee-X-Ray/test was not low, and 
dice_coef_hybrid was not high, as shown below.
<br>
<pre>
categorical_focal_dice_loss,0.0811
dice_coef_hybrid,0.8404
</pre>
For comparison of the four grades case,
please refer to <a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Knee-X-Ray-Edge-Detection">
TensorFlow-FlexUNet-Image-Segmentation-Knee-X-Ray-Two-Classes-Edge-Detection</a>
<br><br>
<h3>
5. Inference
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes</b> folder
and run the following bat file to infer segmentation regions for images using the trained TensorFlowUNet model for Knee-X-Ray.<br>
<pre>
>./3.infer.bat
</pre>
This runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer_aug.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/mini_test_masks.png" width="1024" height="auto"><br>

<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks for Knee-X-Ray Images</b><br>
As shown below, the inferred masks look similar to the ground truth masks, but differ in the detailsc .<br>
<br>
<b>class_color_map = {Doubtful_or_Mild: green, Moderate_or_Severe: dark_red)} </b><br><br>
<table>
<tr>
<th width="320" height="auto">Image</th>
<th width="320" height="auto">Mask (ground_truth)</th>
<th width="320" height="auto">Inferred-mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/DoubtfulG1 (148)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/DoubtfulG1 (148)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/DoubtfulG1 (148)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/DoubtfulG1 (139)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/DoubtfulG1 (139)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/DoubtfulG1 (139)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/hflip_ModerateG3 (32)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/hflip_ModerateG3 (32)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/hflip_ModerateG3 (32)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/MildG2 (26)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/MildG2 (26)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/MildG2 (26)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/vflip_ModerateG3 (46)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/vflip_ModerateG3 (46)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/vflip_ModerateG3 (46)_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/images/vflip_SevereG4 (197)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test/masks/vflip_SevereG4 (197)_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Knee-X-Ray-Two-Classes/mini_test_output/vflip_SevereG4 (197)_5.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. The 4 Stages of Knee Arthritis: What Your Grade Means (With X-Rays)</b><br>
Dr. Cory Calendine, MD<br>
<a href="https://corycalendinemd.com/blog/knee-arthritis-x-ray-grades/">
https://corycalendinemd.com/blog/knee-arthritis-x-ray-grades/
</a>
<br><br>
<b>2. Automatic knee osteoarthritis severity grading based on X-ray images using a hierarchical classification method</b><br>
Jian Pan, Yuangang Wu, Zhenchao Tang, Kaibo Sun, Mingyang Li, Jiayu Sun, Jiangang Liu, Jie Tian, Bin Shen 
<br>
<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11571664/">https://pmc.ncbi.nlm.nih.gov/articles/PMC11571664/</a>
<br><br>
<b>3. Ensemble deep-learning networks for automated osteoarthritis grading in knee X-ray images</b><br>
Sun-Woo Pi, Byoung-Dai Lee, Mu Sook Lee & Hae Jeong Lee <br>
<a href="https://www.nature.com/articles/s41598-023-50210-4">https://www.nature.com/articles/s41598-023-50210-4</a>
<br><br>
<b>4. TensorFlow-FlexUNet-Image-Segmentation-Knee-X-Ray-Two-Classes-Edge-Detection </b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Knee-X-Ray-Edge-Detection">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Knee-X-Ray-Edge-Detection
</a>
<br><br>
<b>5. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model
</a>
<br><br>
