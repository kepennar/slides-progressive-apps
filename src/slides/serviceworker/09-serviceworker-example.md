<!-- .slide: data-background="url(images/slides/serviceworker/serviceworker_l.svg) white no-repeat center" data-background-size="contain"-->

<pre class="language-js" >
<code>
this.addEventListener('install', event => {
  event.waitUntil(
    caches.open('v1')
    .then(cache => {
      return cache.addAll([
        '/index.html',
        '/index.js',
        // ...
      ]);
    })
  );
});
</code>
</pre>