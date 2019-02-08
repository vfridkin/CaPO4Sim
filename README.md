# CaPO4Sim, the virtual physiology simulator
[![Travis build status](https://travis-ci.com/DivadNojnarg/CaPO4Sim.svg?token=wk4LByQczpy1WzofyA7q&branch=master)](https://travis-ci.com/DivadNojnarg/CaPO4Sim)
[![CRAN status](https://www.r-pkg.org/badges/version/CaPO4Sim)](https://cran.r-project.org/package=CaPO4Sim)


>Repository of NCCR project containing shiny apps of Calcium Phosphate homeostasis

### **Staff** ###
+ *Project manager*: [Dr. Diane de Zélicourt and Prof. Vartan Kurtcuoglu](http://interfacegroup.ch/people/)
+ *Experts in Physiology*: 
  - [Prof. François Verrey](https://www.physiol.uzh.ch/en/research/institutegroups/EpithelialTransports/TeamMembers/FVerrey.html),
  - [Prof. Olivier Bonny](https://www.unil.ch/dpt/fr/home/menuinst/recherche/groupe-bonny.html),
  - [Prof. Bernard Rossier](https://hset.org/organization/team/),
  - [Prof. Carsten Wagner](https://www.physiol.uzh.ch/en/research/institutegroups/Acidbasetransport/Grwagner/CWagner.html)
+ *Graphic designer*: [Tara von Grebel](https://www.uzh.ch/id/cl/iframe/org/index.php?id=tg)
+ *Animation*: [Janine Meyer](https://www.uzh.ch/id/cl/iframe/org/index.php?id=jnm)
+ *Model developer*: [Dr. David Granjon](https://divadnojnarg.github.io)
+ *Web/R developer*: Dr. David Granjon
+ *Server management*: Dr. David Granjon
+ *Server expert*: [Dr. Sergio Maffioletti](https://www.id.uzh.ch/en/scienceit/about/team.html)
+ *Consultants*: [Dr. Nathalie Debard](https://hset.org/organization/team/)

### **Aknowledgments** ###

![Figure 1-1](man/figures/about_us.jpg)


I am also very grateful to the [Shiny](http://shiny.rstudio.com) developers 
and [RStudio](https://www.rstudio.com) team, who provide a lot of useful softwares
and packages. 

I finally thanks: Dean Attali ([shinyjs](https://deanattali.com/shinyjs/)), 
Karline Soetaert and Thomas Petzoldt ([deSolve](http://desolve.r-forge.r-project.org)),
Carson Sievert ([plotly](https://plot.ly/r/)), 
the datastorm team ([visNetwork](http://datastorm-open.github.io/visNetwork/)),
the dream R team, especially Victor Perrier ([shinyWidgets](https://dreamrs.github.io/shinyWidgets/index.html)),
Hadley Wickham and the Tidyverse team ([purrr and stringr](https://www.tidyverse.org/packages/)),
Eric Bailey ([shinyMenus and shinyBS](https://github.com/ebailey78)),
Andrew Sali ([shinycssloaders](https://github.com/andrewsali/shinycssloaders)),
Yang Tang ([shinyjqui](https://cran.r-project.org/web/packages/shinyjqui/vignettes/introduction.html)),
Ian Lyttle ([bsplus](http://ijlyttle.github.io/bsplus/)),
Kent Russell ([sweetalertR](http://timelyportfolio.github.io/buildingwidgets/week25/sweetalert_examples.html)),
Carl Ganz and Afshin Mehrabani ([rintrojs](https://carlganz.github.io/rintrojs/)),
Andy Merlino ([shinyFeedback](https://cran.r-project.org/web/packages/shinyFeedback/vignettes/shinyFeedback-intro.html))


```R
library(shiny)
library(ygdashboard)
require(visNetwork)
library(shinyBS)
library(dplyr)
library(plotly)
library(deSolve)
library(shinythemes)
library(shinyjs)
library(shinycssloaders)
library(shinyWidgets)
library(shinyjqui)
library(bsplus)
library(sweetalertR)
library(shinytoastr)
library(shinyMenus)
library(stringr)
library(purrr)
library(rintrojs)
library(shinyFeedback)
library(magrittr)
library(DT)
```

### **Contacts** ###

*david.granjon_at_uzh.ch*

# **To do** list

## General

- set a load balancer (Ready to be done).
- <del>set authentication</del> (DONE).
- <del>use a compiled model instead of only deSolve core<del> (DONE).
- <del>write "about" section for the staff</del> (DONE).
- <del>update the main website</del> (DONE).
- <del>refine video tutorials</del> (DONE).
- <del>make animations on visnetwork (blinking,...)</del> (DONE).


## Global App

- improve the navigation between detailed zoom in the main app
- <del>find another place to put the active slider(s), maybe in the navbar
so that they are always visible</del> (DONE)
- <del>table of modified parameters to remind the user what is changed or not.</del> (DONE)
- the size of the box should scale each screen (and file the whole half page, 
which is not the case now)
- <del>decrease navbar height</del> (DONE)
- <del>improve help navigation</del> (DONE)
- <del>adjust the human background</del> (DONE)

## Case studies App

- check plot scaling when screen size is reduced
- the size of the box should scale each screen (and file the whole half page, 
which is not the case now)
- <del>adjust the human background</del> (DONE)
- <del>slider cursor on 1 by default for each simulation (need to set a reset)</del> (DONE)
- <del>find a way to better user graphs</del> (DONE)
- <del>include detailed zoom?</del> (DONE)
- <del>improve help navigation</del> (DONE)
- change title "steady-state" and "dynamics" simulations (too computational)
- use "explanations"" instead of "notifications"

## Treatments studies App
- <del>update the core to compiled code</del>
- allow simultaneous treatments
