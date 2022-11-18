# MVVM-studying<br><br>
<div align="center">
<h1>MVVM 패턴은 무엇인가?</h1><br>
<h2>MVVM 패턴은 Model, View, ViewModel을 분리해 뷰에 모델간의 의존성을 줄여주도록 한다.</h2>
<img src="https://velog.velcdn.com/images%2Fdddooo9%2Fpost%2F02803dfe-c2e7-4cea-9cf7-74d757e60f2d%2Fimage.png" />

<h4><strong>뷰와 모델이 분리되어 있고, 이 분리된 두 조직 사이에서 뷰의 이벤트에 따라 모델이 데이터를 반환/저장하도록 통신하는 뷰모델이 존재한다.</strong></h4>

|뷰|뷰모델|모델|
|---|---|---|
|이벤트를 발생시켜 데이터 요청|||
||해당 데이터를 불러오는 모델의 메소드를<br> 호출||
|||뷰모델에서 요청하는 값을<br>반환||
||모델로부터 받은 값을 라이브데이터에 저<br>장||
|라이브데이터를 감지해 저장된 값을 뷰에<br> 출력|||
  
<br><br><br>
</div>

## 비즈니스 로직? 프리젠테이션 로직
> #### 비즈니스 로직?? 특정한 값을 얻기 위해 데이터의 처리를 수행, 원하는 값을 얻기 위해 백엔드에서 일어나는 각종 처리<br>
> #### 프리젠테이션 로직?? 보여주기 위한 로직을 말한다. 화면상의 디자인 구성을 위한 로직

<br><br><br>

## DataBinding & LiveData
> ### DataBinding?? xml파일에 Data를 연결해서 사용할 수 있게 도와준다.
> ### LiveData?? 관찰 가능한 데이터를 담아두는 클래스입니다.

<br><br><br>

# AAC(Android Architecture Component)
> ### MVVM 패턴을 쉽게 구현하도록 구글에서는 AAC(Android Architecture Component)를 제공한다.
![image](https://user-images.githubusercontent.com/118269278/202647821-acdc0b79-4f62-4228-ad73-8f53244baf0b.png)<br><br>
> ### ACC는 Android Jetpack의 구성 요소로 테스트와 유지관리가 쉬운 앱을 디자인하도록 돕는 라이브러리 모음
> - #### LiveData를 사용하여 기본 데이터베이스가 변경되면 뷰에 알리는 데이터 객체를 빌드합니다.
> - #### ViewModel은 앱 회전 시 제거되지 않는 UI 관련 데이터를 저장합니다.
> - #### Room은 SQLite 개체 매핑 라이브러리입니다.

# ViewModel
> ### ViewModel 클래스는 수명 주기를 고려하여 UI 관련 데이터를 저장하고 관리하도록 설계된 클래스이다.<br><br>
> ### ViewModel 클래스를 사용하면 화면 회전과 같이 구성을 변경 할 때도 데이터를 유지할 수 있다.
