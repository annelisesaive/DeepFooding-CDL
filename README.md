# DeepFooding

## A software for automatic labeling of human eating behaviors

### The two main goals of the project

(1) Precisely and robustly track movements and actions using video-recordings of dining experiences using pre-trained deep-learning algorithms. The whole pipeline will be developed using the [DeepLabCut software package](https://github.com/annelisesaive/DeepLabCut). More info, demos and ressources detailed below.

(2) Create robust labeling of key eating behaviors based on resulting tracking spatial coordinates (e.g., bite, sip etc.). The labelling results will then be compared with the labels of two datasets manually coded by experts.

### Step 1: Discover the DeepLabCut package in depth

To get familiar with DeepLabCut, I recommend
(1) reading the scientific papers describing the protocol and the incentives of the toolbox especially the [Nature Protocol paper](https://www.nature.com/articles/s41596-019-0176-0). You can find all relevant papers (starting with "0_") in the papers directory
(2) checking out the documentation page of the package [here](https://deeplabcut.github.io/DeepLabCut/docs/intro.html) and the quick [video](https://www.youtube.com/watch?v=A9qZidI7tL8) detailing how to navigate the docs
(3) following the [Course](https://github.com/DeepLabCut/DeepLabCut-Workshop-Materials/blob/master/DLCcourse.md) about the science of DeepLabCut and how to use it. Consider having a look at the DEMO JupyterNotebooks.

### Step 2: Getting started with the Living Lab dataset

**Label you data** - It is now time to use the videos from this project. Pick diverse videos (background, people, colors etc.), create a DLC project and start labeling what you want to track (e.g., fork, knife, glass, facial expressions, hands etc.). You can use the Project Manager GUI or iPyhton (more functions here). You can find all relevant ressources [here](https://github.com/DeepLabCut/DeepLabCut-Workshop-Materials/blob/master/DLCcourse.md#module-1-getting-started-on-data)

**Train and evaluate your model** - Once you label on your laptop, if you want to train on your CPU, you can use and edit as you need the [JupyterNotebook](https://github.com/annelisesaive/DeepFooding-CDL/blob/main/Test_dplc_LivLab.ipynb) in this repo. If you want to use GPUs on the cloud, please upload your project folder to google drive. You can then use this [COLAB NOTEBOOK](https://github.com/DeepLabCut/DeepLabCut/blob/master/examples/COLAB_YOURDATA_TrainNetwork_VideoAnalysis.ipynb) to create a training set, train, and start evaluating. More information for this step can be found [here](https://github.com/DeepLabCut/DeepLabCut-Workshop-Materials/blob/master/DLCcourse.md#module-2-neural-networks)

At this stage, you need to document tracking performance across pretrained networks and data augmentation techniques in a controlled way (watch this [video](https://www.youtube.com/watch?v=WXCVr6xAcCA) for help). You can find more information about what network you should use and why [here](https://github.com/AlexEMG/DeepLabCut/wiki/What-neural-network-should-I-use%3F). Complementary ressources are available [here](https://github.com/DeepLabCut/DeepLabCut-Workshop-Materials/blob/master/DLCcourse.md#module-3-evalution-of-network-performance).

### Step 3: Scaling your analysis to many new videos

**Document and scale your analysis pipeline** Once you have established your analysis pipeline for the specific labels we have targeted together, an important step is to be able to (1) document these choices for future projects, and (2) implement a way to automate your analysis (more info [here](https://github.com/DeepLabCut/DeepLabCut-Workshop-Materials/blob/master/DLCcourse.md#module-4-scaling-your-analysis-to-many-new-videos))

### Step 4: Making sense of poses estimation

The last but not least step is to **make sense of the tracking data** you have estimated so far. For example, you can start by trying to identify when a person takes a bite or a sip during their meal based on the positions of their mouth, glass and cutlery and calculating their distances over time. You can then establish distance thresholds (e.g., a distance < 1cm) that will allow you to automatically code the beginning and end of each bite or sip taken during a meal.

A [rich set of tools](https://github.com/DeepLabCut/DLCutils) already exists and can help you create your own custom analysis. Check out more [here](https://github.com/DeepLabCut/DeepLabCut-Workshop-Materials/blob/master/DLCcourse.md#module-5-got-poses-now-what-)

A compilation of relevant scientific papers can also be found in the "scientific_papers" directory (all papers starting with "1_")

### Github and Git ressources

Here are ressources to help you [setup Git and Atom](https://courses.cs.washington.edu/courses/cse154/19su/resources/assets/atomgit/windows/) and to help you [manage Git and Github](https://www.youtube.com/watch?v=RGOj5yH7evk) for the current project
