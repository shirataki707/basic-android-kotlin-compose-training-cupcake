Cupcake app
=================================

This app contains an order flow for cupcakes with options for quantity, flavor, and pickup date.
The order details get displayed on an order summary screen and can be shared to another app to
send the order.

Screenshot
----------

[//]: # (<img src="" width="300">)

Learn
-----

- Navigation Component
  - NavController
    - 画面遷移を行う
  - NavGraph
    - 画面遷移先の定義を行う
  - NavHost
    - NavGraphの現在地を表示するコンテナ
    - navHostControllerのインスタンスであるnavControllerを持つ
    - startDestinationで最初の画面を指定する
    
    ```kotlin 
    NavHost(
        navController = navController,
        startDestination = CupcakeScreen.Start.name,
        modifier = Modifier.padding(innerPadding)
    ) {
        composable() { } 
    }
    ```
    - NavHost内のcomposable()はrouteとcontentを持つ。つまり、Composableで作った画面がNavGraph上でどんな名前なのかを定義する。

Pre-requisites
--------------
* Experience with Kotlin syntax.
* How to create and run a project in Android Studio.
* How to create composable functions 


Getting Started
---------------
1. Install Android Studio, if you don't already have it.
2. Download the sample.
3. Import the sample into Android Studio.
4. Build and run the sample.
