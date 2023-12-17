# A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models

In recent years, recommender systems, pivotal in both commercial and academic spheres, have spotlighted the 'recommendation system for facial skincare.' This automated system advises consumers on tailored facial skincare product choices, considering individual skin types, issues, and preferences. Current models, relying on collaborative or content-based filtering, fall short of addressing user concerns. To overcome this, a hybrid approach integrating KNN, CNN, Transfer Learning of EfficientNet B0, and content-based filtering is proposed. User inputs like skin tone, type, and acne severity guide the algorithm to recommend the most suitable product. Comparative results showcase the superiority of this hybrid model, aiming to offer a more comprehensive and personalized facial skincare solution. With the implementation of EfficientNet B0, the model achieves a validation accuracy of 80% and a training accuracy of 87.10%, promising enhanced precision and efficiency in skincare recommendations.

# Architecture Diagram
![image](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/6971ee9a-4108-43bd-bed7-1687422baecb)

The system architecture diagram is a symbolic representation of the component architecture of the system. It gives a concise description of the component architecture of the system to facilitate component-component connections and system operation.

The diagram shows the architecture of our application where when a user accesses the application their face is captured and based on the model results and additional inputs provided by the user, we predict the products based on their concerns.

Design specifics are related to the application's software engineering perspective. Any application must always take the user interface into consideration. The transparency of a GUI is the key to a satisfied customer. The application's foundation is that it is a web application, making it available practically everywhere. 

# ML Models
The suggested model is used to assess the amount of acne and skin type and tone. Several well-known algorithms, such as K-Means and EfficientNet, in addition to a content-based recommendation model, are included in
the model so that it may provide the desired results. The following models and approaches are broken down into individual modules and discussed in this section.
## Recommendation for Skin Tone
The skin tone can only be obtained by first locating and isolating the pixels that make up the skin, after which the color values must be assigned to the category corresponding to the desired skin tone. The technique of
skin detection consists of three basic operations: initial segmentation, skin pixel prediction, and k-means clustering.

![image](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/c9c3f04f-169f-4d04-a93f-f7ed96e765c9)

The threshold value is used for initial segmentation, which is the average of TOTSU and TMAX. These numbers were obtained from the grayscale image's image histogram.
## Recommendation for Skin Type
The image is analyzed and classified using convolutional neural networks (CNN), dividing face skin types into standard, oily, and dry. With a training accuracy of 87.10% and a validation accuracy of 80%, transfer learning (EfficientNet B0) is being used to increase the model's accuracy, which currently has a training accuracy of 87.10%.

![image](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/e9f51e82-7cda-4b02-aabe-50a0d795effd)

The above table displays the total number of layers included in the EfficientNet-B0 architecture. Images with a resolution of 224 by 224 pixels may be uploaded to the network without issue. The term "MBConv" refers to a depth-wise separable convolution layer with an inverted linear bottleneck. When x is the input picture, f1 through f7 are the layers of the neural network, and y is the output classification label or probability distribution over the classes, the equation that represents the EfficientNet-B0 design is given in the following formula.

$𝑦 = 𝑓7(𝑓6(𝑓5(𝑓4(𝑓3(𝑓2(𝑓1(𝑥)))))))$

## Acne Severity
One of the metrics about the skin is called the acne
concern level, broken down into three levels: Low,
Moderate, and Severe. The model has achieved an accuracy
of 68% across both the training and validation image sets by
using transfer learning in the model's design. This model's
architecture is analogous to the Skin Types CNN model. The
primary EfficientNet-B0 network is constructed around the
MobileNetV2 inverted bottleneck residual blocks in
addition to the squeeze-and-excitation blocks.

## Working of the Proposed Recommender System
The model needs to know the user's skin features to deliver the products corresponding to the top values of similarity (skin vector, product vector) for the items in the dataset that are classified into that particular category. This can be seen in the figure, It would be an intelligent move to search for products with features compatible with the skin measurements and concerns of the consumer. The user's automated cosine similarity between the user skin attribute vector and the product feature vector may be used to convey this likeness.

![image](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/a95ff28c-8e8f-4fd8-aee6-283c5185d89c)

# EXPERIMENTAL RESULTS
Below are six categorized lists of skin tones: Fair skin is described as having 
+ Light eyes and hair, is easily burned, and rarely tans
+ Brown or hazel eyes, light brown hair, and skin that is light to medium in tone with occasional burning but potential for gradual tanning
+ Brown eyes and dark brown hair are complemented by skin that is medium to olive in tone, rarely burns, and tans easily
+ Brown eyes and black hair complement dark brown complexion, which rarely burns and tans quickly
+ Black eyes and black hair complement the deeply pigmented brown complexion, which never burns and tans easily
+ Black skin: Skin that tans readily, never burns, and has black hair and eyes

![Efficient_Net-based_Expert_System_for_Personalized_Facial_Skincare_Recommendations (1)](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/bd53c8a3-3646-4a79-aa31-9cf36b3a0089)

The data training is done using the Python programming language and Tensorflow. Library (number 8) Plotting and other data processing tasks are accomplished using Matlab. Performance of numerous measurements at the exact location while gently moving the sensor head around the region. After that, the model was used to determine the skin type of the individual whose skin was measured.

Convolutional Neural Network (CNN) analysis is used to determine the face skin type, which divides the picture into three categories: standard, oily, and dry. Transfer learning (EfficientNet B0) improves the model's accuracy, which currently has an accuracy of 87.10% compared to a validation accuracy of 80%. The capabilities of EfficientNet are shown in Table II, and they make it an ideal categorization of the skin spectrum that is exact is achievable. To demonstrate that the suggested model is superior to other methods already in use, a comparison is made between it and other methods.

![Efficient_Net-based_Expert_System_for_Personalized_Facial_Skincare_Recommendations (1)](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/60eaa9ca-a701-4580-8ab1-0fb35c863a6d)

One of the metrics about the skin is called the
acne concern level, broken down into three levels: Low,
Moderate, and Severe. Even though the acne severity level
is categorized, it is appropriate to utilize conventionally numeric values for them: 0 - No Acne, 1 - Clear, 2 - almost
clear, 3-Mild, 4-Moderate, and 5-Severe.

![image](https://github.com/vinit714/A-Recommendation-system-for-Facial-Skin-Care-using-Machine-Learning-Models/assets/52816788/4e595c22-c4cd-4b5d-9f96-0626f14d386f)

The figure depicts the breakdown of the total number of images categorized into many groups based on their degree. There is an uneven
distribution of image classes. The acne is mainly of Class 3
Mild kind. Both the training and the testing images have
different severity levels. This effort was complicated
because picture labels from dermatologists were noisy. It
was observed that the training image collection included
numerous identical (or nearly identical) images.


# Keywords
+ Deep Learning
+ Recommendation System
+ Skin Tone
+ Skin Type
+ Acne
+ Transfer Learning
+ EfficicentNet

# Published Paper

This project has been published in an IEEE paper. For more details and in-depth information, please refer to the corresponding paper:

[IEEE Paper Title](https://ieeexplore.ieee.org/document/10142790)

Feel free to explore the paper for a comprehensive understanding of the project and its contributions.

