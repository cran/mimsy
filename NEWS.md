# mimsy 0.6.5

## Bug fixes
* Fixed error on last step of calculating Ar concentrations: Ar signal was multiplied by the calibration factor for mass 28 rather than by the calibration factor for mass 40

# mimsy 0.6.4

## Bug fixes
* Indexing error on L144 that made all o2Sat.conc_uMol.kg calculate based on the first standard temp, not the collection temp of the sample
* Updated column names to correct units (updated to mg L-1 from mg)

# mimsy 0.6.3

## Minor changes
* Added O2 and N2 saturation concentration calculations for all samples
* Removed "bubble correction" script

# mimsy 0.6.2

## Bug fixes
* Bracketing issue, where only results from group 1 are returned, fixed for single-temp and two-temp

# mimsy 0.6.1

## Bug fixes
* Bracketing issue and subsetting issue now fixed (thanks to Libby Mohr! :) )

# mimsy 0.6.0

## Major changes
* Support for single temperature MIMS bath setups added
* Updated Get Started vignetted with clarified directions and downloadable examples

# mimsy 0.5.0

## Major changes
* Concentrations now calculated using dissolved gas ratios for improved accuracy
* Added bubble correction calculation for dissolved oxygen

# mimsy 0.4.3

## Bug fixes
* Mistake in conversion from barometric pressure in units of Torr to units of atmospheres corrected
* Mistake in checking number of standard temperatures corrected

# mimsy 0.4.2

## Minor changes
* Preparation for submission to CRAN
* `README.md` updated with full workflow example
* logo updated

# mimsy 0.4.1

## Major changes
* `mimsy()` takes `data` input as a dataframe, no longer internally loads from file path

## Minor changes
* `vignettes/mimsy.Rmd` rewritten for clarity and screenshots added

# mimsy 0.3.1

## Major changes
* `mimsy()` std.temps pulled from CollectionTemps column of Group
1 Standards, std.temps input argument now depreciated

## Minor changes
* `mimsy()` now indicates the standard temperatures used in 
an output message to the user
* `mimsy()` now checks that the length of std.temps vector
is appropriate

## Bug fixes
* update `mimsy.save()` to rely on non-depreciated forms of 
`openxlsx` functions

# mimsy 0.2.1

## Minor changes
* `vignettes/mimsy.Rmd` now includes directions to save output
as RData file

## Bug fixes
* `vignettes/mimsy.Rmd` and `README.md` install instructions
updated to fix bug where depenencies weren't downloading properly.

# mimsy 0.2.0

## Major changes
* Added `vignettes/mimsy.Rmd` quick start guide for package.
* Added `NEWS.md` file to track changes to the package.
