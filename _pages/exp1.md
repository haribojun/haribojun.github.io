---  
title: "Experience"
permalink: /exp1/
layout: single
classes: wide
author_profile: true
header:
  overlay_image: /assets/images/background.jpg
  overlay_filter: 0.5
---
  

# Increasing Accuracy of Stock Price Pattern Prediction through Data Augmentation for Deep Learning

![Image](https://haribojun.github.io/assets/images/exp_1.png){: .align-center}


---
  
As Artificial Intelligence (AI) technology develops, it is applied to various fields such as image, voice, and text. AI has shown fine results in certain areas. Researchers have tried to predict the stock market by utilizing artificial intelligence as well. Predicting the stock market is known as one of the difficult problems since the stock market is affected by various factors such as economy and politics. In the field of AI, there are attempts to predict the ups and downs of stock price by studying stock price patterns using various machine learning techniques. This study suggest a way of predicting stock price patterns based on the Convolutional Neural Network(CNN) among machine learning techniques. CNN uses neural networks to classify images by extracting features from images through convolutional layers. Therefore, this study tries to classify candlestick images made by stock data in order to predict patterns. 

This study has two objectives. The first one referred as Case 1 is to predict the patterns with the images made by the same-day stock price data. The second one referred as Case 2 is to predict the next day stock price patterns with the images produced by the daily stock price data. 
- In Case 1, data augmentation methods - random modification and Gaussian noise - are applied to generate more training data, and the generated images are put into the model to fit. Given that deep learning requires a large amount of data, this study suggests a method of data augmentation for candlestick images. Also, this study compares the accuracies of the images with Gaussian noise and different classification problems. All data in this study is collected through OpenAPI provided by DaiShin Securities. Case 1 has five different labels depending on patterns. The patterns are up with up closing, up with down closing, down with up closing, down with down closing, and staying. The images in Case 1 are created by removing the last candle(-1candle), the last two candles(- 2candles), and the last three candles(-3candles) from 60 minutes, 30 minutes, 10 minutes, and 5 minutes candle charts. 60 minutes candle chart means one candle in the image has 60 minutes of information containing an open price, high price, low price, close price. Case 2 has two labels that are up and down. 
- This study for Case 2 has generated for 60 minutes, 30 minutes, 10 minutes, and 5minutes candle charts without removing any candle. Considering the stock data, moving the candles in the images is suggested, instead of existing data augmentation techniques. How much the candles are moved is defined as the modified value. The average difference of closing prices between candles was 0.0029. Therefore, in this study, 0.003, 0.002, 0.001, 0.00025 are used for the modified value. The number of images was doubled after data augmentation. We used Gaussian Noise, with the mean value 0, and the value of variance 0.01. For both Case 1 and Case 2, the model is based on VGG-Net16 that has 16 layers. As a result, 10 minutes -1candle showed the best accuracy among 60 minutes, 30 minutes, 10 minutes, 5minutes candle charts. Thus, 10 minutes images were utilized for the rest of the experiment in Case 1. The three candles removed from the images were selected for data augmentation and application of Gaussian noise. 10 minutes -3candle resulted in 79.72% accuracy. The accuracy of the images with 0.00025 modified value and 100% changed candles was 79.92%. Applying Gaussian noise helped the accuracy to be 80.98%. According to the outcomes of Case 2, 60minutes candle charts could predict patterns of tomorrow by 82.60%. 

To sum up, this study is expected to contribute to further studies on the prediction of stock price patterns using images. This research provides a possible method for data augmentation of stock data.

---

- Youngjun Kim, Yeojeong Kim, Insun Lee, Hong Joo Lee "Increasing Accuracy of Stock Price Pattern Prediction through Data Augmentation for Deep Learning" Journal of Korea Bigdata Society, 4(2), 1-12.

- Korea Intelligent Information Systems Society 19.06.01
  - "Predicting Patterns of Stock Prices Based On Deep Learning"

---
![Image](https://haribojun.github.io/assets/images/exp_1-2.png){: .align-center }



