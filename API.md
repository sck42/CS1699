
# API Documentation

## Edit a Random Image 
* Receive nothing 
* Method: Start Activity
```java 
Intent i = new Intent(this, RandomActivity.class); 
startActivity(i); 
```

Inside random activity
Save edit pic after user pushes save button. 
Send Team 1 Locational Data
Ask User for capture location of image
Compare location to Hillman or Cathy 
If match trigger 1 and send entered location 
