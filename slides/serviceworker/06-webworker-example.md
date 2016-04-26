<!-- .slide: data-background="#fff"-->

<pre class="language-js" >
<code>
/*  *** MAIN *** */
    var worker = new Worker('path/to/worker.js');
    worker.addEventListener('message', event => {
        const message = event.data;
        // Handle message
    });
    worker.postMessage({action: 'do-this', data: actionData});
</code>
</pre>

<pre class="language-js" >
<code>
/*  *** WORKER *** */
    self.addEventListener('message', message => {
        const {action, data} = message;
        // Heavy computing
        self.postMessage({action: 'your-response', data: computedData});
    });
</code>
</pre>