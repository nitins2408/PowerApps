# Power Apps Horizontal Bar Chart Custom Component
This component has the Powerapps Horizontal Bar chart in it. It has Gallerwidth Multiplication factor which helps to make the BarGraph comaptible to your app & resolution. You can further do the customization as per your project & app needs

**The Core Logic**

Basically there is no Out of the Box Bar chart comes with Powerapp as of today (30st July 2020). Added simple solution to conver the Powerapps Gallery to the Horizontal Bar chart by doing small tricks in width, height & adding functions to set the dynamically.

![Horizontal Bar chart](https://github.com/nitins2408/PowerApps/blob/master/Horizontal%20Bar%20Chart/HorizontalBarChart.JPG)

 
 
## Gallery Properties

1. Add the Data Source as 'ColumnChartSample'    {.Items}

2.  Fill Property of Title1 inside Gallery :-> 
          `If (  ThisItem.Population < 8 , RGBA(58,139,249,1),If(ThisItem.Population < 10  , RGBA(229,111,49,1), 
        If( ThisItem.Population < 15,  RGBA(111,05,131,1), RGBA(231,57,159,1 ) ) ) ) `

3. Width Property of the Title1 inside Galleyr to be set to :->

    `(HorizontalBarGraph.GalleryWidthMultiplicationFactor + HorizontalBarGraph.Width-640) * (ThisItem.Population/Max( ColumnChartSample,Population))`

4.  Two subtitle componenet to be adjusted for Name and value accordingly & hide other components your Horizontal Gallery is ready.

## PreRequiste
You Should know how to Import .msapp file as a Custom Component to Powerapps. There are lot of informaation availble on internet, you may refer below blog


[Import .msapp file as Custom Component to Powerapps](http://infofunvilla.com/import-msapp-canvas-custom-component-to-microsoft-powerapps/363/)
 

## Author
- Nitin Sapkal
 
