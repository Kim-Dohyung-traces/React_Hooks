# React_Hooks
React Hooks Fundamentals course  
## Rules of Hooks
* Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
* Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions.


### useState
useState는 가장 기본적인 Hook으로서 함수형 컴포넌트에서도 가변적인 상태를 지니고 있을 수 있게 해줍니다.  
useState를 사용할 때는 코드 상단에서 import 구문을 통하여 불러오고 다음과 같이 사용합니다.  
* 사용 예제 1
```javaScript
const [value, setValue] = useState(0);
```
* 사용 예제 2
```javaScript
const array = ['dog', 'cat', 'sheep'];
const [first, second] = array;
```

### useEffect
useEffect는 리액트 컴포넌트가 랜더링 될 때마다 특정 작업을 수행하도록 설정할 수 있는 Hook입니다.  
useEffect를 사용할 때는 코드 상단에서 import 구문을 통하여 불러오고 다음과 같이 사용합니다.  
클래스형 컴포넌트의 componentDidMount 와 componentDidUpdate를 합친 형태  
useEffect는 기본적으로 랜더링 되고난 직후마다 실행되며 두번째 파라미터 배열에 무엇을 넣느냐에 따라 실행되는 조건이 달라진다.  
만약 컴포넌트가 언마운트되기 전이나 업데이트 되기 직전에 어떠한 작업을 수행하고 싶다면 useEffect에서 뒷정리(cleanup) 함수를 반환해주어야 한다.  
* 마운트 될 때만 실행
```javaScript
 useEffect(() => {
    console.log('마운트 될 때만 실행됩니다.');
  }, []);
```
* 특정 값이 업데이트 될 때만 실행
```javaScript
  useEffect(() => {
    console.log("특정 값이 업데이트 될 때만 실행됩니다.");
  }, [value]);
```
---------------------------
 