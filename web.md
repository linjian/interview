实现一个以下代码中的 useInterval()，使得 MyComponent 组件的 number 每秒 +1；且该组件中的按钮可以开始、暂停该定时器。

```javascript
function MyComponent() {
  const [running, setRunning] = useState(false);
  const [number, setNumber] = useState(0);

  useInterval(
      () => {
          setNumber((number) => number + 1);
      },
      running ? 1000 : null,
  );
  return (
      <div>
        <span>{number}</span>
        <button onClick={() => setRunning((s) => !s)}>
          {running ? '暂停' : '开始'}
        </button>
      </div>
  );
}
```
