# [배열 타입](#array-types)

배열(array)은 순서가 있는 단일 타입 요소들의 연속이다. 요소의 타입은 요소 타입(element type)이라고 부른다. 요소들의 개수는 길이(length) 라고 불리며 절대로 음수가 될 수 없다.

<pre>
<a id="ArrayType">ArrayType</a>   = "[" <a href="#ArrayLength">ArrayLength</a> "]" <a href="#ElementType">ElementType</a> .
<a id="ArrayLength">ArrayLength</a> = [Expression](/Expressions/) .
<a id="ElementType">ElementType</a> = [Type](/Types/) .
</pre>

길이는 배열 타입의 일부이다; 이는 음수가 아닌 `int`타입의 [상수](/Constants/)로 평가(evaluate)되어야 한다. 배열 `a`의 길이는 내장함수인  [len](/Built-in%20functions/length_and_capacity.html)을 통해 알 수 있다. 0 부터 `len(a)-1`까지의 정수 [인덱스](/Expressions/index_expressions.html)를 이용해 요소에 접근할 수 있다. 배열 타입은 기본적으로 1 차원(one-dimensional)이지만, 다차원(multi-dimensional)으로도 만들 수 있다.

```go
[32]byte
[2*N] struct { x, y int32 }
[1000]*float64
[3][5]int
[2][2][2]float64  // 다음과 같음 [2]([2]([2]float64))
```
