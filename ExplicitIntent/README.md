
# Ex.No:2b Explicit Intents

Develop program to create two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a layout,click button and display factorial number using Explicit Intents in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as ExplicitIntent and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display factorial number using Explicit Intents in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Explicit Intents”.
Developed by:D.Amarnath reddy
Registeration Number :212221240012
*/
```
### Main activity java
```
package com.Amarnath.a2b;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    EditText edt1;
    Button btn1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        edt1 = findViewById(R.id.edt1);
        btn1 = findViewById(R.id.btn1);
        Intent i = new Intent(MainActivity.this,SecondActivity.class);
        btn1.setOnClickListener(View->{
            i.putExtra("number",edt1.getText().toString());
            startActivity(i);
        });

    }
}
```
### second activity.java
```
package com.Amarnath.a2b;

import android.os.Bundle;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class SecondActivity extends AppCompatActivity {
    TextView txt2;

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);

        Bundle b = getIntent().getExtras();

        int no = Integer.parseInt(b.getString("number"));
        long f=1;

        for(int i=no; i>0; i--)
        {
            f = f * i;
        }

        txt2 = findViewById(R.id.txt2);
        txt2.setText("Factorial of " + no + " is " + f);
    }

}
```
### activity.main_xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <EditText
        android:id="@+id/edt1"
        android:layout_width="350dp"
        android:layout_height="60dp"
        android:layout_centerHorizontal="true"
        android:hint="Enter a number"
        android:textAlignment="center"
        android:inputType="number"
        android:layout_marginTop="220dp"
        android:textStyle="bold"
        android:textSize="30sp"/>

    <Button
        android:id="@+id/btn1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/edt1"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="50dp"
        android:text="Factorial" />

</RelativeLayout>
```
### activity_second.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
             android:layout_width="match_parent"
             android:layout_height="match_parent">

    <TextView
        android:id="@+id/txt2"
        android:layout_width="500dp"
        android:layout_height="40dp"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="40dp"
        android:textStyle="bold"
        android:textAlignment="center"
        android:textSize="30sp"
        />
</RelativeLayout>
```
## OUTPUT

![Screenshot (110)](https://user-images.githubusercontent.com/94165103/190217041-6dfea17f-fe37-4941-92db-3fe1fcb133c0.png)


![Screenshot (111)](https://user-images.githubusercontent.com/94165103/190216543-0d7d7a46-8da5-4d69-838e-4ff19fb6e585.png)

![Screenshot (112)](https://user-images.githubusercontent.com/94165103/190216561-960eb7d9-47a6-40b3-ba04-de37950d58a1.png)

## RESULT

Thus a Simple Android Application to display factorial of the same number using Explicit Intents using Android Studio is developed and executed successfully.
