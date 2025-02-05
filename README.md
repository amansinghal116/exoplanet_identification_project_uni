# exoplanet_identification_project_uni
## Exoplanet Identification Using Machine Learning

In this project, we used data from the Kepler Space Observatory to distinguish confirmed exoplanets from candidate signals. Our main questions involved how accurately we can classify exoplanets, which features matter most, and whether our results offer deeper insights. We considered several approachesclassical, tree based, ensemble and neural network machine learning models, finding that Gradient Boosting performed best at about 83.6% accuracy. Signal-to-noise ratio and transit duration emerged as key factors in detection. These findings can guide researchers in improving exoplanet surveys and help identify potentially habitable worlds more efficiently.

## Dataset Information
Kaggle, https://www.kaggle.com/datasets/nasa/kepler-exoplanet-search-results

## Introduction

Exoplanets are planets that orbit stars outside our solar system. Scientists use several methods to identify these distant planets. One common technique is the transit method [1], where astronomers observe the slight dimming of a star’s light when an exoplanet passes in front of it. Another method is radial velocity, which detects the subtle wobble of a star caused by the gravitational pull of an orbiting planet. These methods have allowed us to discover thousands of exoplanets, opening up exciting possibilities to discover planets where life could exist.

NASA sent the Kepler Space Telescope into space in 2009 to help Earth telescopes find planets outside our solar system. The telescope could spot planets by noticing changes in light from stars, like when a planet passes in front of its star and makes it dimmer. As more telescopes go up and collect more data, there’s a lot more information to look through and it can be difficult for astronomers to go through a lot of information. Machine learning is important for helping us classify and study exoplanets better. By using information from the Kepler Space Observatory, models can tell the difference between confirmed exoplanets and possible candidates. The dataset from Keplar includes various features about exoplanets. By selecting key features and applying classification models like Logistic Regression, KNN, SVM, Decision Tree, Neural Network, Random Forest, and Gradient Boosting, we can enhance the accuracy of exoplanet identification. Evaluating these models using metrics like accuracy, precision, recall, and F1 score allows us to gain deeper insights into the characteristics of these distant worlds and their potential habitability.

## Database Information

1. KOI Identification- kepid, kepoi name, kepler name- A KOI (Kepler Object of Interest) refers to a target identified by the Kepler Project. It shows at least one transit-like pattern in the data, suggesting it might be a planet.
2. Status- koi disposition- This column indicates the status of an exoplanet candidate, with possible values being CANDIDATE or CONFIRMED. It is also used as the target variable in analyses.
3. Transit Parameters- koi period, koi time, koi impact, koi duration, koi depth, koi prad, koi teq, koi insol - These parameters are derived from fitting a model to the light curves observed by the Kepler telescope. They describe the key characteristics of a planet’s transit across its host star. The main parameters include key characteristics such as Orbital Period, Transit Epoch, Planet-Star Radius Ratio, PlanetStar Distance over Star Radius, and Impact Parameter.
4. ThresholdCrossing Event (TCE) Information- koi model snr, koi tce plnt num, koi tce delivname- The Transiting Planet Search (TPS) module scans data from the Kepler telescope to find signs of planets. It filters out the noise and identifies the most likely planet signals by setting a threshold to minimize false alarms. This way it ensures only the best potential planet signals are kept for consideration.
5. Stellar Parameters- koi steff, koi slogg, koi srad- These parameters include the star’s effective temperature, radius and accelation due to gravity.

