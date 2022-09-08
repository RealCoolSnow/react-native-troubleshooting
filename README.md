# react-native-dev-issues

- 1. Error: spawn ./gradlew EACCES 
fix: 权限问题，在项目目录下执行
```bash
chmod 755 android/gradlew
```
- 2. Mac m1 - pod install Error
fix: 在ios下目录执行
```bash
sudo arch -x86_64 gem install ffi
arch -x86_64 pod install
||
arch -x86_64 pod update && pod install
```
- 3. Ignoring ffi-1.14.1 because its extensions are not built. Try: gem pristine ffi --version 1.14.1
fix: 
```bash
sudo gem install ffi -v 1.14.1
```