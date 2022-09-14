
# Ex.No:2a Implicit Intent

Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a layout,click button,open google page using Implicit Intents in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as ImplicitIntent and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: open google page using Implicit Intents in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Implicit Intent”.
Developed by:D.Amarnath
Registeration Number :212221240012
*/
```
### Main activity.java
```
package com.example.application;

import com.example.application.R;
import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.net.Uri;

public class MainActivity extends AppCompatActivity {
    EditText edit1;
    Button Button1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        edit1 = findViewById(R.id.ram);
        Button1 = findViewById(R.id.but1);

        Button1.setOnClickListener(view ->{
            String  url = edit1.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW,Uri.parse(url));
            startActivity(intent);
        });

    }

}
```
### activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#15D5FB"
    tools:context=".MainActivity" >

    <EditText
        android:id="@+id/ram"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="140dp"
        android:layout_marginBottom="183dp"
        android:hint="Enter url"
        android:textSize="40sp"
        app:layout_constraintBottom_toTopOf="@+id/but1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/but1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"

        android:text="Enter"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

![Screenshot (107)](https://user-images.githubusercontent.com/94165103/190219666-cd97145f-958d-442f-8b99-771d93802b50.png)

![Screenshot (108)](https://user-images.githubusercontent.com/94165103/190219843-f37ac3c7-3fed-4808-98df-2f14cb89dd7d.png)

![Screenshot (109)](https://user-images.githubusercontent.com/94165103/190219879-fcdf4637-08eb-4f9f-bb7d-4d1181b0adde.png)


## RESULT
Thus a Simple Android Application to open google page using Implicit Intents using Android Studio is developed and executed successfully.


