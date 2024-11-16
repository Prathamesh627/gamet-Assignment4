

| Model name  | Training Time (in sec) | Training Loss | Training Accuracy | Testing Accuracy | Number of model parameters  |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Vgg 1 block | 331.011998  | 0.611857              | 66.25 | 52.5 | 1544834  |
| Vgg 3 block  | 303.972066 | 0.693569 |   50.0 | 50.0 | 4058690 |
| Vgg 3 block with data augmentation  | 276.765719 | 0.693269 | 51.25 | 42.5  | 1698882  |
| Transfer learning vgg 16 all layers  tuned | 306.010839  | 0.694345 | 48.750 | 50.0  | 134268738  |
| Transfer learning vgg 16 MLP layers tuned  | 96.339880 |   0.110353 | 99.375  |  97.5 | 68197186 |
| MLP with model parameters comparable to vgg 16 all layers tuned  |  39.618007 | 0.380756 | 90.625 |    57.5  | 135957634  |

# 2\) Does data augmentation help? Why or why not?

\-\> Yes, data augmentation helps. Data augmentation is a technique to increasethe size of the training data by applying various transformations like rotation, flipping, scaling, etc. This helps the model to learn more features and generalize better on the unseen data. Also data augmentation depends on the type of data and the type of augmentation. In this case, we have only 200 images of each class which is very less and the model will overfit the training data. By applying data augmentation we are increasing the size of the training data and the model will learn more features and generalize better on the unseen data.

# 3\) Does it matter how many epochs you fine tune the model? Why or why not?

Yes,In general training the number of epochs matters. The number of epochs is the number of times the model sees the entire training data. If we train the model for fewer epochs the model will not learn the features properly and the model will underfit the data. If we train the model for more epochs the model will learn the training data very well and the model will overfit the data. The model will perform well on the training data but will not perform well on the unseen data.

\-\> fine-tuning is about adjusting weights, so the same data is just recursively updated, which will mean the size of a fine-tune aught to remain the same regardless of the number of epochs it’s trained for. So it does not matters a much because the model is already pre trained on large dataset. So the model has already learned the features of the images. So we don't need to train the model for more epochs. The model will learn the features of the new dataset in few epochs

# 4\) Are there any particular images that the model is confused about? Why or why not?

Yes, the model is confused about the images which are not clear and the images which are not in the center. Also some of the images comtains humans with main objects and the training data is too small to cover all type of positions of main object with respect to other surrounding objects. Hence the model was not extracted those features very well and confused about those images.

