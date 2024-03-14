<svelte:head>
    <title>Calculator</title>
</svelte:head>

<div class="calculator">
    <button class="btn-calc button-toggle">Переключить на режим ввода</button>
    <div class="screen">
      <input type="text" id="screen" class="screen__input" disabled />
    </div>
    <button class="btn-calc clear-btn">C</button>
    <div class="view button-view">
      <div class="keys">
        <button class="btn-calc operator-btn">/</button>
        <button class="btn-calc operator-btn">*</button>
        <button class="btn-calc operator-btn">-</button>
        <button class="btn-calc number-btn">8</button>
        <button class="btn-calc number-btn">9</button>
        <button class="btn-calc operator-btn">+</button>
        <button class="btn-calc number-btn">5</button>
        <button class="btn-calc number-btn">6</button>
        <button class="btn-calc number-btn">7</button>
        <button class="btn-calc number-btn">2</button>
        <button class="btn-calc number-btn">3</button>
        <button class="btn-calc number-btn">4</button>
        <button class="btn-calc zero-btn number-btn">0</button>
        <button class="btn-calc number-btn">1</button>
      </div>
    </div>
    <div class="view input-view hidden">
      <div class="input-group">
        <label for="first-number">Первое число:</label>
        <input type="number" class="first-number" id="first-number" />
      </div>
      <div class="input-group">
        <label for="operator">Оператор:</label>
        <select class="operator" id="operator">
          <option value="+">+</option>
          <option value="-">-</option>
          <option value="*">*</option>
          <option value="/">/</option>
        </select>
      </div>
      <div class="input-group">
        <label for="second-number">Второе число:</label>
        <input type="number" class="second-number" id="second-number" />
      </div>
    </div>
    <button class="btn-calc result-btn">=</button>
</div>

<style>

    * {
  box-sizing: border-box;
}
button {
  padding: 0;
  margin: 0;
  cursor: pointer;
  background-color: aliceblue;
  border: none;
  font-size: 20px;
}
 
.calculator {
  width: 282px;
  height: 400px;
  border: 1px solid lightblue;
  padding: 10px;
  border-radius: 8px;
  background-color: midnightblue;
  display: flex;
  flex-direction: column;
  margin: auto;
}
.screen {
  width: 100%;
  height: 50px;
  background-color: #fff;
}
.screen__input {
  height: 100%;
  font-size: 18px;
}
.keys {
  gap: 1px;
  display: flex;
  flex-wrap: wrap;
  height: 100%;
}
.view {
  height: 60%;
  margin-bottom: 10px;
}
.btn-calc {
  border-radius: 2px;
  height: 19%;
  width: 33%;
  padding: 0;
  margin: 0;
}
.btn-calc:hover {
  opacity: 0.9;
}
.result-btn {
  width: 100%;
  margin-top: auto;
  max-height: 50px;
  height: 10%;
  background-color: lightsteelblue;
}
.clear-btn {
  width: 100%;
  margin: 10px 0;
  max-height: 50px;
  height: 10%;
}
.operator-btn {
  background-color: lightsteelblue;
}
.zero-btn {
  width: 66.5%;
}
.button-toggle {
  font-size: 14px;
  height: 30px;
  margin-bottom: 10px;
  background-color: steelblue;
  border-radius: 4px;
  color: #ffffff;
  width: 100%;
}
.input-group {
  margin-bottom: 10px;
  width: 100%;
  color: #fff;
  font-weight: bold;
}
input,
select {
  width: 100%;
  padding: 10px;
}
.hidden {
  display: none;
}

</style>