# Fix Small Bodies Distance
AstroSynthesis plugin to fix the distance on small bodies to avoid Travel Calculator throwing an invalid floating point violation error

According to NBOS Support
"'Small bodies' is really just a note that there are numerous small, 
unremarkable bodies in orbit (small chunks of rock).  Its not a single 
body with a single orbit, but rather debris found in orbit at various 
places.  So there's no orbital parameters per se, and they arent shown 
in the system diagram.  Think of it as the orbital equivalent of a 'look
 out for falling rocks' sign."

Unfortunately by default 'Small Bodies' have a distance of 0. This 
causes the Travel Calculator to throw an invalid floating point 
violation error, in order to fix this we will set the distance to 0.01. 
 This will achieve the same affect for all intents and purposes without 
causing the error.

This script will run on all bodies and child bodies in a sector.  If a 
body of type 'BODY_TYPE_SMALLBODY' has a distance of 0 this script will 
update the distance to 0.01
