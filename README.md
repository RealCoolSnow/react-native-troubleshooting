# react-native-dev-issues

- Error: spawn ./gradlew EACCES 
fix: 权限问题，在项目目录下执行
```bash
chmod 755 android/gradlew
```
- Mac m1 - pod install Error
fix: 在ios下目录执行
```bash
sudo arch -x86_64 gem install ffi
arch -x86_64 pod install
||
arch -x86_64 pod update && pod install
```
- Ignoring ffi-1.14.1 because its extensions are not built. Try: gem pristine ffi --version 1.14.1
fix: 
```bash
sudo gem install ffi -v 1.14.1
```
- Library not loaded: @rpath/hermes.framework/hermes
```bash
https://github.com/facebook/react-native/issues/34608#issuecomment-1239528471
```