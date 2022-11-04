### Basic-AndroidStudio

### Developed: D.Amarnath reddy
### Registered Number: 212221240012

### MainActivity.java
```
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
```
### activity_main.xml
```
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
```

### Output
![1](https://user-images.githubusercontent.com/94165103/190207270-5e5691b2-f686-43b8-8197-bc9e7a91a416.jpg)
![2](https://user-images.githubusercontent.com/94165103/190207357-4c281b5e-60d6-416c-b786-86bdd4e8ccc0.jpg)
![3](https://user-images.githubusercontent.com/94165103/190207453-75c61a5e-3cd4-44cc-a9e0-bf9979f663c5.jpg)
![4](https://user-images.githubusercontent.com/94165103/190207613-b225cd2b-24e0-4151-a84a-bd08efe84aa5.jpg)
![5](https://user-images.githubusercontent.com/94165103/190207677-afbb3b0d-ffc5-412a-bd97-293c0c351441.jpg)
![6](https://user-images.githubusercontent.com/94165103/190207777-872e5fd1-f622-43e9-b1dc-cce76a228682.jpg)


### REsult!

Therefore a program is return to develop a program to detect the various life cycles of an activity. The program is successfully executed.
