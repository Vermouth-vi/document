
# Android 代码更新后RUN红屏

### 解决办法

新建文件夹  android/app/src/main/assets  
  
执行命令  
>> react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res  

重新 react-native run-android  

# IOS 代码更新后显示 No Bundle Url Present  

### 解决办法  
  
在 info.plist 文件中添加  

> <key>NSAppTransportSecurity</key>
	<dict>
		<key>NSAllowsArbitraryLoads</key>
		<true/>
		<key>NSAllowsArbitraryLoadsInWebContent</key>
		<true/>
		<key>NSAllowsLocalNetworking</key>
		<true/>
	</dict>
