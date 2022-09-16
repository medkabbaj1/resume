# resume
---
title: "El Mehdi Kabbaj"
author: El Mehdi Kabbaj
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

Contact 
--------------------------------------

<i class="fa fa-envelope"></i> mehdi.kabbaj10@gmail.com

<i class="fa fa-phone"></i> 0620536801

<i class="fa fa-linkedin"></i> <a href="https://www.linkedin.com/in/mehdi-kbbj">linkedin.com/in/mehdi-kbbj</a>

<!-- hope you like my joke -->
<i class="fa fa-map-marker-alt"></i> <a href="https://www.onzemondial.com/ligue-1/2020-2021/lille-les-images-folles-de-la-celebration-du-titre-avec-les-supporters-en-delire-629723">Lille, France</a>

<i>View html with links at my github: 

https://github.com/medkabbaj1) </i>



Technical Skills
---------------------------------------

```{r skill plot, fig.height=15, fig.width=10}

skill<-c("R", "SQL", "Pythone", "Data Visualization (ggplot / PowerBI)", "github", "HTML & CSS", "Trading")
level<-c(7,8,6,6,6,7,8)
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

Personal development - Travelling – Fitness - Following economic current events - Learning Data




Main
=======================================

El Mehdi Kabbaj
---------------------------------------

Creative, responsible and self-taught graduate in international finance with excellent problem-solving and communication skills with an obsession to deliver results beautifully. The last two years have been experiencing, I didn't succeed to find a job in my field of studies. I spent the last two years working as a manager in a restaurant, at the same time learning about financial markets and data.

I lack experience in the field, but i recognise my determination, my work ethic and my capacity to learn is what going to differentiate from other candidates.

Education
--------------------------------------------------------------------------------

2018- 2020: M2 (Second year of Master’s Degree) in International Finance – IAE METZ School of MANAGEMENT, Metz, France.
2017- 2018: M1 (First year of Master’s Degree) in Finance, Control, Accounting - IAE METZ School of MANAGEMENT, Metz, France
2016- 2017: Bachelor’s Degree in Accounting - IAE METZ School of MANAGEMENT, Metz, France.
2014- 2016: Preparatory classes HEC – CPGE Omar El Khayyam, Rabat – Morocco.

Main Courses : 
--------------------------------------------------------------------------------

Financial Markets: Forex, commodities, stock market, bond market and Investments decisions.
Treasury management: Asset liability management (ALM), Risk management, Banking regulations.
Fund management: Portfolio management strategies, Performance analysis via R studio, Equity investments, Compliance.
Accounting: Balance Sheet, Cash Flow Statements, Income Statements, IFRS financial instruments.
Data Analysis : Reviews of data to identify key insights via SQL and Showcase the results on Microsoft Power BI.

Experience : 
--------------------------------------------------------------------------------
### <i class="fa fa-chart-area"></i> Cunipic

Export Assistant: 

Lleida, Spain

01/2020 - 06/2020

- The management of the French market :
  + Sales and forecasting oversight by converting data from Excel into data series on Power BI
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
