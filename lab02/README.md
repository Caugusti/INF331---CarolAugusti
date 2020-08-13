# INF331---CarolAugusti

## Tarefa sobre catálogo de componentes

> [Tarefa sobre Catálogo de Componentes](notebook/tarefas_components_catalog.ipynb)

## Tarefa Web Components 1

~~~html
<dcc-trigger label="Mundo"
             action="noticia/mundo/politica"
             value="nova notícia da politica mundial">
</dcc-trigger>

<dcc-trigger label="Brasil P"
             action="noticia/brasil/politica"
             value="nova notícia da politica do Brasil">
</dcc-trigger>

<dcc-trigger label="Brasil E"
             action="noticia/brasil/esporte"
             value="nova notícia esportiva do Brasil">
</dcc-trigger>

<dcc-trigger label="Bahia"
             action="noticia/bahia/esporte"
             value="nova notícia esportiva da Bahia">
</dcc-trigger>

<dcc-lively-talk duration="0s"
                 character="doctor"
                 speech="Eu ouvi sobre uma ">
 <subscribe-dcc topic="noticia/#/politica"></subscribe-dcc>
</dcc-lively-talk>

</dcc-trigger>
<dcc-lively-talk duration="0s"
                 character="nurse"
                 speech="Eu ouvi sobre uma ">
 <subscribe-dcc topic="noticia/b#"></subscribe-dcc>
</dcc-lively-talk>

</dcc-trigger>
<dcc-lively-talk duration="0s"
                 character="patient"
                 speech="Eu ouvi sobre uma ">
 <subscribe-dcc topic="noticia/#"></subscribe-dcc>
</dcc-lively-talk>

~~~

## Tarefa Web Components 2

~~~html

<dcc-trigger label="Next Item" 
             action="next/rss">
</dcc-trigger>

<dcc-rss publish="rss/science" 
         source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" 
                quantity="3">
   <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-rss publish="rss/design" 
         source="https://www.wired.com/category/design/feed">
   <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="nurse"
                 speech="News ">
   <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Noticia ">
   <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk duration="0s"
                 character="patient"
                 speech="Noticia ">
   <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>

~~~