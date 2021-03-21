# Face-Mask-Recognition-using-Deep-Learning

In these tough times during the COVID-19 pandemic, wearing masks has become at most important to protect ourselves from the infection and also to prevent spreading of the virus.

I have worked on this interesting problem statement as a part of selection process for an internship. The experience of learning was totally amazing.

### 1) Dataset preparation:

* Collected the dataset from various sources available online like Kaggle, Github etc.
* Shot video of myself with different variations in my positions, background, without wearing mask, with wearing mask, different angles etc and extracted the frames in the video as images and added to the dataset.
* The dataset had 2 different folders for 2 separate classes, i.e; with_mask & without_mask.

### 2) Data Preprocessing & Forming DataMatrix:

* To create labels for the images, extracted the file name as class name and stored in the list.
* The images were resized to required size (here 200 * 200), converted into array form, and then stored in the list.
* Both the labels and datamatrix were converted into numpy arrays and used for further purposes.

### 3) Model Architecture:

* I used the pre-trained model, MobileNetV2, which is trained on a large dataset called 'ImageNet' which has more than 3 million images in it. This model works exceptionally well on any kind of image related problem statements. It is also less time complex, requires very less number of parameters for predicting.
* The head of model was removed and customized for my requirements. I added layers on top of that and froze the parameters in the MobileNetV2 model from getting trained.
* Checkpoint was added to just store best scoring model. Here it monitored over 'val_loss'.

### 4) Training and Evaluating:

* The data matrix & labels are now divided into 70% train, 20% validation, 10% test datasets.
* The model was trained on Train dataset, and evaluated on validation dataset. Accuracy was the metric which was looked upon. I could achieve around 95.42% accuracy on validation dataset.

### 5) Improvements:

* We can extend this work for real-time face maks recognition which has many more variations and constraints.
* Build more sophisticated model architectures.
* I analysed only pictures with only one person in it, we can train on dectecting many people in the picture.

## Thank You!
### Any kind of feedback is much appreciated.

For Code credits, I don't remember which articles I referred.
