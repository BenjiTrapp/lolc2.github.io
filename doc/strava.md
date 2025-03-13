##### Abusing Strava for C2

Attackers can use Strava’s API to send and receive commands by embedding encoded data in activity descriptions. The client polls for new activities, decodes commands, executes them, and posts the output as a new activity

![stravac2](doc/strava_c2.png)