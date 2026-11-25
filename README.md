
# Ex.No:7 Design an application that draws basic graphical primitives on the screen.


## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by:Piyush Kumar
Registeration Number :212223220075
*/
```
## MainAvtivity.java
```
package com.example.graphics;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}
```
## DrawingView.java
```
package com.example.graphics;

import android.content.Context;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.Path;
import android.util.AttributeSet;
import android.view.View;

public class DrawingView extends View {

    Paint paint;

    public DrawingView(Context context) {
        super(context);
        init();
    }

    public DrawingView(Context context, AttributeSet attrs) {
        super(context, attrs);
        init();
    }

    public DrawingView(Context context, AttributeSet attrs, int defStyleAttr) {
        super(context, attrs, defStyleAttr);
        init();
    }

    private void init() {
        paint = new Paint();
        paint.setAntiAlias(true);
        paint.setStrokeWidth(5);
    }

    @Override
    protected void onDraw(Canvas canvas) {
        super.onDraw(canvas);

        // Draw Line
        paint.setColor(Color.RED);
        canvas.drawLine(50, 50, 300, 50, paint);

        // Draw Circle
        paint.setColor(Color.BLUE);
        canvas.drawCircle(150, 150, 50, paint);

        // Draw Rectangle
        paint.setColor(Color.GREEN);
        canvas.drawRect(50, 230, 250, 330, paint);

        // Draw Oval
        paint.setColor(Color.MAGENTA);
        canvas.drawOval(50, 370, 250, 450, paint);

        // Draw Triangle
        paint.setColor(Color.BLACK);

        Path path = new Path();
        path.moveTo(150, 480);
        path.lineTo(50, 600);
        path.lineTo(250, 600);
        path.close();

        canvas.drawPath(path, paint);
    }
}
```
## MainActivity.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="10dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:padding="15dp"
        android:text="Graphical Primitives"
        android:textSize="25sp"
        android:textStyle="bold" />

    <com.example.graphics.DrawingView
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</LinearLayout>
```

## OUTPUT
<img width="1915" height="1005" alt="image" src="https://github.com/user-attachments/assets/3ae20c08-a513-48b0-8656-e33240778ea1" />





## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
