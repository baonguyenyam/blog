---
title: Fix lỗi kinh điển không scroll được page khi sử dụng phím trên Angular Material
layout: post-single
subtitle: Nếu bạn đang sử dụng AngularJS hay nói cách khác là Angular 1 cùng với bộ
  Material của Google thường gọi là Angular Material thì bạn sẽ gặp phải một lỗi kinh
  điển muôn thở của nó là khi chưa focus page bạn không thể cuộn trang bằng cách sử
  dụng phím mũi tên
date: '2016-03-17 20:00:00'
background: null
---

Nếu bạn đang sử dụng AngularJS hay nói cách khác là Angular 1 cùng với bộ Material của Google thường gọi là Angular Material thì bạn sẽ gặp phải một lỗi kinh điển muôn thở của nó là khi chưa focus page bạn không thể cuộn trang bằng cách sử dụng phím mũi tên lên/xuống hay PageUp/PageDown được ngay cả trang chính [https://material.angularjs.org](https://material.angularjs.org) cũng dính bug này. 

Để fix bug này bạn chỉ cần thêm 

```html
<div ng-keyup="watchKey($event)" ng-keydown="watchKey($event)"></div>
```

vào thẻ body và đặt id cho thẻ md-content ví dụ tôi đặt là khoai-content

# HTML  

```html
<body ng-keyup="watchKey($event)" ng-keydown="watchKey($event)">
   <md-content id="khoai-content"></md-content>
</body>
```

Sau cùng là copy đoạn JS dưới vào MainController của bạn là xong 

# JS 

```js
$scope.watchKeycount = 0, $scope.watchKey = function(e) { 
 var o = document.getElementById("khoai-content"),
 n = $scope.watchKeycount + 20,
 l = $scope.watchKeycount + 120,
 t = angular.element(o).scrollTop() - n,
 c = n + angular.element(o).scrollTop(),
 a = angular.element(o).scrollTop() - l,
 m = l + angular.element(o).scrollTop();
 38 === e.keyCode ? angular.element(o).scrollTop(t) : 33 === e.keyCode ? angular.element(o).scrollTop(a) : 34 === e.keyCode ? angular.element(o).scrollTop(m) : 40 === e.keyCode && angular.element(o).scrollTop(c) };
```


Trong này:

1. 20: là số pixel cuộn trang khi sử dụng mũi tên lên/xuống 
2. 120: là số pixel cuộn trang khi sử dụng PageUp/PageDown
3. document.getElementById("khoai-content"): Gán ID mà bạn đặt cho thẻ md-content vào đây 

DONE

Bảo Nguyên - HCM 2017