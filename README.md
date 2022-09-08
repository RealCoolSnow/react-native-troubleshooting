- Error: spawn ./gradlew EACCES 
```bash
权限问题，在项目目录下执行:
chmod 755 android/gradlew
```
- Mac m1 - pod install Error
```bash
在ios下目录执行:
sudo arch -x86_64 gem install ffi
arch -x86_64 pod install
#arch -x86_64 pod update && pod install
```
- Ignoring ffi-1.14.1 because its extensions are not built. Try: gem pristine ffi --version 1.14.1
```bash
sudo gem install ffi -v 1.14.1
```
- Library not loaded: @rpath/hermes.framework/hermes
```bash
https://github.com/facebook/react-native/issues/34608#issuecomment-1239528471
```
- 构建iOS release版本
```bash
  1. 建立目录release_ios
  2. 执行 npx react-native bundle --entry-file index.js --platform ios --dev false --bundle-output release_ios/main.jsbundle --assets-dest release_ios/
  3. 拷贝/release_ios下内容到/ios目录，xcode打开工程即可开始正常打包流程
```
- 构建Android release版本
```bash  
1. 建立/android/app/src/main/assets文件夹
2. 执行 npx react-native bundle --entry-file index.js --platform android --dev false --bundle-output ./android/app/src/main/assets/index.android.bundle --assets-dest ./android/app/src/main/res/
3. 用Android Studio打开工程即可
```