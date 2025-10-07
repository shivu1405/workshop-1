# WORKSHOP ----SUMMATION OF TWO NUMBERS USING ANDROID STUDIO.
# AIM:
To develop an Android application using Android Studio that takes two numbers as input from the user and displays their sum when a button is clicked.

# EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

# ALGORITHM:
1.Start the program.

2.Design the UI with two EditTexts, one Button, and one TextView.

3.Read the two numbers from the EditTexts.

4.Convert the input values to integers.

5.Add the two numbers and store the result.

6.Display the sum in the TextView.

7.Stop the program.

# Program:
```
/*
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: SHIVASRI
RegisterNumber:  21224220098
*/
```
ACTIVITY_MAIN.XML:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="24dp"
    android:gravity="center">
    <TextView
        android:id="@+id/workshop"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Workshop 1"
        android:textSize="18sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginTop="20dp" />
    <TextView
        android:id="@+id/addition"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Addition Of Two Numbers"
        android:textSize="18sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginTop="20dp" />
    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number"
        android:layout_marginTop="12dp" />

    <Button
        android:id="@+id/btnSum"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Calculate Sum "
        android:layout_marginTop="16dp" />

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Result will appear here"
        android:textSize="18sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginTop="20dp" />

</LinearLayout>



```
MAINACTIVITY JAVA:
```
package com.example.sumapp;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button btnSum;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Link UI elements
        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        btnSum = findViewById(R.id.btnSum);
        result = findViewById(R.id.result);

        btnSum.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Get numbers from EditText
                String s1 = num1.getText().toString();
                String s2 = num2.getText().toString();

                if (s1.isEmpty() || s2.isEmpty()) {
                    result.setText("Please enter both numbers!");
                    return;
                }

                // Convert to integers
                int a = Integer.parseInt(s1);
                int b = Integer.parseInt(s2);

                // Calculate sum
                int sum = a + b;

                // Display result
                result.setText("Sum: " + sum);
            }
        });
    }
}
```
# OUTPUT:
<img width="1919" height="1137" alt="Screenshot 2025-10-07 180418" src="https://github.com/user-attachments/assets/563dbccb-5cb3-41b7-974b-3fdef31c2c33" />

# Result:
The Android application for the summation of two numbers was successfully developed and executed.
