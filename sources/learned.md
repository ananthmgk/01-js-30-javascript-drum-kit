# CSS:
- `transition: all 0.07s;` (it changes their shape in 0.7 seconds speed).
- `transform: scale(1.1);` (it changes their shape to (1.1) times bigger).

# General:
[Click here to the site](https://www.toptal.com/developers/keycode) to get the javascript event code for each ecah key in the keyboard.

# HTML:
`data-key = '65'`  is an attribute that the value of the key letter can be stored.

# Javascript:
`window.addEventListener("keydown", () => {}` this `keydown` event works, when we press any key in the keyboard.
`document.querySelector(`audio[data-key ="${e.keyCode}"]`);` in this `audio[]` denotes the audio attributes.

- to remove the classList we can do in two methods. 
(1): by using `setTimeout()`;
(2):
```
function removeTransition(e) {
    if (e.propertyName !== 'transform') return;
    e.target.classList.remove('playing');
  }

  const keys = document.querySelectorAll('.key');
  keys.forEach(key => key.addEventListener('transitionend', removeTransition));
```