# strapPy

## Summary

Performs bootstrapping of a dataset column to produce plots and statistics for use in final reports and documents.

The purpose of this package is to simplify and automate the process of creating simple bootstrap distributions of numerical data columns. The package will have a module which intakes a dataset column and relevant parameters such as the desired confidence bounds and number of simulations. The module will perform the simulation statistics to generate the bootstrap mean distribution and relevant statistics such as the sample mean and bootstrapped confidence interval. The package will also contain a module for visualization of the bootstraped confidence interval, and a module for creating a professional publication-ready table of the relevant statistics.

## Package context within the Python ecosystem

The package will likely build on scipy's [stats module](https://docs.scipy.org/doc/scipy/reference/stats.html), which allows one to conduct the boostrap sampling in the first place using the bootstrap method. strapPy will streamline and extend this process from the pure statistical process done in this module. sklearn has a utils module with a [resample](https://scikit-learn.org/stable/modules/generated/sklearn.utils.resample.html) method which also seems popular and achieves similar functionality. While we cannot be certain that one does not exist, there does not seem to be a package which streamlines the process from data to visualization and presentation as proposed in this document. Some tutorials on bootstrap confidence intervals from [machinelearningmastery.com](https://machinelearningmastery.com/calculate-bootstrap-confidence-intervals-machine-learning-results-python/) and [towardsdatascience.com](https://towardsdatascience.com/bootstrapping-using-python-and-r-b112bb4a969e) encourage the reader to plot the results manually.


## Installation

```bash
$ pip install -i https://test.pypi.org/simple/ strappy
```

## Function Usage

- **bootstrap_distribution:** A sampling distribution of `rep` replicates is generated for a specified estimator with replacement for a given bootstrap sample size.  
- **calculate_boot_stats:** Calculates a confidence interval for a given sampling distribution as well as other bootstapped statistics.  
- **histogram_ci_plot:** Makes a histogram of a boostrapped sampling distribution with its confidence interval and oberserved sample statistic.  
- **summary_tabels:** Generates a table that contains a given sampling distribution's mean and standard deviation along with relevant statistics as well as a summary table of the bootstrap distributions parameters  

## Contributing
Julien Gordon, Gautham Pughazhendhi, Zack Tang, and Margot Vore.

## License

`strapPy` was created by Julien Gordon, Gautham Pughazhendhi, Zack Tang, Margot Vore. It is licensed under the terms of the MIT license.

## Credits

`strapPy` was created with [`cookiecutter`](https://cookiecutter.readthedocs.io/en/latest/) and the `py-pkgs-cookiecutter` [template](https://github.com/py-pkgs/py-pkgs-cookiecutter).
