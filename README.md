*******************************************************************************
*******************************************************************************

	1) Trainer

		Reads given train data and trains it with BOWKMeansTrainer and 
		extracts  descriptors  with BOWImgDescriptorExtractor. As soon 
		as training is done, application will save the state to a file.
	
	2) Classifier
		
		While  classifying first  image,  the application will load the 
		saved BOWKMeansTrainer and BOWImgDescriptorExtractor. This step
		needs to be executed only once.  Application  immediately tries
		to classify given image and write the prediction. 

-------------------------------------------------------------------------------

OpenCV's features extractor, descriptors and classifiers used: 

  FlannBased DescriptorMatcher and  SURF DescriptorExtractor were used in
  BOWImgDescriptorExtractor, in order to perform "BagOfWords" based image 
  classification.

  SURF FeatureDetector was also used to detect features. 

  Train images were described with BOWImgDescriptorExtractor and trained with 
  BOWKMeansTrainer.

  At the end NormalBayesClassifier was trained, in order to be able to predict
  classes of given images. 

*******************************************************************************
*******************************************************************************
