# WeatherComp
Jupyter notebooks for downloading weather by lat/long and doing quick matplotlib analysis


This quick notebook is a quick portfolio peak for some of Charles' code. 
There are two main files:

LAWeather_getFullYear.ipynb  

    A notebook that pulls weather data from darksky.net.  You can do up to 1k API calls per day. This notebook currently makes one call for each day in 2018. Data returned is a rich set of hourly data points from the lat/Long specified in location.
    
    You will need to add forecastiopy to your python libraries.  Also, you'll need to add your API Key to run this.
    
    Sign up to get a Key here: https://darksky.net/dev/login?next=/account
    
    Each Run generates a file (currently set to hard code the name... I just wrote this in the last two days, call it "tech debt" that outfile name isn't dynamic.  It wouldn't be hard, but this does what it needs to.
    
LAXwx compare share.ipynb

      Loads the data downloaded by the getFullYear notebook into Pandas arrays, does some cleanup, then displays the results.
      Graphical results can be toggled through by changing out the function showWeather('Lax', 'temp')
      Possible values for the first parameter: 'Lax','Den','Btv'
      Possible values for the second parameter: 'temp', 'wind', 'icon','humidity'
      
      The results can be read as: For each grouping of weather conditions, what is the cound of those happening at that level each month of the year?
      
Some quick insights (none very surprising):
    <ul><li>Burlington (Btv) has a much wider temperature range than LA.  LA is quite moderate - but yikes, it got really hot <110F last year.</li>
    <li>Btv is windier than LAX, but less that Denver - denver more frequenly high winds.  LA has pretty calm winds for a lot of the winter</li>
    <li>Den is the driest of the three locales</li>
    <li>Lots of sunshine in Den and LAX. Lots of clouds in BTV.</li>
    </ul>
    
The other files are the generated data files as .csv
    
