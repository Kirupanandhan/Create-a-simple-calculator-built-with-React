# Create-a-simple-calculator-built-with-React
## Program :-
```rjs
import React, { useState } from 'react';
const Calculator = () => {
  const [result, setResult] = useState('');
  const handleButtonClick = (value) => {
    setResult((prevResult) => prevResult + value);
  };
  const calculateResult = () => {
    try {
      const evaluatedResult = eval(result);
      setResult(evaluatedResult.toString());
    } catch (error) {
      setResult('Error');
    }
  };
  const clearResult = () => {
    setResult('');
  };
  return (
    <div className="calculator">
      <input type="text" value={result} readOnly />
      <div className="buttons">
        <button onClick={() => handleButtonClick('7')}>7</button>
        <button onClick={() => handleButtonClick('8')}>8</button>
        <button onClick={() => handleButtonClick('9')}>9</button>
        <button onClick={() => handleButtonClick('+')}>+</button>
        <button onClick={() => handleButtonClick('4')}>4</button>
        <button onClick={() => handleButtonClick('5')}>5</button>
        <button onClick={() => handleButtonClick('6')}>6</button>
        <button onClick={() => handleButtonClick('-')}>-</button>
        <button onClick={() => handleButtonClick('1')}>1</button>
        <button onClick={() => handleButtonClick('2')}>2</button>
        <button onClick={() => handleButtonClick('3')}>3</button>
        <button onClick={() => handleButtonClick('*')}>*</button>
        <button onClick={() => handleButtonClick('0')}>0</button>
        <button onClick={() => handleButtonClick('.')}>.</button>
        <button onClick={() => calculateResult()}>=</button>
        <button onClick={() => handleButtonClick('/')}>/</button>
        <button onClick={() => clearResult()}>C</button>
      </div>
    </div>
  );
};
export default Calculator;
```
### Output:-
![image](https://github.com/Kirupanandhan/Create-a-simple-calculator-built-with-React/assets/94386222/d5a6139d-26ac-4e1e-abb7-28edb45faa37)
