﻿Android Pulley Menu
==========

Pulley menu is an alternate to traditional Menu which allows user to select any option for an activity intuitively. The menu is revealed by dragging the screen downwards and in that gesture user can also select any of the options. 


This Libraray has been implemented in the following android applications :-

[Pulley Menu Demo][2] 


Please drop a mail at ans_hul_1994@yahoo.co.in if you are using it in your application so that it can be listed here.


ScreenShots
=====

![Alt text](https://lh4.ggpht.com/kn6a9FJ0ywIQfhOEfa-pCDgT55O-RzPaq2Ht6AEBgTvK6K0avsAZf7Tnteopt7xrnhg=h310-rw ) 
....
![Alt text](https://lh5.ggpht.com/jX2cyhj39Pk2Qr0PM8sY6LkLvOA-w6wDiyVfIgjc7Jrt-332PO63GYa7tRIXYflUKg=h310-rw ).....
![Alt text](https://lh6.ggpht.com/ekTeiHHF77VIqCKU7QCOgMnzsEubGd0PZ4ZqSIIQIdpoVOwhljintGkoXalL4GbS1hpF=h310-rw )

Usage
=====

This library is very simple to use. It requires no extension of custom classes,
it's simply added to an activity by calling the method  

PulleyMenu(Context,ParentView,Menuview,Normal Background Color,Highlighted Color)`
methods.

For examples on how to use this library, check out the sample app.


Sample Call
-------
```java
	final ListView menuview = new ListView(this);
		menuview.setPadding(0, 30 , 0, 0);

		ArrayList<String> list = new ArrayList<String>();
		list.add("Start");
		list.add("Stop");
		list.add("Reset");

		anshul.pulleymenu.CustomListViewAdapter adapter = new anshul.pulleymenu.CustomListViewAdapter(this,
				android.R.layout.simple_list_item_1, list);
		menuview.setAdapter(adapter);
		menuview.setOnItemClickListener(this);
		int color1 = Color.WHITE;
		int color2 = Color.argb(255, 50, 255, 255);
		pulleymenu = new anshul.pulleymenu.PulleyMenu(this,R.layout.activity_topmenu,menuview,color1,color2);
```
-------

Including in your project
=========================

Include it in your project as an android library project.
Please take care of the following points:-

1. The target build should be kept at Android 4.0 though it will work with previous versions too

Credits
=======

 * Cyril Mottier for his [articles][1] on this pattern
 * Simon VT for his library [Android menu Drawer][3]


License
=======

    Copyright 2013 Anshul Bansal

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


[1]: http://android.cyrilmottier.com/?p=658
[2]: https://play.google.com/store/apps/details?id=net.anshul.pulleymenu.samples
[3]: https://github.com/SimonVT/android-menudrawer
