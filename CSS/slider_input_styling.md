## HOLY MOTHER OF DON'T USE ABSOLUTE POSITIONING!!!
unless you want weird bleepin jumpy scrolly page-bloaty behaviour!

```css
input[type=range].cc-questionBlock-slider {
  width: 80%;
  min-width: 90px;
  display: inline-block;
  margin: 0px 5px;
}

.cc-questionBlock-bottom-slider label.cc-questionBlock-sliderLabel {
  color: #a4a4a4;
  display: inline-block;
  width: 100px;
  text-align: center;
  white-space: normal;
  overflow-wrap: break-word;
  word-wrap: break-word;
  word-break: break-word;
}

input[type=range] {
  -webkit-appearance: none;
  border: 1px solid white;
}

input[type=range]:hover {
  cursor: pointer;
}

input[type=range]::-webkit-slider-runnable-track {
  height: 4px;
  background: #4EC1FF;
  border: none;
}

input[type=range]::-webkit-slider-thumb {
  -webkit-appearance: none;
  border: 3px solid #a4a4a4;
  height: 16px;
  width: 16px;
  border-radius: 50%;
  background: #f0f0f0;
  margin-top: -6px;
}

input[type=range]:focus {
  outline: none;
}

input[type=range]:focus::-webkit-slider-runnable-track {
  background: #4EC1FF;
}

input[type=range]::-moz-range-track {
  height: 5px;
  background: #4EC1FF;
  border: none;
}

input[type=range]::-moz-range-thumb {
  border: 3px solid #a4a4a4;
  height: 10px;
  width: 10px;
  border-radius: 50%;
  background: #f0f0f0;
}

input[type=range]:-moz-focusring{
  outline: 1px solid white;
  outline-offset: -1px;
}

input[type='range']::-moz-focus-outer {
  border: 0;
}

input[type=range]::-ms-track {
  height: 5px;
  background: transparent;
  border-color: transparent;
  border-width: 6px 0;
  color: transparent;
}

input[type=range]::-ms-fill-lower {
  background: #4EC1FF;
}

input[type=range]::-ms-fill-upper {
  background: #4EC1FF;
}

input[type=range]::-ms-thumb {
  border: 3px solid #a4a4a4;
  height: 10px;
  width: 10px;
  border-radius: 50%;
  background: #f0f0f0;
}

input[type=range]:focus::-ms-fill-lower {
  background: #4EC1FF;
}

input[type=range]:focus::-ms-fill-upper {
  background: #4EC1FF;
}
```