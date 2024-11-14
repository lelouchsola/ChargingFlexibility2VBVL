# Electric Vehicles as Interoperable Grid Batteries and Wires: Quantifying Spatiotemporal Charging Flexibility for a Net-zero Future

[![DOI](https://zenodo.org/badge/888169921.svg)](https://doi.org/10.5281/zenodo.14158753)

This repository accompanies the paper: 

G. Chen, N. R. Shishvan, Z. Guo, and J. Qin, *"Electric Vehicles as Interoperable Grid Batteries and Wires: Quantifying Spatiotemporal Charging Flexibility for a Net-zero Future."*

### Contact
- Email: chen4911 (at) purdue (dot) edu
- Email: jq (at) purdue (dot) edu

### Overview

The increasing adoption of electric vehicles (EVs) necessitates substantial investments in grid and charging infrastructure. Such costly upgrades can be deferred/offset by leveraging the spatiotemporal flexibility inherently existing in EV charging loads. This study develops a framework to characterize the charging flexibility. It integrates constraints from infrastructure and transportation energy demands to ensure the flexibility is realizable, brings a new spatial dimension to enable a granular characterization, and models this flexibility as virtual batteries and power lines to provide a universal interface that supports various applications. Applying this framework to the Chicago Metropolitan and San Francisco Bay areas, we find that coordinated EV charging can yield substantial flexibility, equivalent to billions of dollars in battery storage and power line investments. Our framework also enables in-depth analysis of diverse infrastructure upgrade plans and EV adoption scenarios, revealing that supporting a growing EV population and fully unlocking the associated charging flexibility require balanced upgrades in grid and charging infrastructure that align with EV travel patterns and penetration levels.

### Citation

Please cite this code as:

G. Chen, N. R. Shishvan, Z. Guo, and J. Qin. (2024). SiobhanPowell/speech-grid-impact: (v1.0.0). Zenodo. doi: 10.5281/zenodo.5789549

---

### Contents

This repository contains three groups of Jupyter Notebooks:

1. **Chicago Metropolitan Area Case**
   - **Chicago2017_1_Parameters**: Calculates parameters for trip chains and charger availability, including weights of trip chains, maximum charging power, cumulative energy demands, and EV locations.
   - **Chicago2017_2_omega_scale_availability**: Solve problem (11) to obtain the EV charging demands that can be supported, denoted by $\omega_j$, under the base case (i.e., the case in Section 3) and different EV hosting capacity scales and public charger availability; Caculate the percentage of supportable charging energy demands (i.e., the results illustrated in Figure 5). 
   - **Chicago2017_2_omega_spatial**: Solve problem (11) to obtain the EV charging demands that can be supported, denoted by $\omega_j$, under different spatial allocations of EV hosting capacity.
   - **Chicago2017_3_aggregateBounds_scale_availability**: Solves problem (4) to determine inner approximation set parameters, including the bounds on charging power and cumulative energy under various EV hosting capacity scales and availabilities.
   - **Chicago2017_3_aggregateBounds_spatial**: Solves problem (4) to determine inner approximation set parameters, including the bounds on charging power and cumulative energy under various spatial allocations of EV hosting capacity.
   - **Chicago2017_4_Specify_VB_VL**: Determines parameters for virtual batteries and power lines based on Eq. (7) and problem (10), generating Figures 6 and 7 for the base case and the analysis in Section 4 and 5.
   - **Chicago2017_geoPlot**: Generates figures for base cases, including Figures 3(a)-(b) and Supplementary Figures 4 and 5.

2. **San Francisco Bay Area Case**
   - **Bay_1_Parameters**: Calculates parameters for trip chains and charger availability, including weights of trip chains, maximum charging power, cumulative energy demands, and EV locations.
   - **Bay_2_omega**: Solve problem (11) to obtain the EV charging demands that can be supported, denoted by $\omega_j$, under the base case.
   - **Bay_3_aggregateBounds**: Solves problem (4) to determine inner approximation set parameters for charging power and cumulative energy in the base case.
   - **Bay_4_Specify_VB_VL**:Determines parameters for virtual batteries and power lines based on Eq. (7) and problem (10) for the base case. 
   - **Bay_geoPlot**: Generates base case figures, including Figures 3(c)-(d) and Supplementary Figures 6 and 7.

3. **Result Comparison of the Two Areas**
   - **plot_AreasCompare**: Compares total parking hours and virtual battery power/energy capacities across counties in both areas, generating Figure 5.

Please run the notebooks in each group sequentially.

---

### Data Source

The sources for real-world datasets are detailed in our paper. Cleaned datasets provided in this repository include:
- **TripChains/Chicago2017_Raw**: Trip chains and weights for the Chicago area.
- **TripChains/California_Raw**: Trip chains and weights for the San Francisco Bay area.
- **geo/capacity_county_ordered.csv**: EV hosting capacity data for the Chicago area.
- **geo_California/LoadCapacity_bay.csv**: EV hosting capacity data for the San Francisco Bay area.
- **Home charging availability**: Embedded within Chicago2017_1_Parameters.ipynb and Bay_1_Parameters.ipynb.

---

### Acknowledgements

This research was supported by the U.S. National Science Foundation under Grant No. ECCS-2339803.
