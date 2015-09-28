#JavaMaltego

Maltego Library coded in Java for developing Maltego Local transforms in Java.

## How to use

Compile code and import to your project.

## Code 

**1. Create a object of MaltegoTransform**

	MaltegoTransform me = new MaltegoTransform();

**2. Adding Entity**

	me.addEntity(Type, Value); 

**3. Adding property** 

For adding property you have get entity from the list by referencing index of it. (Remember first element in array is 0, (I know you know this) :) )

	me.listEntities.get(i).addProperty(fieldName,displayName,matchingRule,value);

**4. Returning output.**

	me.returOutput();

Library will generate and return XML. 

## Running application in Maltego.

Create a shell code with the following code.

	#!bin/bash
	java -jar [path to you application.jar]

Change the permission.

	chmod +x nameOfFile.sh
	chmod 755 nameOfFile.sh

In the Maltego add the path to shell script, while adding Maltego transform.

## Currently available methods

### class MaltegoEntity

	addProperty(String fieldName,String displayName,String matchingRule,String value);
	setWeight(String weight); - sets weights
	setLinkColor(String color); - sets Link color
	setLinkStyle(String style); - sets style of Link
	setLinkThichkness(String thick);- sets thickness of the link 
	setBookmark(String bookmark);- sets a bookmark. Available colors are:(BOOKMARK_COLOR_NONE, BOOKMARK_COLOR_BLUE,BOOKMARK_COLOR_GREEN,BOOKMARK_COLOR_YELLOW,BOOKMARK_COLOR_ORANGE,BOOKMARK_COLOR_RED)
	setNote(String Note); - sets a note about entity
	setIconUrl(String url); - sets icon url of entity

### class MaltegoTransform 

	addEntity(String Type, String Value); - adds entity
	returnOutput(); - generates and returns XML 
	
**Other methods will be added.** 
