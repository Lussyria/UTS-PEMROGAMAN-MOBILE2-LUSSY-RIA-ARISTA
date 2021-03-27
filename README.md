# UTS-PEMROGAMAN-MOBILE2-LUSSY-RIA-ARISTA
Coding program yang menampilkan menu utama dari sebuah aplikasi yang menggunakan gridview dan routing ke halaman lainnya


coding activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

coding menu.xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto">
<item
    android:id="@+id/keranjang"
    android:icon="@drawable/keranjang_icon"
    android:title="Keranjang"
    app:showAsAction="always"/>
    <item
        android:id="@+id/kontak"
        android:title="kontak"
        app:showAsAction="never"/>
    <item
        android:id="@+id/nama"
        android:title="nama"
        app:showAsAction="never"/>
    <item
        android:id="@+id/alamat"
        android:title="alamat"
        app:showAsAction="never"/>
    <item
        android:id="@+id/nirm"
        android:title="nirm"
        app:showAsAction="never"/>
    <item
        android:id="@+id/jurusan"
        android:title="jurusan"
        app:showAsAction="never"/>
    <item
        android:id="@+id/kelas"
        android:title="kelas"
        app:showAsAction="never"/>
    <item
        android:id="@+id/matakuliah"
        android:title="mata kuliah"
        app:showAsAction="never"/>



</menu>

coding mainActivity.Java
package com.example.lussyriaarista;

import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.menu,menu);
        return super.onCreateOptionsMenu(menu);
    }

    @Override
    public boolean onOptionsItemSelected(@NonNull MenuItem item) {
        setMode(item.getItemId());
        return super.onOptionsItemSelected(item);
    }

    public void setMode(int selectedMode) {
        switch (selectedMode) {
            case R.id.kontak:
                Toast.makeText(this, "Hubungi saya di 0812 6530 4724", Toast.LENGTH_LONG).show();
                break;
            case R.id.nama:
                Toast.makeText(this, "Perkenalkan Nama Saya Lussy Ria Arista", Toast.LENGTH_LONG).show();
                break;
            case R.id.alamat:
                Toast.makeText(this, "Jl.Luku 1 kwala bekala, medan johor", Toast.LENGTH_LONG).show();
                break;
            case R.id.nirm:
                Toast.makeText(this, "2018020162", Toast.LENGTH_LONG).show();
                break;
            case R.id.jurusan:
                Toast.makeText(this, "Sistem Informasi", Toast.LENGTH_LONG).show();
                break;
            case R.id.kelas:
                Toast.makeText(this, "6SIA10", Toast.LENGTH_LONG).show();
                break;
            case R.id.matakuliah:
                Toast.makeText(this, "Pemrogaman Mobile2", Toast.LENGTH_LONG).show();
                break;

        }


    }  
   
