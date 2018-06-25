---
title: Viết SASS nhanh chóng với k-sass-core
layout: post-single
subtitle: Một khi bạn thấy một số thứ được viết liên tục và tẻ nhạt trong CSS, đó
  là lúc mixin có thể giúp bạn bỏ được các công việc lặp đi lặp lại
date: '2018-06-25 18:00:00'
background: null
---

Nếu bạn sử dụng SASS trong quá trình phát triển các dự án của mình, chắc chắn rằng bạn biết về tầm quan trọng của mixin. Một khi bạn thấy một số thứ được viết liên tục và tẻ nhạt trong CSS, đó là lúc mixin có thể giúp bạn bỏ được các công việc lặp đi lặp lại. K-SASS-CORE chính là bản mixin chứa các khai báo CSS mà bạn có thể sử dụng lại trên toàn bộ trang web của mình.

Có rất nhiều mixins được thực hiện bởi các nhà phát triển khác nhau, tuy nhiên để giúp bạn khi làm việc với SASS cực hiệu quả tôi đã viết bộ CORE này từ kinh nghiệm thực tế và đã được nhiều lập trình viên áp dụng, hãy tìm hiểu và sẽ thấy được nhiều thứ khác nữa trong các thư viện mix-in K-SASS-CORE.

![https://raw.githubusercontent.com/baonguyenyam/k-sass-core/master/dist/images/img_01.png](https://raw.githubusercontent.com/baonguyenyam/k-sass-core/master/dist/images/img_01.png)

Hiện bộ này có hỗ trợ sử dụng cùng với Bootstrap vô cùng hiệu quả. 

Dưới đây là một vài ví dụ cơ bản:

#### SASS

```sass
.sample-0
  +pad(5px 'calc(100% - 4px)_' null 0) 
```

#### Kết quả 

```css
.sample-0 {
  margin-top: 5px;
  margin-right: calc(100% - 4px) !important;
  margin-left: 0;
}
```

#### SASS

```sass
.sample-0
  +pos(fixed, 1rem null null 0_)
```

#### Kết quả 

```css
.sample-0 {
  position: fixed;
  top: 1rem;
  left: 0 !important;
}
```

#### SASS

```sass
.box-shadow-2
  +box-shadow(2px 2px 5px rgba(0, 0, 0, 0.4), inset)
```

#### Kết quả 

```css
.box-shadow-2 {
  -ms-box-shadow: inset 2px 2px 5px rgba(0, 0, 0, 0.4);
  -o-box-shadow: inset 2px 2px 5px rgba(0, 0, 0, 0.4);
  box-shadow: inset 2px 2px 5px rgba(0, 0, 0, 0.4);
}
```

#### SASS

```sass
.background-gradient
  +background-gradient(#FFF, #DFDFDF)
```

#### Kết quả 

```css
.background-gradient {
  background: -webkit-gradient(linear, left top, right top, color-stop(0%, #FFF), color-stop(100%, #DFDFDF));
  background: -webkit-linear-gradient(0deg, #FFF 0%, #DFDFDF 100%);
  background: -webkit-linear-gradient(left, #FFF 0%, #DFDFDF 100%);
  background: linear-gradient(90deg, #FFF 0%, #DFDFDF 100%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#FFF', endColorstr='#DFDFDF', GradientType=0 );
}
```

[Link APIs](https://github.com/baonguyenyam/k-sass-core/wiki/Welcome-to-K-SASS-CORE)
[Link Source](https://github.com/baonguyenyam/k-sass-core)