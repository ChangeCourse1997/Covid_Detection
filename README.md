# Covid_Detection
Using computer vision to detect Covid from chest X-ray images obtained on kaggle https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset

 If your doctor thinks you may have pneumonia, an imaging test may be performed to confirm the diagnosis. One or more of the following tests may be ordered to evaluate for pneumonia: Chest x-ray, CT scan of the lungs, ultrasound of the chest, MRI scan of the chest and needle biopsy of the lung. Identifying covid-19 speicifically from X-ray images alone is extremely difficult.
 
 
 After creating a basic CNN model to perform multiclassification with 3 classes, normal, pnuemonia non-covid and covid, the model had a low accuracy which could be due to several reasons. The dataset is too small and imbalanced, the X-ray images are almost exact making it hard to identify features, further tuning of model parameters are needed. However, creating a model for binary classification yielded much better results where the recall for pnuemonia class was quite high, although this might not be a good thing as false positives might put an unnecessary strain on hospital resources. At the same time a false negative is also detrimental as an infected patient could go on to infect more people unknowingly. Hence, it all depends on the needs of the consumer.
 
 To make a better model, I will create a transfer learning model in the next part to attempt to improve the model.

![X-ray image example](https://github.com/ChangeCourse1997/Covid_Detection/blob/main/IM-0128-0001.jpeg?raw=true)

# Part 2: Transfer Learning 

Using Transfer learning, the model accuracy increased greatly. With ResNet50, the pretrained model has the weights and biases I can use after it has trained on million of images in the image net. The results are summarized below




              precision    recall  f1-score   support

           0       0.83      0.86      0.84       234
           1       0.91      0.89      0.90       390

    accuracy                           0.88       624
   macro avg       0.87      0.88      0.87       624
weighted avg       0.88      0.88      0.88       624

This model, the AutoDoc.h5 could save doctors so much time and contribute greatly to hospitals. This will be extra beneficial to countries struggling with Covid cases like India with 349,691 cases daily as at 24 Apr 2021. With so many cases, doctors need to identify patients with pneumonia and those who have similar symptoms but not infected with pneumonia.

In conclusion, deep learning can be so beneficial and useful not just for businesses, but for the society as a whole. This has been an enjoyable project and displays the power of transfer learning. Thank you for reading!
