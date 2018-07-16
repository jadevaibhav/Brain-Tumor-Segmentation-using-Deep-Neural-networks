# Brain-Tumor-Segmentation-using-Deep-Neural-networks
Keras implementation of paper by the same name

I have uploaded the code in FinalCode.ipynb. For explanation of paper and the changes I have done, the information is in there with .pptx file. I would be uploading detailed readme file, until then please refer to this .pptx file.

## Resources
https://arxiv.org/pdf/1505.03540.pdf
(this is sound and complete paper, refer to this and it's references for all questions)

## Modifications
##### Instead of two-way training process as mentioned in paper, I have used weighted-categorical-loss function for which weights are calculated per slice basis.
##### I have used batchnormalization instead of dropout(Keras does not provide implementation for dropout in 2D convs).
##### Batchnorm also smoothens the optimazation curve(refer to https://arxiv.org/pdf/1805.11604.pdf).
##### As per the paper, the loss is defined as cumulative loss of categorization of all patches-per-pixel of the given slice. Instead, I am creating a dataset for such slice and training using mini-batch gradient descent(where it should batch gradient descent in accordance of the paper).
