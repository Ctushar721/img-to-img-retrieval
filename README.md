#### Image to Image retrieval
A NN model for image-to-image retrieval, which involves finding similar images in a gallery when given a specific image as a query.

#### Baseline Model Implementation

-  **Simple CNN**:
    -   **Architecture**: Start with a basic Convolutional Neural Network (CNN).
    -   **Training**: Train the CNN on the dataset to classify images based on their actions.
    -   **Evaluation**:
        -   Accuracy: 61%
        -   Mean Average Precision (mAP): 52%
        -   Mean Rank: 314

#### Improving the Model with Transfer Learning

-  **ResNet50 [Best mAP]**:
    -   **Architecture**: Use ResNet50, a more advanced and pre-trained CNN architecture.
    -   **Custom Classifier**: Add a custom classifier on top of ResNet50 to fine-tune the model for the specific action classification task.
    -   **Training**: Fine-tune the model on the dataset.
    -   **Evaluation**:
        -   Accuracy: 74%
        -   mAP (K=50): 68%
        -   Mean Rank: 288

#### Implementing a Siamese Network for Similarity Learning

-  **Siamese Network**:
    -   **Architecture**: Design a Siamese Network with two identical subnetworks that share weights.
    -   **Loss Function**: Use a contrastive loss function to train the model to distinguish between similar and dissimilar image pairs.
    -   **Distance Metric**: Employ Euclidean distance to measure the similarity between image embeddings.
    -   **Training**:
        -   Create positive pairs (similar images) and negative pairs (dissimilar images) from the dataset.
        -   Experiment with different ratios of positive to negative pairs to find the optimal balance for training.
