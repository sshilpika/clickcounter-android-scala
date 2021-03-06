[![Build Status](https://travis-ci.org/LoyolaChicagoCode/clickcounter-android-scala.svg?branch=master)](https://travis-ci.org/LoyolaChicagoCode/clickcounter-android-scala) 
[![Coverage Status](https://img.shields.io/coveralls/LoyolaChicagoCode/clickcounter-android-scala.svg)](https://coveralls.io/r/LoyolaChicagoCode/clickcounter-android-scala) 
[![Download](https://api.bintray.com/packages/loyolachicagocode/generic/clickcounter-android-scala/images/download.svg) ](https://bintray.com/loyolachicagocode/generic/clickcounter-android-scala/_latestVersion)

# Learning Objectives

This example is intended as a starting point for anyone planning develop
Android applications using Scala. Its learning objectives are:

- Android application development using Scala
    - using the Simple Build Tool (sbt) for Scala in conjunction with 
      [pfn's well-maintained plugin](https://github.com/pfn/android-sdk-plugin)
    - using IntelliJ IDEA
- Android application architecture for testability and maintainability
    - [Dependency Inversion Principle (DIP)](http://en.wikipedia.org/wiki/Dependency_inversion_principle)
    - [Model-View-Adapter](http://en.wikipedia.org/wiki/Model-view-adapter) architectural pattern
    - Separation of Android activity into event-handling and lifecycle management
    - Use of Scala primarily as a "better Java" (including mutable state)
- Effective testing
    - Unit testing and [Behavior-Driven Development (BDD)](http://en.wikipedia.org/wiki/Behavior-driven_development) 
      with ScalaTest
    - [Mock objects](http://en.wikipedia.org/wiki/Mock_object) with [Mockito](http://mockito.googlecode.com/)
    - Functional testing (out-of-container) using [Robolectric](http://robolectric.org/)

# Observations

- Existing isolation frameworks for Scala do not seem to handle dependencies
  added using the stackable trait (mixin) idiom. It is usually necessary to
  create one's own fakes, whether they are used as stubs or mocks.
- Robolectric-based tests cannot run in parallel, though regular unit tests
  can (and usually should). Therefore, it is easiest just to stack all
  abstract test superclasses (realized as stackable traits) onto a single
  concrete subclass (the Robolectric suite).


# Building and Running

Please refer to [these notes](http://lucoodevcourse.github.io/notes/scalaandroiddev.html) for details.

