# MVVM-studying<br><br>
<div align="center">
<h1>MVVM 패턴은 무엇인가?</h1><br>
<h4>MVVM 패턴은 Model, View, ViewModel을 분리해 뷰에 모델간의 의존성을 줄여주도록 한다.</h4>
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

- ## MVVM 패턴 적용방법
> 데이터바인딩까지 적용한다.
```
android {
        ...
        dataBinding {
            enabled = true
        }
    }
```
