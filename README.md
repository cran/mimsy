# mimsy <img src="man/figures/logo.png" align = "right" width = "200" />

[![Travis CI Build Status](https://travis-ci.com/michelleckelly/mimsy.svg?branch=master)](https://travis-ci.com/michelleckelly/mimsy)
[![Lifecycle: maturing](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)

"Calculate MIMS dissolved gas concentrations without getting a headache."  

`mimsy` is a data analysis package that transforms raw MIMS (Membrane Inlet Mass Spectrometer) signal data into dissolved gas concentration readings using standard solubility equations. `mimsy` is designed to be simple and accessible for non-R users.  

Click on the **Get started** tab above to read through the detailed how-to guide. 

### Crunch data in 5 lines of code or less
```R
# Load data into R
data <- read.csv(file = "data.csv", header = TRUE, stringsAsFactors = FALSE)

# Run the mimsy function
results <- mimsy(data, baromet.press = 977.2, units = "hPa")

# Save the results
mimsy.save(results, file = "results.xlsx") # To Excel file
save(results, file = "results.RData") # To RData file

# Done! :)
```

### Installation instructions 

```R
# Pull package from github using devtools
library(devtools)
install_github("michelleckelly/mimsy", dependencies = "Depends")

# Load package into your R environment
library(mimsy)
```

### Recommended citation

To see the recommended citation for this package, run `citation("mimsy")` in the R console:
```R
citation("mimsy")
```

### Disclaimer
`mimsy` holds no official endorsement from the Bay Instruments company. This software is preliminary and subject to revision. By the use of this software, the user assumes their own responsibility for ensuring the accuracy of the program. 

### References
Garcia, H., and L. Gordon (1992), _Oxygen solubility in seawater: Better fitting
equations._ Limnology and Oceanography, 37(6). https://doi.org/10.4319/lo.1992.37.6.1307

Benson, B. B. & Krause, D. (1984). _The concentration and isotopic
fractionation of oxygen dissolved in freshwater and seawater in equilibrium
with the atmosphere._ Limnology and Oceanography, 29(3), 620-632.
https://doi.org/10.4319/lo.1984.29.3.0620

Stull, D. R. (1947). _Vapor Pressure of Pure Substances. Organic and
Inorganic Compounds._ Industrial & Engineering Chemistry, 39(4), 517-540.
https://doi.org/10.1021/ie50448a022

Hamme, R. C. & Emerson, S. R. (2004). _The solubility of neon, nitrogen and argon
in distilled water and seawater._ Deep-Sea Research I, 51(11), 1517-1528. 
https://doi.org/10.1016/j.dsr.2004.06.009