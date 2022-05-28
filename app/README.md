### Ex.No:6 Build a program to create a first display screen of any search engine using Auto Complete Text View.
## AIM:
To develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)

## ALGORITHM:
# Step 1: 
Open Android Stdio and then click on File -> New -> New project.
# Step 2: 
Then type the Application name as searchengine and click Next.
# Step 3:
Then select the Minimum SDK as shown below and click Next.
# Step 4: 
Then select the Empty Activity and click Next. Finally click Finish.
# Step 5: 
Design layout using AutoComplete TextView in activity_main.xml.
# Step 6: 
Display screen of search engine in MainActivity file.
# Step 7: 
Save and run the application.

## PROGRAM:
```java
Program to print the text “display screen of any search engine”.
Developed by: ASHWIN A O
Registeration Number : 212220230005
```
## activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    android:background="@drawable/leaf"
    android:outlineAmbientShadowColor="@color/black"
    tools:context=".MainActivity">


    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textStyle="italic"
        android:textSize="25dp"
        android:completionThreshold="1"
        android:text="search"
        android:textColor="@color/white" />


    <TextView
        android:id="@+id/textview1"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:fontFamily="sans-serif-black"
        android:textSize="36sp"
        android:textColor="#FDD835"
        android:textColorHighlight="#4CAF50"
        android:textColorHint="#03A9F4"
        android:textColorLink="#E91E63"
        android:textStyle="italic" />
</LinearLayout>
``` 

## MainActivity.java
```java
package com.example.displayscreen;

import androidx.appcompat.app.AppCompatActivity;

import android.app.Activity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends Activity {
    AutoCompleteTextView text;

    String[] words={"Ashwin","Ao","Artist","cat","dog","elephant","idk","i","python","kit","lick","sight","tick","zebraz"};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        text = (AutoCompleteTextView) findViewById(R.id.autoCompleteTextView);


        ArrayAdapter adapter = new
                ArrayAdapter(this, android.R.layout.simple_list_item_1, words);

        text.setAdapter(adapter);
        text.setThreshold(1);


    }
}
```
## OUTPUT
![Screenshot 2022-05-28 122953](https://user-images.githubusercontent.com/75235601/170814574-13c5a887-5616-4c07-9418-2d17b0c39d47.jpg)

![Screenshot 2022-05-28 123020](https://user-images.githubusercontent.com/75235601/170814577-c0773feb-05b7-4ca5-abc9-01c0a8cc2c4c.jpg)


## RESULT
Thus a Simple Android Application develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio is developed and executed successfully.
