# Command almanac

This is a list of commands I frequently use. Most of them have to do with development for Apple platforms, although not all! 

## 📓 Almanac
### [Git] Remove all cached files to ensure there are no .gitignore files being tracked
```git rm --cached -r .```

### Swiftlint
```swiftlint autocorrect```

### Line count (for Obj-C/Swift/C++ project)
```find . "(" -name "*.m" -or -name "*.mm" -or -name "*.cpp" -or -name "*.swift" ")" -print0 | xargs -0 wc -l```

### Swift version (handy when reporting bugs)
```swift -version```

### Updating cocoapod
```
pod spec lint {{name}}.podspec
pod trunk push {{name}}.podspec
```

### Number of commits for git repo
```git rev-list --all --count```

### Delete unavailable iOS/watchOS/tvOS simulators
```xcrun simctl delete unavailable```

### Compile .java to .class and inspect bytecode
```
javac File.java
javap -c File.class
```

### LLDB debugging for tvOS (Swift)
```po self.view!.performSelector(Selector("_whyIsThisViewNotFocusable"))```

### LLDB debugging for tvOS with view address (Obj-C)
```po [((UIView *)0x{{address}}) performSelector:@selector(_whyIsThisViewNotFocusable)]```
