# Cooperative-Driver-Assistance-System

To obtain the dataset (_2-TBN.csv_) used in the learning *2-TBN* structure, five collision situations were developed using a new version of the simulation framework. The five collision situations used were:

* lead vehicle moving at lower constant speed;
* following vehicle making a lane change maneuver;
* vehicles making (and not making) a lane change maneuver with opposite direction;
* vehicles on two-way road; and
* following vehicle making a lane change maneuver with traffic on the two lanes.

A video showing each of the collision situations can be found in <https://www.youtube.com/watch?v=P_ASXVc7eGI>.

In each of these situations, during _four hours_, fifteen _Ov_ vehicles interact with _Ev_ performing the collision maneuver. Each collision situation is simulated independently. During the simulations of collision situations records are made of the random variables' states determined (_Lane (L), Vehicle direction (Vd) and Location (Lc)_). The records obtained by each simulation were joined in a single file (dataset.csv) at the end of the simulations. Then, in this final file, the states of the random variables _Lane, Vehicle direction and Location_ are used to obtain the states of the hypothesis variable (_Decision_).

The dataset (_dataset.csv_) obtained in the previous stage must be adapted to obtain the dataset (_2-TBN.csv_), used to learn the *2−TBN* structure. Considering Brownlee (<https://machinelearningmastery.com/time-series-forecasting-supervised-learning/>), it is possible to restructure a time series dataset as a supervised learning problem by using the value at the previous time step to predict the value at the next time-step. Furthermore, Brownlee (<https://machinelearningmastery.com/convert-time-series-supervised-learning-problem-python/>), shows how it is possible to do this using python. In this paper, it was considered the sliding window method proposed by Brownlee, with a window width equal to one, taking into account the structure of the *2−TBN* model (two time slides). The datasets created in the previous steps (_dataset.csv_ and _2-TBN.csv_) can be found in this github repository.

  
