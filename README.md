1. Introduction

	In dermatology, skin lesion classification is the key to differentiating melanoma from nevi and other
	benign lesions using deep learning techniques. This project will therefore zero in on how deep learning
	can be used in automating this classification procedure to better facilitate early detection and improved
	patient outcomes. Unlike variability and complexity of skin conditions in standardized datasets, this makes
	it quite an alluring area of research.

	Datasource:
	https://challenge.isic-archive.com/data/#2018

3. Methods
   
	CNN  VGG19  ResNet  DenseNet

 4. Data Processing and Augmentation

	1. Data Augmentation: We applied a unified data augmentation technique to improve the robustness
	and generalization capability of the models.
	Rotation: Randomly rotating images within a span of 10 degrees.
	Zoom: Applying a random zoom within a range of 0.1.
	Width and Height Shifts: Shifting images horizontally and vertically by up to 10% of the total width
	and height.
	Horizontal Flip: Randomly flipping images horizontally to increase dataset diversity.

	2. Model Parameters: For consistency across models, we standardized the input shape, number of
	classes, batch size, and number of training epochs:
	Input Shape: Resized to 75x100x3 (height, width, and color channels).
	Number of Classes: 7; Batch Size: 16; Epochs: 20

	3. Regularization Techniques: To reduce overfitting, we used dropout and batch normalization across
	all models. These techniques help stabilize training and make models more robust, addressing limitations
	identified in related work.

	4. Training and Evaluation: The augmented dataset was used to train the models, which were then
	linked to the validation and test sets in order to test their performance. This work includes some important
	evaluation metric measures, such as accuracy, confusion matrix, and F1 score; thus, it is able to show a
	full overview for how effective each model will be in classifying skin lesions.

5. results

	CNN: Validation Accuracy: 84%; Test Accuracy: 68%; F1: 66.26%

	VGG19: Validation accuracy: 91.72%; Test accuracy: 74.14%; F1: 74.63%

	ResNet-50: Validation Accuracy: 86.53%; Test Accuracy: 79.10%; F1:78.27%

	DenseNet: Validation accuracy: 81.35%; Test accuracy: 75.40%; F1: 74%
