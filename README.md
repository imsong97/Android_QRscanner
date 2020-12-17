# Android_QRscanner
<h3>2020.12.09</h3>
안드로이드 QR코드 스캐너<br>
(zxing 라이브러리 이용)<br>

<img src="https://user-images.githubusercontent.com/56987664/101708543-c8b75a00-3ad0-11eb-8c1f-632a6e4dd25a.png" width="30%">
<br>
SCAN 버튼을 클릭하여 스캐너 실행<br>
스캔이 되면, Result에 스캔한 값 표시

<h4><2020.12기준 설정 방법><h4>

[build.gradle]<br>
implementation('com.journeyapps:zxing-android-embedded:4.1.0') { transitive = false } <br>
implementation 'com.google.zxing:core:3.3.0'

[AndroidMaifest.xml]<br>
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.CAMERA"/>
<uses-sdk tools:overrideLibrary="com.google.zxing.client.android" />
android:hardwareAccelerated="true"
 <activity
    android:name="com.journeyapps.barcodescanner.CaptureActivity"
    android:screenOrientation="fullSensor"
    tools:replace="screenOrientation" >
</activity>
