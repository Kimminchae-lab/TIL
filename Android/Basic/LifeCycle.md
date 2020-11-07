# 안드로이드 액티비티 생명주기

#### 1. 안드로이드의 4대 컴포넌트
- **액티비티**
- **서비스**
- **콘텐트제공자**
- **방송수신자**

## **1. 액티비티**

- **사용자가 상호작용하는 앱의 단일 화면**,
**UI를 담당하는 컴포넌트**

**(Android Studio**에서 **New Project** 생성 시, **Activity_Main.xml**, **MainActivity.kt** 두 가지  **Activity**가 만들어짐.**)**

- 안드로이드 앱은 반드시 하나 이상의 **Activity**를 가진다.
- **Activity**클래스를 상속받아 **Manifest**에 선언

### 액티비티 생명주기란?
- 배달 앱 실행 시, 로고가 뜬 후 마지막으로 있었던 탭으로 진입함.
- 로고 탭: **Activity**, 마지막으로 있었던 탭: **Activity**

이때, 액티비티들은 생명주기를 가진다. 생명주기에 따라 액티비티가 켜질수도, 멈출수도, 혹은 꺼질수도 있다.

#### 생명주기 함수
- **onCreate()**: 처음으로 앱을 실행할 때 호출된다. 주로 *화면 정의* 등의 용도로 수행함. **(배달 앱 실행)**
- **onStart()**: 말 그대로 **시작**. **onStart()** 후부터 사용자가 실제로 *Activity*를 볼 수 있음.**(로고 등장)**
- **onResume()**: *Activity*가 실제 사용자와 상호작용이 가능한 포그라운드에 위치하면 호출된다. 이 상태를 액티비티가 실행 중인 것으로 본다.
- **onPause()**: 포커스를 잃을 시 **(!hasFocus)** 호출된다.
- **onStop()**: *Activity*가 더 이상 보이지 않을 때 호출된다. 
- **onDestroy()**: *Activity*가 종료되거나 앱 프로세스 자체가 종료되면 호출된다.