# animations
* all propertions
    * @keyframes
    * animation-name
    * animation-duration
    * animation-delay
    * animation-iteration-count
    * animation-direction
    * animation-timing-function
    * animation-fill-mode
    * animation
## Правило @keyframes
Когда вы указываете стили CSS внутри @keyframes правила, анимация в определенные моменты будет постепенно меняться с текущего стиля на новый.

Чтобы анимация работала, вы должны привязать анимацию к элементу.

В следующем примере анимация «example» привязывается к элементу <div>. Анимация будет длиться 4 секунды и постепенно изменит цвет фона элемента <div> с «красного» на «желтый»:

``` css
    /* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```
[ try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation1)
## Свойство animation-duration определяет

сколько времени потребуется для завершения анимации. Если animation-durationсвойство не указано, анимации не будет, поскольку значение по умолчанию — 0 с (0 секунд). 

В приведенном выше примере мы указали, когда будет меняться стиль, используя ключевые слова «от» и «до» (что соответствует 0 % (начало) и 100 % (завершение)).

Также можно использовать проценты. Используя проценты, вы можете добавить столько изменений стиля, сколько захотите.

В следующем примере будет изменен цвет фона элемента <div>, когда анимация завершена на 25%, на 50% и снова, когда анимация завершена на 100%:

```css
/* The animation code */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation2)