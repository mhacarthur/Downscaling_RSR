# Spatial Downscaling of Remote Sensing and Reanalysis (RSR) 

## Methodology

This methodology is based on the stochastic downscaling method proposed by Zorzetto and Marani (2019 [[1]](#ref1)), which transforms area-averaged precipitation statistics from RSR grid cells into an estimated point-scale precipitation distribution, with particular attention to extremes, and builds on the metastatistical approach to rainfall extremes proposed by Marani and Ignaccolo (2015 [[2]](#ref2))

## Study Area

## Spatial Downscaling Approach

The repository also includes the application of a spatial statistical downscaling method [[3]](#ref3). This approach links precipitation statistics at the satellite grid scale with those at the point scale by exploiting the scaling properties of rainfall fields. In particular, the parameters of the Weibull distribution describing rainfall intensities are translated from the satellite resolution to the point scale through two key functions: the intermittency function, called beta ($\beta$), which accounts for the scaling of the wet fraction, and the variance reduction function, called gamma ($\gamma$), which describes how rainfall variance changes across spatial scales. These parameters are estimated directly from the satellite datasets using high-temporal-resolution rainfall information and the spatial correlation structure of the rainfall field. The resulting point-scale Weibull parameters are then used within the MEVD framework to derive extreme precipitation statistics at the point scale from satellite observations.

The GIF below illustrates a conceptual representation of the procedure applied over the Veneto region to estimate the two key parameters involved in the spatial downscaling process: $\beta$ (intermittency function) and $\gamma$ (variance reduction function). The animation highlights how the methodology is applied independently to each pixel within the study area in order to derive the spatial distribution of these parameters.

<div align="center">
  <img src="https://raw.githubusercontent.com/Downscaling_RSR/refs/heads/main/figures/gif/Veneto_box_beta_gamma_v3.gif" alt="Seasonal_Climatology" />
</div>

## RSR Data

format: netcdf

## Acknowledgements and Code Attribution

The downscaling code in this repository is based on the work of Enrico Zorzetto, available in the [`downpy`](https://github.com/EnricoZorzetto/downpy) repository.

The original code was used as the basis for the downscaling implementation presented here and was updated and adapted to work with more recent software versions and the specific analyses presented in this study.

All other code, data processing procedures, analyses, and scripts contained in this repository were developed by the authors of this study.

The original `downpy` repository is distributed under the MIT License, and the original work of Enrico Zorzetto is acknowledged here accordingly.

Original repository: https://github.com/EnricoZorzetto/downpy

## References

<a id="ref1"></a>[1] Marani M, Ignaccolo M (2015). *A Metastatistical Approach to Rainfall Extremes*. Advances in Water Resources, 79: 121–126. https://doi.org/10.1016/j.advwatres.2015.03.001

<a id="ref2"></a>[2] Zorzetto, E. and Marani, M.: *Downscaling of rainfall extremes from satellite observations*, Water Resources Research, 55, 156–174, 2019. https://doi.org/10.1029/2018WR022950


