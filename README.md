Cupcake app
=================================

This app contains an order flow for cupcakes with options for quantity, flavor, and pickup date.
The order details get displayed on an order summary screen and can be shared to another app to
send the order.

Screenshot
----------

<img src="https://github.com/user-attachments/assets/62dd51d8-dbad-45e1-93be-33e1f27dda7e" width="300">

Learn
-----

- Navigation Component
  - NavController
    - 画面遷移を行う
    - NavHostが完成したら、後は各画面のComposableにnavControllerを渡して画面遷移すればよいが、Composableがnavigationを持つのは微妙。
      navigationは一元管理すべきだし、画面同士の関心を分離したい。なので、Callbackを使って画面遷移を行う。
    - navController.navigate()で画面遷移を行う
    - 戻る操作はnavController.popBackStack()で行う。routeで指定した画面に戻る。また、inclusiveでtrueを指定すると、指定した画面も含めてpopする。
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
