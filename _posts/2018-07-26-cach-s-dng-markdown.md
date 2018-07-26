---
title: Cách sử dụng markdown
layout: post-single
subtitle: Markdown là ngôn ngữ đánh dấu văn bản được tạo ra bởi John Gruber, sử dụng
  cú pháp khá đơn giản và dễ hiểu, dễ nhớ.
date: '2018-07-26 10:30:00'
background: null
---

<h1>Mở đầu</h1>
<p>Markdown là ngôn ngữ đánh dấu văn bản được tạo ra bởi John Gruber, sử dụng cú pháp khá đơn giản và dễ hiểu, dễ nhớ. Nếu nắm vững các cú pháp của Markdown bạn có thể trình bày bài viết của mình một cách mạch lạc, ấn tượng mà không mất nhiều thời gian. Bài viết dưới đây sẽ hướng dẫn để bạn có thể hiểu và sử dụng được ngay những cú pháp đó.</p> 
<h1>Nội dung</h1>
<h2>Tiêu đề</h2>
<p>Bạn có thể viết các lớp tiêu đề h1, h2, h3 cho đến h6 bằng cách thêm số lượng ký tự # tương ứng vào đầu dòng. Một ký tự # tương đương với h1, 2 ký tự # tương đương với h2 ...</p>
<p>Ví dụ khi viết</p>
<pre class="language-none"><code class="language-none"># h1
## h2
### h3
#### h4
##### h5
###### h6
</code></pre>
<p>thì kết quả sẽ là</p>
<h1>h1</h1>
<h2>h2</h2>
<h3>h3</h3>
<h4>h4</h4>
<h5>h5</h5>
<h6>h6</h6>
<h2>Nhấn mạnh, highlight</h2>
<p>Bạn có thể kẹp một từ ở đầu và cuối bằng 1 ký tự * để <em>in nghiêng</em>, 2 ký tự ** để <strong>bôi đậm</strong>, và 3 ký tự *** để <em><strong>vừa in nghiêng vừa bôi đậm</strong></em>.</p>
<pre class="language-none"><code class="language-none">*in nghiêng*
**bôi đậm**
***vừa in nghiêng vừa bôi đậm***
</code></pre>
<p>Để viết <code>inline code</code>, bạn dùng cú pháp</p>
<pre class="language-none"><code class="language-none">`inlide code`
</code></pre>
<p>Để highlight block code, bạn viết</p>
<p>```php</p>
<p>echo (&quot;highlight code&quot;);</p>
<p>```</p>
<p>sẽ được kết quả là</p>
<pre class="language-php"><code class="language-php"><span class="token keyword">echo</span> <span class="token punctuation">(</span><span class="token double-quoted-string string">"highlight code"</span><span class="token punctuation">)</span>
</code></pre>
<h2>Link, image</h2>
<h3>Link</h3>
<p>Để chèn link vào bài viết, bạn dùng cú pháp sau</p>
<pre class="language-none"><code class="language-none">[title](http://~)
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">[Markdown](http://https://vi.wikipedia.org/wiki/Markdown)
</code></pre>
<p>=&gt; <a href="http://https://vi.wikipedia.org/wiki/Markdown" target="_blank">Markdown</a></p>
<h3>Image</h3>
<p>Cú pháp chèn hình ảnh như sau</p>
<pre class="language-none"><code class="language-none">![alt](http://~)
</code></pre>
<p>Ví dụ nếu viết</p>
<pre class="language-none"><code class="language-none">![alt](http://http://mikemclin.net/mmwp/wp-content/uploads/2013/03/markdown-syntax-language.png)
</code></pre>
<p>thì bạn sẽ chèn được hình ảnh như thế này rồi.
<img src="http://mikemclin.net/mmwp/wp-content/uploads/2013/03/markdown-syntax-language.png" alt="alt"></p>
<h2>List</h2>
<h3>List dạng gạch đầu dòng</h3>
<pre class="language-none"><code class="language-none">* item
</code></pre>
<p>Ví dụ bạn viết</p>
<pre class="language-none"><code class="language-none">* item 1
* item 2
* item 3
</code></pre>
<p>thì sẽ được kết quả như sau</p>
<ul>
<li>item 1</li>
<li>item 2</li>
<li>item 3</li>
</ul>
<h3>List dạng số</h3>
<pre class="language-none"><code class="language-none">1. item
</code></pre>
<p>Ví dụ bạn viết</p>
<pre class="language-none"><code class="language-none">1. item 1
2. item 2
3. item 3
</code></pre>
<p>thì sẽ được kết quả như sau</p>
<ol>
<li>item 1</li>
<li>item 2</li>
<li>item 3</li>
</ol>
<h2>Horizonal rules</h2>
<p>Để có được horizonal rules bạn chỉ cần viết *** như sau</p>
<pre class="language-none"><code class="language-none">***
horizonal rules
</code></pre>
<p>kết quả là</p>
<hr>
<p>horizonal rules</p>
<h2>Blockquotes</h2>
<p>Cú pháp blockquotes là</p>
<pre class="language-none"><code class="language-none">&gt; text
</code></pre>
<p>kết quả:</p>
<blockquote>
<p>text</p>
</blockquote>
<h2>Escape markdown</h2>
<p>Đôi khi trong khi viết bài bạn sẽ sử dụng những kí kiệu trùng với cú pháp của markdown. Để phân biệt, bạn chỉ cần thêm dấu \ trước những kí hiệu đó là được.</p>
<p>Ví dụ nếu bạn viết</p>
<pre class="language-none"><code class="language-none">\*text*
</code></pre>
<p>thì kết quả sẽ là *text* chứ không phải <em>text</em>(in nghiêng)</p>
<h2>Viblo advanced Markdown Embedment</h2>
<p>Hiện tại Viblo hỗ trợ chèn link từ <strong>Youtube</strong>, <strong>Vimeo</strong>, <strong>Slideshare</strong>, <strong>Codepen</strong>, <strong>Gist</strong>, <strong>JSFiddle</strong> và <strong>Google Slide</strong>. Cú pháp như dưới đây:</p>
<h3>Youtube</h3>
<pre class="language-none"><code class="language-none">{@youtube: Youtube ID or URL}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@youtube: https://www.youtube.com/watch?v=HndN6P9ke6U}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" type="text/html" src="https://www.youtube.com/embed/HndN6P9ke6U" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div></p>
<h3>Vimeo</h3>
<pre class="language-none"><code class="language-none">{@vimeo: Vimeo ID or URL}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@vimeo: https://vimeo.com/62604492}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" type="text/html" src="https://player.vimeo.com/video/62604492" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div></p>
<h3>Slideshare</h3>
<pre class="language-none"><code class="language-none">{@slideshare: Slideshare ID or URL}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@slideshare: http://www.slideshare.net/asanzdiego/markdown-slides-en}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" type="text/html" src="https://viblo.asia/embed/slideshare/?url=http://www.slideshare.net/asanzdiego/markdown-slides-en" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div></p>
<h3>Codepen</h3>
<pre class="language-none"><code class="language-none">{@codepen: Codepen ID or URL}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@codepen: https://codepen.io/nickmoreton/pen/gbyygq}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" height="400" src="https://codepen.io/nickmoreton/embed/gbyygq?height=400&theme-id=0&default-tab=js,result&embed-version=2" frameborder="0" allowtransparency webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div></p>
<h3>Gist</h3>
<pre class="language-none"><code class="language-none">{@gist: Gist ID or URL}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@gist: https://gist.github.com/JeffreyWay/207e3bfdb5cafff050a1d75dbf755a5c}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" id="sdehpyj" type="text/html" srcdoc="<html><body><script src='https://gist.github.com/JeffreyWay/207e3bfdb5cafff050a1d75dbf755a5c.js'></script></body></html>" frameborder="0"></iframe></div></p>
<h3>JSFiddle</h3>
<pre class="language-none"><code class="language-none">{@jsfiddle: JSFiddle URL}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@jsfiddle: http://jsfiddle.net/kizu/zfUyN/}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://jsfiddle.net/kizu/zfUyN/embedded" height="400"></iframe></div></p>
<h3>Google slide</h3>
<p>Đối với tài liệu bạn muốn chia sẻ từ Google slide thì bạn cần phải public tài liệu đó để mọi người có thể xem được, rồi dùng link tài liệu đã được public với cú pháp sau:</p>
<pre class="language-none"><code class="language-none">{@googleslide: document_link}
</code></pre>
<p>Ví dụ</p>
<pre class="language-none"><code class="language-none">{@googleslide: https://docs.google.com/presentation/d/1nJ65LUlu9k_tfuQJ4jq4z-qmqOQZ0DjKKw8wn5qnnFA/edit#slide=id.p}
</code></pre>
<p><div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://docs.google.com/presentation/d/1nJ65LUlu9k_tfuQJ4jq4z-qmqOQZ0DjKKw8wn5qnnFA/embed?start=false&loop=false&delayms=3000" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div></p>
<p>Đối với những người mới sử dụng thì hẳn là chưa thể nhớ hết được những cú pháp của markdown, nhưng bạn hãy yên tâm vì bạn luôn có thể xem chỉ dẫn cú pháp markdown bằng cách click vào biểu tưởng dấu hỏi được đính ở phía trên của editor.</p>
<h2>Công thức toán học</h2>
<p>Bên cạnh các cú pháp Markdown phổ biến, Viblo còn hỗ trợ viết các công thức toán học theo cú pháp của <span class="katex"><span class="katex-mathml"><math><semantics><mrow><mi>T</mi><mi>e</mi><mi>X</mi></mrow><annotation encoding="application/x-tex"> TeX </annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.68333em;vertical-align:0em;"></span><span class="mord mathit" style="margin-right:0.13889em;">T</span><span class="mord mathit">e</span><span class="mord mathit" style="margin-right:0.07847em;">X</span></span></span></span>.</p>
<h1>Kết</h1>
<p>Hy vọng thông qua bài hướng dẫn này bạn sẽ có được những bài viết không chỉ có chất lượng cao về nội dung mà còn có trình bày đẹp mắt và ấn tượng nữa nhé!</p>