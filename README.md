# Debounce And Throttle Typescript

## Throttling
  Throttling is a technique used to control the rate at which a function is executed, 
  ensuring it doesn’t run too frequently. In React Native development, 
  it’s vital for managing resource-intensive operations.

```
  static throttle<T extends (...args: any[]) => void>(func: T, delay: number): (...args: Parameters<T>) => void {
    let throttling = false;

    return (...args: Parameters<T>): void => {
      if (!throttling) {
        throttling = true;
        func(...args);
        setTimeout(() => {
          throttling = false;
        }, delay);
      }
    };
  }
```

## Debounce

  Debouncing is another JavaScript technique that ensures a function is only executed 
  after a certain delay following the last invocation. In React Native, 
  it’s crucial for smoother user interactions.

  ```
  static throttle<T extends (...args: any[]) => void>(func: T, delay: number): (...args: Parameters<T>) => void {
    let throttling = false;

    return (...args: Parameters<T>): void => {
      if (!throttling) {
        throttling = true;
        func(...args);
        setTimeout(() => {
          throttling = false;
        }, delay);
      }
    };
  }

```
