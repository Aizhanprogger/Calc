package com.example.fwd.myapplication;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity implements View.OnClickListener {

    Double d;
    Double j;
    String simbol;
    TextView a;
    Button b1;
    Button b2;
    Button b3;
    Button b4;
    Button b5;
    Button b6;
    Button b7;
    Button b8;
    Button b9;
    Button b10;
    Button b11;
    Button b12;
    Button b13;
    Button b14;
    Button b100;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        a=(TextView)findViewById(R.id.textView);
        b1=(Button)findViewById(R.id.button1);
        b2=(Button)findViewById(R.id.button2);
        b3=(Button)findViewById(R.id.button3);
        b4=(Button)findViewById(R.id.button4);
        b5=(Button)findViewById(R.id.button5);
        b6=(Button)findViewById(R.id.button6);
        b7=(Button)findViewById(R.id.button7);
        b8=(Button)findViewById(R.id.button8);
        b9=(Button)findViewById(R.id.button9);
        b10=(Button)findViewById(R.id.button10);
        b11=(Button)findViewById(R.id.button11);
        b12=(Button)findViewById(R.id.button12);
        b13=(Button)findViewById(R.id.button13);
        b14=(Button)findViewById(R.id.button14);
        b100=(Button)findViewById(R.id.button100);

        a.setOnClickListener(this);
        b1.setOnClickListener(this);
        b2.setOnClickListener(this);
        b3.setOnClickListener(this);
        b4.setOnClickListener(this);
        b5.setOnClickListener(this);
        b6.setOnClickListener(this);
        b7.setOnClickListener(this);
        b8.setOnClickListener(this);
        b9.setOnClickListener(this);
        b10.setOnClickListener(this);
        b11.setOnClickListener(this);
        b12.setOnClickListener(this);
        b13.setOnClickListener(this);
        b14.setOnClickListener(this);
        b11.setOnClickListener(this);
        b100.setOnClickListener(this);




    }

    @Override
    public void onClick(View v) {
        String c=a.getText().toString();
        switch (v.getId()){
            case R.id.button1:
                a.setText(c+b1.getText()); break;
            case R.id.button2:
                a.setText(c+b2.getText()); break;
            case R.id.button3:
                a.setText(c+b3.getText()); break;
            case R.id.button4:
                a.setText(c+b4.getText()); break;
            case R.id.button5:
                a.setText(c+b5.getText()); break;
            case R.id.button6:
                a.setText(c+b6.getText()); break;
            case R.id.button7:
                a.setText(c+b7.getText()); break;
            case R.id.button8:
                a.setText(c+b8.getText()); break;
            case R.id.button9:
                a.setText(c+b9.getText()); break;
            case R.id.button100:
                a.setText(c+b100.getText()); break;
            case R.id.button10:
                simbol="/";
                d=Double.parseDouble(a.getText().toString());
                a.setText("");
                 break;
            case R.id.button11:
                simbol="*";
                d=Double.parseDouble(a.getText().toString());
                a.setText("");
                break;
            case R.id.button12:
                simbol="-";
                d=Double.parseDouble(a.getText().toString());
                a.setText("");
                break;
            case R.id.button13:
                simbol="+";
                d=Double.parseDouble(a.getText().toString());
                a.setText("");
                break;
            case R.id.button14:
                j=Double.parseDouble(a.getText().toString());
                double rez=0;
                switch (simbol){
                    case "/": rez=d/j;
                    break;
                    case "*": rez=d*j;
                        break;
                    case "-": rez=d-j;
                        break;
                    case "+": rez=d+j;
                        break;
                }

                a.setText(Double.toString(rez));


        }
    }
}
