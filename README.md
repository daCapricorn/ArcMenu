#ArcMenu & RayMenu
##ArcMenu

An android custom view which looks like the menu in [Path 2.0](https://path.com/) (for iOS).

![Preview](https://dl.dropbox.com/u/11369687/preview0.png)
![Preview](https://dl.dropbox.com/u/11369687/preview1.png)

##RayMenu
![Preview](https://dl.dropbox.com/u/11369687/raymenu.png)
##About

The user experience in [Path 2.0](https://path.com/) (for iOS) is amazing, but the android version miss much.

Just for fun, I try to realize the amazing menu for android, which could be equal to the iOS version's.

##Usage

If you want to use this library you must before all indicate to your application
that you want to use it by launching the following command from the root
directory of your application

```
$ android update project --library ../relative/path/to/the/library --path .
```
where the path is the relative path to the ``library`` directory in this repository.

To setup the menu:

``` java
ArcMenu menu = (ArcMenu) findViewById(R.id.arc_menu);

final int itemCount = ITEM_DRAWABLES.length;
for (int i = 0; i < itemCount; i++) {
	ImageView item = new ImageView(this);
	item.setImageResource(ITEM_DRAWABLES[i]);

	final int position = i;
	menu.addItem(item, new OnClickListener() {

		@Override
		public void onClick(View v) {
			Toast.makeText(MainActivity.this, "position:" + position, Toast.LENGTH_SHORT).show();
		}
	});// Add a menu item
}
```

If you want to change the default appearence for ArcMenu:

in **arc_menu.xml**

    custom:childSize="50px"
    custom:fromDegrees="0.0"
    custom:toDegrees="300.0"

or in **ArcMenu.java**

``` java    
arcLayout.setChildSize(50);
arcLayout.setArc(0.0f, 300.0f);    
```
##TODO

Use attribute like ``custom:childSize`` directly into ``RayMenu`` and ``ArcMenu`` XML declaration. Also
indicate the ``Drawable`` instances as sub elements of these tags.

##Author

**Capricorn**

I'm glad to make friends with the people who persist in faith and follow their dreams.

Please let me know you are around.

Google+: [+魔羯](https://plus.google.com/107460592910747948011)





