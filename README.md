# Ex.No:12 Design an application that draws basic graphical primitives on the screen.
# AIM:
To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

# EQUIPMENTS REQUIRED:
Android Studio(Latest Version)

# ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

# PROGRAM:
/*
Program to create and design an android application that draws basic graphical primitives on the screen.

Developed by:VISHNU PRIYA.S

Registeration Number :212221040181
*/
# activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout android:layout_height="match_parent"
    android:layout_width="match_parent"
    xmlns:android="http://schemas.android.com/apk/res/android">
    <ImageView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:id="@+id/ImageView"/>
</RelativeLayout>
```
# MainActivity.java
```
package com.example.graphical;

import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        //Creating a Bitmap
        Bitmap bg = Bitmap.createBitmap(720, 1280,
                Bitmap.Config.ARGB_8888);
        //Setting the Bitmap as background for the ImageView
        ImageView i = (ImageView) findViewById(R.id.ImageView);
        i.setBackgroundDrawable(new BitmapDrawable(bg));
        //Creating the Canvas Object
        Canvas canvas = new Canvas(bg);
        //Creating the Paint Object and set its color & TextSize
        Paint paint = new Paint();
        paint.setColor(Color.BLACK);
        paint.setTextSize(50);
        //To draw a Rectangle
        canvas.drawText("Rectangle", 420, 150, paint);
        canvas.drawRect(400, 200, 650, 700, paint);
        //To draw a Circle
        canvas.drawText("Circle", 120, 150, paint);
        canvas.drawCircle(200, 350, 150, paint);
        //To draw a Square
        canvas.drawText("Square", 120, 800, paint);
        canvas.drawRect(50, 850, 350, 1150, paint);
        //To draw a Line
        canvas.drawText("Line", 480, 800, paint);
        canvas.drawLine(520, 850, 520, 1150, paint);

    }
}
```
# OUTPUT
![image](https://github.com/vishnupriya20052004/Graphical_Primitives/assets/133640291/31ed3d98-c969-4211-9a9e-74a5439a8713)


![image](https://github.com/vishnupriya20052004/Graphical_Primitives/assets/133640291/b60a96c3-9d4d-486b-b98a-d20e1f27c289)


![image](https://github.com/vishnupriya20052004/Graphical_Primitives/assets/133640291/b997cab9-9911-461e-940f-f18ddb85b5b9)


# RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
