# Data Binding

> DOM 기반 HTML Template 에  Vue 데이터를 바인딩 하는 방법은 아래와 같이 크게 3가지

* Interploation (값 대입)
* Binding Expressions (값 연결)
* Directives (디렉티브 사용)

<br />

---

# 예제

* Interpolation 

> 기본직인 바인딩 체계 MUstche {{}} 를 따름.

```html
<span>Message : {{ msg }}</span>
<span>This will never change : {{ * msg }}</span> <!--에스크립은 변하지 않게 선언, 예전방 -->
<span v-once>{{ msg }}</span>                     <!--최근의 사용방법-->
<div id="item-{{ id }}"></div>
```

* Binding Expressions 

> {{}}를 이용한 데이터 바인딩을 할 때 자바스크립트 표현식을 사용할 수 있다.

```html
<div>{{ number + 1}}</div> <!--가장 지향하는 방법-->
<div>{{ message.split(''}.reverse().join('')}</div>
<div>{{ if (ok){ return message}}</div> <!--여러 연산의 경우에는 허용하지않음-->
```

* Directives

> Vue에서 제공하는 특별한 Attributes이며 v-의 접두사를 가짐

```html
<p v-if="login">Hello</p>
<p v-on:click="doSomething"></p>
```

* class Binding

> CSS 스타일링을 위해서 class를 아래 방법으로 추가할 수 있

```html
<div class="static" v-bind:class="{{ 'class-a' : isA , 'class-b' : isB}}"></div> <!--클래스로 받아옮-->
<script>
    data : {
        isA: true,
        isB: false
    };
</script>
```


