# Logistic Regression with TensorFlow

- **Recall Linear Regression with TensorFlow before starting**

## What is different between Linear and Logistic Regression?
While Linear Regression is suited for estimating continuous values (e.g estimating house price), it is not the best tool for predicting the class in which an observed data point belongs.  
In order to provide estimate for classification, we need some sort of guidance on what would be the most probable class for that data point. For this, we use Logistic Regression.    

Logistic Regression is a variation on Linear Regression, and is useful when the observed dependent variable (y) is categorical.  
It produces a formula that predicts the probability of the class label as a function of the independent variables.  

Despite the name logistic regression, it is actually a probabilistic classification model. Logistic regression fits a special s-shaped curve by taking the linear regression and transforming the numeric estimate into a probability with the following function:

![equation](http://www.sciweavers.org/upload/Tex2Img_1601222951/render.png)

So, briefly, Logistic Regression passes the input through the logistic/sigmoid function but then treats the result as a probability:

![model_probability_graph](https://public.boxcloud.com/d/1/b1!zF5N-Ee3kDikMZpyfrc6E42JkGUsRvB2yG0uc_4m_J8bWsVuiKb1G7RfwCA58f08USZqABcC1FusxvpaPuZXDrt1TStTtsV47i4FxEjbLNaxCHvczQXw2yYrxda_I82cCq-nYB98Z_9jVTM9cN_ZRzq0Le8OBbomQKHFdkoaajVcnwfHzX3GbPhFST-gFGlZowfbk7d3JwRo69GEbUWuaO42tnvdLKCJcmD9ibb-PoEcll19jucFx5Wx8LPYyC4m0NRBZ8IJZwdfSNqZjiMsX4z4vm9q0nGfKEJW-cCDai5o92DW5DRrdJSVgRkE1Lx-nM-Xm90lL_kLUvfhsZJp5ORrB-yBHM_Ec2JiFiAkHNo1Vq1jFbWgj9lTobYYtcYjpk-YzKf8wtXeagUmhRDZARoE2JEW4DKyZ-CfX3l8JQA9B9hnEVGvZKcq7kPxk0UGKIe9bUgLJh6_fmHkW4FPpJUJv9mvcQOxFEHvS16iwYTaINrQ58bOVWwOSkSmT75OM8H1pDijbyaq0DQJ_DZMJWfRnwZVPknXWGVG55taT_r3uhmNt5y5BrWhP5muTicxLFWEFMbohVkO1vGrEoWK-luscpi6DxyPL8c0_wTqN9345ZX36sEd8IHqz30HQP9hPP0BX7aWLd-xt_S9XkGGisaxh_B2vf22wmMrckHJlczvHVmKNlb6wdPuMSwBzl8bBbyidRTJkHv4pKqyvbG49BlrLOl-Ex_NgGcQdDJ46wz4Sr4kt8JGqhTrTdwr5AelZ7_lOVULs6gUUD_o0gL5hinTgWbgORhi8VGDFNRGlM6WpZ15H-xDy1Vc69IfCqlecg_Qgg97n1bwWa3gp9QOJHMtbuG5omNMWwqDgU74HglfbgvEcLws7fsjFmjFQ25tlBxkBRV7W9tZVdwmAxUqfawVkPULi1MZLzUB7Qbpp597URCoHKVGKt5MeQ6AruRNwCofBxzybNTw8bnZJYpbhHheAifCP1bAYuHBcOdeKeuNJRtUEtgzAg1MHJo070_gOrpyxh-v9RoBRL4bzFMH7U9izseaxES-oKf5AkpKf4ncBmlrfMV2fRoOmLzHLdzd4iwfCyYqqxLqa4ZUUcDXgVs8AC4pgR-6z_keczYMh_WF9hhBOiWGZrPixvecBxZbsQ7E4aRrwO7mOKL-CFRnVuSq33O6Ce4RbDpf1YTsFjJxLbumfy2yMYW3j3JN3JSeJsO5w160TJeo9msV7unXXdMBiyZZHxhpeOBhur_YQYkirNkB3BdK-Ro9u8TIDekMJMwdjneZ9LJ6-KmiYajuvos0zlussL1t8kRxoPhOy7DK6K9Vz1ANSQR0YELetl8PC28S1CyWt67EEJm7M_BsNJSQgwYGkjjoCprMJYTsPrjJkJZpVhDGcXHObvKFTuZcifwLtd7NvnP3f0wwwaqMDy8kt0wgbg../download)

## Dependencies

Packages:

```
pip install pandas
pip install numpy
pip install tensorflow
pip install matplotlib
pip install sklearn
```

Dataset `iris` which is built-in, no need for external download.  
The dataset consists of 50 samples from each of three species of iris (plant).  
In total it has 150 records under five attributes:

- **Petal Length** (Independent)
- **Petal Width** (Independent)
- **Sepal Length** (Independent)
- **Sepal Width** (Independent)
- **Species** (Dependent) (Setosa/Virginica/Versicolor)

## File Structure (in order)

- 0_utilize.py
