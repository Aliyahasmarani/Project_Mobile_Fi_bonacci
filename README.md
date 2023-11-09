# Project_Mobile_Fi_bonacci

# TUGAS PERTAMA

## 1. Buatlah code pada layout (.xml) yang berisikan sbb:

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:padding="10dp"
    tools:context="com.example.fibonacci.Fibonacci">

    <Button
        android:id="@+id/button_toast"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:background="@color/colorPrimary"
        android:text="Toast"
        android:textColor="@android:color/white"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:onClick="showtoast" />


    <Button
        android:id="@+id/button_count"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginBottom="8dp"
        android:background="@color/colorPrimary"
        android:onClick="countUp"
        android:text="Count"
        android:textColor="@android:color/white"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />
    <TextView
        android:id="@+id/show_count"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginStart="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginBottom="8dp"
        android:background="#FFFF00"
        android:gravity="center_vertical"
        android:text="0"
        android:textAlignment="center"
        android:textColor="@color/colorPrimary"
        android:textSize="160sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toTopOf="@+id/button_count"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button_toast" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
### HASIL DARI CODE LAYOUT DESIGN:

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/684d9b30-53b3-424b-813b-da7c50588764)

## 2. Selanjutnya, Menyiapkan Activity (java) Untuk Fibonacci:

### Berikut code yang saya buat:

```
package com.example.fibonacci;

import android.os.Bundle;
import android.view.View;
import android.widget.TextView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class Fibonacci extends AppCompatActivity {
    int first = 0;
    int second = 1;
    TextView Fibonacci;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Fibonacci = findViewById(R.id.show_count);
        updateFibonacciText();
    }

    public void showToast(View view) {
        Toast.makeText(this, "Fibonacci", Toast.LENGTH_SHORT).show();
    }

    public void countUp(View view) {
        int next = first + second;
        first = second;
        second = next;
        updateFibonacciText();
    }

    private void updateFibonacciText() {
        Fibonacci.setText(Integer.toString(first));
    }
}
```

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/673770a3-2f30-4620-8a54-8573103c038f)

### HASIL DARI CODE ACTIVITY DIATAS :

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/bea6f4e3-f445-4d36-a56e-dd965bc15d28)

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/1866abb9-4c10-4dfe-9e01-6ee2800032f8)

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/3ab0876e-00c6-4264-9674-c864c9070d6d)

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/26890147-ed5b-406c-ac0f-fdccf36323c4)

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/6473f075-0b65-4d8e-a76a-c32d2f146472)

![image](https://github.com/Aliyahasmarani/Project_Mobile_Fi_bonacci/assets/115197672/b3d098b5-9441-4bcb-9bd1-a97649704730)










