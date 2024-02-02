# Fashion Recommender MNIST
Fashion classification and recommender system based on [Fashion MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist) and [Param Aggrawal's Fashion Product Images](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-small) dataset. The model was trained using 84000 images across 9 different classes (t-shirts, trousers, sweaters, shoes, etc), with [EfficientNet v2](https://keras.io/api/applications/efficientnet_v2/) B3 as the base model.

![Class Distribution](_docs/screenshot/class_distrib.svg)

## Result
- The classification model can reach > 92% accuracy (with balanced class weight) when using images from both datasets, but can only reach about 72% accuracy when using only Aggrawal's dataset. It seems that using greyscale images and canny filter (along with more samples) will improve the accuracy greatly. See input image examples below.

    <details>
        <summary>Input Images (After Augmentation)</summary>
        <img src="_docs/screenshot/preproc.svg">
    </details>

- The recommender system result (from global pooling layer) can be seen from the images below (using 3 different distance similarity metrics).

    <details>
        <summary>Recommendations using Cosine</summary>
        <img src="_docs/screenshot/rec_cosine.svg">
    </details>
    <details>
        <summary>Recommendations using Euclidean</summary>
        <img src="_docs/screenshot/rec_euclidean.svg">
    </details>
    <details>
        <summary>Recommendations using Manhattan</summary>
        <img src="_docs/screenshot/rec_manhattan.svg">
    </details>

## Similar Datasets
Datasets that are similar but not used due to the large size:
- [H&M Personalized Fashion Recommendations](https://www.kaggle.com/c/h-and-m-personalized-fashion-recommendations)
- [Fashion Product Images Dataset](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset) (bigger, more samples)