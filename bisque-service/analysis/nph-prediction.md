# NPH Prediction

## NPH Prediction using 3D UNET

#### Overview

This module is for segmenting a CT scan of a brain into 3 parts: lateral ventricles, cerebral matter, and subarachnoid space using a 3D UNet. A Support Vector Machine is then used to determine if the subject has possible Normal Pressure Hydrocephalus (NPH).

**NPH Prediction Module Homepage**

**How to Run NPH Prediction Module**

### STEP 1. Login

From the [BisQue Homepage](https://bisque.ece.ucsb.edu/), the top right-hand corner has the **Sign In** button.

If you do not have an account, you can create one. If you already have an account, login using your credentials. There is even an option to reset your password just in case you forgot!

### STEP 2. Upload Image(s)

BisQue supports many of the popular medical imaging file formats, i.e. `NIFTI`, `DICOM`. We will cover two of them here.

#### **Upload `NIFTI`**

Once logged in successfully, you will see **Upload** in the top menu bar. Click on **Upload** and feel free to **Drag-and-Drop** files or Select **Choose Files** or **Choose Directory**. Navigate to the `NIFTI` files on your computer and select the ones you want to upload, either individual files or an entire folder/directory.

{% hint style="info" %}
**File Formats**

The supported `NIFTI` file types should end with `.nii` or `.nii.gz`
{% endhint %}

#### Example

```
CT35000.nii.gz
CT36000.nii
YOUR-FILENAME.nii.gz
```

**Upload `DICOM`**

Once logged in successfully, you will see **Upload** in the top menu bar. Click on **Upload** and feel free to **Drag-and-Drop** files or Select **Choose Files** or **Choose Directory**.

{% hint style="warning" %}
**WARNING: DICOM FILES MUST BE ZIPPED!**&#x20;

Before uploading your folder of `DICOM` files, make sure they are compressed/zipped. On Mac, two-finger click on the file and hit **Compress `YOUR-FOLDERNAME`**. This will zip the folder and allow you to upload that single zipped file to BisQue. _We currently do not support uploading the raw directory to BisQue._
{% endhint %}

#### Example

Folder of Raw `DICOM`.

```
IM-0001-0001-0001.dcm
IM-0001-0001-0002.dcm
IM-0002-0001.dcm
IM-0002-0002.dcm
IM-0002-0003.dcm
IM-0002-0004.dcm
IM-0002-0005.dcm
IM-0002-0006.dcm
IM-0002-0007.dcm
IM-0002-0008.dcm
IM-0002-0009.dcm
IM-0002-0010.dcm
IM-0002-0011.dcm
IM-0002-0012.dcm
IM-0002-0013.dcm
[...]
```

Zip the folder containing these files and you are good to go!

Select the option that says **Several DICOM files in a package (unpack and inspect)**. BisQue will correctly parse the `DICOM` files and upload them as dataset if there are multiple images. After its uploaded, you can click on the **Blue Text** to be taken to your uploaded files.

### STEP 3. Go To NPH Prediction Module Homepage

Once you are logged in successfully, you can access the NPH Prediction module by [Clicking Here](https://bisque.ece.ucsb.edu/module\_service/nphprediction/?wpublic=1) or by using the Menu bar at the top of the homepage.

> **From the Menu Bar.** Using the Menu bar at the top of the screen, go to `Analyze --> NPH Prediction`. You might have to scroll down a little bit since we are adding more modules.

### STEP 4. Run NPH Prediction Module

Once on the NPH Prediction homepage,

* `Select an image` you uploaded
* `Select file` from PyTorch Model (Old or Young)
* `Hit RUN!`
