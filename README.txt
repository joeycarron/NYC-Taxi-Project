Dataset sources: http://chriswhong.com/open-data/foil_nyc_taxi/
		http://www.andresmh.com/nyctaxitrips/
		http://www.claygervaisgibson.com/nyc-taxi-data/ (explains payment type categories)


NYC Taxi's-Descriptive: Contains overview of dataset and was the first notebook I worked on. I used the
			descriptive stats and outputs to feel my way around and get a bearing for what is going
			on with the data.

NYC Taxi's-Regression Stats: More in-depth analysis of taxi trip features. Correlation plots and matrices.

NYC Taxi's-Time Series: Contains time series plots and descriptive analysis based on dates and times of day.
			High volume on New Years.

NYC Taxi's-Cluster-Denormalized: Dendrogram, PCA, and K-means analysis. Machine learning generates cluster labels,
				and once cluster labels are obtained with normalized data I attach cluster labels
				back onto the original denormalized dataset to more closely analyze each cluster.

NYC Taxis-Cluster: Same as the denormalized cluster notebook, but this is a rough copy that I'm only including
		to show what I did before I realized I should denormalize the data after cluster labels were
		generated. This is meant to be supplementary to show what I did for some preliminary work and
		shouldn't be viewed as one of the polished, commented notebooks.



Here is some feedback from Professor Eytan Adar and GSI Xin Rong that I would use to improve later iterations: 
		"What could have been better:

		- your read of the k-means elbow is a bit off.  you're looking for where the curve starts to level 		off not where it ends.  2 or 3 seems like the right number.  You can see that you only have two 			classes in the end in the PCA plot, 7 of them are empty.

		- some of the time series data would be more usable (less noisy, easier to read/analyze, etc.) 				with binning

		- some of the distributions are not really appropriate for fitting a linear correlation to (e.g., 			the ones that are stratified such as passenger_count versus tip_amount.  Looking at the central 			tendency--mean/median/etc.--of the box-plot and running an anova is the way to do that)

		- report correlations appropriately. The correlation graphs are a bit weird -- we used that in the 		homework to show differences as part of question. But normally correlations should be reported as 			a number (or together with significance level). Pick the right stat and use that.

		- plots with weird distributions that pile into some corner can be made into log-log plots to 				better see the pattern"

	