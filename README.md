# 实验二——安卓布局
## 实验目的 ：学习网络上ConstraintLayout, LinearLayout和TableLayout的相关内容
## 实验环境
Android Studio3.2
## 实验步骤
在res的layout目录下新建你所需要的.xml文件
### 一、利用线性布局实现
实验重要源码：
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="#000">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:padding="2dp">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,One"
            android:layout_weight="1" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Two"
            android:layout_weight="1"/>

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Three"
            android:layout_weight="1"/>

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Four"
            android:layout_weight="1"/>
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,One"
            android:layout_weight="1"/>

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Two"
            android:layout_weight="1"/>

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Three"
            android:layout_weight="1"/>

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Four"
            android:layout_weight="1"/>
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Three,One"/>

        <Button
            android:id="@+id/button10"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Three,Two" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Three,Three" />

        <Button
            android:layout_width="79dp"
            android:layout_height="wrap_content"
            android:text="Three,Four"/>
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,One" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,Two" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,Three" />

        <Button
            android:layout_width="116dp"
            android:layout_height="wrap_content"
            android:text="Four,Four" />
    </LinearLayout>
</LinearLayout>`
**源码调用**

```
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}
```
### 实验结果
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190319104735370.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2M4MTU4NTI1MTc=,size_16,color_FFFFFF,t_70)
## 二、利用ConstraintLayout实现如下界面
源码 `<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#000">

    <Button
        android:layout_width="172dp"
        android:layout_height="150dp"
        android:background="#FF0000"
        android:text="RED"
        tools:layout_editor_absoluteX="0dp"
        tools:layout_editor_absoluteY="0dp" />

    <Button
        android:layout_width="185dp"
        android:layout_height="164dp"
        android:background="#FF6100"
        android:text="ORANGE"
        tools:layout_editor_absoluteX="557dp"
        tools:layout_editor_absoluteY="3dp" />

    <Button
        android:layout_width="174dp"
        android:layout_height="164dp"
        android:background="#00FF00"
        android:text="GREEN"
        tools:layout_editor_absoluteX="345dp"
        tools:layout_editor_absoluteY="249dp" />

    <Button
        android:layout_width="168dp"
        android:layout_height="161dp"
        android:background="#0000FF"
        android:text="BLUE"
        tools:layout_editor_absoluteX="568dp"
        tools:layout_editor_absoluteY="250dp" />

    <Button
        android:layout_width="161dp"
        android:layout_height="161dp"
        android:background="#A020F0"
        android:text="INDIGO"
        tools:layout_editor_absoluteX="789dp"
        tools:layout_editor_absoluteY="252dp" />

    <Button
        android:layout_width="154dp"
        android:layout_height="153dp"
        android:background="#fff000"
        android:text="YELLOW"
        tools:layout_editor_absoluteX="1122dp"
        tools:layout_editor_absoluteY="0dp" />

    <Button
        android:layout_width="1275dp"
        android:layout_height="104dp"
        android:background="#FFC0CB"
        android:text="VIOLET"
        tools:layout_editor_absoluteX="3dp"
        tools:layout_editor_absoluteY="561dp" />
        </android.support.constraint.ConstraintLayout>
**源码调用**

```
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.constraintlayout);
    }
}
```

### 实验结果
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190319105215244.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2M4MTU4NTI1MTc=,size_16,color_FFFFFF,t_70)
## 三、利用表格布局实现如下界面
源码：`<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:stretchColumns="1"
    android:background="#000000">

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Open..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-O"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>

    </TableRow>

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Save..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-S"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>
    </TableRow>

    <TableRow>
        <TextView
            android:layout_column="1"
            android:text="Save As..."
            android:padding="3dip"
            android:textColor="#ffffff"/>
        <TextView
            android:text="Ctrl-Shift-S"
            android:gravity="right"
            android:padding="3dip"
            android:textColor="#ffffff"/>
    </TableRow>

    <View
        android:layout_height="2dip"
        android:background="#ffffff"/>
    <TableRow>
        <TextView
            android:text="X"
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Import..."
            android:textColor="#ffffff"
            android:padding="3dip"/>
    </TableRow>
    <TableRow>
        <TextView
            android:text="X"
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Emport..."
            android:textColor="#ffffff"
            android:padding="3dip"/>
        <TextView
            android:text="Ctrl-E"
            android:gravity="right"
            android:textColor="#ffffff"
            android:padding="3dip"/>
    </TableRow>
    <View
        android:layout_height="2dip"

        android:background="#ffffff"/>
    <TableRow>
        <TextView
            android:layout_column="1"
            android:textColor="#ffffff"
            android:text="Quit"
            android:padding="3dip"/>
    </TableRow>
</TableLayout>
**源码调用**

```
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.tablelayout);
    }
}

```
### 实验结果
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190319105406855.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2M4MTU4NTI1MTc=,size_16,color_FFFFFF,t_70)
