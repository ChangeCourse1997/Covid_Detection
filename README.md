# Covid_Detection
Using computer vision to detect Covid from chest X-ray images obtained on kaggle https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset

 If your doctor thinks you may have pneumonia, an imaging test may be performed to confirm the diagnosis. One or more of the following tests may be ordered to evaluate for pneumonia: Chest x-ray, CT scan of the lungs, ultrasound of the chest, MRI scan of the chest and needle biopsy of the lung. Identifying covid-19 speicifically from X-ray images alone is extremely difficult.
 
 
 After creating a basic CNN model to perform multiclassification with 3 classes, normal, pnuemonia non-covid and covid, the model had a low accuracy which could be due to several reasons. The dataset is too small and imbalanced, the X-ray images are almost exact making it hard to identify features, further tuning of model parameters are needed. However, creating a model for binary classification yielded much better results where the recall for pnuemonia class was quite high, although this might not be a good thing as false positives might put an unnecessary strain on hospital resources. At the same time a false negative is also detrimental as an infected patient could go on to infect more people unknowingly. Hence, it all depends on the needs of the consumer.
 
 To make a better model, I will create a transfer learning model in the next part to attempt to improve the model.
