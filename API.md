
# API Documentation

## Edit a Random Image 
* Trigger: Receive nothing 
* Method: Start Activity
```java 
Intent i = new Intent(this, RandomActivity.class); 
startActivity(i); 
```
`User can edit a random image from database.` 

## Rename an image 
* Trigger: Receive image
* Method: Broadcast Receiver 
```java 
Intent i = new Intent(this, RenameActivity.class); 
Drawable d = getDrawable(R.drawable.<imageName>);
Bitmap _bitmap = ((BitmapDrawable) d).getBitMap(); 
ByteArrayOutputStream _bs = new ByteArrayOutputStream();
_bitmap.compress(Bitmap.CompressFormat.PNG, 50, _bs);
i.putExtra("byteArray", _bs.toByteArray());
sendBroadcast(i); 
```
`User can store and image under a new name.`

## Image Look Up 
* Trigger: Receive Nothing  
* Method: Broadcast Receiver
```java 
Intent i = new Intent(this, LookUpActivity.class); 
startService(i); 
startActivity(i); 
```
`User can look up a image by name and make edits.`

## Image Edits 
* Trigger: Receive an Image file 
* Method: Broadcast Receiver
```java 
Intent i = new Intent(this, Edit.class); 
Drawable d = getDrawable(R.drawable.<imageName>);
Bitmap _bitmap = ((BitmapDrawable) d).getBitMap(); 
ByteArrayOutputStream _bs = new ByteArrayOutputStream();
_bitmap.compress(Bitmap.CompressFormat.PNG, 50, _bs);
i.putExtra("byteArray", _bs.toByteArray());
sendBroadcast(i); 
```
`User can edit an image they provide and store it in our database.`