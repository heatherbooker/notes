## HOLY MOTHER OF DON'T USE ABSOLUTE POSITIONING!!!
unless you want weird bleepin jumpy scrolly page-bloaty behaviour!

```css
label.cc-radioLabel {
  display: block;
  cursor: pointer;
  font-size: 12pt;
}

[type="radio"] {
  border: 0; 
  clip: rect(0 0 0 0); 
  height: 1px; margin: -1px; 
  overflow: hidden; 
  padding: 0; 
  width: 1px;
  display: none;
}

[type="radio"] + span {
  display: block;
  font-weight: 400;
}

[type="radio"] + span::before {
  content: '';
  display: inline-block;
  width: 15px;
  height: 15px;
  vertical-align: -1px;
  border-radius: 50%;
  border: 4px solid #fff;
  box-shadow: 0 0 0 1px #3c5a71;
  margin-right: 0.75em;
}

[type="radio"]:checked + span::before {
  background: #4EC1FF;
}
```