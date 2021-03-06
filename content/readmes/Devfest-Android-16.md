---
title: Devfest-Android-16
date: 2020-12-12T08:27:16+0000
draft: false
---
# Devfest-Android-16

These are some basic guidelines everyone need to follow to keep the code uniform and clean as this is a single collaborative project.

- **Architecture:** This refers to the whole project structure including packaging techniques, hierarchies and Object Oriented Concepts used. 

   1. Entire Java part of the project will be divided into 3 major packages namely **Boundary**, **Control** and **Entity**. <br/>**Boundary** will include all the sub packages and classes that will handle the background tasks or act as an interface between the View (Front End) and underlying non-view APIs in SDK. For example network connection, REST or SDK APIs implementation, database connections, Content Providers etc-. <br/>**Control** will include all the sub packages and classes that are mostly non-instantiated. They are used for providing static content, perform calculation, algorithms,  contracts etc. For example static names and ids classes for database, constant Strings and integers, Calculators or Evaluators etc- <br/> **Entity** as the name suggest will include all the classes and packages that have some property and attributes. They are instantiated and their properties can be altered. For example Activities, Fragments, Dialogs and other Views, Object Oriented Entities like actors and real world entities.<br/>
  2. True **inheritance** and **interfaces** should be used where ever required. This could be needed where hierarchical objects are required with additional features other from base class, interfaces to subsequent callbacks to observe and transfer data between objects and classes.<br/>
  3. Avoid inner classes if possible and instead place the class in the corresponding packages which include other similar classes. <br/>
  4. In some places it is helpful to use inner classes like while building up **Gson** structure, View adaptors like of RecyclerView, View Pager etc. So try to use inner classes at those places.<br/>
  5.  In every activity, fragment, dialog and service, there should be three functions calls in onCreate() (or any other main function) : **init()** -> **setInit()** -> **setData()**. Rest of onCreate() function should be mostly empty. **init()** will initialise all the class variables, for example, initialising all views in the layouts. **setInit()** will initially setup those variables using their class functions like setting onClickListeners and others. **setData()** will finally be used to populate views with data, call network actions, request Loaders etc.

- **Nomenclature:** This refers to the naming scheme followed for files, packages, classes, methods variables, in-elements and attributes etc.
   1. **XML files:** These should be named hierarchically on the basis of their location with each entity separated by **underscore**. The name should be entirely in small case. For example *activity and fragments layouts* should be named as "**activity_name**" and "**fragment_name**" respectively. Another example like, if there is a *RecyclerView* inside a fragment (fragment_name) than its view holder layout should be named as "**fragment_name_recycler_row**". <br/>**Drawables** files should we named with same convention and icons should be preceded by "**ic**".
   2. **Classes:** All Java files includes classes and interfaces. These classes and interfaces should be strongly named in **Sentence Case** (SentenceCase) in **English**. The name should reflect the entity or purpose of class and should be minimal. Some of examples are "**NameActivity**", "**NameFragment**", "**User**", "**Profile**", "**SliderPagerAdapter**". Classes name should be minimal as most of its purpose will be reflected by its package name.
  3. **Variables and methods:** All the variables names, objects and methods mustl be named in **CamelCase** (*camelCase*). Like classes the names should be minimal and self-explanatory. **Static Variables** must be named in **Upper case** (*UPPER_CASE*) each word separated by underscore. 
   4. **Packages:** All Packages names should be single word and in **Sentence Case**. For example Activities, Fragments, Entity, Actors, Receivers etc-
   5. **In-elements and attributes:** All naming attributes in xml such as ids, transition names, strings and others should be named similar to xml files. Each word separated by underscore and entirely in lower case. These name should include the necessary hierarchy required. Some examples are "**@+id/submit_button**", "**@+id/title**", "**@string/disconnectivity_label**" etc.

- **Other Tips:** These tips will be useful to build a professional level and clean code.
  1. In order to document the code and for better understanding to everyone, try making comments wherever possible. While documenting methods, you can explain their each params and return value. 
  2. Parts of code which are incomplete or needed help should be mentioned with **TODOs** so that either others can complete it or won't touch it at all.
  3. Always before committing and pushing your code, pull the latest code from repository first. This will help avoiding merge conflicts and even if their is any you can rectify easily. Do not keep a long wait commit, frequent commits will help you know the status as well as to the team. This would also avoid code redundancy.
  4. If facing any issues related to project, may that be logical, or GitHub issues or some build errors, you need to raise a issue on this dependency. No problems will be rectified personally as this is part of transparency.
  5. No one should modify the base project structure that include build version, SDK version, API level, dependencies, and others. Currently the project is running on latest Gradle version 2.2.0-alpha3 and with latest Android Studio 2.2 Preview 3. Please update your Android Studio to latest in Canary Channel as well your SDK.<br/> <br/>
  

**These are the basic guidelines that are mandatory to  follow by all the contributors. These guidelines will ensure a uniform, professional and a pleasant code as well as uniformity among the team.**<br/>
**Everyone should abide by the guidelines and follow them strictly. If anyone found violating them, an issue can be raised against them here or can be warned by comments on his/her commits. An appropriate action will be taken if a contributor found violating guidelines repeatedly after warnings.**<br/>

*Prince Bansal* 
