# Stratification
Case about stratification sampling

This case is about stratification sampling when the amount of each stratum in the sample is different from the amount in the general population.
File download_data.ipynb consists of functions for general data sets general population with 1 mln users and sample with 10k users.
File stratification.ipynb consists realization of stratification sampling that includes several steps:
1) generating data frame of the general population with columns ['user_id', 'country', 'device', 'partner_id', 'view']
2) generating data frame of the sample with the same columns but with different stats, for instance, it has more users from country 'ZW' etc.
3) choose columns that will use as strata, in my example country and device
4) computing weights for each stratum in the general population
5) use these weights for stratification sampling from the sample dataset with the conditions:
    If amounts of users in stratum in the sample dataset are less than what needs to be, so I use replace=True the function get_stats_sample
    Stratums (columns) must be the same in general and sample populations
    The stats were not randomized, because I didn't consider changing metrics in this case
