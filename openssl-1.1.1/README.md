Applied changes to `config` file

```diff
diff --git a/config b/config
index b8adf34..88ffdf3 100755
--- a/config
+++ b/config
@@ -815,11 +815,13 @@ case "$GUESSOS" in
   # these are all covered by the catchall below
   i[3456]86-*-cygwin) OUT="Cygwin-x86" ;;
   *-*-cygwin) OUT="Cygwin-${MACHINE}" ;;
+  x86_64-*-android) OUT="android-x86_64" ;;
   x86-*-android|i?86-*-android) OUT="android-x86" ;;
   armv[7-9]*-*-android)
       OUT="android-armeabi"
       __CNF_CFLAGS="$__CNF_CFLAGS -march=armv7-a"
       __CNF_CXXFLAGS="$__CNF_CXXFLAGS -march=armv7-a";;
+  arm64-*-android) OUT="android-arm64" ;;
   arm*-*-android) OUT="android-armeabi" ;;
   *) OUT=`echo $GUESSOS | awk -F- '{print $3}'`;;
 esac
```
