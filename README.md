# Exchange Rate Forecasting

### In order to predict the exchange rates between Norway and US for the next 15 days, LSTM and DLinear are utilized for this time series forecasting task.

#### LSTM stands for long short-term memory networks. It is a variety of recurrent neural networks (RNNs) that are capable of learning long-term dependencies, especially in sequence prediction problems. Refer to [https://en.wikipedia.org/wiki/Long_short-term_memory] for more details.
**Results from LSTM**
MSE for ALL:0.014008814. The detailed MSE is shown in the table below.
![image](https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/ca8cda5c-a292-4dfb-a6bb-ffd6247bb879)

The following figure shows the prediction vs the grouth truth for each of the 15 days in the test dataset containing 442 data points.
<img width="1225" alt="Screenshot 2023-08-30 at 13 19 48" src="https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/d2a0cc1f-9e15-40f4-acf4-5da2a469ce6b">
<img width="1231" alt="Screenshot 2023-08-30 at 13 20 32" src="https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/a2b207a1-bcc8-49a7-88b6-cb38a179b161">
<img width="1229" alt="Screenshot 2023-08-30 at 13 21 18" src="https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/626c43f2-7fb5-4dd2-9288-0cf7f2044837">


#### DLinear is a combination of a Decomposition scheme with linear layers. It first decomposes raw data input into a trend component by a moving average kernel and a seasonal component. Then, two one-layer linear layers are applied to each component and are summed up to get the final prediction. It has been proved to be the **BEST** model for long-term exchange rate prediction. Refer to: 
1. Wu, H., Hu, T., Liu, Y., Zhou, H., Wang, J., & Long, M. (2022). Timesnet: Temporal 2d-variation modeling for general time series analysis. arXiv preprint arXiv:2210.02186.
2. Zeng, A., Chen, M., Zhang, L., & Xu, Q. (2023, June). Are transformers effective for time series forecasting? In Proceedings of the AAAI conference on artificial intelligence (Vol. 37, No. 9, pp. 11121-11128).

**Results from DLinear**
MSE for All: 0.013180631. The detailed MSE is shown in the table below.
![image](https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/30392e36-3b0b-4caf-88bc-9a320e071827)

The following figure shows the prediction vs the grouth truth for each of the 15 days in the test dataset containing 442 data points.
<img width="1216" alt="Screenshot 2023-08-30 at 13 22 42" src="https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/2ec25bc7-1e5c-4157-b34d-d2f862741882">
<img width="1217" alt="Screenshot 2023-08-30 at 13 23 17" src="https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/be02eddc-4d58-4ef4-b821-396a0eec4cb1">
<img width="1225" alt="Screenshot 2023-08-30 at 13 23 45" src="https://github.com/EmmaHLU/ExchangeRateForecasting/assets/124171401/db2ce714-bbd2-4156-b84c-17dfab7d7817">



