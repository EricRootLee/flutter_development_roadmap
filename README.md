# A Flutter Development Roadmap
by [Robert Henley](https://www.linkedin.com/in/robertallenhenley/)

After completing the "Complete 2020 Flutter Development Bookcamp" from The App Brewery, I found myself lost. There was a lot of Flutter documentation, videos, and other resources. I was not sure where to go next. I was one of a couple of people to raise this issue at the FlutterLDN/Flutter Berlin joint meetup in May 2020, but no one had an answer.

Serendipity struck that night when I found Oleksandr Leuschenko's (@olexale) [Highly Subjective Roadmap to Flutter Development](https://github.com/olexale/flutter_roadmap) on [Awesome Flutter](https://github.com/Solido/awesome-flutter). That roadmap let me assess where I was on my journey toward professional Flutter development.

I recommend you have a look at that roadmap; it's a beautiful infographic and the page has a lot of useful links.  

Over time, I found that I had my own ideas about the topic. So here is my version of a Flutter development roadmap. It is more detailed than the original, and at least as subjective. Please note that there is no one true path to learn Flutter, and I'm not following this roadmap in linear order myself -- I've skipped around it as various courses and activities filled in gaps. But it serves to keep me oriented as I progress, knowing what I know and what I've yet to learn. I hope it can help you find your own way.


## Getting Started

* **Flutter: What and Why?** (required)
  * High-level overview
  * Flutter's architecture
  * Walk through starter app code
  * Why Dart?

  Every course and book on Flutter covers this to a greater or lesser extent. 


* **Development Environment**
  * Android Studio or Visual Studio Code (required)
  * Flutter Command Line Interface (CLI) (helpful)
  * XCode and iOS emulator (helpful)
  * Git (helpful)
  * DartPad (optional)

  The App Brewery course covers development environment setup well, including iOS, but not including git. They show how to get starting by pulling projects from Github, but not the important source code control issues like branching, committing, pull requests, and merging. Seek that knowledge elsewhere, because it will be required in a professional job -- and even on your side projects, knowing you have the safety of saved code versions helps.

  DartPad is also a useful tool to know about. Whether you use it or not depends on your needs, but most video courses will introduce you to it when demonstrating Dart language concepts.


* **The Dart Language**
  * Dart basics: expressions, data types, identifiers and assignment, conditionals, basic looping. (required)
  * Objects: classes, properties, constructors, methods, and simple inheritance (required)
  * Functions: function declarations, positional parameters, named parameters, return values, callbacks (required)
  * Code Style (required)
  * Static analysis and linters, e.g. extra\_pedantic package (eventually required)
  * Essential Dart Libraries: dart:core and dart:math (eventually required)

  This is the level of Dart knowledge that you'll get from a chapter in a Flutter introductory book, and it's all you'll need to get going. The AppBrewery course introduces Dart language feature as they are needed for the sample applications being constructed and it will take you to the minimum level necessary. So would _Flutter in Action_.
  
  The "Effective Dart" section of the Flutter docs is your best resource about coding style. The IDEs will also help you adopt common coding conventions with warnings. You can enhance those warnings greatly with static analysis packages like extra\_pedantic.

  You also need to know some basic Dart library methods. But you don't yet need to know deep Object-Oriented Programming or Functional Programming practices at this stage -- they will come along later.

You're now ready to learn Flutter.

## Basic Flutter

* **Basic Widgets**
  * Material Widgets (required)
  * Stateful vs. Stateless widgets (required)
  * Basic Material Design (required)
  * Application assets (required)
  * Fonts (helpful)
  * Cupertino Widgets (helpful)
  * Material Design and Apple Mobile Human Interface Guidelines (eventually required)

  Flutter is all about widgets. The most used widgets in one survey were: Text, Container, Padding, Column, Icon, Row, SizedBox, Center, Expanded, and Scaffold. Those, plus StatelessWidget, StatefulWidget, and MaterialApp are a bare minimum. Learning the Icon widget also means you need to know about app assets, and font handling for Text is helpful. The AppBrewery class covers those and more; it even gives an introduction to the Cupertino widgets. But to learn many more widgets, watch the [Widget of the Week](https://bit.ly/2Njce4W) videos from the Flutter team and explore Material Design.
  
  
* **Basic Package Management**
  * Pub and pub.dev (required)
  * pubspec.yaml (required)
  * Popular libraries and plug-ins (helpful)

  Knowing how to find libraries and plug-ins on [pub.dev](https://pub.dev) and install them in your applications is essential. Knowing what packages are popular and fit your apps' needs will come over time: the "Package of the Week" videos on the Flutter YouTube channel can help. Some packages for specific needs are suggested below.


* **Basic Application Architecture -- State Management**
  * Local State via StatefulWidget vs. Shared state (required)
  * Lifting State Up pattern (required)
  * Provider package (required)

  The App Brewery full course has you covered here. See also the video ["Pragmatic State Management in Flutter"](https://www.youtube.com/watch?v=d_m5csmrf7I) from Google I/O 2019. Alternative state management approaches are discussed below, because they take a more holistic view of application architecture.


* **Multi-Page Applications**
  * Routing 1.0 (required)
  * Routing 2.0 and wrappers like the flow\_builder package (helpful -- required in some cases)
  * Code generation-based routing, e.g. the auto\_route package (helpful)
  * Hero animations (helpful)

  Moving beyond a single page is a key step in application organization. The AppBrewery course covers the Routing 1.0 methods, but not Routing 2.0, which is newer and more complex. Look into the Routing 2.0 wrapper packages that are emerging, like flow\_builder, or code-generating alternatives like auto\_route. And "hero animations" are a useful page transition technique.

By this point, you can create basic Flutter applications. Now move on to learn the tools for creating more sophisticated applications.

## Mid-Level Flutter

* **Networking**
  * Asynchronous Dart programming: Future, async/await (required)
  * HTTP client-server concepts and the http package (required)
  * JSON parsing and serialization: the dart:convert library (required)
  * RESTful API concepts (helpful)
  * Advanced http packages: dio (helpful)
  * Code-generation-based packages for networking: retrofit for Dart (uses dio and json\_serializable) (helpful) 
  * GraphQL concepts and the flutter\_graphql package (optional)

  The App Brewery course (and most books) covers the must-haves for Networking. As you go deeper, you'll want to understand how Representational State Transfer (REST) works, more advanced networking (like interceptors and transformers), and how to handle code-generation-based packages. Later, you can learn how GraphQL provides an alternative to REST.


* **Intermediate User Interfaces**
  * How layouts work (required)
  * Displaying lists: Dart Streams, StreamBuilder, and ListView (required)
  * Responsive UI: Change layout by display size
      * MediaQueryData display parameters (required)
      * responsive\_builder or responsive\_framework (helpful)
  * Adaptive UI: Show Material widgets on Android and Cupertino widgets on iOS
      * flutter\_platform\_widgets (helpful)
  * Animations
      * Implicit animations (required)
      * Transition animations (required)
      * Explicit animations (helpful)
      * Staggered animations (helpful)
      * Animation accessibility: when, how, and why not to animate (helpful)
      * Lottie (optional)
      * Rive (optional)

  Learning how layouts actually work is critical, and the [Understanding Constraints](https://flutter.dev/docs/development/ui/layout/constraints) documentation covers it best.
  
  Most user interfaces also need lists, which are driven by Dart Streams. Most books and courses cover this.
  
  More professional apps should also adapt to the display they run onto and probably should adapt to the platform as well. But you won't find much about this in introductory courses or books. At least learn about MediaQueryData.
  
  Animations are also helpful for some applications -- and you need to know how MediaQueryData tells your app not to animate, as well as how flashing, blinking, and parallax motion can harm users. Most Flutter books and video courses cover animation, except animation accessibility.
  
  
* **Simple Persistence**
  * Serializers: dart:convert library for non-JSON data (required)
  * Files: path\_provider and dart:io (required)
  * Local storage: the localstorage plugin (required)
  * Code-generation-based serialization: the built\_value package (helpful)
  * Keychain and Keystore: the flutter\_keychain package (optional)

  When you just need to store simple data, use the simplest storage solution possible.


* **Authentication**
  * Firebase Auth (required)
  * Google Sign In and google\_sign\_in package (helpful)
  * Sign In with Apple (eventually required)
  * Facebook sign in (optional)
  * Local market authentication providers (optional, but critical in some markets)

  Most apps have some sort of sign-in system: some based on id and password, others based on more complex server interactions. Mostly, Firebase Auth has your back here, and the App Brewery course covers it lightly, but in some cases you want more specific forms of authentication. Look for appropriate packages on [pub.dev](https://pub.dev). Know your user base: some less-obvious authentication providers are necessary in local markets, such as LINE Login in Japan. Also, Sign In with Apple is required for iOS apps that use other social login systems.


* **Database**
  * Firebase Firestore (required)
  * Relational databases: SQLite with sqflite package (required)
  * NoSQL databases: hive package (helpful)
  * Moor (optional)

  When your data storage requirements are larger, more complex, or more structured, use a database. The App Brewery course covers Firebase Firestore, which is a service, but client-local databases are also available.


* **Application Architecture -- Seperation of Concerns**
  * Business Logic Component (BLoC) pattern and flutter\_bloc package (required)
  * Dependency Injection: get\_it and injectable packages (required)
  * Immutability and Unidirectional Data Flow: the freezed package (helpful)
  * Design Patterns and Clean Architecture (helpful)
  * Redux (optional)
  * MobX (optional)
  * MV* architecture patterns: MVC, MVP, MVVM, etc. (optional)

  This is where apps start to get serious: these techniques separate larger apps into maintainable pieces. This is also the point where the ideas from books like _Design Patterns_ and _Clean Code_ / _Clean Architecture_ begin to come into play. You won't find this in introductory courses. Some of these topics are covered by [@resocoder's YouTube videos](https://www.youtube.com/c/ResoCoder). The BloC pattern is recommended by Google, especially in conjunction with the Provider state management package. (_Flutter: An Hands-On Guide to App Development_ has a good write-up of BLoC.) Redux and MobX come out of the React web community and remain popular and powerful, so although using them is optional, it's good to know what they are and what they can do. Ditto the MV* architectures: while they are less used in Flutter, people talk about them often as points of comparison.


* **Testing**
  * Unit Testing (required)
  * Mock Objects and the mockito package (required)
  * Widget Testing (required)
  * On-device testing with flutter\_driver package (required)
  * Integration testing with integration\_test package (required)
  * Behavior-Driven Development (BDD) and the gherkin package (for Dart), and/or the bdd\_widget\_test or flutter\_gherkin packages (for Flutter) (helpful)
  *	 Test-Driven Development (TDD) (helpful)

  The subject of testing is critical, and could easily be introduced earlier in training -- right after basic Dart, in fact. But that's not how most courses are structured, and it does help to have architectural patterns that seperate concerns in place first, because they make the app more testable. _Flutter in Action_ covers testing somewhat. The integration\_test package is new; see [Updates on Flutter Testing](https://medium.com/flutter/updates-on-flutter-testing-f54aa9f74c7e).

You can now build complex Flutters applications, but not quite professional-grade ones.

## Industrial-Grade Flutter

* **Advanced User Interfaces**
  * The widget lifecycle (required)
  * Element Tree and RenderObject (required)
  * Internationalization and Localization
      * flutter\_localization, \*App.localizationDelegates and .supportedLocales (required)
      * Intl package (required)
      * easy\_localization (helpful)
      * Localization services and automation (optional)
  * Accessibility: Allow assistive technologies like TalkBack and VoiceOver or an external keyboard/switch device to present and operate your app to people with disabilities
      * semanticLabel and excludeFromSemantics attributes (required)
      * Semantics widget (required)
      * SemanticsService.announce() (required)
      * MediaQueryData accessibility flags (eventually required)
      * Android Accessibility Analyzer and iOS Accessibility Inspector (helpful)
      * Manual accessibility testing (helpful)
  * Custom Painting (helpful)

  There's a lot more than widgets to a complex user interface. _Flutter in Action_ covers the widget lifecycle, the Render tree, accessibility, and custom painting. Internationalization is covered in the Flutter docs.


* **Advanced Dart**
  * Null Safety (required)
  * Isolates (required)
  * Modules and Libraries (helpful)
  * Intermediate to advanced Object-Oriented Programming (OOP) (helpful)
  * More Design Patterns and Design Principles: Gang of Four, SOLID, DRY, ... (helpful)
  * Functional Programming (FP) (optional)

  Null safety is critical for robust programming, but new to Dart -- or I would have listed it at the beginning. Dart Isolates allow true parallel execution of code, which is great for large computations. How Dart code can be modularized and placed in independent libraries will help simplify your projects. More advanced OOP, Design Patterns, and Design Principles become even more relevant at this level of complexity: look especially at SOLID to be sure your class hierarchies make sense and DRY to make sure your methods are small and well-structured. With Functional Programming, the discipline of using only immutable objects is elevated to high art with the introduction of higher-order functions, which are genuine power tools of abstract coding.


* **Performance Profiling**
  * Memory Leaks (required)
  * DevTools (required)
  * App Size (helpful)
  * CPU load and Jank (helpful)

  Sooner or later the size or speed of your app will not be what users need. Profiling tools will help you find out why and fix it. See the [Flutter Performance Docs](https://flutter.dev/docs/perf). See also Filip Hráček's [Performance Testing of Flutter Apps](https://medium.com/flutter/performance-testing-of-flutter-apps-df7669bb7df7) article and [Performance: Optimizing Your Flutter App](https://www.youtube.com/watch?v=SQcmrl_NkqY) video.


* **Plug-ins** (helpful)
  * Native Platform APIs:
      * iOS and Swift
      * Android and Kotlin
  * Platform Channels
  * Creating and publishing libraries and plug-ins on pub.dev

  You have already encountered packages and the [pub.dev](https://pub.dev) site. Learning how to create your own packages is valuable for large projects. And it's likely that someday you're going to have to debug a plug-in your app uses or write your own; at which point, you're going to need to know how to deal with the underlying native platform, its language(s) and API.


* **Flutter Internals (optional)**
  * Framework Architecture
  * Rendering Engine in-depth
  * Dart VM

  It's nice to know the underlying mechanisms of your framework, but you can be a very effective Flutter developer without it. Just be prepared to dive in and understand how things _really_ work when you have to. 

By this point, you know enough to build professional-grade applications with Flutter. But that doesn't get your app into people's hands.

## End-Game

* **Continuous Integration**
  * CI servers/services: Codemagic, Bitrise, Travis, GitHub Actions, Circle CI, etc. Pick one. (required)
  * Test Build Distribution: Microsoft AppCenter, TestFlight, Google Play Store Alpha, etc. (required)
  * FastLane (helpful)
  * Code metrics (optional)

  Automated builds based on your source code control system are a must! You'll also need a way to distribute test builds to manual testers, and ways to measure your code base health (e.g., test code coverage, static code analysis). This is "Flutter Ops" and you need to know about it.


* **Analytics (required)**
  * Usage Analytics
  * Crash Logging
  * A/B Testing

  Always measure your apps or you'll be just guessing who your users are and what they do with your app. Firebase Analytics is one tool for that. Especially, get crash reports from the field, because you can't find edge cases nearly as well as a lot of users can. A/B testing lets you figure out which alternative designs work better for people.


* **Stores (required)**
  * AppStore Guidelines
  * Google Play Store Guidelines
  * App Store Connect
  * Google Dev Console

  The stores are the final end-game: where you want your app to go. But can it? There are rules, and it's on you to know them. Plus, you have to know how to actually push the button to publish and what happens next.

## The End (of the Beginning)

Congratulations! You can now go deeper on anything above. Learning Flutter is an iterative process -- there is more to learn in any category, and likely categories you will discover that I haven't thought of. Also, new widgets, packages, and plug-ins are constantly being created, and you'll want to keep learning them. Have fun!


A Flutter Development Roadmap by [Robert Henley](https://www.linkedin.com/in/robertallenhenley/) is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1) <img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" />