# 1.4 Library vs Framework

### 라이브러리는 코드 내에서 불러와 내가 직접적으로 사용하는 코드

### 프레임워크는 내가 실제로 수정하며 사용하는 코드가 아닌, 프레임워크의 규칙에 맞게 사용하고 프레임워크가 자동적으로 실행하는 것

# 2.3 SSR vs CSR

### 리액트는 Client Side Rendering 사용

##### CSR은 클라이언트에서 렌더링을 담당하기 때문에 소스코드에서 HTML의 내용을 확인할 수 없고 자바스크립트가 실행되어 구현된 컴포넌트를 렌더링함

##### 따라서 자바스크립트가 비활성화된 웹 브라우저는 리액트 컴포넌트들이 렌더링되지 않으며, 인터넷 속도가 느리다면 자바스크립트가 전체 컴포넌트를 가져오는 데 오랜 시간이 걸릴 수 있음

### 넥스트는 Server Side Rendering 사용

##### SSR은 서버에서 컴포넌트를 렌더링한 뒤 화면에 출력하기 때문에 소스코드에서 작성된 내용을 확인할 수 있다.

##### 자바스크립트의 영향을 받지 않는다(단순 HTML을 화면에 출력하는 것이기 때문).

# 2.4 Hydration

### JS가 활성화되어 있지 않을 때는 Link 태그가 HTML에서 a 태그로 변환되어 클릭하였을 때 Hard Navigation 방식으로 작동함 => 클릭할 때마다 새로고침됨

### JS를 활성화하면 a태그를 Link 태그가 a 태그를 대체하여 Client Side Only Navigation 방식으로 작동함 => 클릭해도 새로고침되지 않고 링크가 전환됨

##### Example : /about-us -> HTML로 변환 -> 화면에 출력 -> (React) -> init(HTML) -> 동적 상호작용 가능

# 2.5 'use client'

### Client에서 interactive 하게 하기 위해선 use client 필요 (Hydration)

### use client가 없는 컴포넌트는 기본적으로 server component

### use client를 사용한 컴포넌트도 기본적으로 서버에서 먼저 렌더링된 뒤 client에서 interactive하게 됨

# 2.6 Recap

### Client 컴포넌트엔 Server 컴포넌트가 들어갈 수 없기 때문에 Client 컴포넌트 내에 존재하는 컴포넌트는 Client 컴포넌트가 됨
