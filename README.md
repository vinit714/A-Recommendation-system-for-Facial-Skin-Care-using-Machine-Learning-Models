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


# Keywords
+ Deep Learning
+ Recommendation System
+ Skin Tone
+ Skin Type
+ Acne
+ Transfer Learning
+ EfficicentNet

