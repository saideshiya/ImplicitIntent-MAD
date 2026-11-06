# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.youtube.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1. Start the application: Open the Android application created in Android Studio.

2. Design the user interface: Create an EditText to enter the website URL and a Search button in the XML layout file.

3. Initialize the components: In MainActivity.java, connect the EditText and Button using findViewById().

4. Create the implicit intent: When the user clicks the Search button, retrieve the URL www.youtube.com and create an Intent using Intent.ACTION_VIEW and Uri.parse().

5. Launch the webpage: Call startActivity(intent) to open YouTube in the browser or supported application and stop the execution.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: SAI DESHIYA K
Registeration Number : 212224220084
*/
```
## MainActivity.java:
```
package com.example.implicitant;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
        editText = findViewById(R.id.editText);

        button.setOnClickListener(view -> {
            String url = editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:autofillHints="url"
        android:hint="@string/enter_url"
        android:inputType="textUri"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/search"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText" />

</androidx.constraintlayout.widget.ConstraintLayout>
```


## OUTPUT :
<img width="1738" height="1077" alt="image" src="https://github.com/user-attachments/assets/1569316f-94ab-4aaa-8983-b2f2b1858022" />

<img width="1728" height="1076" alt="image" src="https://github.com/user-attachments/assets/22ea36ef-3d75-44d0-ab38-62566ef0672d" />





## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


