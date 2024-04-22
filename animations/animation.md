# animations
* all propertions
    * [@keyframes](#keyframes)
    * [animation-name](#animation-name)
    * [animation-duration](#animation-duration)
    * [animation-delay](#animation-delay)
    * [animation-iteration-count](#animation-iteration-count)
    * [animation-direction](#animation-direction)
    * [animation-timing-function](#animation-timing-function)
    * [animation-fill-mode](#animation-fill-mode)
    * [animation](#animation)
## Правило <a id="keyframes">@keyframes</a>
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
## Свойство <a id="animation-duration">animation-duration</a> определяет


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

## <a id="определяет задержку">animation-delay</a>  начала анимации.

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

## <a id="animation-iteration-count">animation-iteration-count</a> определяет количество раз, которое должна запускаться анимация.

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

##    <a id="animation-direction">animation-direction</a> определяет, должна ли анимация воспроизводиться вперед, назад или поочередно.
Свойство анимации-направления может иметь следующие значения:

* __normal__- Анимация воспроизводится как обычно (вперед). Это значение по умолчанию
* __reverse__- Анимация воспроизводится в обратном направлении (назад)
* __alternate__ - Анимация воспроизводится сначала вперед, затем назад
* __alternate-reverse__- Анимация воспроизводится сначала назад, затем вперед.

В следующем примере анимация будет запущена в обратном направлении (назад):

```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_direction)

В следующем примере используется значение «alternate», чтобы анимация сначала запускалась вперед, а затем назад:

Пример
```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_direction2)

В следующем примере используется значение «alternate-reverse», чтобы анимация сначала запускалась назад, а затем вперед:

```css
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate-reverse;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_direction3)

## <a id="animation-timing-function">animation-timing-function</a>  определяет кривую скорости анимации.

* Свойство анимации-тайминг-функции может иметь следующие значения:

    * __ease__- Определяет анимацию с медленным началом, затем быстрым, затем медленным завершением (это значение по умолчанию)
    * __linear__- Определяет анимацию с одинаковой скоростью от начала до конца
    * __ease-in__- Задает анимацию с медленным стартом
    * __ease-out__- Определяет анимацию с медленным концом
    * __ease-in-out__- Определяет анимацию с медленным началом и концом
    * cubic-bezier(n,n,n,n)- Позволяет определять собственные значения в функции кубической Безье.
В следующем примере показаны некоторые из различных кривых скорости, которые можно использовать:

```css
#div1 {animation-timing-function: linear;}
#div2 {animation-timing-function: ease;}
#div3 {animation-timing-function: ease-in;}
#div4 {animation-timing-function: ease-out;}
#div5 {animation-timing-function: ease-in-out;}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_speed)


## <a id="animation-fill-mode">animation-fill-mode</a> определяет стиль целевого элемента, когда анимация не воспроизводится (до ее начала, после ее окончания или и то, и другое).

CSS-анимация не влияет на элемент до воспроизведения первого ключевого кадра или после воспроизведения последнего ключевого кадра. Свойство __animation-fill-mode__ может переопределить это поведение.

Свойство animation-fill-modeопределяет стиль целевого элемента, когда анимация не воспроизводится (до ее начала, после ее окончания или и то, и другое).

* Свойство анимации-fill-mode может иметь следующие значения:

    * none- Значение по умолчанию. Анимация не будет применять стили к элементу до или после его выполнения.
    * forwards- Элемент сохранит значения стиля, заданные последним ключевым кадром (зависит от направления анимации и количества итераций анимации).
    * backwards- Элемент получит значения стиля, заданные первым ключевым кадром (в зависимости от направления анимации), и сохранит их в течение периода задержки анимации.
    * both- Анимация будет следовать правилам как вперед, так и назад, расширяя свойства анимации в обоих направлениях.

В следующем примере элемент <div> сохраняет значения стиля из последнего ключевого кадра после завершения анимации:

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}
```
[try it ](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_fill-mode)

В следующем примере элемент <div> получает значения стиля, установленные первым ключевым кадром перед началом анимации (во время периода задержки анимации):

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: backwards;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_fill-mode2)

В следующем примере элемент <div> получает значения стиля, установленные первым ключевым кадром перед началом анимации, и сохраняет значения стиля из последнего ключевого кадра, когда анимация заканчивается:

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: both;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation_fill-mode3)

Сокращенное свойство анимации
В приведенном ниже примере используются шесть свойств анимации:

```css
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation4)

Тот же эффект анимации, что и выше, может быть достигнут с помощью сокращенного animationсвойства:

```css
div {
  animation: example 5s linear 2s infinite alternate;
}
```
[try it](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation5)

* [@__keyframes__](https://www.w3schools.com/cssref/css3_pr_animation-keyframes.asp)	Specifies the animation code
* [__animation__](https://www.w3schools.com/cssref/css3_pr_animation.asp)	A shorthand property for setting all the animation properties
* [__animation-delay__](https://www.w3schools.com/cssref/css3_pr_animation-delay.asp)	Specifies a delay for the start of an animation
* [__animation-direction__](https://www.w3schools.com/cssref/css3_pr_animation-direction.asp)	Specifies whether an animation should be played forwards, backwards or in alternate cycles
* [__animation-duration__](https://www.w3schools.com/cssref/css3_pr_animation-duration.asp)	Specifies how long time an animation should take to complete one cycle
* [__animation-fill-mode__](https://www.w3schools.com/cssref/css3_pr_animation-fill-mode.asp)	Specifies a style for the element when the animation is not playing (before it starts, after it ends, or both)
* [__animation-iteration-count__](https://www.w3schools.com/cssref/css3_pr_animation-iteration-count.asp)	Specifies the number of times an animation should be played
* [__animation-name__](https://www.w3schools.com/cssref/css3_pr_animation-name.asp)	Specifies the name of the @keyframes animation
* [__animation-play-state__](https://www.w3schools.com/cssref/css3_pr_animation-play-state.asp)	Specifies whether the animation is running or paused
* [__animation-timing-function__](https://www.w3schools.com/cssref/css3_pr_animation-timing-function.asp) Specifies the speed curve of the animation