# Baitaptuan1_a42964_Tr-nTh-MaiHoa
package com.example.myapplication.tuan1;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;


import com.example.myapplication.R;

public class Tuan11MainActivity extends AppCompatActivity {
    //khai ba cac control
    EditText txt1, txt2;
    Button btn1;
    TextView tv1;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_tuan11_main);
        // anh xa control
        txt1 = findViewById(R.id.demo11txt1);
        txt2 = findViewById(R.id.demo11txt2);
        btn1 = findViewById(R.id.demo11Btn1);
        tv1 = findViewById(R.id.demo11Tv1);

        //xy ly su kien
        btn1.setOnClickListener(v->{
            //goi ham tinh tong
            tinhtong();
        });

    }
    //Dinh nghia ham
    private void tinhtong() {
        String str1 = txt1.getText().toString();
        float so1 = Float.parseFloat(str1); //chuyen du lieu sang so
        //lay du lieu nhap vao tu edittext2
        String str2 = txt2.getText().toString();
        float so2 = Float.parseFloat(str2);
        //tinh tong
        float tong = so1 + so2;
        //in kq ra man hinh

        tv1.setText(String.valueOf(tong));


    }

}
