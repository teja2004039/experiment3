# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: charan
Registeration Number : 212221040067
*/

activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">
<TextView
android:id="@+id/textView"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:layout_marginTop="296dp"
android:gravity="center"
android:text="Hello World!"
android:textSize="25sp"
android:textStyle="bold"
app:layout_constraintBottom_toTopOf="@+id/button1"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.266"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
tools:ignore="MissingConstraints" />
<Button
android:id="@+id/button1"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="20dp"
android:layout_marginBottom="48dp"
android:gravity="center"
android:text="Change font size"
android:textSize="25sp"
app:layout_constraintBottom_toTopOf="@+id/button2"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.25"
app:layout_constraintStart_toStartOf="parent"
tools:ignore="MissingConstraints" />
<Button
android:id="@+id/button2"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="20dp"
android:gravity="center"
android:text="Change color"
android:textSize="25sp"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.4"
app:layout_constraintStart_toStartOf="parent"
tools:ignore="MissingConstraints" />
</androidx.constraintlayout.widget.ConstraintLayout>
MainActivity.java
package com.example.ex2;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Color;
import android.os.Bundle;


import android.view.View;
import android.widget.Button;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
int ch=1;
float font=30;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
final TextView t = (TextView) findViewById(R.id.textView);
Button b1 = (Button) findViewById(R.id.button1);
b1.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
t.setTextSize(font);
font = font + 5;
if (font == 50)
font = 30;
}
});
Button b2 = (Button) findViewById(R.id.button2);
b2.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
switch (ch) {
case 1:
t.setTextColor(Color.RED);
break;
case 2:
t.setTextColor(Color.GREEN);
break;
case 3:
t.setTextColor(Color.BLUE);
break;
case 4:
t.setTextColor(Color.CYAN);
break;
case 5:
t.setTextColor(Color.YELLOW);
break;
case 6:
t.setTextColor(Color.MAGENTA);
break;
}
ch++;
if (ch == 7)
ch = 1;
}
});
} }
```
## OUTPUT


![image](https://github.com/Sudhindev/Experiment-3/assets/130021386/5245ad13-fb13-4e2b-8d96-48e6e41e570a)





## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
