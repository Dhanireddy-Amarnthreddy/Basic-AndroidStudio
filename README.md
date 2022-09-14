### Basic-AndroidStudio

Developed: D.Amarnath reddy
Registered Number: 212221240012

### MainActivity.java
package com.Amarnath.lifecycle;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);




        Toast toast = Toast.makeText(getApplicationContext(), "OnCreate Executed", Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onStart(){
        super.onStart();
        Toast toast=Toast.makeText(getApplicationContext(),"OnStart Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onResume(){
        super.onResume();
        Toast toast=Toast.makeText(getApplicationContext(),"OnResume Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onPause(){
        super.onPause();
        Toast toast=Toast.makeText(getApplicationContext(),"OnPause Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onStop(){
        super.onStop();
        Toast toast=Toast.makeText(getApplicationContext(),"OnStop Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onRestart(){
        super.onRestart();
        Toast toast=Toast.makeText(getApplicationContext(),"OnRestart Executed",Toast.LENGTH_LONG);
        toast.show();
    }

    protected void onDestroy(){
        super.onDestroy();
        Toast toast=Toast.makeText(getApplicationContext(),"OnDestroy Executed",Toast.LENGTH_LONG);
        toast.show();
    }
}
### activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="HelloWorld!"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true"
        android:textSize="20sp"
        android:textColor="@color/black"

        />
</RelativeLayout>

### Output

<img width="1440" alt="1" src="https://user-images.githubusercontent.com/94165103/190054686-9b4a5dc4-f331-4990-a399-0695d3a635cb.png">

<img width="1440" alt="2" src="https://user-images.githubusercontent.com/94165103/190054828-4cab1ccb-fdba-4b26-9967-5a0d016e24e4.png">

<img width="1440" alt="3" src="https://user-images.githubusercontent.com/94165103/190054899-5f6d9a42-a960-409b-a304-8562a68d496b.png">

<img width="1440" alt="4" src="https://user-images.githubusercontent.com/94165103/190055059-af5f63c1-830e-42e0-b6be-18837dc74c55.png">

<img width="1440" alt="5" src="https://user-images.githubusercontent.com/94165103/190055083-09a22bab-3ffa-4837-a5a6-8ac26ac30885.png">

<img width="1440" alt="6" src="https://user-images.githubusercontent.com/94165103/190055115-cea71a64-f0e3-491c-80d9-7152979827d7.png">

<img width="1440" alt="7" src="https://user-images.githubusercontent.com/94165103/190055160-32c24aa2-334d-42dd-be0d-e25c8f4aa5ae.png">
### REsult
Therefore a program is return to develop a program to detect the various life cycles of an activity. The program is successfully executed.
