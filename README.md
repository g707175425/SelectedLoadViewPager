#SelectedLoadViewPager
####(切换到指定页再加载数据的ViewPager,比直接用onPageSelected方法做处理更流畅,页面不再发生卡顿)

###预览效果:
![](https://github.com/g707175425/SelectedLoadViewPager/blob/master/selectedloadviewpager.gif)

###代码中实现:

####1.在XML中引入
```
	<cn.schope.lightning.view.SelectedLoadViewPager
        android:id="@+id/vp_list"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
```
####2.在代码中监听页面改变事件,在监听中刷新数据
```
	vp_list.setOnPageSelectedFlushListener(new SelectedLoadViewPager.OnPageSelectedFlushListener() {
			@Override
			public void onPageSelected(int position) {
				flushData(position);
			}
		});
```

by QQ:707175425
