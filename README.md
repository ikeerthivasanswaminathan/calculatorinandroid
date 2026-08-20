# Ex.No:5 Develop a program to create a simple calculator using android studio.

## Aim:
To create and design an android application for a simple calculator using android studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6:Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

### Program to create and design an android application simple calculator using Intent.

Developed by : KEERTHIVASAN S

Registeration Number : 212223220046

### activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:background="@color/background"
    android:padding="16dp">

    <!-- Display -->
    <TextView
        android:id="@+id/txtResult"
        android:layout_width="match_parent"
        android:layout_height="120dp"
        android:gravity="end|center_vertical"
        android:padding="20dp"
        android:text="0"
        android:textColor="@color/white"
        android:textSize="48sp"
        android:textStyle="bold" />

    <!-- Buttons -->
    <GridLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:columnCount="4"
        android:alignmentMode="alignMargins"
        android:useDefaultMargins="true">

        <!-- Row 1 -->

        <Button
            android:id="@+id/btnC"
            style="@style/CalcButtonRed"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="C" />

        <Button
            android:id="@+id/btnDel"
            style="@style/CalcButtonBlue"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="⌫" />

        <Button
            android:id="@+id/btnPercent"
            style="@style/CalcButtonOrange"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="%" />

        <Button
            android:id="@+id/btnDivide"
            style="@style/CalcButtonOrange"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="÷" />

        <!-- Row 2 -->

        <Button
            android:id="@+id/btn7"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="7" />

        <Button
            android:id="@+id/btn8"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="8" />

        <Button
            android:id="@+id/btn9"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="9" />

        <Button
            android:id="@+id/btnMultiply"
            style="@style/CalcButtonOrange"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="×" />

        <!-- Row 3 -->

        <Button
            android:id="@+id/btn4"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="4" />

        <Button
            android:id="@+id/btn5"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="5" />

        <Button
            android:id="@+id/btn6"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="6" />

        <Button
            android:id="@+id/btnMinus"
            style="@style/CalcButtonOrange"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="-" />

        <!-- Row 4 -->

        <Button
            android:id="@+id/btn1"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="1" />

        <Button
            android:id="@+id/btn2"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="2" />

        <Button
            android:id="@+id/btn3"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="3" />

        <Button
            android:id="@+id/btnPlus"
            style="@style/CalcButtonOrange"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="+" />

        <!-- Row 5 -->

        <Button
            android:id="@+id/btn00"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="00" />

        <Button
            android:id="@+id/btn0"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="0" />

        <Button
            android:id="@+id/btnDot"
            style="@style/CalcButtonWhite"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="." />

        <Button
            android:id="@+id/btnEqual"
            style="@style/CalcButtonGreen"
            android:elevation="6dp"
            android:stateListAnimator="@null"
            android:text="=" />

    </GridLayout>

</LinearLayout>
```

### background.xml

```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <gradient
        android:angle="270"
        android:startColor="#1E1E1E"
        android:centerColor="#121212"
        android:endColor="#000000"/>

    <corners android:radius="20dp"/>

</shape>
```

### styles.xml

```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <!-- Base Button Style -->
    <style name="CalcButtonWhite">
        <item name="android:layout_width">0dp</item>
        <item name="android:layout_height">70dp</item>
        <item name="android:layout_margin">6dp</item>
        <item name="android:layout_columnWeight">1</item>
        <item name="android:background">@drawable/number_button</item>
        <item name="android:textColor">@color/numberText</item>
        <item name="android:textSize">22sp</item>
        <item name="android:textStyle">bold</item>
    </style>

    <!-- Operator Buttons -->
    <style name="CalcButtonOrange" parent="CalcButtonWhite">
        <item name="android:background">@drawable/operator_button</item>
        <item name="android:textColor">@android:color/white</item>
    </style>

    <!-- Equal Button -->
    <style name="CalcButtonGreen" parent="CalcButtonWhite">
        <item name="android:background">@drawable/equal_button</item>
        <item name="android:textColor">@android:color/white</item>
    </style>

    <!-- Clear Button -->
    <style name="CalcButtonRed" parent="CalcButtonWhite">
        <item name="android:background">@drawable/clear_button</item>
        <item name="android:textColor">@android:color/white</item>
    </style>

    <!-- Delete Button -->
    <style name="CalcButtonBlue" parent="CalcButtonWhite">
        <item name="android:background">@drawable/delete_button</item>
        <item name="android:textColor">@android:color/white</item>
    </style>

</resources>
```

### number_button.xml

```
<?xml version="1.0" encoding="utf-8"?>
<ripple xmlns:android="http://schemas.android.com/apk/res/android"
    android:color="#80FFFFFF">

    <item>
        <shape android:shape="rectangle">
            <solid android:color="@color/numberButton"/>
            <corners android:radius="18dp"/>
        </shape>
    </item>

</ripple>
```

### operator_button.xml

```
<?xml version="1.0" encoding="utf-8"?>
<ripple xmlns:android="http://schemas.android.com/apk/res/android"
    android:color="#80FFFFFF">

    <item>
        <shape>
            <solid android:color="@color/operatorButton"/>
            <corners android:radius="18dp"/>
        </shape>
    </item>

</ripple>
```

### equal_button.xml

```
<?xml version="1.0" encoding="utf-8"?>
<ripple xmlns:android="http://schemas.android.com/apk/res/android"
    android:color="#80FFFFFF">

    <item>
        <shape>
            <solid android:color="@color/equalButton"/>
            <corners android:radius="18dp"/>
        </shape>
    </item>

</ripple>
```

### clear_button.xml

```
<?xml version="1.0" encoding="utf-8"?>
<ripple xmlns:android="http://schemas.android.com/apk/res/android"
    android:color="#80FFFFFF">

    <item>
        <shape>
            <solid android:color="@color/clearButton"/>
            <corners android:radius="18dp"/>
        </shape>
    </item>

</ripple>
```

### delete_button.xml

```
<?xml version="1.0" encoding="utf-8"?>
<ripple xmlns:android="http://schemas.android.com/apk/res/android"
    android:color="#80FFFFFF">

    <item>
        <shape>
            <solid android:color="@color/deleteButton"/>
            <corners android:radius="18dp"/>
        </shape>
    </item>

</ripple>
```

### values\themes.xml

```
<?xml version="1.0" encoding="utf-8"?>
<resources xmlns:tools="http://schemas.android.com/tools">

    <style name="Theme.Calculator"
        parent="Theme.Material3.DayNight.NoActionBar">
        <!-- Primary Colors -->
        <item name="colorPrimary">@color/operatorButton</item>
        <item name="colorPrimaryContainer">@color/operatorButton</item>
        <!-- Background -->
        <item name="android:windowBackground">@color/background</item>
        <!-- Status Bar -->
        <item name="android:statusBarColor">@color/background</item>
        <item name="android:navigationBarColor">@color/background</item>
        <!-- Light status bar icons -->
        <item name="android:windowLightStatusBar">false</item>
    </style>

</resources>
```

### night\themes.xml

```
<?xml version="1.0" encoding="utf-8"?>
<resources xmlns:tools="http://schemas.android.com/tools">

    <style name="Theme.Calculator"
        parent="Theme.Material3.DayNight.NoActionBar">
        <!-- Primary Colors -->
        <item name="colorPrimary">@color/operatorButton</item>
        <item name="colorPrimaryContainer">@color/operatorButton</item>
        <!-- Background -->
        <item name="android:windowBackground">@color/background</item>
        <!-- Status Bar -->
        <item name="android:statusBarColor">@color/background</item>
        <item name="android:navigationBarColor">@color/background</item>
        <!-- Dark mode -->
        <item name="android:windowLightStatusBar">false</item>
    </style>

</resources>
```

### MainActivity.java

```
package com.example.calculator;

import android.os.Bundle;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

import java.util.Locale;

public class MainActivity extends AppCompatActivity {

    private TextView txtResult;

    private String firstNumber = "";
    private String secondNumber = "";
    private String operator = "";

    private boolean isSecondNumber = false;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        txtResult = findViewById(R.id.txtResult);

        // Number Buttons
        int[] numberButtons = {
                R.id.btn0, R.id.btn00, R.id.btn1, R.id.btn2, R.id.btn3,
                R.id.btn4, R.id.btn5, R.id.btn6, R.id.btn7, R.id.btn8, R.id.btn9
        };

        for (int id : numberButtons) {
            Button btn = findViewById(id);
            if (btn != null) {
                btn.setOnClickListener(v -> {
                    animateButton(btn);
                    appendNumber(btn.getText().toString());
                });
            }
        }

        // Decimal Button
        Button btnDot = findViewById(R.id.btnDot);
        if (btnDot != null) {
            btnDot.setOnClickListener(v -> {
                animateButton(btnDot);
                appendDot();
            });
        }

        // Operator Buttons
        setupOperatorButton(R.id.btnPlus, "+");
        setupOperatorButton(R.id.btnMinus, "-");
        setupOperatorButton(R.id.btnMultiply, "×");
        setupOperatorButton(R.id.btnDivide, "÷");

        // Percentage
        Button btnPercent = findViewById(R.id.btnPercent);
        if (btnPercent != null) {
            btnPercent.setOnClickListener(v -> {
                animateButton(btnPercent);
                percentage();
            });
        }

        // Clear
        Button btnC = findViewById(R.id.btnC);
        if (btnC != null) {
            btnC.setOnClickListener(v -> {
                animateButton(btnC);
                clear();
            });
        }

        // Delete
        Button btnDel = findViewById(R.id.btnDel);
        if (btnDel != null) {
            btnDel.setOnClickListener(v -> {
                animateButton(btnDel);
                deleteLast();
            });
        }

        // Equal
        Button btnEqual = findViewById(R.id.btnEqual);
        if (btnEqual != null) {
            btnEqual.setOnClickListener(v -> {
                animateButton(btnEqual);
                calculate();
            });
        }
    }

    private void setupOperatorButton(int id, String op) {
        Button btn = findViewById(id);
        if (btn != null) {
            btn.setOnClickListener(v -> {
                animateButton(btn);
                setOperator(op);
            });
        }
    }

    // Button Press Animation
    private void animateButton(Button button) {
        button.animate()
                .scaleX(0.90f)
                .scaleY(0.90f)
                .setDuration(80)
                .withEndAction(() ->
                        button.animate()
                                .scaleX(1f)
                                .scaleY(1f)
                                .setDuration(80)
                                .start())
                .start();
    }

    // Append Numbers
    private void appendNumber(String number) {
        if (!isSecondNumber) {
            if (firstNumber.equals("0")) {
                if (number.equals("0") || number.equals("00")) return;
                firstNumber = number;
            } else {
                firstNumber += number;
            }
        } else {
            if (secondNumber.equals("0")) {
                if (number.equals("0") || number.equals("00")) return;
                secondNumber = number;
            } else {
                secondNumber += number;
            }
        }
        updateDisplay();
    }

    // Decimal Point
    private void appendDot() {
        if (!isSecondNumber) {
            if (!firstNumber.contains(".")) {
                if (firstNumber.isEmpty()) firstNumber = "0";
                firstNumber += ".";
            }
        } else {
            if (!secondNumber.contains(".")) {
                if (secondNumber.isEmpty()) secondNumber = "0";
                secondNumber += ".";
            }
        }
        updateDisplay();
    }

    // Set Operator
    private void setOperator(String op) {
        if (firstNumber.isEmpty()) return;
        
        // If we already have a second number, calculate first (chaining)
        if (!secondNumber.isEmpty()) {
            calculate();
        }
        
        operator = op;
        isSecondNumber = true;
        updateDisplay();
    }

    // Calculate Result
    private void calculate() {
        if (firstNumber.isEmpty() || secondNumber.isEmpty() || operator.isEmpty()) {
            return;
        }

        try {
            double num1 = Double.parseDouble(firstNumber);
            double num2 = Double.parseDouble(secondNumber);
            double result;

            switch (operator) {
                case "+": result = num1 + num2; break;
                case "-": result = num1 - num2; break;
                case "×": result = num1 * num2; break;
                case "÷":
                    if (num2 == 0) {
                        Toast.makeText(this, "Cannot divide by zero", Toast.LENGTH_SHORT).show();
                        return;
                    }
                    result = num1 / num2;
                    break;
                default: return;
            }

            String answer = formatResult(result);
            txtResult.setText(answer);

            // Prepare for next calculation
            firstNumber = answer;
            secondNumber = "";
            operator = "";
            isSecondNumber = false;
        } catch (Exception e) {
            Toast.makeText(this, "Error in calculation", Toast.LENGTH_SHORT).show();
        }
    }

    private String formatResult(double result) {
        if (result == (long) result) {
            return String.valueOf((long) result);
        } else {
            return String.format(Locale.US, "%g", result).replaceFirst("0+$", "").replaceFirst("\\.$", "");
        }
    }

    // Percentage
    private void percentage() {
        String target = isSecondNumber && !secondNumber.isEmpty() ? secondNumber : firstNumber;
        if (target.isEmpty()) return;

        try {
            double value = Double.parseDouble(target) / 100.0;
            String answer = formatResult(value);
            
            if (isSecondNumber && !secondNumber.isEmpty()) {
                secondNumber = answer;
            } else {
                firstNumber = answer;
            }
            updateDisplay();
        } catch (Exception ignored) {}
    }

    // Delete Last Character
    private void deleteLast() {
        if (!isSecondNumber) {
            if (!firstNumber.isEmpty()) {
                firstNumber = firstNumber.substring(0, firstNumber.length() - 1);
            }
        } else {
            if (!secondNumber.isEmpty()) {
                secondNumber = secondNumber.substring(0, secondNumber.length() - 1);
            } else {
                operator = "";
                isSecondNumber = false;
            }
        }
        updateDisplay();
    }

    // Clear Calculator
    private void clear() {
        firstNumber = "";
        secondNumber = "";
        operator = "";
        isSecondNumber = false;
        updateDisplay();
    }

    private void updateDisplay() {
        if (!isSecondNumber) {
            txtResult.setText(firstNumber.isEmpty() ? "0" : firstNumber);
        } else {
            String display = firstNumber + " " + operator + (secondNumber.isEmpty() ? "" : " " + secondNumber);
            txtResult.setText(display);
        }
    }
}
```

### AndroidManifest.xml

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.Calculator">

        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>
                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## OUTPUT:

### Starting Page

<img width="1919" height="1079" alt="exp5op1" src="https://github.com/user-attachments/assets/9f99f369-bd02-4ade-8c1b-825df1ced29b" />

### Basic Calculation - Addition

<img width="1919" height="1079" alt="exp5op2" src="https://github.com/user-attachments/assets/0614a745-1d8c-43e3-ac3c-fbf634b5fa19" />

<img width="1919" height="1079" alt="exp5op3" src="https://github.com/user-attachments/assets/989ddc3e-268e-496f-b5ea-56c7c8764a79" />

### Basic Calculation - Subtraction

<img width="1919" height="1079" alt="exp5op4" src="https://github.com/user-attachments/assets/ea5f210a-6b36-4703-965a-c4a22366f643" />

<img width="1919" height="1079" alt="exp5op5" src="https://github.com/user-attachments/assets/511124df-2b11-4f4a-9a1e-2eb4dc94a498" />

### Basic Calculation - Multiplication

<img width="1919" height="1079" alt="exp5op6" src="https://github.com/user-attachments/assets/88c4ffba-1091-4e73-be3f-3cbcfdbadfcf" />

<img width="1919" height="1079" alt="exp5op7" src="https://github.com/user-attachments/assets/20857eac-39bc-4779-b13a-5a20ffad0296" />

### Basic Calculation - Division

<img width="1919" height="1079" alt="exp5op8" src="https://github.com/user-attachments/assets/227936bf-7192-4034-babe-994390a1345e" />

<img width="1919" height="1079" alt="exp5op9" src="https://github.com/user-attachments/assets/3a73e181-25cb-49dd-8d5b-e8023dcc07de" />

## RESULT:
Thus, a Simple Android Application create a simple calculator using Android Studio is developed and executed successfully.
