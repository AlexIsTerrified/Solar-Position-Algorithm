# Solar-Position-Algorithm
Algorithm used to determine the solar azimuth and elevation angles of a given date-time and geo location

This algorithm is based on the equations form Astronomical Algorithms by Jean Meanus and is adapted from the summary provided by the U.S. Department of Energy Laboratory. [Solar Position Algorithm for
Solar Radiation Applications](https://www.nrel.gov/docs/fy08osti/34302.pdf)

## Exported Function
### result(latitude,longitude,year.month,date,hour,minute,second): javascript Object

## Parameters
latitude | The geographical latitude of a position on earth in degrees | values:-90.0 - 90.0

longitude | The geographical longitude of a position on earth in degrees | values:-180.0 - 180.0

year | The given year eg. 2022

month | The number of the given month where January = 1 and December = 12

date | The date of the given month eg. 1, 28, 30,31

hour | The hour of the given day in a 24 hour format eg. 5pm = 17

minute | The minute of the given hour | values: 0 - 60

second | The second of the given minute | values: 0 - 60

## Return Value
the result() function returns a javascript object with the following attributes

{
 
 el: // The elevation angle in degrees
  
  az: // The azimuth anlge in degrees
  
  dec: // The declination angle of the sun
  
  eot: // The equation of time in minutes
  
  sunrise: // the sunrise time of day in hours where the decimal value is a fraction of an hour eg. 6.25 = 6:15am, 22.80 = 10:48pm | accurate to the nearest second
  
  sunset: // the sunset time of day in hours where the decimal value is a fraction of an hour eg. 6.25 = 6:15am, 22.80 = 10:48pm | accurate to the nearest second
  
  transit: // the noon time of day in hours where the decimal value is a fraction of an hour eg. 6.25 = 6:15am, 22.80 = 10:48pm | accurate to the nearest second
  
}
