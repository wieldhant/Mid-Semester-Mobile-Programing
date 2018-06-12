# Mid-Semester-Mobile-Programing
program Calculator
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
                xmlns:tools="http://schemas.android.com/tools"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:paddingBottom="@dimen/activity_vertical_margin"
                android:paddingLeft="@dimen/activity_horizontal_margin"
                android:paddingRight="@dimen/activity_horizontal_margin"
                android:paddingTop="@dimen/activity_vertical_margin"
                tools:context=".MainActivity">
 
    <EditText
        android:id="@+id/result_id"
        android:layout_width="match_parent"
        android:layout_height="70dp" />
 
    <Button
        android:id="@+id/Btn7_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/result_id"
        android:onClick="btn7Clicked"
        android:text="7" />
 
    <Button
        android:id="@+id/Btn8_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/result_id"
        android:layout_toRightOf="@id/Btn7_id"
        android:onClick="btn8Clicked"
        android:text="8" />
 
    <Button
        android:id="@+id/Btn9_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/result_id"
        android:layout_toRightOf="@id/Btn8_id"
        android:onClick="btn9Clicked"
        android:text="9" />
 
    <Button
        android:id="@+id/Btnclear_id"
        android:layout_width="90dp"
        android:layout_height="60dp"
        android:layout_below="@id/result_id"
        android:layout_toRightOf="@id/Btn9_id"
        android:onClick="btnclearClicked"
        android:text="clear" />
 
    <Button
        android:id="@+id/Btn4_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn7_id"
        android:onClick="btn4Clicked"
        android:text="4" />
 
    <Button
        android:id="@+id/Btn5_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn8_id"
        android:layout_toRightOf="@id/Btn4_id"
        android:onClick="btn5Clicked"
        android:text="5" />
 
    <Button
        android:id="@+id/Btn6_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn9_id"
        android:layout_toRightOf="@id/Btn5_id"
        android:onClick="btn6Clicked"
        android:text="6" />
 
    <Button
        android:id="@+id/Btnplus_id"
        android:layout_width="90dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btnclear_id"
        android:layout_toRightOf="@id/Btn6_id"
        android:onClick="btnplusClicked"
        android:text="+" />
 
    <Button
        android:id="@+id/Btn1_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn4_id"
        android:onClick="btn1Clicked"
        android:text="1" />
 
    <Button
        android:id="@+id/Btn2_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn5_id"
        android:layout_toRightOf="@id/Btn1_id"
        android:onClick="btn2Clicked"
        android:text="2" />
 
    <Button
        android:id="@+id/Btn3_id"
        android:layout_width="70dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn6_id"
        android:layout_toRightOf="@id/Btn2_id"
        android:onClick="btn3Clicked"
        android:text="3" />
 
    <Button
        android:id="@+id/Btnminus_id"
        android:layout_width="90dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btnplus_id"
        android:layout_toRightOf="@id/Btn3_id"
        android:onClick="btnminusClicked"
        android:text="-" />
 
    <Button
        android:id="@+id/Btnequal_id"
        android:layout_width="110dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn1_id"
        android:onClick="btnequalClicked"
        android:text="=" />
 
    <Button
        android:id="@+id/Btndivide_id"
        android:layout_width="90dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btn1_id"
        android:layout_toRightOf="@id/Btnequal_id"
        android:onClick="btndivideClicked"
        android:text="/" />
 
    <Button
        android:id="@+id/Btnmulti_id"
        android:layout_width="100dp"
        android:layout_height="60dp"
        android:layout_below="@id/Btnminus_id"
        android:layout_toRightOf="@id/Btndivide_id"
        android:onClick="btnmultiClicked"
        android:text="*" />
 
</RelativeLayout>
package com.okedroid.aplikasisaya;
 
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.view.View;
import android.widget.EditText;
 
 
public class MainActivity extends AppCompatActivity {
 
    public String str ="";
    Character op = 'q';
    float i,num,numtemp;
    EditText showResult;
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
 
        showResult = (EditText)findViewById(R.id.result_id);
 
    }
    public void btn1Clicked(View v){
        insert(1);
 
    }
 
    public void btn2Clicked(View v){
        insert(2);
 
    }
    public void btn3Clicked(View v){
        insert(3);
 
    }
    public void btn4Clicked(View v){
        insert(4);
 
    }
    public void btn5Clicked(View v){
        insert(5);
 
    }
    public void btn6Clicked(View v){
        insert(6);
    }
    public void btn7Clicked(View v){
        insert(7);
 
    }
    public void btn8Clicked(View v){
        insert(8);
 
    }
    public void btn9Clicked(View v){
        insert(9);
 
    }
    public void btnplusClicked(View v){
        perform();
        op = '+';
 
    }
 
    public void btnminusClicked(View v){
        perform();
        op = '-';
 
    }
    public void btndivideClicked(View v){
        perform();
        op = '/';
 
    }
    public void btnmultiClicked(View v){
        perform();
        op = '*';
 
    }
    public void btnequalClicked(View v){
        calculate();
 
    }
 
    public void btnclearClicked(View v){
        reset();
    }
    private void reset() {
        // TODO Auto-generated method stub
        str ="";
        op ='q';
        num = 0;
        numtemp = 0;
        showResult.setText("");
    }
    private void insert(int j) {
        // TODO Auto-generated method stub
        str = str+Integer.toString(j);
        num = Integer.valueOf(str).intValue();
        showResult.setText(str);
 
    }
    private void perform() {
        // TODO Auto-generated method stub
        str = "";
        calculateNoShow();
        numtemp = num;
 
    }
    private void calculate() {
        // TODO Auto-generated method stub
        if(op == '+')
            num = numtemp+num;
        else if(op == '-')
            num = numtemp-num;
        else if(op == '/')
            num = numtemp/num;
        else if(op == '*')
            num = numtemp*num;
        showResult.setText(""+num);
    }
 
    private void calculateNoShow() {
        // TODO Auto-generated method stub
        if(op == '+')
            num = numtemp+num;
        else if(op == '-')
            num = numtemp-num;
        else if(op == '/')
            num = numtemp/num;
        else if(op == '*')
            num = numtemp*num;
    }
}
