# Spreadsheet-app

goormthon fullstack training PBL 04

### 주요 기능

1. 현재 focus된 cell의 row header와 column header가 함께 하늘색으로 하이라이트 되어야 한다.
2. "Export SpreadSheet" 버튼을 클릭하면 작성된 모든 데이터들을 csv파일로 생성 및 저장할 수 있다.
3. 생성된 Excel 파일을 구글 SpreadSheet에서 Import하면 동일한 데이터가 표시된다.

### 새로 배운 것

> #### [Blob Object]
>
> - Binary Large Object - 이미지, 사운드, 비디오 등의 멀티미디어 데이터를 다룰 때 사용하는 파일류의 불변 미가공 데이터
> - 텍스트와 이진 데이터 형태로 읽을 수 있다
> - File → Blob에 기반한 인터페이스. 사용자 시스템의 파일 지원을 위해 Blob 인터페이스를 상속해 기능을 확장한 것
> - `new Blob(array, options)`
>   - `array` : ArrayBuffer, ArrayBufferView, Blob(file), DOMString 객체
>   - `options` : type, ending 설정. type은 데이터의 MIME타입을 설정하며 기본값은 “”이다.
>
> #### [URL.createObjectURL()]
>
> - 매개변수에 제공된 객체를 나타내는 URL이 포함된 문자열(DOMString)을 생성함
> - 새 객체 URL은 지정된 File 또는 Blob 객체를 나타낸다
>
> #### [CSV파일 생성 및 저장]
>
> - 각 행 속 열 데이터를 “,”로, 각 행의 값들을 “\n”로 묶어 문자열 변수 생성
> - 이 문자열을 매개 변수로 하는 새로운 Blob 객체 생성
> - URL.createObjectURL()메소드를 이용, Blob 객체에 대한 URL 돔 스트링 생성
> - 변수에 새로운 a태그 element 생성해 할당
>   - href = 위의 URL을 넣어줌
>   - download = “저장할 파일명.csv” 속성 지정
> - a 태그가 담긴 변수.click() 해 파일이 저장되도록 함

### Preview

![spreadsheet-preview](/spreadsheet-preview)
