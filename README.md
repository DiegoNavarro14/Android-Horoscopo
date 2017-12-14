# Android-Horoscopo
Horoscopo con base de datos

Activity_inicio

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context="com.example.sixgu.horoscopod.Inicio">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Horoscopo"
        android:layout_gravity="center"
        android:textSize="50dp"
        android:layout_marginTop="50dp"
        android:textColor="@color/azul"
        />

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Ingresar"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="50dp"
        android:layout_marginRight="30dp"
        android:background="@color/azul"
        android:id="@+id/BtnIngresar"/>

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Registrarse"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="50dp"
        android:layout_marginRight="30dp"
        android:background="@color/azul"
        android:id="@+id/BtnRegistrarse"/>

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Eliminar"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="50dp"
        android:layout_marginRight="30dp"
        android:background="@color/azul"
        android:id="@+id/BtnEliminar"/>

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Modificar"
        android:layout_marginLeft="30dp"
        android:layout_marginTop="50dp"
        android:layout_marginRight="30dp"
        android:background="@color/azul"
        android:id="@+id/BtnModificar"/>

</LinearLayout>

Main activity Inicio

package com.example.sixgu.horoscopod;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class Inicio extends AppCompatActivity {
    Button BtnRegistrarse,BtnIngresar,BtnModificar,BtnEliminar;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_inicio);
        BtnRegistrarse=(Button)findViewById(R.id.BtnRegistrarse);
        BtnIngresar=(Button)findViewById(R.id.BtnIngresar);
        BtnEliminar=(Button)findViewById(R.id.BtnEliminar);
        BtnModificar=(Button)findViewById(R.id.BtnModificar);

        BtnRegistrarse.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                startActivity(new Intent(Inicio.this,Registro.class));
            }
        });

        BtnIngresar.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                startActivity(new Intent(Inicio.this,Ingreso.class));
            }
        });

        BtnEliminar.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                startActivity(new Intent(Inicio.this,BorrarUsuario.class));
            }
        });

        BtnModificar.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                startActivity(new Intent(Inicio.this,ModificarUsuario.class));
            }
        });


    }
}


