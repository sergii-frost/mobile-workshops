# [fit] Mobile: Common Mistakes & Solutions

---

# Agenda

- iOS: No No 😑
- iOS: Solutions 😋
- Android: No No 😑
- Android: Solutions 😋
- Android Architecture Components
- Worth Reading
- Homework

---

# iOS: No No 😑

- MVC aka Massive View Controller?
- Base Bean anti-pattern (BaseViewController)
- Heavy storyboards
- ...

---

# iOS: Solutions 😋

- Use MVVM to avoid Massive View Controllers
- Extract logic from ViewController to Util/Helper classes (if not UI related)
- Use extensions instead of Inheritance
- Use Coordinators
- 1 VC per storyboard
- Protocol Oriented Programming [WWDC](https://developer.apple.com/videos/play/wwdc2015/408/), [Realm](https://academy.realm.io/posts/appbuilders-natasha-muraschev-practical-protocol-oriented-programming/)

---

# Android: No No 😑

- `BaseActivity`
- `getActivity()` with class cast directly in fragments :)
- EventBus for sending data between Activities/Fragments
- Sending data to `newInstance()` without saving it to Fragment's `arguments`
- Updating UI from success/failure callbacks when app is not active

---

# Android: Solutions 😋

- Use Lifecycle callbacks [solution](https://blog.edfora.com/commonly-used-anti-patterns-in-android-a0c6fe070678)
- Use annotations, e.g. `@ActivityLayout`
- Use Listeners and implementaions, class cast in `onAttach`
- Always save Parcelable objects to fragment's arguments
- `EventBus` can be used, but NOT overused
- Use MVVM and LiveData updates

---

# [fit] Android Architecture Components

---

# Components

- Room
- ViewModel
- LiveData
- Lifecycle
- ...
- [Source](https://developer.android.com/topic/libraries/architecture/)

---

![Android Architecture Components](https://www.youtube.com/watch?v=vOJCrbr144o)

---

# Ideas:

- MessageHelper should be standalone class
- Logger should be standalone class
- Network layer structure? Normally we should support switching between platforms
- Extensions instead of subclasses (Swift, Kotlin)
- Localization handling (iOS)?
- Struct for Model classes (Swift)

---

# Worth Reading:

- [Fantastic iOS Architecture](https://github.com/onmyway133/fantastic-ios-architecture)
- [Fantastic Android Architecture](https://github.com/onmyway133/fantastic-android-architecture)
- [iOS Architecture Patterns](http://slides.com/borlov/arch/fullscreen#/8)
- [VIPER](https://www.objc.io/issues/13-architecture/viper/)
- [SOLID principles](https://medium.com/@ansujain/solid-principles-with-examples-in-ios-swift-bd3f4722a1f7)

---

# Homework

- Task: show github public repos for the user
- ⬇️
- iOS: Implement MVVM in basic UIViewController with UITableView + Network layer
- Android: Implement MVVM based on Android Architecture Components
