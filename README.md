# resume
---
title: "Bo Olson"
author: Bo Olson
output: 
  pagedown::html_resume:
    css: ['resume_css.css', 'resume']
#knit: pagedown::chrome_print
editor_options: 
  chunk_output_type: console
---

```{r global options, include = FALSE}
knitr::opts_chunk$set (echo = FALSE, warning = FALSE, message = FALSE, dev.args=list(bg="transparent"))
```

```{r libraries used }
library(pagedown)
library(tidyverse)
library(ggridges)
library(wesanderson)
library(viridis)
```


<div class = "densityplot">

```{r fun density plot, fig.height=.5, fig.width=2, fig.align='right'}
wes <- wesanderson::wes_palette("Royal1", type = "continuous", n=12)
data <- data_frame(label = 1, density = c(rnorm(100, mean = 7))) %>% 
          union(data_frame(label = 5, density = c(rnorm(100, mean = 6)))) %>% 
          union(data_frame(label = 6, density = c(rnorm(100, mean = 5)))) %>% 
          union(data_frame(label = 7, density = c(rnorm(100, mean = 4)))) %>% 
          union(data_frame(label = 8, density = c(rnorm(100, mean = 3)))) %>% 
          union(data_frame(label = 9, density = c(rnorm(100, mean = 2)))) 
data %>% ggplot(aes(x =density, y = as.factor(label), fill = factor(label))) + 
                  geom_density_ridges(scale = 2, height =.5, color = "#D5DCBC") + 
                      scale_fill_manual(values = wes)+
                      theme_void()+
                      theme(legend.position = "none",
                            panel.background = element_rect(fill = "transparent", color = NA))
```

</div>

::: aside

Contact {#contact}
--------------------------------------

<i class="fa fa-envelope"></i> bo.olson@gmail.com

<i class="fa fa-phone"></i> 847.224.4208

<i class="fa fa-linkedin"></i> <a href="https://linkedin.com/in/OlsonBo">linkedin.com/in/OlsonBo</a>

<!-- hope you like my joke -->

<i class="fa fa-map-marker-alt"></i> <a href="https://www.seattletimes.com/seattle-news/flying-fish-fries-power-for-dozens-of-seattle-city-light-customers/" target="_blank">Seattle, WA</a>

<i>View html with links at my github: 

https://github.com/bo-olson/cv/ </i>


Technical Skills {#skills}
---------------------------------------

```{r skill plot, fig.height=15, fig.width=10}
skill<-c("R", "SQL", "Azure Platform & ETL", "Databricks & Spark", "Python", "Data Visualization (ggplot / PowerBI)", "HTML & CSS")
level<-c(10,10,10,7,6,10,5)
wes <- wesanderson::wes_palette("Royal1", type = "continuous", n=6)
skills <- data_frame(skill = skill,
                     level = level)
skills %>% ggplot(aes(reorder(skill, level), level)) + 
              geom_col(aes(fill = wes[[2]])) + 
                coord_flip() +
                  scale_fill_manual(values = wes[[2]]) +
                    theme_void() +
                      theme(
                        legend.position = "none",
                        panel.border = element_blank(),
                        panel.background = element_rect(fill = "transparent", color = NA)
                          ) +
              geom_text(aes(skill, 0, label=skill, group = skill),
                        nudge_y = .25,
                        hjust = 0,
                        family = "Gill Sans",
                        size = 14,
                        color = "white")
```



Interests
---------------------------------------

Avid fly fisher, outdoor wanderer, dog walker, whitewater rower, guitar picker, and poem reader.



Disclaimer
---------------------------------------

Built using the awesome <a href="https://github.com/rstudio/pagedown#resume-pagedownhtml_resume">pagedown</a> package

See the source code on my <a href="https://github.com/bo-olson/cv/">github</a>


:::

Main
=======================================

Bo Olson {#title}
---------------------------------------

I'm an applied data scientist and analyst with strong data engineering skills, a creative mind for building enterprise-level ML solutions, coaching data literacy, and an obsession with communicating results beautifully. 

I'm experienced in driving a data team from descriptive to prescriptive analytics, and bringing stakeholders along for the journey. 

Experience {data-icon=briefcase}
--------------------------------------------------------------------------------

### <i class="fa fa-chart-area"></i> Microsoft 

Senior Marketing Analytics Manager: US Central Marketing Organization

Bellevue, WA

Current - 2016

- Development of enterprise machine learning solutions for US field marketing:
  + Identified key KPIs and built ML-based marketing engagement targets to provide USCMO with intelligent goals designed to directly impact revenue, presented in real-time reports used in daily RoB. (<i>What does good look like?</i> I can help with that!)
  + Real-time marketing program recommendations at the account level driven by custom models, optimized to drive marketing impact on revenue by 2x - 5x
  + Built, deployed and maintained production models using clustering, linear models, boosted trees, as well as custom implementations to directly address the relevant business problem at hand
  + Developed spend optimization and causal inference models to measure successful customer investment funds and provide real-time recommendations on spend, working across multiple disciplines and teams
- Development and maintenance of data pipelines, visual dashboards for hundreds of internal users in sales and marketing
  + Deep experience in SQL Server/SSIS/SSAS, R/RShiny, Azure Notebooks, Data Factory & Storage, Databricks, and PowerBI to drive daily insights


### <i class="fa fa-chart-area"></i> Yesler <i>(Now Accenture)</i>

Marketing Program Manager

Seattle, WA

2016 - 2014

- Supported Microsoft Enterprise Marketing through reporting platform development:
  + Established KPIs and best practices for email nurture, web traffic, and sales engagement reporting
  + Built and managed 30+ PowerBI dashboards to measure success
  + Development and management of SSIS, SSAS, PowerBI stack


### <i class="fa fa-book-open"></i> Amazon

Site Merchandiser - Books

Seattle, WA

2014 - 2013

- Owned marketing program strategy for a "Big 5" publisher account, helped generate MM dollar growth of +20% YoY
- Data analysis, modeling, customer behavior testing
- Workflow modeling and marketing automation improvements to generate team-wide time savings of over 200hrs / month
- Merchandising strategy for high-traffic specialty stores & seasonal events

### <i class="fa fa-coffee"></i> The Tea Spot

Director of Sales

Boulder, CO

2013 - 2009

- Managed wholesale sales department, generated leads and sales in Grocery, Retail & Foodservice, bringing startup into profitability
- Brand & product development, public speaking at industry events
- Copywriting for marketing materials, retail packaging and branding concepts
- Feature Speaker at World Tea Expos 2012, 2013

Education {data-icon=university}
--------------------------------------------------------------------------------

### <i class = "fa fa-pen-fancy"></i> Bachelor of English, Creative Writing

University of Colorado

Boulder, CO

2010 - 2006

- Concentration in Poetry
- Editor: Honors Journal (Poetry), Walkabout Arts Journal
- Awards: Jovanovich Award in Poetry (2009), Featured Writer: Cornell’s <i>Rainy Day, 2009 Ed.</i>
- Cohead of the Fly Fishing Club
