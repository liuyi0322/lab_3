# UI组件用法演示
本教程将演示几组Android UI组件的用法  

首先是导航页面，添加几个按钮跳转到不同的界面演示不同UI组件的用法： 

![导航界面](https://github.com/llfjfz/AndroidTutorials/blob/master/UiComponentTutorials/screenshots/1.png)  

SimpleAdapterDemo演示SimpleAdapter的用法；CustomDialogDemo演示自定义对话框的实现；XmlMenuDemo演示如何使用xml文件定义菜单；AcitonModeContextDemo演示如何使用ACtionMode形式的上下文菜单；ProgressBarDemo演示如何使用ProgressBar组件。

## SimpleAdapter用来装配ListView的用法
![SimpleAdapter](https://github.com/llfjfz/AndroidTutorials/blob/master/UiComponentTutorials/screenshots/simpleadapter.png)

本界面演示了SimpleAdapter用来装配ListView的用法。ListView每个Item的布局采用相对布局，包含一个ImageView和一个TextView，并且指定ImageView对齐父类布局的右侧。

**注意：ListView条目单击显示颜色可以指定其listSelector属性。**  

    <ListView
        android:id="@+id/simpleListView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:divider="#000"
        android:dividerHeight="2dp"
        android:listSelector="#600"/>

## 自定义对话框的实现
![CustomDialog](https://github.com/llfjfz/AndroidTutorials/blob/master/UiComponentTutorials/screenshots/dialog.png)

自定义对话框使用getLayoutInflater()获取LayoutInflater实例，并利用LayoutInflater的inflate()方法从自定义布局文件中加载对话框的布局，从而实现自定义对话框。对话框的布局如下：

    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    	android:orientation="vertical"
    	android:layout_width="wrap_content"
    	android:layout_height="wrap_content">
	    <ImageView
	        android:src="@drawable/header_logo"
	        android:layout_width="match_parent"
	        android:layout_height="64dp"
	        android:scaleType="center"
	        android:background
