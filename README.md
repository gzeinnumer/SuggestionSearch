# SuggestionSearch

```java
public class MainActivity extends AppCompatActivity {
    String[] fruits = {"Apple", "Banana", "Cherry", "Date", "Grape", "Kiwi", "Mango", "Pear"};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        ArrayAdapter<String> adapter = new ArrayAdapter<>(this, android.R.layout.select_dialog_item, fruits);
        AutoCompleteTextView actv = findViewById(R.id.autoCompleteTextView);
        actv.setThreshold(1);//will start working from first character
        actv.setAdapter(adapter);//setting the adapter data into the AutoCompleteTextView
        actv.setTextColor(Color.RED);
    }
}
```

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout ...>

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentLeft="true"
        android:layout_alignParentTop="true"
        android:layout_marginTop="15dp"
        android:text="Name a fruit from (Apple Banana Cherry Date Grape Kiwi Mango Pear)"
        android:textAlignment="center" />

    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/textView"
        android:layout_alignParentLeft="true"
        android:layout_marginTop="17dp"
        android:ems="10"
        android:text="">

        <requestFocus />
    </AutoCompleteTextView>

</LinearLayout>
```

---

```
Copyright 2021 M. Fadli Zein
```