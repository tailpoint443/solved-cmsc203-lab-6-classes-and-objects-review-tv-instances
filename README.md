Download Link: https://assignmentchef.com/product/solved-cmsc203-lab-6-classes-and-objects-review-tv-instances
<br>
<strong>Lab Objectives</strong>

 Be able to declare a new class

 Be able to write a constructor

 Be able to write instance methods that return a value

 Be able to write instance methods that take arguments

 Be able to instantiate an object

 Be able to use calls to instance methods to access and change the state of an object

<strong>Introduction</strong>

Everyone is familiar with a television. It is the object we are going to create in this lab.

First we need a blueprint. All manufacturers have the same basic elements in the televisions they produce as well as many options. We are going to work with a few basic elements that are common to all televisions. Think about a television in general. It has a brand name (i.e. it is made by a specific manufacturer). The television screen has a specific size. It has some basic controls. There is a control to turn the power on and off. There is a control to change the channel. There is also a control for the volume. At any point in time, the television’s state can be described by how these controls are set. We will write the television class. Each object that is created from the television class must be able to hold information about that instance of a television in fields. So a television object will have the following attributes:

 <strong>manufacturer</strong>. The manufacturer attribute will hold the brand name. This cannot change once the television is created, so will be a named constant.

 <strong>screenSize</strong>. The screenSize attribute will hold the size of the television screen.

This cannot change once the television has been created so will be a named constant.

 <strong>powerOn</strong>. The powerOn attribute will hold the value true if the power is on, and false if the power is off.

 <strong>channel</strong>. The channel attribute will hold the value of the station that the television is showing.

 <strong>volume</strong>. The volume attribute will hold a number value representing the loudness (0 being no sound).

These attributes become <strong>fields </strong>in our class.

The television object will also be able to control the state of its attributes. These controls become <strong>methods </strong>in our class.

 <strong>setChannel</strong>. The setChannel method will store the desired station in the channel field.

 <strong>power</strong>. The power method will toggle the power between on and off, changing

the value stored in the powerOn field from true to false or from false to true.

 <strong>increaseVolume</strong>. The increaseVolume method will increase the value stored in

the volume field by 1.

 <strong>decreaseVolume</strong>. The decreaseVolume method will decrease the value stored in

the volume field by 1.

 <strong>getChannel</strong>. The getChannel method will return the value stored in the channel

field.

 <strong>getVolume</strong>. The getVolume method will return the value stored in the volume

field.

 <strong>getManufacturer</strong>. The getManufacturer method will return the constant value

stored in the MANUFACTURER field.

 <strong>getScreenSize</strong>. The getScreenSize method will return the constant value stored in the SCREEN_SIZE field.

We will also need a constructor method that will be used to create an instance of a Television.

These ideas can be brought together to form a UML (Unified Modeling Language) diagram for this class as shown below.

<strong> </strong>

<strong> </strong>

<strong>Task #1 Creating a New Class</strong>

<ol>

 <li>In a new file, create a class definition called Television.</li>

 <li>Put a documentation string right before the class header</li>

</ol>

/**

*The purpose of this class is to model a television

*<em>Your name </em>and <em>today’s date</em>

*/

<ol start="3">

 <li>Declare the two constant fields listed in the UML diagram.</li>

 <li>Declare the three remaining fields listed in the UML diagram.</li>

 <li>Write a comment for each field indicating what it represents.</li>

 <li>Save this file as Television.java.</li>

 <li>Compile and debug. Do not run.</li>

</ol>




<strong>Task #2 Writing a Constructor</strong>

<ol>

 <li>Create a constructor definition that has two parameters, a manufacturer’s brand and a screen size. These parameters will bring in information.</li>

 <li>Inside the constructor, assign the values taken in from the parameters to the corresponding fields.</li>

 <li>Initialize the powerOn field to false (power is off), the volume to 20, and the channel to 2.</li>

 <li>Write comments describing the purpose of the constructor above the method header.</li>

 <li>Compile and debug. Do not run.</li>

</ol>




<strong>Task #3 Methods</strong>

<ol>

 <li>Define accessor methods called getVolume, getChannel, getManufacturer, and</li>

</ol>

getScreenSize that return the value of the corresponding field.

<ol start="2">

 <li>Define a mutator method called setChannel accepts a value to be stored in the</li>

</ol>

channel field.

<ol start="3">

 <li>Define a mutator method called power that changes the state from true to false or</li>

</ol>

from false to true. This can be accomplished by using the NOT operator (!). If

the boolean variable powerOn is true, then !powerOn is false and vice versa.

Use the assignment statement

powerOn = !powerOn;

to change the state of powerOn and then store it back into powerOn (remember

assignment statements evaluate the right hand side first, then assign the result to

the left hand side variable.

<ol start="4">

 <li>Define two mutator methods to change the volume. One method should be called</li>

</ol>

increaseVolume and will increase the volume by 1. The other method should be

called decreaseVolume and will decrease the volume by 1.

<ol start="5">

 <li>Write javadoc comments above each method header.</li>

 <li>Compile and debug. Do not run.</li>

</ol>




<strong>Task #4 Running the application</strong>

<ol>

 <li>You can only execute (run) a program that has a main method, so there is a driver</li>

</ol>

program that is already written to test out your Television class. Copy the file

TelevisionDemo.java (see code listing 3.1) from the Student CD or as directed by

your instructor. Make sure it is in the same directory as Television.java.

<ol start="2">

 <li>Compile and run TelevisionDemo and follow the prompts.</li>

 <li>If your output matches the output below, Television.java is complete and correct.</li>

</ol>

You will not need to modify it further for this lab.

<strong> </strong>

<strong>OUTPUT (underlined is user input)</strong>

A 55 inch Toshiba has been turned on.

What channel do you want? <strong><u>56</u></strong>

Channel: 56 Volume: 21

Too loud!! I am lowering the volume.

Channel: 56 Volume: 15

<strong> </strong>

<strong>Task #5 Creating another instance of a Television</strong>

<ol>

 <li>Edit the TelevisionDemo.java file.</li>

 <li>Declare another Television object called portable.</li>

 <li>Instantiate portable to be a Sharp 19 inch television.</li>

 <li>Use a call to the power method to turn the power on.</li>

 <li>Use calls to the accessor methods to print what television was turned on.</li>

 <li>Use calls to the mutator methods to change the channel to the user’s preference and decrease the volume by two.</li>

 <li>Use calls to the accessor methods to print the changed state of the portable.</li>

 <li>Compile and debug this class.</li>

 <li>Run TelevisionDemo again.</li>

 <li>The output for task #5 will appear after the output from above, since we added onto the bottom of the program. The output for task #5 is shown below.</li>

</ol>

<strong> </strong>

<strong>OUTPUT (underlined is user input)</strong>

A 19 inch Sharp has been turned on.

What channel do you want? <strong><u>7</u></strong>

Channel: 7 Volume: 18

<strong> </strong>

<strong> </strong>

<strong>Code Listing 4.1 (TelevisionDemo.java)</strong>

/** This class demonstrates the Television class*/

import java.util.Scanner;




public class TelevisionDemo

{

public static void main(String[] args)

{

//create a Scanner object to read from the keyboard

Scanner keyboard = new Scanner (System.in);

//declare variables

int station; //the user’s channel choice

//declare and instantiate a television object

Television bigScreen = new Television(“Toshiba”, 55);

//turn the power on

bigScreen.power();

//display the state of the television

System.out.println(“A ” + bigScreen.getScreenSize()


bigScreen.getManufacturer() + ” has been turned on.”);

//prompt the user for input and store into station

System.out.print(“What channel do you want? “);

station = keyboard.nextInt();

//change the channel on the television

bigScreen.setChannel(station);

//increase the volume of the television

bigScreen.increaseVolume();

//display the the current channel and volume of the television

System.out.println(“Channel: ” + bigScreen.getChannel()


” Volume: ” + bigScreen.getVolume());

System.out.println(“Too loud!! I am lowering the volume.”);

//decrease the volume of the television

bigScreen.decreaseVolume();

bigScreen.decreaseVolume();

bigScreen.decreaseVolume();

bigScreen.decreaseVolume();

bigScreen.decreaseVolume();

bigScreen.decreaseVolume();

//display the current channel and volume of the television

System.out.println(“Channel: ” + bigScreen.getChannel()


” Volume: ” + bigScreen.getVolume());

System.out.println(); //for a blank line

//HERE IS WHERE YOU DO TASK #5

}

}