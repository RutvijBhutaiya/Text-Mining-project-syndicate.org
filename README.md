# Text Mining : www.project-syndicate.org

Project Syndicate is a prominent website. The website's tag line is 'World's Opinion Page', that is indeed true. World Leaders, Economists, and scholars around the globe publish their views on various topics, ranging from macroeconomics to world politics. 

For this study, we decided to analyze their views - especially on the COVID19 crisis - with the help of NLP and text analysis. 
For the study, we specifically only chose Artiles related to the COVID19 topic - [Link](https://www.project-syndicate.org/topic/the-covid-19-crisis) .

<br>

<p align="center"><img width=100% src=https://user-images.githubusercontent.com/44467789/82111133-768f9f80-9760-11ea-92a3-7e203c051f99.png>
                       
                                           Source: www.project-syndicate.org

<br>

Due to the limited time - we studied articles from 1st April 2020 to 14th May 2020. And which also counts 91 articles. 

We successfully, did web scraping, with the help of 'rvest' package in R Studio. Full code - [Click Here](https://github.com/RutvijBhutaiya/Text-Mining-project-syndicate.org/blob/master/Pages.R)

```
ibrary(rvest)

page1 <- read_html("https://www.project-syndicate.org/commentary/woman-leaders-covid-19-crisis-ardern-by-raj-persaud-2020-05?a_la=english&a_d=5ebd1126a430fb519c6cd891&a_m=&a_a=click&a_s=&a_p=%2Ftopic%2Fthe-covid-19-crisis&a_li=woman-leaders-covid-19-crisis-ardern-by-raj-persaud-2020-05&a_pa=topic-commentaries&a_ps=&a_ms=&a_r=");

page1 <- page1 %>%
  html_nodes(xpath = '//*[@id="main"]/article/div[2]/div[2]/div/div[2]') %>%
  html_text()
```

For text analysis we also used MS Excel tool for data cleaning. 



