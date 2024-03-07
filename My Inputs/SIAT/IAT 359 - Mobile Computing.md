---
created: 2023-12-31
status: 🔴
tags:
  - input
  - siat
links: "[[My Inputs]]"
professor: Helmine Serban
semester: Spring 2023
---
## Summary
### Context
- android app development course
### Main Takeaways
- when you flip your phone the app is destroyed and recreated whoa
- activity always running in background/on other threads
- phone functioning is not what you think!
### Questions/Connections/Thoughts
- 
## Notes


Lecture 1: Intro to Mobile Computing

  

First Mobile Information Platform:

1. clay or stone with markings
    
2. papyrus scroll and ink pen
    
3. printed book (1800)
    

  

Recent History of Mobile Information Platforms:

1. The Brick/Motorola DynaTAC 8000X (1983)
    

-first commercially available cell phone

-2.5 lbs, 30 minute battery life, $3,995

-not successful due to weight/short battery/price

2. Personal Digital Assistant (PDA)/Apple Newton (1987)
    

-first tablet with pen

-not great success but set in motion PDA development

-became iPhone in 2007 and iPad in 2010

3. Motorola Wireless Device/Envoy, Marco (1995)
    

-looks like a tablet with apps on literal desktop

Form Factor: (1995)

1. PDA: large, 2 hands
    
2. Palm-sized devices: introduced later
    

-used Palm OS

-later handheld form factor was common for many devices (Windows CE, WIndows entrance into PDA/mobile platform arena)

1999 - 2000: proliferation of handheld device experimentation with form factor

4. Telecommunication Industry: Nokia Communicator (1996)
    

-combined PDA features (clock, agenda, calendar, notes) and networked applications (telnet, phone, fax)

-clam shell design, qwerty keyboard

  

Initial Innovations:

1. Low power mobile processors
    
2. Higher quality/bigger displays
    

-gave promise as multimedia/gaming device

-disappearance of keyboard for multi-touch screens with intuitive input gestures

  

Initial Technologies:

1. Low-power meter accuracy GPS: allowing for location-based services
    
2. Embedded sensors providing higher level services to users
    

1. digital compass, proximity, acceleration
    
2. digital cameras, NFC sensor
    

  

Android: 

1. Mobile Operating System:
    

-based on Linux

-designed for mobile platforms

2. Application Framework:
    

-allow to create custom apps

-built for many screen sizes and versions of Android![](https://lh7-us.googleusercontent.com/VNvkqrjQSQekIIda73u7iSto98JExp0zyqq1tF2eiXaY3LdOdjQtQ2D1S6MS4sP8LD0qPpKYu7v3muTvl1uVcMC8V1i_aakD3X0Q3cQBSWeqp1kIzZ14WxnQhznlPZLtbEVCWP1sqSD84STu6iuVpKM)

Architecture:

1. Linux Kernel: drivers (where manufacturers spend time)
    
2. Hardware Abstraction Level (HAL): bridging hardware implemented in unique way to universal library able to be used without rewriting code
    
3.   
    

1. Native C/C++ Libraries: libraries for various functionalities to be reused
    
2. Android Runtime: app is own self-contained unit
    

5. Java API Framework: collection of managers allowing access to sensor input and functionalities (where devs spend time)
    
6. System Apps: camera, email, phone, downloaded/custom apps (where users spend time)
    

  

Application Components:

1. Activities: facilitates user interactions
    

-screens made up of views, views arranged into layouts

2. Services: one single task on in background/for long period of time
    

-usually no visual component

3. Broadcast Receivers: change app behaviours based on system state/messages
    

-react to system/other app messages

4. Content Providers: allows app to access other data
    

-app is self-enclosed data unit unless permissions granted

-allows apps to exchange data with each other (contacts shared with all apps)

  

Android Development Environment:

-empty activity, API 24

Emulator:

- can test apps on virtual representations of various hardware/screen sizes
    

- missing features (hardware for sensing GPS, camera, video recording)
    

-keyboard is keyboard

-mouse is finger

-uses host internet connection

-buttons work

Ctrl-F11: toggle landscape and portrait orientation

Alt-Enter: toggle full screen

  

Files: use Android view, classified by nature

1. res: default resources:
    

1. drawable: bitmap/XMLs for images/icons
    

1. bitmap
    
2. nine-patches (resizable bitmaps)
    
3. state lists
    
4. shapes
    
5. animation drawables
    
6. other drawables
    

3. layout: XML layout files for each page
    
4. menu: XML menus in the app
    
5. mipmap: drawable files for different launcher icon densities
    
6. values: XML files containing simple values
    

1. strings (all text) <string> tag
    
2. int
    
3. colors <color> tag
    
4. dimens
    
5. arrays
    
6. styles
    

8. raw: general purpose files (audio)
    

3. manifests: all activities/permissions needed in the application
    

-used to communicate with other apps/system

3. java: behaviour files for each activity
    

  

Log Class (android.util): used to log messages at runtime

Tag: name of activity

Msg: telling where error is (content displayed)

Log.e(String tag, String msg): Log an error 

Log.w(String tag, String msg): Log a warning 

Log.i(String tag, String msg): Log an informational message 

Log.d(String tag, String msg): Log a debugging message 

Log.v(String tag, String msg): Log a verbose message

Log.wtf(String tag, String msg): Log a “What a Terrible Failure” message (to report an exception that should never happen)

  

Logcat: where to view log messages, can filter by severity

-also viewed in debugger and Android Device Monitor

  

|   |   |
|---|---|
|Log.d(String tag, String Message);|Print out a log message to logcat|
|tag:TAGNAME|filter by TAGNAME in logcat search box|

  
  

Lecture 2: Activity Lifecycle and Working with Resources

  
![](https://lh7-us.googleusercontent.com/TC2Aq262_NhV_wYfrIzeQtDQoADUOt6KQ1peFBISwTBFEiQ_CirWtK_b0Ovqx_WqbjxlIY_f61v9irTHOHQ6XyBni9QW4ndiWP2wc2Nsw94Ty230KObDRiE-4s-380dnBu4IwfwG0Xv7VzAnQppJrmw)

Activity Lifecycle

Activity: application component providing a screen

Main Activity: first activity implemented on app open

View: everything the user interacts with

  

Activity Stack:

1. Activity 1: current interaction
    
2. Activity 2: back/destroy will bring A2 to top![](https://lh7-us.googleusercontent.com/4Yddg1PzYB_AfTd7ygdMX_ivNSGGLHw3ro0jHj7zmSALR3RPVeYKVtjU9scAUEjny_R0rwNM_uxQLS6RO6IZNpIgICYX-3MeHq1hYEWj1zZrSWRZTIftCzerL7hpgfqvdQR0AHx0owGmUPXud5XOmBc)
    
3. Activity 3: if above activities take too much space activity 3+ are destroyed
    

  

Start/Stop Activities:

- app can start activities belonging to itself
    
- new activity start = previous activity stop
    
- lifecycle callback methods tell us if activity is implemented/visible/called properly
    

  

Activity Lifecycle Methods:

- keep user progress and data
    
- stop heavy processing/network operations when not in use
    
- when viewable be fully functional and do not crash
    

Callback Methods: called automatically by Android System in phases of Android activity, override parent methods

  

|   |   |
|---|---|
|onCreate()|called on startup|
|onStart()|UI elements are initialized and displayed|
|onResume()|UI becomes interactable, most app usage happens here|
|onPause()|app is interrupted but still viewable, very fast unless still viewable|
|onStop()|not visible anymore, not interactable|
|onRestart()|restores state of activity from when stopped<br><br>*app already exists so no need to re onCreate()|
|onDestroy()|Android system kills activity due to low memory or explicitly killed in code|

- screen rotation destroys and recreates activity
    
- back arrow destroys activity, onSave and onRestore are not called, data is gone
    

  

Logging Activity States:

  

|   |   |
|---|---|
|android.util.Log.d(String tag, String message);|All logs behave the same so can use any<br><br>Tag: used to filter<br><br>Message: information about action|

  

-logs use memory/CPU, delete when app is done

  

Saving Activity State:

- activity kept in memory when app stopped/paused until explicitly destroyed
    

Bundle: key-value map, primitive types, contains information about each view

  

|   |   |
|---|---|
|onSaveInstanceState(Bundle outState){<br><br>super.onSaveInstanceState(outState);<br><br>  <br><br>outState.putInt(“SAVED_INT”, intVariable);<br><br>}|called after onPause(), saved in a Bundle (not long term)<br><br>  <br><br>save an int value to Bundle|
|onRestoreInstanceState(Bundle savedState){<br><br>super.onRestoreInstanceState);<br><br>  <br><br>int retrievedInt = savedInstanceState.getInt(“SAVED_INT”);<br><br>}|called after onStart()<br><br>  <br>  <br>  <br>  <br><br>retrieve int value from Bundle|

  
  
  
  

Resources: res folder

Context class: interface with global information about application environment 

- app’s private files/data
    
- device/system-wide resources
    

  

|   |   |
|---|---|
|Context context = getApplicationContext()|Retrieve Context for current processes|

  

Access Application-Wide Resources

|   |   |
|---|---|
|getAssets()||
|getResources()||
|getPackageManager()||
|getString()||
|getSharedPrefsFile()||

  

Retrieve application Resources

|   |   |
|---|---|
|String greeting = getResources().getString(R.string.hello);|Retrieve string instance from app resources by resource ID|

  

Accessing App Preferences

|   |   |
|---|---|
|getSharedPreferences()||
|SharedPreferences|class to save simple app data (configuration settings and persistent app state information)|

  

Managing App Resources

1. App Resources: defined by developer within Android project, specific to app
    
2. System Resources: defined by Android platform, accessible to all apps through Android SDK
    

  

Retrieve Colour

  

|   |   |
|---|---|
|int textColor = ContextCompat.getColor(getApplicationContext(),R.id.colorid)|get colour resource using colour id|

  

Lecture 3: Building User Interface

  

Button Click: listeners react to event

  

|   |   |
|---|---|
|android.widet.Button;||

XML (layout): add button from design layout and give id

|   |   |
|---|---|
|<Button<br><br>android:id=”@id/button1”<br><br>/>|create new button object with id button1|

  

Java (behaviour):

|   |   |
|---|---|
|implements View.onClickListener(this)|implement onClickListener interface|
|protected void onCreate(){<br><br>  <br><br>myButton = (Button) findViewById(R.id.button1);<br><br>  <br><br>myButton.setOnClickListener(this);|assign XML button element to Java variable<br><br>  <br><br>set button to be click responsive|
|onClick(View v){<br><br>Toast.makeToast(“message”, Toast.LENGTH_LONG).show();<br><br>}|behaviour code called when button is clicked|

  

View Structure: 

View: everything in UI, rectangular area responsible for handling user events (like buttons)

View Group: invisible rectangular area on screen holding other views in certain structure (vertical, horizontal, grid, table)

- in XML all views and view groups are placed in one root view hierarchy (taking up whole screen with match_parent width and height)
    

1. Linear Layout:
    

1. Horizontal (columns)
    
2. Vertical (rows)
    

View Attributes:

  

|   |   |
|---|---|
|android:layout_weight|affect size of view in relation to other views<br><br>- default: 0 (no weights, takes only as much as needs)<br>    <br>- 1: takes all remaining space<br>    <br>- height or weight set to 0dp when using this for less processing<br>    <br>- consistent/responsive across devices|
|android:layout_gravity|position of view within parent layout, constrained by this layout<br><br>- will not change column (for horizontal) or row (for vertical) with LinearLayout|
|android: gravity|content position within view|

  

Elements:

|   |   |
|---|---|
|EditText plaintext|field user can enter text into|
|TextView|textbox showing text|
|||

  

RecyclerView:

- displays large amounts of data
    
- manages data for display of different devices
    
- more flexible than older listview control
    

  

Components:

LayoutManager: controls appearance of items (LinearLayoutManager, GridLayoutManager, StaggeredGridLayoutManager)

Data Model: represents one single item

Adapter: pulls items from Data Model and presents items on screen via ViewHolder, creates view for each item

View Holder: xml layout for one single item inflated/converted to java code

Item Animator: animations on the RecyclerView

Item Decorator: sectioning recyclerview into different sections

  

Architecture:![](https://lh7-us.googleusercontent.com/gcuzgQi6TMEf0NaUCtk0JUkjs8JvqHjekIlrqbvNpUfwgn71gwq9l7K9EZKcXOxS3RqW-wx4emeHxMinH1C85IFN1JVNDDflUiBXullb8CIGtK2JUlI_tcaFALdLN0iMWPak454z1bsw_Ad4WtBoqq0)

1. View holder: how data is set up to appear onscreen
    

1. Content View: how content fits into holder
    

3. Adapter: takes data and prepares it for display
    
4. Layout Manager: takes care of layout
    
5. Item Animator: adds animation (optional)
    
6. Item Decorator: decorations to items (optional)
    

  

Implementation:

- recyclerview component defined in own library rather than core sdk, part of support repository
    
- need to add dependency to gradle build file in app module
    
- add recyclerview to xml file
    

Data Adapter: pulls items from data model and presents onscreen via viewholder, created view for each item

- ViewHolder class: xml layout for one single item inflated/converted to java code, set up bindings to view in xml layout file
    
- onCreateViewHolder(): created automatically by the adapter each time it needs new representation of data item
    
- onBindViewHolder(): called each time adapter encounters a new data item that needs to display, take data object and display values
    
- getItemCount: returns number of items in data collection
    

Handling user events: need reference to view that represents single data item, expose view item as member of viewholder class (public field, set reference in constructor, this way the view reference will be available to all adapter class)

- click listener for item
    

  

Lecture 4: Intents, Hardware, RecyclerView

  

Intents: asynchronous messages allowing Android components to request functionality from other components (can start activity/service/broadcast receiver)

- can also be signal that specific event has occurred
    

1. Explicit: specified by Java class name (accessing activity within same app)
    

|   |   |
|---|---|
|Intent i = new Intent (this (context), ActivityTwo.class (Java class name);<br><br>startActivity(i);|create explicit intent to start activity <br><br>  <br><br>start activity using intent|
|i.putExtra(“key (string)”, “value (primitive type)”);<br><br>  <br><br>i.putExtra(“value1”, value);|send data with intent using key value pairs where key is String and value is primitive type|

  

2. Implicit: specified by activity to be performed
    

- Android system searches for all components registered for specific action and data type (if one: started directly, if multiple: user chooses)
    

|   |   |
|---|---|
|Intent i = new Intent(Intent.ACTION_VIEW);<br><br>  <br><br>i.setData(Uri.parse(“[https://www.sfu.ca](https://www.sfu.ca)”));<br><br>startActivity(i);|make new intent to view <br><br>  <br>  <br><br>send data to be viewed (retroactive)<br><br>  <br><br>start intent activity (typically web browser is registered to this intent)|
|startActivity(Intent);<br><br>startService(Intent);|start specified intent activity<br><br>start specified intent service|
|Uri number = Uri.parse(“tel:6048169266”);<br><br>Intent callIntent = new Intent(Intent.ACTION_DIAL, number);|package telephone number using uniform resource identifier<br><br>  <br><br>send number with intent to dial|
|Uri location = Uri.parse(“geo:0,0? q=1600+Amphitheatre+Parkway,+Mountain+View, +California");<br><br>  <br><br>Uri location = Uri.parse(“geo:37.5, -122.8?z=14”);<br><br>  <br><br>Intent mapIntent = new Intent(Intent.ACTION_VIEW, location);|map point based on address<br><br>  <br>  <br>  <br><br>map point based on coordinated (z is zoom level)<br><br>  <br><br>create intent to view location on map|
|Uri webpage = Uri.parse(“[http://www.android.com](http://www.android.com)”);<br><br>  <br><br>Intent webIntent = new Intent.ACTION_VIEW, webpage);|webpage<br><br>  <br>  <br><br>create intent to view webpage|
|Intent emailIntent = new <br><br>Intent(Intent.ACTION_SEND);<br><br>  <br><br>emailIntent.setType(HTTP.PLAIN_TEXT_TYPE);<br><br>  <br><br>emailIntent.putExtra(Intent.EXTRA_EMAIL, new String[] {“[jon@example.com](mailto:jon@example.com)”});<br><br>  <br><br>emailIntent.putExtra(Intent.EMAIL_SUBJECT, “Email subject”);<br><br>  <br><br>emailIntent.putExtra(Intent.EMAIN_TEXT, “email message text”);<br><br>  <br><br>emailIntent.putExtra(Intent.EXTRA_STEAM, Uri.parse(“content://path/to/email/attachment”));|create intent to send email (using key-value pairs)<br><br>  <br>  <br><br>this intent does not have URI so decare the “text/plain” type<br><br>  <br><br>send recipient of email<br><br>  <br>  <br><br>send subject of email<br><br>  <br>  <br><br>send message of email<br><br>  <br>  <br><br>send path to attachment of email (can also attach multiple items using ArrayList of Uris)|
|Intent.ACTION_||

Actions:

  

|   |   |
|---|---|
|ACTION_VIEW|use when information to show user|
|ACTION_SEND|use when sharing information through another app|
|ACTION_EDIT|edit a document (Uri of document to edit)|

  
  

Verify: must check there is component to complete intent (when first activity starts)

|   |   |
|---|---|
|Package Manager|knows/can access all packages installed on device|
|queryIntentActivities()|returns list of activities capable of handling intent (if list != 0 then intent can be used safely)|
|Uri location = Uri.parse(“geo:0,0?q=1600+Amphitheatre+Parkway,+Mountain+View,+California”);<br><br>  <br><br>Intent mapIntent = new Intent(Intent.ACTION_VIEW, location);<br><br>  <br><br>PackageManager packageManager = getPackageManager();<br><br>  <br><br>List<ResolveInfo> activities = packageManager.queryIntentActivities(mapIntent, 0);<br><br>  <br><br>boolean isIntentSafe = activities.size() > 0;<br><br>  <br><br>if (isIntentSafe){<br><br>startActivity(mapIntent);<br><br>}|build map intent<br><br>  <br>  <br>  <br>  <br>  <br>  <br>  <br><br>access PackageManager<br><br>  <br>  <br><br>get list of potential activities that can resolve intent<br><br>  <br>  <br><br>save if list is greater than 0<br><br>  <br>  <br><br>start intent if list  greater than 0|

PackageManager: has all information about what packages are installed on the device

  

Getting Data Back:

  

|   |   |
|---|---|
|startActivityforResult()|called in Activity1 to start Activity2|
|onActivityResult(requestCode, resultCode, resultData);|callback called automatically in Activity1 once Activity2 is over|
|public void onClick(View v){<br><br>Intent i = new Intent(this, ActivityTwo.class);<br><br>i.putExtra(“value1”, value);<br><br>i.putExtra(“value2”, value);<br><br>  <br><br>startActivityforResult(i, REQUEST_CODE); }|create intent in onClick() method in ActivityOne<br><br>  <br>  <br>  <br>  <br>  <br><br>start activity with request code (identifying request so knows when returned)|
|@Override <br><br>public void finish(){<br><br>  <br><br>Intent data = getIntent();<br><br>  <br><br>data.putExtra(“returnKey”, result);<br><br>data.putExtra(“returnKey2”, result);<br><br>  <br><br>setResult(RESULT_OK, data);<br><br>super.finish();}|method in ActivityTwo to send data back to ActivityOne when finished<br><br>  <br><br>make intent and put in data<br><br>  <br>  <br>  <br>  <br><br>set that activity/result were completed successfully|
|@Override   <br><br>protected void onActivityResult(int requestCode, int resultCode, Intent data){<br><br>  <br><br>if (resultCode == RESULT_OK && requestCode == REQUEST_CODE){<br><br>  <br>  <br><br>if (data.hasExtra(“returnKey”)){<br><br>  <br><br>Toast.makeText(this, data.getExtras().getString(“returnKey”), Toast.LENGTH_SHORT).show();<br><br>}}}|method to retrieve ActivityTwo result called automatically in ActivityOne after A2 finish()<br><br>  <br>  <br><br>if result code is what we specified (OK)<br><br>if request code is what we specified when sending intent (using startActivityforResult())<br><br>  <br><br>if intent holding data has key we set<br><br>  <br><br>show data sent back on screen|

  

onActivityResult(int requestCode, int resultCode, Intent data)

- requestCode: what was passed to startActivityforResult() originally
    
- resultCode: RESULT_OK or RESULT_CANCELED
    
- result data(Intent with key-value pairs)
    

  

Accessing Hardware: 

Sensors:

1. Motion (3 values)
    

1. acceleration, forces, rotational forces along 3 axes (accelerometer, gravity sensor, rotational vector sensors, gyroscopes)
    

3. Environmental (1 value)
    

1. ambient air temperature sensor, pressure, illumination, humidity
    

5. Position
    

1. physical position of device (orientation sensors, magnetometers)
    

Guidelines:

1. cannot assume device has all sensors (always check before using)
    
2. using sensors takes computational/battery power, acquire late, release asap
    
3. put permissions for sensors in manifest (even if not necessary sensor)
    

Framework: part of android.hardware package

1. identifying sensors and sensor capabilities (disable functions using unavailable sensors, pick best sensor for optimum performance)
    
2. monitoring sensor events (get sensor data, name, timestamp)
    

|   |   |
|---|---|
|SensorManager<br><br>  <br><br>private SensorManager sensorManager;<br><br>sensorManager = (SensorManager) getSystemService(Context.SENSOR_SERVICE);<br><br>  <br><br>List<Sensor> deviceSensors = sensorManager.getSensorList(Sensor.TYPE_ALL);<br><br>  <br><br>if (sensorManager.getDefaultSensor(Sensor.TYPE_MAGNETIC_FIELD) != null){<br><br>//there is a magnetometer}<br><br>else{ //there is no magnetometer}|class to create instance of sensor service<br><br>  <br><br>get instance of SensorManager class to access sensor information with<br><br>  <br>  <br>  <br><br>get list of all sensors<br><br>  <br>  <br>  <br>  <br><br>check/perform action if there is a specific sensor|
|public List<Sensor> getSensorList(int type);<br><br>  <br><br>TYPE_ACCELEROMETER  <br>TYPE_GYROSCOPE  <br>TYPE_LIGHT  <br>TYPE_MAGNETIC FIELD  <br>TYPE_ORIENTATION  <br>TYPE_PRESSURE  <br>TYPE_PROXIMITY  <br>TYPE_TEMPERATURE  <br>TYPE_ALL|getting list of specific sensor type<br><br>  <br>  <br><br>all sensor type constant options|
|Sensor<br><br>  <br><br>private Sensor light;<br><br>light = sensorManager.getDefaultSensor(Sensor.TYPE_LIGHT);|class to create instance of specific sensor<br><br>  <br><br>declare light sensor variable<br><br>  <br><br>initialize light sensor variable with default light sensor using sensor type parameter from Sensor class|
|SensorEvent|class to create sensor event object providing information about sensor event data/type/timestamp|
|SensorEventListener (implements)<br><br>  <br>  <br><br>public final void onAccuracyChanged(Sensor s, int accuracy){}<br><br>  <br><br>public final void onSensorChanged(SensorEvent e){<br><br>float lux = e.values[0];}|interface with callbacks to receive sensor events when accuracy or values change<br><br>  <br><br>called when sensor accuracy is changed<br><br>  <br>  <br>  <br><br>called when sensor value is changed<br><br>- contains all data about sensor (accuracy, current reading, timestamp)<br>    <br>- rate may be high so do as little processing as possible in this method|
|protected void onResume(){<br><br>super.onResume();<br><br>  <br><br>sensorManager.registerListener(this, light, SensorManager.SENSOR_DELAY_NORMAL);}<br><br>  <br><br>protected void onPause(){<br><br>super.onPause();<br><br>sensorManager.unregisterListener(this);}|register sensor as late as possible in onResume()<br><br>  <br><br>unregister listener as soon as possible in onPause()|
|SENSOR_DELAY_NORMAL<br><br>SENSOR_DELAY_UI  <br>SENSOR_DELAY_GAME|constants to specify speed of sensor refresh (game is fastest)|
|<uses-feature android:name=”android.hardware.sensor.barometer” /><br><br>  <br><br><uses-feature android:name=”android.hardware.sensor.gyroscope”<br><br>android:required=”false” />|sensors used are specified in manifest file to indicate what application requires|

Process:

1. determine available sensors on device
    
2. determine sensor capabilities (max range, manufacturer, power requirements, resolution)
    
3. acquire raw sensor data, define minimum rate to acquire it
    
4. register and unregister sensor event listeners to monitor sensor changes
    

  

System Services:

1. Power Service
    
2. Vibration Service
    

  

|   |   |
|---|---|
|Vibrator vibrator = (Vibrator) getSystemService(Context.VIBRATOR_SERVICE);|get instance of vibrator|
|vibrate(long amtTime);<br><br>cancel();<br><br>vibrate(long[] pattern, int repeat)<br><br>  <br><br>needs android.permission.VIBRATE|set length of time to vibrate<br><br>cancel vibrations<br><br>vibrate in pattern|

  

3. KeyGuard Service
    
4. Alarm Service
    

  

|   |   |
|---|---|
|AlarmManager as = (AlarmManager) getSystemService(Context.ALARM_SERVICE);|get instance of alarm service|
|set(int type, long triggerAtTime, PendingIntent operation);<br><br>  <br><br>type is one of:<br><br>  <br><br>SystemClose.elapsedRealTime();<br><br>ELAPSED_REALTIME<br><br>ELAPSED_REALTIME_WAKEUP<br><br>  <br><br>System.currentTimeMillis();<br><br>  <br><br>RTC<br><br>RTC_WAKEUP<br><br>  <br><br>setRepeating(int type, long triggerAtTime, long interval, PendingIntent operation);<br><br>INTERVAL_HOUR<br><br>INTERVAL_HALF_DAY<br><br>  <br><br>cancel(PendingIntent operation)<br><br>match with filterEquals(Intent anotherIntent)|set alarm<br><br>  <br>  <br>  <br>  <br>  <br>  <br>  <br>  <br>  <br>  <br>  <br>  <br>  <br><br>set repeating alarm<br><br>  <br>  <br>  <br>  <br>  <br><br>cancel alarm|

  

5. Sensor Service
    
6. Audio Service
    
7. Telephony Service
    
8. Connectivity Service
    
9. Wi-Fi Service
    

  

UI RecyclerView: complex UI control (view)

- useful when displaying scrolling list of elements with large data sets/frequently changing data
    

Components:

1. RecyclerView object: overall container for data added to layout
    

  

|   |   |
|---|---|
|protected void onCreate(Bundle savedInstanceState){<br><br>  <br><br>super.onCreate(savedInstanceState);<br><br>setContentView(R.layout.activity_main);<br><br>  <br><br>recycler = (RecyclerView) findViewById(R.id.my_recycler);<br><br>  <br><br>layoutManager = new LinearLayoutManager(this);<br><br>recycler.setLayoutManager(layoutManager);<br><br>  <br><br>adapter = new MyAdapter(courses, getApplicationContext());<br><br>recycler.setAdapter(adapter);|initialize recycler object<br><br>  <br>  <br><br>initialize linear layout<br><br>set recycler layout to linear layouy<br><br>  <br>  <br>  <br><br>initialize adapter object<br><br>  <br><br>set adapter to recycler object|

  

2. LayoutManager: controls positioning of views within RecyclerView
    

1. LinearLaroutManager (horizontal or vertical)
    
2. GridLayoutManager (table or staggered)
    
3. Custom
    

4. ViewHolder: represents views in list of items, each view holder displays single item with view, ViewHolder objects are managed by adapter
    

  

|   |   |
|---|---|
|public static class MyViewHolder extends RecyclerView.ViewHolder implements View.OnClickListener{|make new class for ViewHolder that extends parent class|
|Public MyViewHolder(View v){<br><br>super(v);<br><br>myTextView = (TextView) v;<br><br>v.setOnClickListener(this);<br><br>context = v.getContext();}|ViewHolder class constructor|
|public void onClick(View v){<br><br>Toast.makeText(context, “You have clicked” + ((TextView) v).getText().toString(), Toast.LENGTH_SHORT).show();|display TextView content onscreen when clicked|

  

4. Adapter
    

  

|   |   |
|---|---|
|onCreateViewHolder()|sets view to hold the data|
|onBindViewHolder()|binds view holders to the data, assigns the view holder to a position<br><br>- uses view holder’s position to determine where contents should be based on list position|

  

Lecture 5: Managing Data in Android

  

Data Storage Options

1. SharedPreferences: private key-value pair primitive data
    
2. internal storage: device memory private files
    
3. external storage: shared external storage for public data
    
4. SQLite Databases: structured private data
    
5. network connection: available on web
    

Internal: private files saved directly into app, if uninstalled data is removed

External: removable external storage (SD card) and non-removable internal storage, readable by anyone

  

SharedPreferences: primitive data stored in key-value pairs private to app in XML file (can have multiple files for different data types)

- for data that does not change often
    
- private to app (all app components can access
    

Directory: data/ data/ <package-name>/ shared-prefs/ XML file

Simple Data: settings, theme, username, font size, background colour

Primitive Types: int, boolean, String, float, long

Saving Data:

|   |   |
|---|---|
|SharedPreferences sp = getSharedPreferences(“MyData”, Context.MODE_PRIVATE);|get reference to SharedPreferences “MyData” file with sp object|
|SharedPreferences.Editor spEditor = sp.edit();|get reference to SharedPreferences  editor to edit|
|spEditor.putString(“key”, value);|use editor to add data with key|
|spEditor.commit();|commit changes to save|

  

Retrieving Data:

|   |   |
|---|---|
|SharedPreferences sp = getSharedPreferences(“MyData”, Context.MODE_PRIVATE);|get reference to SharedPreferences object|
|String key = sp.getString(“key”, DEFAULT_VALUE);|get String object by key (DEFAULT_VALUE is if nothing is under that key)|

  

SQLite Database: structured complex data private to app

SQLite: language for managing data in relational databases, private database to app

- self contained, transaction-based, no external server
    

- for data consistently/often changed and collected with many parts
    

Directory: data/ data/ <package-name>/ database folder

Method:

1. Define Schema: how many tables/items (database structure)
    

_id: primary key each column is identified with, convention to start with underscore

|   |   |
|---|---|
|public class HelperClass extends SQLiteOpenHelper{|class extends SQLiteOpenHelper class|
|private static final String DATABASE_NAME = “plantdatabase”;<br><br>  <br><br>private static final String TABLE_NAME = “PLANTSTABLE”;<br><br>  <br><br>private static final String UID = “_id”;<br><br>  <br><br>private static final String Name = “Name”;<br><br>  <br><br>private static final int DATABASE_VERSION = 1;|name of database for table<br><br>  <br>  <br><br>name of table<br><br>  <br>  <br><br>id number (column 1)<br><br>  <br><br>name value (column 2)<br><br>  <br>  <br><br>constant fields do not change|
|public HelperClass (Context context){<br><br>super(context, DATABASE_NAME, null, DATABASE_VERSION);||

  

2. Create Database: use queries to create
    

SQLiteOpenHelper subclass implement onCreate() and onUpgrade()

- opens database if it exists
    
- creates database if does not exist
    
- updates database as necessary
    

  

|   |   |
|---|---|
|private static final String CREATE_TABLE = “ CREATE TABLE “ +TABLE_NAME+ “ ( “ +UID+ “ INTEGER PRIMARY KEY AUTOINCREMENT, “ +NAME+ “ VARCHAR(255));”;<br><br>  <br><br>onCreate(SQLiteDatabase db){<br><br>  try {<br><br>  db.execSQL(CREATE_TABLE);}<br><br>  catch(SQLException e){<br><br>  //send a Toast or sm}<br><br>}|get initialization statement ready<br><br>(column 1 = id autoincrement, column 2 = name up to 255 characters)<br><br>  <br>  <br>  <br>  <br><br>called when database is first created, creates tables and fills with initial data (using initialization statement)|
|private static final String DROP_TABLE = “DROP TABLE IF EXISTS “ + TABLE_NAME;<br><br>  <br><br>public void onUpgrade (SQLiteDatabase db, int oldVersion, int newVersion){<br><br>  try{<br><br>  db.execSQL(DROP_TABLE);}<br><br>  catch(SQLException e){<br><br>  //send Toast or sm}<br><br>  <br>  <br><br>}|get statement ready<br><br>  <br>  <br><br>called when database is updated (drop or add tables, changing database structure)|
|private static final String CREATE_TABLE = “ CREATE TABLE “ +TABLE_NAME+ “ ( “ +UID+ “ INTEGER PRIMARY KEY AUTOINCREMENT, “ +NAME+ “ VARCHAR(255));” +TYPE+ “ VARCHAR(255));”;|to add a column just add another statement (type) to CREATE_TABLE and it will update in onUpgrade()|
|public class MainActivity extends Activity{<br><br>  <br><br>HelperClass helper;<br><br>  <br><br>onCreate{<br><br>helper = new HelperClass(this);<br><br>SQLiteDatabase myDatabase = helper.getWriteableDatabase();<br><br>}|initialize SQL helper class in main activity<br><br>  <br><br>returns SQLite database object (created when called first time)|

**ONLY CREATED WHEN ATTEMPTING TO ACCESS FOR FIRST TIME**

Code Organization:

1. MyDatabase Class: contains SQLite database instance, helper, context and methods to edit database (insert data, get data, everything to do with accessing)
    
2. MyHelper Class: extends SQLiteOpenHelper and overwrites onCreate() and onUpgrade()
    
3. Constants Class: contains all schema constants
    

  

3. Execute Queries: insert, update, delete
    

SQLiteDatabase class: object representing database

  

Insert Query:

|   |   |
|---|---|
|ContentValues cv = new ContentValues();<br><br>  <br><br>cv.put(Constants.NAME, name);<br><br>cv.put(Constants.TYPE, type);<br><br>  <br><br>long id = db.insert(Constants.TABLE_NAME, null, cv);<br><br>  <br><br>if (id > 0){<br><br>access data}|making contentvalues key value bundle instance to put data in <br><br>  <br><br>putting column name (key) and user entry (value) into bundle<br><br>  <br><br>returns id of newly inserted row in table, blank row and data<br><br>  <br>  <br><br>if fails returns -1, if positive data has successfully been inserted|

  

Accessing Query:

1. public Cursor query (boolean distinct, String table, String[] columns, String selection, String[] selectionArgs, String groupBy, String having, String orderBy, String limit);
    

- distinct: true if want each row to be distinct
    
- table: name of table accessing
    
- columns: list of columns to return/read (null = all)
    
- selection: filter of rows (null = all)
    
- groupBy: how to group rows
    
- having: filter saying what groups to use in cursor
    
- orderBy: how to order rows
    
- limit: limits number of rows returned by query
    

** null for any of these returns all available**

2. Cursor object: gives access to results returned by database query (results, entire column, subset of table), allows navigation through results set
    

- android.database.Cursor
    

Cursor Methods:

|   |   |
|---|---|
|String getColumnName (int columnIndex)|get name of column returned|
|int getCount()|get how many rows were returned in result|
|boolean moveToNext()|for navigation through rows of result set (true if still rows left to navigate)|

Getting Data:

1. MyDatabase Class:
    

|   |   |
|---|---|
|public String getData(){<br><br>  <br><br>SQLiteDatabase db - helper.getWriteableDatabase();<br><br>  <br><br>String[] columns = {Constants.UID, Constants.NAME, Constants.TYPE};<br><br>  <br><br>Cursor cursor = db.query(Constants.TABLE_NAME, columns, null, null, null, null, null, null);<br><br>  <br><br>StringBuffer buffer = new StringBuffer();<br><br>  <br><br>while(cursor.moveToNext(){<br><br>int index = cursor.getInt(0);<br><br>String name = cursor.getString(1);<br><br>String type = cursor.getString(2);<br><br>buffer.append(index+ “” +name+ “” + “\n”);}<br><br>  <br><br>return buffer.toString();}|method to get database data in MyDatabase class<br><br>  <br><br>get instance of database<br><br>  <br><br>get columns to access (id, name and type)<br><br>  <br><br>get cursor object and initialize it with table and columns to access<br><br>  <br>  <br><br>make buffer to store results<br><br>  <br><br>while there are more rows to go through continue to add values to buffer<br><br>  <br>  <br>  <br>  <br><br>return buffer as string|

2. MainActivity Class
    

|   |   |
|---|---|
|public void viewResults(View v){<br><br>String data = db.getData();<br><br>//make toast or sm<br><br>}|access data|

  

Accessing Query with Condition:

1. MyDatabase Class:
    

Format: Constants.TYPE = ‘herb’ (or whatever type it is you want to filter by)

|   |   |
|---|---|
|String selection = Constants.TYPE +”=’ ” +type+ “ ‘ “;<br><br>  <br><br>Cursor cursor db.query(Constants.TABLE_NAME, columns, selection, null, null, null, null);|specify type to filter by<br><br>  <br>  <br><br>use cursor object to access results|

  

2. MainActivity Class
    

|   |   |
|---|---|
|public void viewQueryResults(View v){<br><br>  <br><br>String userInputType = textEntryEditText.getText().toString();<br><br>  <br><br>String queryResults = db.getSelectedData(userInputType);}|get type specified by user in edit text<br><br>  <br><br>apply filter to results|

  
  

Lecture 7: Threading, Asynchronous Processes, Services

  

Process and Threads in Android:

Processes: executing instance of app, run in own memory space

Thread: smaller softwares within process, run in shared memory space, one by default

Default:

- app runs first time
    
- starts new process in single thread of execution
    
- another component of app starts (eg. service), runs in same process and same thread (serial processing)
    

Using Threads:

- put different application components in own threads for parallel processing
    

Long-Running Operations: operations requiring heavy computational power, block UI update when executed in main thread

- network services
    
- location services
    
- database queries
    
- parsing data sets
    
- looking through databases of unknown size (large)
    
- accessing/processing multimedia files
    
- calculations
    
- accessing content provider
    

ANR: app not responding dialogue, comes up after 5 seconds of unresponsive UI

Avoiding Freezing:

1. Main Thread: UI elements (can implement StrictMode to enforce this)
    
2. use services and additional threads for long-running operations
    

|   |   |
|---|---|
|SystemClock.sleep(ms);|stops running for specified ms|

Enabling Responsiveness:

1. Main Thread: handles events from Views and Components
    
2. ActivityManager/WindowManager: monitor app for responsiveness, ANR if inactive for 5 seconds
    

|   |   |
|---|---|
|Java Thread Class|complete processing as normal|
|Loader Class|facilitate loading of data for use in Activity or Fragment while still starting up quickly|

  

Implementing Threads:

|   |   |
|---|---|
|private class MyThread implements Runnable{<br><br>  <br><br>public void run(){ //thing to do in thread}}|make anonymous inner class for thread containing method to do desired function|
|Thread t = new Thread(new MyThread());<br><br>t.start();|start thread using custom class in activity|

  

Process Termination: lowest importance is terminated first

1. Foreground Processes (highest)
    

1. activity in onResume()
    
2. service executing lifecycle methods/user interacting with
    
3. broadcast receiver executing onReceive()
    

3. Visible Processes
    

1. activity on onPause()
    
2. service bound to visible activity
    

5. Service Processes (can have UI)
    

1. no direct user interaction but service running (eg. playing music), so impacting user
    

7. Background Processes
    

1. no interaction at all, app most recently seen will be destroyed
    

9. Empty Processes
    

1. no active component running but still alive for caching purposes
    

  

Services: long-running operations in background performing one function, no UI, started by another app component, continues in background even when starting app closed/user switches to other app

ex: music player, file opener, handle network transactions, interact with content provider

- use services to be higher on process importance hierarchy and not terminated prematurely (as background or empty process)
    
- run in main thread by default in ‘background’ (no UI)
    
- newer devices have less premature killing cause more RAM
    

1. Started Service: started and stopped explicitly by app components (or self), most frequently used
    

1. started by app component startService()
    
2. runs in background even if starting component destroyed
    
3. does not return result to caller
    
4. have to stop manually (in code with stopSelf() or with activity with stopService()
    

Creating: file > new > service (adds to manifest automatically)

|   |   |
|---|---|
|Service class|base class for all services, create new thread to perform service’s intensive work|
|IntentService class|subclass of service, uses a worker thread to handle all start requests one at a time<br><br>- implements onHandleIntent() which receives intent for each start request|
|onCreate(){ //functionality of service when started}<br><br>  <br><br>onDestroy(){ //functionality of service when stopped}<br><br>  <br><br>onBind() { }<br><br>  <br>  <br>  <br><br>startService()<br><br>stopService()|override onCreate() and onDestroy() methods<br><br>  <br>  <br>  <br>  <br><br>override onBind() method (for services that bind to new components after creation)<br><br>  <br><br>called from an activity to activate and stop service|

  

2. Bound Service: started by app component, stopped automatically when unused
    

1. app component(s) bind to it using bindService()
    
2. client-server interface, send requests and get results
    
3. runs as long as component(s) are bound to it
    

  

Service Lifecycle: most important is starting and ending services

1. onStartCommand()
    
2. onBind()
    
3. onCreate()
    
4. onDestroy()
    

  

5. Started:
    

startService() call from activity

1. onCreate()
    
2. onStartCommand()
    

service running

service is stopped by itself or client

3. onDestroy()
    

service shut down

  

6. Bound:
    

bindService() call from activity

1. onCreate()
    
2. onBind()
    

clients are bound to service

unbindService() called from all clients

3. onUnbind()
    
4. onDestroy()
    

service shut down

  

Lecture Week 8: Adding Google Maps and Camera

  

1. Maps SDK: adding data from Google Maps
    

- API automatically handles access to Google Maps data (data downloading, map display, response to map gestures
    
- can use API call to add markers, polygons, overlays to map and change view of map area
    

Requirements: Google Account, register app, billing information, get API key, enable API that you want to use

Starting Map Project: (from empty activity)

1. Permissions from Manifest
    

|   |   |
|---|---|
|<uses-permission<br><br>android:name=”android.permission.WRITE_EXTERNAL_STORAGE”<br><br>android:maxSdkVersion=”22”/><br><br>  <br><br><uses-permission<br><br>android:name=”android.permission.READ_EXTERNAL_STORAGE”<br><br>android:maxSdkVersion=”22”/><br><br>  <br><br><uses-permission<br><br>android:name=”android.permission.ACCESS_FINE_LOCATION/><br><br>  <br><br><uses-permission<br><br>android:name=”android.permission.ACCESS_COARSE_LOCATION/>|permission to write data externally (to Google Maps)<br><br>  <br>  <br>  <br><br>permission to read external data (from Google Maps)<br><br>  <br>  <br>  <br><br>permission to access fine location (from GPS)<br><br>  <br>  <br><br>permission to access coarse location (from cell towers)|

  

2. Get API Key (place in manifest file)
    

  

|   |   |
|---|---|
|<meta-data<br><br>android:name=”com.google.android.geo.API_KEY”<br><br>android:value=” **key here**” />|placing API key within <application> tag|

  

3. Configuration (follow instructions on documentation pages)
    
4. Displaying Map
    

1. New layout file
    

  

|   |   |
|---|---|
|<fragment xmlns:android=”http:mmschemas.android.com/apk/res/android”<br><br>  <br><br>xmlns:map=”[http://scemas.android.com/apk/res-auto](http://scemas.android.com/apk/res-auto)”<br><br>  <br><br>android:name=”com.google.android.gms.maps.MapFragment”<br><br>  <br><br>android:id=”@+id/map”  <br>android:layout_width=”match_parent”<br><br>android:layout_height=”match_parent”/>|create new fragment (reusable element)|

- map always opens centered on equator and prime meridian (Lat and Lng doubles are 0.0 by default)
    

2. Starting Map from Set Location:
    

1. XML: set camera attributes
    

|   |   |
|---|---|
|<fragment ….<br><br>  <br><br>map:cameraTargetLat=”00.0”<br><br>map:cameraTargetLng=”00.0”<br><br>map:cameraZoom=”15”<br><br>/>|set starting Lat<br><br>set starting Lng<br><br>set starting zoom level|

  

2. Java
    

|   |   |
|---|---|
|GoogleMap myMap;<br><br>private static final int ERROR = 0;<br><br>  <br><br>private static final double<br><br>VANCOUVER_LAT = 49.2772,<br><br>VANCOUVER_LNG=-123.123;|initialize variables for map and lat/lng values|
|private void gotoLocation(double lat, double lng, float zoom){<br><br>  <br><br>LatLng ll = new LatLng(lat, lng);<br><br>CameraUpdate update = CameraUpdateFactory.newLatLngZoom(ll, zoom);<br><br>myMap.moveCamera(update);<br><br>  <br><br>myMap.animateCamera(update);<br><br>}|method to go to specified location variables<br><br>  <br>  <br><br>making object to move camera<br><br>  <br><br>actually moving camera<br><br>  <br><br>move is a to b<br><br>animate is smoother|
|public void onMapReady(GoogleMap map){<br><br>myMap = map;<br><br>checkLocationPermission();<br><br>gotoLocation(VANCOUVER_LAT, VANCOUVER_LNG, 15);<br><br>}|callback called by Map API when map is ready<br><br>  <br><br>opening map in set location|

  

5. Manipulating Map
    

1. Changing Map Type
    

1. XML
    

|   |   |
|---|---|
|<fragment …<br><br>  <br><br>map:mapType=”satellite”<br><br>map:mapType=”hybrid”<br><br>map:mapType=”terrain”<br><br>map:mapType=”normal”<br><br>map:mapType=”none”<br><br>/>|satellite image<br><br>satellite image with labels<br><br>terrain type cartoon<br><br>terrain with labels<br><br>no map|

  

2. Java: add select menu
    

|   |   |
|---|---|
|XML:<br><br>  <br><br><menu xmlns:android=”[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)”><br><br>  <br><br><item <br><br>android:id=”@+id/normalMap”<br><br>android:title=”normal” /><br><br>  <br><br><item <br><br>android:id=”@+id/satelliteMap”<br><br>android:title=”satellite” /><br><br>  <br><br><item <br><br>android:id=”@+id/terrainMap”<br><br>android:title=”terrain” /><br><br>  <br><br><item <br><br>android:id=”@+id/hybridMap”<br><br>android:title=”hybrid” /><br><br>  <br><br><item <br><br>android:id=”@+id/noneMap”<br><br>android:title=”none” /><br><br><menu/>|making dropdown menu from menu bar to select map type|
|Java:<br><br>  <br><br>public boolean onCreateOptionsMenu(Menu menu){<br><br>getMenuInflater().inflate(R.menu.menu_main, menu);<br><br>return true;<br><br>}<br><br>  <br><br>public boolean onOptionsItemSelected (MenuItem item){<br><br>int id = item.getItemId();<br><br>  <br><br>switch(id){<br><br>  <br><br>case R.id.noneMap:<br><br>myMap.setMapType(GoogleMap.MAP_TYPE_NONE);<br><br>break;<br><br>  <br><br>case R.id.hybridMap:<br><br>myMap.setMapType(GoogleMap.MAP_TYPE_HYBRID);<br><br>break;<br><br>  <br><br>case R.id.satelliteMap:<br><br>myMap.setMapType(GoogleMap.MAP_TYPE_SATELLITE);<br><br>break;<br><br>  <br><br>case R.id.terrainMap:<br><br>myMap.setMapType(GoogleMap.MAP_TYPE_TERRAIN);<br><br>break;<br><br>  <br><br>case R.id.normalMap:<br><br>myMap.setMapType(GoogleMap.MAP_TYPE_NORMAL);<br><br>break;<br><br>}<br><br>  <br><br>return super.onOptionsItemSelected(item);<br><br>}|callback method that inflates the menu with menu options<br><br>  <br>  <br>  <br><br>callback responding to option item selection<br><br>  <br>  <br>  <br><br>programmatically set map type|

2. Adding Map Markers
    

  

|   |   |
|---|---|
|public void geolocate()....{<br><br>  <br><br>MarkerOptions options = new MarkeOptions()<br><br>.title(locality)<br><br>.position(new LatLng(lat, lng));<br><br>myMap.addMarker(options);<br><br>}}|create new marker object after all other geolocate code|

  

2. Geocoding API: allows for map searching
    

- pass in lat/lng and return matching location
    
- pass in city name/postal code/landmark and return lat/lng
    
- usage limits (but not an issue to us)
    

Geocoder Class: wraps all request/response functionality and returns Java object

  

|   |   |
|---|---|
|getFromLocation()||
|getFromLocationName()||
|public void geolocate() throws IO Exception{<br><br>  <br><br>Geocoder myGeo = new Geocoder(this);<br><br>hideSoftKeyboard(v);<br><br>  <br><br>if (v.getId() == R.id.locationButton){<br><br>  <br><br>locationString = locationEntry.getText().toString();<br><br>  <br><br>List<Address> list = myGeo.getFromLocationName(locationString, 1);<br><br>  <br>  <br><br>if(list.size() > 0){<br><br>Address add = list.get(0);<br><br>  <br><br>String locality = add.getLocality();<br><br>  <br><br>double lat = add.getLatitude;<br><br>double lng = add.getLongitude();<br><br>  <br><br>gotoLocation(lat, lng, 15);<br><br>}}<br><br>  <br><br>if (v.getId() == R.id.latLngButton){<br><br>  <br><br>latString = latEntry.getText().toString();<br><br>lngString = lngEntry.getText().toString();<br><br>  <br><br>List <Address> list = myGeo.getFromLocation(Double.parseDouble(latString), Double.parseDouble(lngString);<br><br>  <br><br>if (list.size > 0){<br><br>Address add = list.get(0);<br><br>String locality = add.geLocality();<br><br>  <br><br>double lat = add.getLatitude();<br><br>double lng = add.getLongitude();<br><br>  <br><br>gotoLocation(lat, lng, 15);<br><br>}}|method to go to location based on name input<br><br>  <br><br>get new geocoder class object<br><br>  <br>  <br><br>if getting location by name<br><br>  <br><br>get location name String<br><br>  <br>  <br><br>get first result of location name using getFromLocationName(String, result)<br><br>  <br><br>if there are results get address of result <br><br>  <br><br>getLocality() returns full name<br><br>  <br><br>get latitude of address result<br><br>get longitude of address result<br><br>  <br><br>go to location result specified<br><br>  <br>  <br><br>if getting location by lat/lng<br><br>  <br><br>get lat/lng entry in Strings<br><br>  <br>  <br><br>get first result from lat/lng Strings (converted to Doubles)<br><br>  <br>  <br>  <br><br>if results list has result get address from result <br><br>get full name from address<br><br>  <br><br>get lat<br><br>get lng<br><br>  <br><br>go to location|

  

3. Current Location API: must add permission to Manifest file
    

  

|   |   |
|---|---|
|<uses-permission<br><br>android:name=”android.permission.ACCESS_FINE_LOCATION/><br><br>  <br><br><uses-permission<br><br>android:name=”android.permission.ACCESS_COARSE_LOCATION/>|based on GPS<br><br>  <br>  <br>  <br><br>based on phone towers and wireless networks|

  

1. Non-Code Approach: press current location button
    

|   |   |
|---|---|
|public void onMapReady(GoogleMap map){<br><br>myMap = map;<br><br>checkLocationPermission();<br><br>gotoLocation(VAN_LAT, VAN_LNG, 15);<br><br>  <br><br>myMap.setMyLocationEnabled(true);<br><br>myMap.setOnMyLocationButtonClickListener(this);<br><br>myMap.setOnMyLocationClickListener(this);|add location button handling to onMapReady callback<br><br>  <br>  <br>  <br><br>(implements OnMapReadyCallback, GoogleMap.OnMyLocationButtonClickListener, GoogleMap.OnMyLocationClickListener)|

  

2. Code Approach in Java
    

getLastLocation(): returns task that can be used to get Location object with lat/lng of geographic location

- location may be null if location turned off, device has never recorded location (new/restored to factory settings), Google Play services has restarted on device and no active Fused Location Provider client has requested location since
    

|   |   |
|---|---|
|public void showCurrentLocation(MenuItem item){<br><br>  <br><br>fusedLocationClient.getLastLocation().addOnSuccessListener(this, new OnSuccessListener<Location>(){<br><br>  <br><br>public void onSuccess(Location location){<br><br>  <br><br>LatLng ll = new LatLng(location.getLatitude(), location.getLongitude());<br><br>  <br><br>CameraUpdate update = CameraUpdateFactory.netLatLngZoom(ll, 15);<br><br>  <br><br>if (location != null){<br><br>//code to handle location object<br><br>}|fused location is fine and coarse together for most accurate location<br><br>  <br>  <br><br>*boilerplate code*|

  
  

2. CameraX: library to work with camera

Use Cases:

1. Preview: display camera preview in activity
    
2. ImageCapture: take photo and save to storage
    
3. ImageAnalysis: analyze frames from camera in real time
    
4. VideoCapture: capture and store video
    

Steps:

1. Add gradle dependencies (copy and paste)
    
2. Permission handling (in manifest)
    

|   |   |
|---|---|
|<uses-feature android:name=”android.hardware.camera.any”/><br><br>  <br>  <br>  <br>  <br>  <br><br><uses-permission android:name=”android.permission.CAMERA”/>|makes sure device has camera (can be front or back) if used without camera.any will not work for devices without back camera<br><br>  <br><br>adds permission to access camera|

  

3. Add PreviewView in layout
    

|   |   |
|---|---|
|<view <br><br>android:id=”@+id/previewView”<br><br>class=”androidx.camera.view.PreviewView”<br><br>android:layout_width=”match_parent”<br><br>android:layout_height=”0dp”<br><br>android:layout_margimBottom=”20dp”<br><br>android:layout_weight=”1” />|PreviewView is used to show camera live|

  

4. Get instance of ProcessCameraProvider (copy code)
    
5. Select camera and bind to lifecycle  (copy code)
    

  

Lecture Week 9: Android Touch Framework

  

Android Touch Framework: 

  

TouchEvent: starts when screen is touched with 1 or more fingers

MotionEvent: delivered to onTouchEvent callback providing detail of interaction

Information Gathered: 

- x/y coordinates
    
- number of pointers
    
- event time
    
- velocity
    
- pressure
    
- for each sequence of touch TouchEvents onTouchEvent can be fired multiple times
    

|   |   |
|---|---|
|ACTION_DOWN  <br>ACTION_UP  <br>ACTION_MOVE  <br>ACTION_POINTER_DOWN  <br>ACTION_POINTER_UP  <br>ACTION_CANCEL|user touching screen<br><br>user lifts finger<br><br>finger touching and moving<br><br>2nd finger down<br><br>2nd finger up<br><br>touch and release (touch done)|

  

Gesture: beginning with ACTION_DOWN, ends with ACTION_UP

Gestures in Android: can be made of multiple touch events or motions, different sequences lead to different gestures

Android Core Gestures:

Single Touch: 1 finger gestures (scroll, fling)

- touch: default functionality
    
- long press: enters data selection mode
    
- swipe: scrolls overflowing content
    
- drag: rearranging data within view
    
- double-touch: zooms into content
    

Multi-Touch: 2+ finger gestures (scale up, scale down)

- pinch open: zoom in
    
- pinch closed: zoom out
    

Challenges:

- made of multiple touch events
    

  

Approaches to Gesture Recognition:

1. MotionEvent information gathered with onTouchEvent, process information ourselves in code, see if gesture matches conditions (code heavy)
    
2. GestureDetector class to detect Android Core Gestures
    

- class made by finger interaction
    
- detects gestures and events using supplied MotionEvents
    
- use GestureDetector.OnGestureListener to respond when particular gesture has occurred
    

Classes:

|   |   |
|---|---|
|GestureDetector<br><br>  <br><br>onDown<br><br>onShowPress<br><br>onSingleTapUp<br><br>onSingleTapConfirmed<br><br>onDoubleTap<br><br>onDoubleTapEvent<br><br>onLongPress<br><br>onScroll<br><br>onFling|single touch gesture<br><br>  <br><br>called when user first presses<br><br>first press to indicate visually<br><br>when user lifts single tap<br><br>when single tap occurs<br><br>when double tap occurs<br><br>when event within double tap occurs<br><br>called when holds down longer than press <br><br>called on press and move (drag)<br><br>called on press and accelerate fast|
|ScaleGestureDetector|multi touch gesture|

  

Drag and Drop Framework: allows users to move data from one view to another in current layout using graphical drag and drop gesture

Framework:

1. Drag event class
    
2. Drag listeners
    
3. Touch listeners
    
4. Helper methods and classes (to show user data visualization)
    

Operation:

1. user makes gesture (signal to start dragging data)
    
2. app tells system drag is starting
    
3. system calls back to app to get representation of object being dragged (drag shadow visualization)
    
4. system sends drag events to drag event listener objects and drag event callback methods associated with View objects in layout
    
5. once user releases drag shadow system ends drag operation (show change in appearance to indicate data has been dropped)
    

Drag Event Listener

|   |   |
|---|---|
|setOnDragListener()<br><br>  <br><br>onDragEvent()|set drag event listener for view (what to drag view into)<br><br>callback for each view object|

Drag and Drop Process:

1. Started: gesture to begin drag
    

|   |   |
|---|---|
|startDrag(ClipData data, View.DragShadowBuilder shadowBuilder, Object myLocalState, int flags)|starts drag action<br><br>  <br><br>ClipData is data to move<br><br>shadowBuilder is drag visualization<br><br>myLocalState is object that initialized drag<br><br>flags: 0|

  

2. Continuing: continues to drag
    

- drag shadow intersects bounding boxes of View objects
    
- system sends one or more drag events to registered listeners
    
- listener can highlight view appearance (to indicate hover)
    

3. Dropped: drop drag shadow within bounding box of accepting view
    

- user releases drag shadow within bounding box of view that can accept data
    
- listener returns true if code to accept drop succeeds
    

4. Ended: drag over
    

- after user releases drag shadow
    
- system sends out drag action with type ACTION_DRAG_ENDED regardless of where drag shadow is released, event sent to every registered listener
    

  

Drag Events: system sends out drag event in form of DragEvent object containing action type telling step in drag/drop process

- get action type using getAction()
    

  

|   |   |
|---|---|
|ACTION_DRAG_STARTED<br><br>ACTION_DRAG_ENTERED<br><br>ACTION_DRAG_LOCATION<br><br>ACTION_DRAG_EXITED<br><br>ACTION_DRAG_DROP<br><br>ACTION_DRAG_ENDED|after startDrag() called<br><br>when enters listener<br><br>location in listener<br><br>when leaves listener<br><br>dragged view dropped in listener<br><br>when drag operation ending|

  

Drag Shadow: system displays drag shadow during drag to visualize where data is

|   |   |
|---|---|
|View.DragShadowBuilder(View)|get drag shadow with same appearance as view centered where user touching screen|
|View.DragShadowBuilder()|invisible drag shadow|

  

Designing Drag and Drop:

1. start drag
    

- starts with drag gesture (touch or long press on view with ontouchlistener or longclicklistener)
    
- in response create clipdata and shadowbuilder and startDrag()
    

2. respond to events during drag
    

- system dispatches drag event listeners of view objects and current layout
    
- listeners react by calling getAction() to get type
    

3. respond to drop
    

- during drag listeners that returned true in response to ACTION_DRAG_STARTED continue to receive drag events
    
- types of events: location of drag shadow, visibility of listeners view
    

4. end drag and drop operation
    

- uses releases drag shadow on view in application
    
- if view previously reported it could accept view being dragged sends ACTION_DROP
    

DropTarget: registered with onDragListener()

5. responding to drag end
    

- immediately after user releases drag shadow system sends drag event to all drag event listeners with action type ACTION_DRAG_ENDED indicating drag operation is over
    

  

Lecture Week 10: Network Operations

  

Web Services: means of exposing an API over a technology-neutral network endpoint/calling remote method that’s not tied to specific platform or vendor and get a result

JSON: JavaScript Object Notation: represents JavaScript objects as Strings, alternative to XML for passing data between servers and clients

Two Structures:

1. name-value pairs
    
2. ordered list of values (array)
    

|   |   |
|---|---|
|“Rock”|Value (string)|
|[“Rock”, “Dallas”, “Houston”]|Array|
|{“height”:70, “weight”:165}|Object|

  

Steps:

1. Check network connection
    

  

|   |   |
|---|---|
|getActiveNetworkInfo()<br><br>isConnected()|device may be out of network range or disconnected, check first if connected|
|public void checkConnection(){<br><br>  <br><br>ConnectivityManager cm = (ConnectivityManager)getSystemService(Context.CONNECTIVITY_SERVICE);<br><br>  <br><br>NetworkInfo ni = cm.getActiveNetworkInfo();<br><br>if (ni != null && ni.isConnected()){<br><br>//fetch data}<br><br>}|check if network connected before fetching data|

  

2. Perform network operation on separate thread (because of unpredictable delays, use external thread any time user accesses external services)
    

  

|   |   |
|---|---|
|public void getNetworkInfo(){<br><br>Thread t = new Thread(new GetNetworkInfoThread());<br><br>t.start();<br><br>}|create and start thread|
|JSONObject jo = new JSONObject(result);<br><br>JSONObject items = new JSONObject(jo.getString(“root”);|Thread takes JSON result and parses it<br><br>1. JSON result passed to constructor of JSONObject class creating new JSONObject with key/value mappings from JSON string<br>    <br>2. then get value of root key by using getString() method<br>    <br>3. values are passed as constructor of JSONObject class creating another JSONObject of items<br>    <br>4. extract items by calling getString method of items|

  

3. Connect and download data
    

HttpURLConnection: use HTTP to send and receive data, URL class also used, other classes from package java.io to process requests and responses

- lightweight client, suited for use with web services
    

|   |   |
|---|---|
|<uses-permission android:name=”android.permission.INTERNET”/><br><br>  <br><br><uses-permission android:name=”android.permission.ACCESS_NETWORK_STATE”/>|manifest permissions to access|

Usage:

1. Obtain new HttpURLConnection by calling URL.openConnection() and casting result to HttpURLConnection
    

|   |
|---|
|Url url = new URL(myUrl);<br><br>HttpURLConnection c = (HttpURLConnection) url.openConnection();|

  

2. Prepare the request
    

|   |
|---|
|c.setReadTimeout(1000);<br><br>c.setConnectTimeout(1500);<br><br>c.setRequestMethod(“GET”);|

  

3. Transmit data by writing to stream returned by getInputStream()
    

|   |
|---|
|c.setDoInput(true);<br><br>c.connect();<br><br>int response = c.getResponseCode();<br><br>is = c.getInputStream();|

4. Read response, response body may read from the stream returned by getInputStream(), if response has no body method returns empty stream
    

|   |
|---|
|String contentAsString = readIt(is, len);<br><br>return contentAsString;<br><br>  <br><br>public String readIt(InputStream stream, int len) throws IOException, UnsupportedEncodingException{<br><br>Reader reader = null;<br><br>reader = new InputStreamReader(stream, “UTF-8”);<br><br>char[] bugger = new char[len];<br><br>reader.read(buffer);<br><br>return new String(buffer);<br><br>}|

  

5. Disconnect
    

|   |
|---|
|}finally{<br><br>if (is != null){<br><br>is.close();<br><br>conn.disconnect();}|

  

Apache HttpClient: minimal code for simple HTTP processing, stable, very few bugs, development frozen since 2011, NOT recommended approach

4. Convert data from network into target data type
    

  
  

Lecture 11: Fragments in Android (LAST LECTURE!!!!)

  

Fragment:

- chunks of UI that can be reused and reconfigured within activity, activated or deactivated by user actions
    
- has own lifecycle, can process own elements (user interactions)
    
- introduced in API 11 Honeycomb
    
- can be added or removed from activity dynamically with Java or statically in XML
    

Usage: often used to create reconfigurable layouts to be responsive to multiple devices

Why? offers flexibility and dynamically changing UI

Steps:

1. Create Java class for Fragment extending Fragment class
    
2. Provide layout appearance for Fragment in XML
    
3. Override onCreateView() to link layout to Java class
    
4. Use fragment in XML (static bound to UI) or Java (dynamic, preferred)
    

  

Lifecycle:

1. fragment creation
    
2. fragment running
    
3. fragment destruction
    

States:

1. Java object
    
2. attached to layout XML (inflate)
    
3. visible UI on screen
    

  

Creation Methods:

|   |   |
|---|---|
|Activity|Fragment|
|onCreate()|onAttach() - after fragment is associated with the activity, get reference to activity object (context)|
|onAttachFragment()|onCreate() - class object created, do not access ui objects in this method, activity onCreate may not be completed yet|
||onCreateView() - layout is linked, return view for fragment|
||onActivityCreated() - called after activity onCreate has completed, finished creation, visible, can access/modify UI elements|
|onStart()|onStart()|
|onResume()|onResume()|

**activity created first, fragment needs activity to exist in

  

Destruction Methods:

  

|   |   |
|---|---|
|Activity|Fragment|
||onPause()|
|onPause()|onSaveInstanceState() - used to save information inside Bundle object|
|onSaveInstanceState()|onStop()|
|onStop()|onDestroyView() - layout destroyed, after fragment view hierarchy is no longer visible|
||onDestroy() - class destroyed, fragment still object attached to activity but not usable|
|onDestroy()|onDetach() - fragment untied from activity|

  

Adding a Fragment:

1. Create class (create new fragment file)
    
2. Create XML file for layout
    
3. Override onCreateView() method to link layout to Java class
    

  

|   |   |
|---|---|
|public View onCreateView (LayoutInflated inflater, ViewGroup container, Bundle savedInstanceState){<br><br>return inflater.inflate(R.layout.fragment_name, container, false);<br><br>}|done automatically in Android Studio when creating the fragment class|

  

1. XML: static association of fragment with activity with <fragment> tag
    
2. Java: programmatically add fragment at runtime in response to user interaction, preferred
    

Fragment Manager: one for each activity, maintains references to all fragments in activity

  

|   |   |
|---|---|
|getFragmentManager()|get reference to Fragment Manager|
|findFragmentById()<br><br>findFragmentByTag()|get reference to specific fragment|

  

Fragment Transactions:

1. Begin transaction
    

  

|   |   |
|---|---|
|MyFragmentClass f = new MyFragmentClass();<br><br>FragmentManager m = getFragmentManager();<br><br>  <br><br>FragmentTransaction t = m.beginTransaction();|get reference to fragment and fragment manager<br><br>  <br><br>begin transaction|

  

2. Add/remove/replace fragments in an activity
    

  

|   |   |
|---|---|
|t.add(R.id.MyLayout, f, “Fragment2”);|use transaction add method to add fragment f to MyLayout with “Fragment2” as key to identify value (f)|

  

3. Commit transaction
    

  

|   |   |
|---|---|
|t.commit();|save the transaction and apply|

  

Communication Between Fragments:

- interaction in F1 triggers response in F2, can be across more than one activity
    
- no direct communication between Fragments (not always together in same activity)
    
- use intermediary interface
    

Interface: 

- in code create interface
    
- contains method to carry out event
    
- activity implements interface to override method
    

Interface in Java: allow you to standardize across code![](https://lh7-us.googleusercontent.com/n455BsFvAvRMUOBM-oqZlAMMHg_woYotmtnsVleb_hzP3W3IXuxyT3dLiJLpwMyXHlTbCNEVlLJBPZhiWoT5pI-rtvR9FYXdv2gkL1xZ4jbAaa-aFkX-5f7eKj3qHsQDLDDfyd9R6xxwvBH16t7r5xo)

- contain methods with no body/implementation (have to instantiate when implemented)
    
- cannot create object of interface but can declare variable of interface type
    
- include comments describing methods so understand implementation
    

  

Communication Between Fragments:

F1: variable of interface type to access method

Activity: implements interface and transmit method, uses FragmentManager to get reference to Fragment 2, call fragment method

  

Flexible UI:

- fragments often used for modular design between portrait and landscape mode
    

