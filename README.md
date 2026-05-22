# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Use Intent Concept in the MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: LOKESHVARAN S
Registeration Number : 212223040105
*/
```

#### MainActivity.java
```
package com.example.ex2implicit;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText editText;
        Button button;

        button = findViewById(R.id.button);
        editText = findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String url = editText.getText().toString();
                Intent i = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(i);
            }
        });

    }
}
```

#### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="288dp"
        android:ems="10"
        android:hint="Enter a Link Here"
        android:inputType="text"
        android:text=""
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="28dp"
        android:text="Navigate"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

<img width="417" height="835" alt="image" src="https://github.com/user-attachments/assets/bb0a9374-7f79-4443-b717-a986f9307f0f" />


<img width="456" height="865" alt="image" src="https://github.com/user-attachments/assets/f8fa15d9-527d-4257-a935-12a0d89b2790" />



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


