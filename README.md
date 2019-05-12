![experimental](https://img.shields.io/badge/stability-experimental-orange.svg)

# drakeplanner

This R/Shiny app is a companion to the [`drake`](https://github.com/ropensci/drake) R package. It helps new users learn [`drake`](https://github.com/ropensci/drake), and it helps new and experienced users set up new [`drake`](https://github.com/ropensci/drake)-powered projects. Simply provide a [`drake` plan](https://ropenscilabs.github.io/drake-manual/plans.html), and `drakeplanner` will show you the end-to-end dependency graph of your workflow and produce a downloadable R script to get your project started.

# Access

This app is available online at [https://wlandau.shinyapps.io/drakeplanner](https://wlandau.shinyapps.io/drakeplanner). If you cannot access it, you can install it locally in an R session.

```r
install.packages("remotes")
remotes::install_github("wlandau/drakeplanner")
```

Then run it on your own machine.

```r
drakeplanner::drakeplanner()
```

# Usage

1. Navigate to the `Plan` view (left sidebar).
2. Write your [`drake` plan](https://ropenscilabs.github.io/drake-manual/plans.html) in the `Plan` box. The code must return a valid `drake` plan at the end, ideally with a call to the [`drake_plan()`](https://ropensci.github.io/drake/reference/drake_plan.html) function.
3. Write your [custom functions](https://ropenscilabs.github.io/drake-manual/plans.html) in the `Functions` box.
4. Click `Update` button in the `Control` box.
5. Optional: click the `Download` button in the `Control` box to save your workflow as an R script.

# Tips

- Large plans may take time to render. If you encounter slowness, consider setting the `max_expand` argument of [`drake_plan()`](https://ropensci.github.io/drake/reference/drake_plan.html) to a small number. See [this section of the manual](https://ropenscilabs.github.io/drake-manual/plans.html#start-small) for a demonstration.
