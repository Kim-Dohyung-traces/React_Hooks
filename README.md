# React_Hooks
React Hooks Fundamentals course  
-------------------
## Rules of Hooks
* Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
* Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions.


### useState
useState는 가장 기본적인 Hook으로서 함수형 컴포넌트에서도 가변적인 상태를 지니고 있을 수 있게 해줍니다.
useState를 사용할 때는 코드 상단에서 import 구문을 통하여 불러오고 다음과 같이 사용합니다.
use
```javaScript
const [value, setValue] = useState(0);
```