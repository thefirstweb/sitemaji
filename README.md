Sitemaji SDK
--

* Setup SDK
	
	* AndroidManifest.xml
	
	```
	<application android:hardwareAccelerated="true" ...>
	
	OR
	
	<activity android:hardwareAccelerated="true" ...>
	
	```
	
	* Import sitemaji-1.0.0.jar


* provider ad url size

```

```

* check suport ad szie 

```java
// Chcke is support ad size
int[] screenSize = SitemajiAdView.parseUrlSize(url);
boolean isSupport = SitemajiAdView.checkSupportSize(mContext, screenSize[0], screenSize[1]);
```

* enable log

```java
// Enable log
Sitemaji.setDebug(true);
```

```
08-16 17:52:41.311 18590-18590/showsky.com.tw.flurrydemo D/sitemaji: [SitemajiAdView] load page finish url: http://www.dm5.com/wxhfm.html?cid=1059&s=366x549
08-16 17:52:41.694 18590-18590/showsky.com.tw.flurrydemo D/sitemaji: [SitemajiAdView] load page finish url: http://www.dm5.com/wxhfm.html?cid=1059&s=320x480

```

* load adView from url

	* xml

	```xml
	<com.sitemaji.view.SitemajiAdView 
        android:id="@+id/sitemajiAdView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
	```
	
	```java
	SitemajiAdView sitemajiAdView = (SitemajiAdView) findViewById(R.id.sitemajiAdView);
	sitemajiAdView.loadUrl(url);
	```
	
	* programmatically
	
	```java
	SitemajiAdView sitemajiAdView = new SitemajiAdView(mContext);
	LinearLayout.LayoutParams params = new LinearLayout.LayoutParams(
	    LinearLayout.LayoutParams.WRAP_CONTENT,
	    LinearLayout.LayoutParams.WRAP_CONTENT
	);
	
	addView(sitemajiAdView, params);
	
	sitemajiAdView.loadUrl(url);
	```

