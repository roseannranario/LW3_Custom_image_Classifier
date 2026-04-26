https://colab.research.google.com/drive/1-p3irsg8MpQUg2GsWuo2qQFpv6mokOqa?usp=sharing

Guide Questions (Student Explanation & Reflection)
Students must answer:
Visualization & Overfitting
   1. What signs indicated overfitting in your first model?
      - The main indication of overfitting in the first model was the substantial difference between the training and validation performance metrics; in particular, the 
        validation loss started to rise rather than fall and the training accuracy increased toward 100% while the validation accuracy plateaued at a much lower level.
        
   2. How did data augmentation affect validation accuracy?
      - By making the model learn more robust and broad properties, including plant textures and shapes, instead than memorizing the precise orientation or lighting of the  
        original training photos, data augmentation increased validation accuracy.

Model Improvement
   3.What is the purpose of dropout layers?
      - By randomly deactivating a portion of neurons during each training session, a dropout layer serves as a regularization tool that keeps the model from becoming
        overly dependent on any one path and promotes the learning of more dependable patterns.
   4. Why does data augmentation improve generalization?
      - By artificially increasing the diversity of the training set, data augmentation enhances generalization by enabling the model to handle variances in real-world 
        settings that were not present in the original dataset, such as varied angles, rotations, and lighting.
        
  
Performance Comparison    
   5. Compare accuracy before and after improvements.
     - Prior to the modifications, the model had a sizable "accuracy gap" in which it performed well on training data but badly on validation data. This gap considerably  
       shrank once dropout and augmentation were included, leading to a more consistent and dependable validation accuracy.
       
   6. Which technique contributed most to improvement?
     - By preventing the model from over-fitting to the particular training samples, data augmentation typically improves picture classification the most, while the  
       performance may vary depending on the particular dataset. Dropout further guarantees the network's resilience.

Deployment & Application
   7. Why is saving the model important?
     - In order to use the model for real-world predictions without having to invest the substantial time and computational resources necessary to retrain it from start,  
       saving the model is essential since it enables you to permanently preserve the learnt patterns and weights.
   8. How can this model be deployed in a real-world system?
     - TensorFlow Lite (TFLite) can be used to run the model directly on mobile devices for offline plant identification, or it can be wrapped in a web API using frameworks 
       like Flask or FastAPI for server-side processing.
