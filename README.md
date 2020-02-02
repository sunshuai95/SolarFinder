# SolarFinder: Automatic Detection of Solar Photovoltaic Arrays.

Power generation from distributed rooftop solar photovoltaic arrays has grown rapidly in recent years due to the rapid decline in solar module prices. Smart cities and utilities are having pressure on managing this stochastic green energy, such as accurately predicting solar generation capacity and react to the variations in the electric grid. Recently, there is a rising interest in automatically collecting solar installation information that are necessary to manage this stochastic green energy among utilities, third-parties, and government agencies. Given a geospatial region, these information may include the quantity and locations of solar deployments within the region, and also the profiling information for each deployment such as orientation, size, inverter inefficiency, etc. Traditional approaches such as online assessment and utilities interconnection filings are time consuming and costly, and also limited in geospatial resolution and thus do not scale up to every location. Significant recent work focuses on using aerial imagery to train machine learning or deep learning models to automatically detect solar arrays. Unfortunately, these approaches all require training data that includes Very High Resolution (VHR) images and human handcrafted image templates, which have a minimum cost of $15 per km^2 and are not always available at every location.

To address the problem, we design a new approach --- SolarFinder that can automatically detect distributed solar photovoltaic arrays in a given geospatial region without any extra cost. SolarFinder first automatically fetches low or regular resolution satellite images within the region using publicly-available maps APIs. Then, SolarFinder leverages multi-dimensional K-means algorithm to automatically segment a hybrid linear regression approach that integrates support vectors machine (SVM) (with RBF kernel) modeling with a deep convolutional neural network (CNN) approach to accurately identify rooftop solar arrays and also learn the detailed installation information for each solar array simultaneously. We evaluate SolarFinder using 41,683 public satellite images that include 180,833 contours from 11 geospatial regions in the U.S. We find that pre-trained (or unsupervised) SolarFinder yields a MCC of 0.17, which is 3 times better than the most recent pre-trained CNN approach and is the same as a supervised CNN approach. Thus, SolarFinder achieves similar accuracy without access to any training data from testing sites as a fully supervised approach with complete access to such training data.
