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

В следующем примере будет изменен как цвет фона, так и положение элемента <div>, когда анимация завершена на 25%, на 50% и снова, когда анимация завершена на 100%:

```css
/* The animation code */
@keyframes example {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}

```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation3)

## animation-delay определяет задержку начала анимации.
В следующем примере перед запуском анимации имеется задержка в 2 секунды:
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
}
```
[try it ](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_delay)
Отрицательные значения также допускаются. При использовании отрицательных значений анимация начнется так, как если бы она уже воспроизводилась в течение N секунд.

В следующем примере анимация начнется так, как если бы она уже воспроизводилась в течение 2 секунд:
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: -2s;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_delay2)

## animation-iteration-count определяет количество раз, которое должна запускаться анимация.

```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 3;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_count)

## В следующем примере используется значение «бесконечно», чтобы анимация продолжалась вечно:

```css

div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}
```
[try it ](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_count2)