# 四则运算
#请编一个小软件，实现四则运算（《构建之法》中开篇的题目），并具有以下功能：
（1）能根据题目回答情况，自动判别答案的正误，完成最后总成绩的统计、输出；
（2）题目不要出现重复；
（3）可定制题目数量和打印方式；
（4）可以控制下列参数：是否有乘除法、是否有括号、数值范围、加减法有无负数、除法有无余数、是否支持分数（真分数、假分数......）、是否支持小数（精确到多少位）、打印时每行的间隔

#扩展要求：
（5）支持二元一次方程；
（6）能开根号；
（7）能按指定范围和要求生成期中、期末试卷；
（8）做成手机app应用程序；
（9）做成台式机上的服务器模式；
......


### 部分代码
```
<?xml version="1.0" encoding="utf-8"?>
<android.support.v7.widget.LinearLayoutCompat xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="5dp"
    tools:context="homework.calc.MainActivity">

    <GridLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:columnCount="3"
        android:orientation="horizontal">

        <android.support.v7.widget.AppCompatCheckBox
            android:id="@+id/check_box_mul_and_divide"
            android:text="乘除法" />

        <android.support.v7.widget.AppCompatCheckBox
            android:id="@+id/check_box_bracket"
            android:text="括号" />

        <android.support.v7.widget.AppCompatCheckBox
            android:id="@+id/check_box_negative"
            android:text="负数" />

        <android.support.v7.widget.AppCompatCheckBox
            android:id="@+id/check_box_remains"
            android:text="除法余数" />

        <android.support.v7.widget.AppCompatCheckBox
            android:id="@+id/check_box_fraction"
            android:text="分数" />

        <android.support.v7.widget.AppCompatCheckBox
            android:id="@+id/check_box_decimal"
            android:text="小数" />
    </GridLayout>

    <android.support.v7.widget.LinearLayoutCompat
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">


        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="数值范围" />

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">

            <EditText
                android:id="@+id/minimum_value"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:gravity="center"
                android:inputType="numberSigned"
                android:text="-10" />

            <TextView
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:gravity="center"
                android:text="~" />

            <EditText
                android:id="@+id/maximum_value"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:gravity="center"
                android:inputType="numberSigned"
                android:text="10" />
        </LinearLayout>


        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="打印行间隔" />

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal">

            <TextView
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:gravity="center"
                android:text="1" />

            <SeekBar
                android:id="@+id/line_space"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="5"
                android:max="100" />

            <TextView
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:gravity="center"
                android:text="100" />
        </LinearLayout>
    </android.support.v7.widget.LinearLayoutCompat>

    <android.support.v7.widget.LinearLayoutCompat
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:id="@+id/button_generate"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="生成" />

        <Button
            android:id="@+id/button_check"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="提交" />
    </android.support.v7.widget.LinearLayoutCompat>


    <ListView
        android:id="@+id/list_questions"
        android:layout_width="match_parent"
        android:layout_height="match_parent"></ListView>

</android.support.v7.widget.LinearLayoutCompat>
```

### PSP表格
![Image text](https://github.com/Jenson66/sizeyunsuan/sizeyunsuan/PSP.png)

