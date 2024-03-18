# sandWind

sandWind is a wind forecasting system for Lake Constance based on artificial intelligence. The system monitors the observations of 189 weather stations in Switzerland and southern Germany and compares the actual weather conditions with the forecasts of numerical weather models. Based on the differences between actual and predicted weather conditions, the system produces corrected forecasts of local wind speeds at Lake Constance for the next 48 hours.

The basis of the model is a deep learning architecture based on LSTM cells. These generate an abstract state of the current weather conditions from the observations of the last 24 hours, which serves as a starting point for the interpretation of the numerical weather forecast models. This makes it possible to correct the wind forecasts at short notice if the general weather situation in Switzerland and southern Germany does not match the forecasts. For Lake Constance, this is particularly relevant in the case of foehn influences, as these are difficult to predict in advance.

In contrast to numerical weather prediction models, which require several hours of computing time on a supercomputer to produce their forecasts, the sandWind system updates its wind forecasts every 10 minutes. This is possible because the computationally intensive learning of the model takes place once before the actual production of the forecasts. The generation of forecasts, on the other hand, requires little computing power and can therefore be carried out every 10 minutes.

The system currently predicts the average, maximum and minimum wind speed as well as the wind direction for Constance in 10-minute increments up to a forecast horizon of 48 hours.
