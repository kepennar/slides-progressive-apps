<!-- .slide: data-background="url(images/slides/serviceworker/serviceworker_l.svg) white no-repeat center" data-background-size="contain"-->

<pre class="language-js" >
<code>
this.addEventListener('fetch', event => {
  event.respondWith(getResponse);
});

function getResponse() {
    caches.match(event.request)
    .then(function(response) {
        caches.open('v1')
        .then(cache => {
            cache.put(event.request, response);
        });
        return response.clone();
    })
    .catch(() => {
        return fetch(event.request);
    })
}
</code>
</pre>