# DEVELOPING-ENERGY-CONSUMPTION-CALCULATOR-APPLICATION.-

## AIM:
To develop an android application to perform energy calculation.

## APPARATUS REQUIRED:
ØComputer
ØAndroid studio software


## THEORY:
The Energy Calculator App allows the user to calculate the energy consumption of electrical appliances based on power usage (in watts) and time (in hours). The app takes these two inputs, calculates the energy consumed in kilowatt-hours (kWh), and displays the result. This experiment involves basic arithmetic calculations and user input handling in Android. It uses EditText for input, Button for user interaction, and TextView to display the result. The app demonstrates how to handle user input for numerical values and perform unit conversions. It is a useful application for understanding how to develop apps that perform mathematical calculations based on user input.

## PROCEDURE:
1. Open Android Studio and then click on File -> New -> New project. 24. Then type the application name as “ex.no.3″ and click Next.
2. Then select the Minimum SDK as shown below and click next. 26. Then select the Empty Activity and click next.
3. Finally click Finish.
4. Click on app -> java -> com.example -> MainActivity.java
5. Now click on Text and type the program, so now the programming part of the main activity is completed.
6. Click on app -> res -> layout -> activity_main.xml.
7. Now click on Text and type the program, so now the designing part of Activity main is also completed.
8. Select the suitable available device to display the output. 33. Now run the application to see the output. 

## PROGRAM:

## MainActivity.java

```

package com.example.myapplication;

 

import android.os.Bundle;

 

import android.widget.Button;

 

import android.widget.EditText;

 

import android.widget.TextView;

 

import androidx.appcompat.app.AppCompatActivity;

 

public class MainActivity extends AppCompatActivity {

 

EditText watts, hours;

 

Button calc;

 

TextView result;

 

@Override

 

protected void onCreate(Bundle savedInstanceState) {

 

super.onCreate(savedInstanceState);

 

setContentView(R.layout.activity_main);

 

watts = findViewById(R.id.watts);

 

hours = findViewById(R.id.hours);

 

calc = findViewById(R.id.calc);

 

result = findViewById(R.id.result);

 

calc.setOnClickListener(v -> {

 

double w = Double.parseDouble(watts.getText().toString());

 

double h = Double.parseDouble(hours.getText().toString());

 

double kwh = (w * h) / 1000.0;

 

result.setText("Energy Used: " + kwh + " kWh");

 

});

 

 

 

}}

```

## activity_main.xml

```

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:orientation="vertical" android:layout_width="match_parent" android:layout_height="match_parent" android:padding="16dp">

 

<EditText android:id="@+id/watts" android:hint="Enter Power (Watts)" android:layout_width="match_parent" android:layout_height="wrap_content"

android:inputType="numberDecimal"/>

 

<EditText android:id="@+id/hours" android:hint="Enter Time (Hours)" android:layout_width="match_parent" android:layout_height="wrap_content"

android:inputType="numberDecimal"/>

 

<Button android:id="@+id/calc" android:text="Calculate Energy" android:layout_width="match_parent" android:layout_height="wrap_content"/>

 

<TextView android:id="@+id/result" android:paddingTop="16dp" android:layout_width="match_parent" android:layout_height="wrap_content"/>

</LinearLayout>
```

## OUTPUT:


<img width="1919" height="1020" alt="Screenshot 2025-10-06 223237" src="https://github.com/user-attachments/assets/e20e794a-ec64-48b4-bdf7-0424012c2a3f" />



## RESULT:
Thus, the energy consumption calculator app is developed and the output is verified. 

