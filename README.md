# **OpenGL-MyPaintProject**

# 프로젝트 개요

## 목적

이번 프로젝트는 OpenGL 라이브러리를 활용하여 간단한 그림판 프로그램을 만들어보는 것이다.  
처음부터 개발하는 것이 아니라 기존에 개발되었던 베이스 샘플 프로그램에 추가적으로 강력한 몇 가지 기능들을 추가해보겠다.

- 개발 환경: Visual Studio  
- 개발 언어: C++
- 활용 도구: OpenGL 라이브러리 

<br>

## 기존 프로그램

![image](https://user-images.githubusercontent.com/57826388/78450948-46fb6b00-76bd-11ea-8b56-ea01bf91a946.png)

 - 기본 Paint 프로그램은 다섯 가지의 주요 기능과 두 가지의 부가 기능으로 구성되어 있으	며 전체적인 실행 화면은 다음과 같다. 
 
 - 선 그리기와 사각형 그리기는 화면상의 두 지점을 지정하여 그리는 방식이고 삼각형 그리	기는 화면상의 세 지점을 지정하여 그리는 방식이다.  
 점 그리기는 랜덤한 색상으로 찍히	는 방식이며 텍스트 입력은 한글을 제외한 영문자, 숫자, 특수문자가 입력이 가능하도록 	구성되어 있다.  
 부가 기능은 마우스 우클릭으로 프로그램을 종료하는 quit과 화면	을 초기화하는 clear로 구성되어 있다.


<br>

# 추가 기능 구현

- 새롭게 추가된 페인팅과 관련된 주요 기능들은 열두 가지로 
  원 그리기, 브러쉬, 지우개, 스프레이, 별 그리기, 하트 그리기, 브러쉬 두께 지정, 
  점선 기능, 배경색 지정 및 무작위 배경 색상, 무작위 색상 지정, 잘라내기 기능들이 있다. 

<br>

 ## 원 그리기

- 원 그리기 기능에 해당하는 아이콘은 다음과 같으며 
   극좌표 원 그리기 알고리즘을 이용하여 구현하였다.
   해당 기능 예시와 원 그리기 기능과 관련된 코드는 
   다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78450996-a35e8a80-76bd-11ea-9747-6ad025b98ca4.png)

<br>

 ## 브러쉬 기능

 - 브러쉬 기능에 해당하는 아이콘은 다음과 같으며 
  원을 반복적으로 누적표현 함으로써 구현하였다.  
  브러쉬 기능 예시와 관련된 코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78451029-c9842a80-76bd-11ea-8ca4-6ea36f24e188.png)

<br>

 ## 지우개 기능
 
 - 지우개 기능에 해당하는 아이콘은 다음과 같고 
      기능 구현은 브러쉬와 동일하며 색상만 배경색과   동일하게 적용하여 구현하였다.  
      지우개 기능 예시와 관련된 코드는 다음과 같다. 

![image](https://user-images.githubusercontent.com/57826388/78451045-f1738e00-76bd-11ea-957c-80b70235bce2.png)

<br>

 ## 스프레이 기능

 - 스프레이 기능에 해당하는 아이콘은 다음과 같고 
   구현 원리는 원그리기 알고리즘에서 rand() 옵션을 
   사용하였으며, 원을 그릴 때 무작위로 정점을 선택
   하여 구현하였다.  
    스프레이 기능 예시와 관련된 
    코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78451070-297ad100-76be-11ea-8fcd-6aa7effd5fa6.png)

<br>

 ## 별 그리기 기능

  - 별 그리기 기능에 해당하는 아이콘은 다음과 같고 
  극좌표 방정식을 이용하여 구현하였다.  
  별 그리기 기능 예시와 관련된 코드는 다음과 같다.
 
 ![image](https://user-images.githubusercontent.com/57826388/78451085-4b745380-76be-11ea-816c-15eb6011e4e2.png)

<br>

 ## 하트 그리기 기능
 
 ![image](https://user-images.githubusercontent.com/57826388/78451095-63e46e00-76be-11ea-9a0a-3ec9b1f0640a.png)

<br>

 ## 브러쉬 두께 지정

 - 브러쉬 두께 기능은 Pixel Size라는 메뉴를 통해 구현되어
  있으며 각각 픽셀의 크기를 2배, 배씩 증감시켜 두께를
  표현한다.  
  해당 기능 예시와 코드는 다음과 같다.
 
 ![image](https://user-images.githubusercontent.com/57826388/78451126-84142d00-76be-11ea-9724-fd221af8166d.png)

<br>

 ## 점선 기능

 - 점선 기능은 Line 메뉴를 통해 구현되어 있으며, 메뉴는 6가지 점선 스타일과 다시 실선으로 만들어 주는 기능들로 이루어져 있다.  
점선 스타일은 넘버링이 증가할수록 점선의 간격이 넓어진다.  
  해당 기능 예시와 관련된 코드는 다음과 같다.
 
 ![image](https://user-images.githubusercontent.com/57826388/78451165-bd4c9d00-76be-11ea-84dc-0ee3cf8b0333.png)

<br>

 ## 배경색 및 배경색 무작위 색상 지정 기능

 - 배경색 지정 관련 기능은 Background Color 메뉴를 통해 구현되어 있으며, 9가지 지정 색상(Default 포함)과 무작위 색상 지정 기능으로이루어져 있다. 무작위 색상 지정 기능은 누를 때마다 색상이 바뀌는 방식이다.  
 해당 예시와 코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78451181-e2411000-76be-11ea-81e7-5dfdedb9ec82.png)

<br>

 ## 무작위 색상 지정 기능
 - 기존 색상 지정 메뉴에 있던 8가지 색상에 무작위 색상 지정 기능을추가한 것으로, 해당 기능을 선택한 후 드로잉을 할 때마다 색상이 바뀌는 방식이다.  
 텍스트 입력과 지우개 기능엔 적용되지 않으며, 원의 누적 표현 방식을 이용한 스프레이와 무작위 정점을 활용한 브러쉬 기능에서는 원의 색상이 촘촘히 바뀌는 것을 확인할 수 있다.  
 해당 예시와 코드는 다음과 같다.

 ![image](https://user-images.githubusercontent.com/57826388/78451208-1c121680-76bf-11ea-9805-c6b7fa5078c6.png)
 
<br>

 ## 잘라내기 기능

 - Erase Type 메뉴는 기본 지우개 타입과 잘라내기 타입으로 이루어져 있으며, 잘라내기 기능은 배경색과 동일한 색상으로 사각형 영역을 지정하는 방식으로 구현되어 있다.  
 해당 예시와 코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78451247-6e533780-76bf-11ea-977e-07103bf1905a.png)
![image](https://user-images.githubusercontent.com/57826388/78451248-714e2800-76bf-11ea-89c9-1ad168a7e0b5.png)

 <br>

 ## 안티앨리어싱 기능

 - 안티앨리어싱은 각종 이미지나 도형, 문자 등을 구현하는 과정에서 발생하는 계단현상(Aliasing)을 완화해주는 기술이다. ON/OFF 두 가지 기능으로 이루어져 있다.  
 해당 예시와 코드는 다음과 같다.

 ![image](https://user-images.githubusercontent.com/57826388/78451266-8dea6000-76bf-11ea-8b10-b000916a4d1d.png)
![image](https://user-images.githubusercontent.com/57826388/78451267-90e55080-76bf-11ea-8bda-fb118074a822.png)

 <br>

 ## 저장하기 기능

- 기존의 마우스 우클릭에서 존재하던 두 가지 기능에서 새로 추가된 기능으로 입력한 내용을 비트맵 형식으로 저장한다. 실행파일을 포함하는 폴더에 capture.bmp 형식으로 저장된다.  
해당 기능과 예시와 관련된 코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78451292-b1ada600-76bf-11ea-9161-8eb76dc9227c.png)

 <br>

 ## 불러오기 기능

 - 앞의 저장하기 기능과 동일하게 새로 추가된 기능이다. 실행파일이 있는 폴더 속의 capture.bmp 파일을 실행파일로 읽어와 화면에 뿌려준다.  
 해당 예시와 관련 코드는 다음과 같다.

![image](https://user-images.githubusercontent.com/57826388/78451304-c2f6b280-76bf-11ea-928c-7912049e37fa.png)
![image](https://user-images.githubusercontent.com/57826388/78451306-c5f1a300-76bf-11ea-9b2b-7a8a0db7faf8.png)

 <br>

 # 최종 결과

 - 다음은 최종 시연 결과이며, 기존의 기능과 추가된 기능들 모두 원활하게 	동작하는 것을 확인할 수 있다.

 ![image](https://user-images.githubusercontent.com/57826388/78451314-da35a000-76bf-11ea-9a5f-a8fbf671eee6.png)

