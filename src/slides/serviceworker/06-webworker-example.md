<!-- .slide: data-background="#fff"-->

<pre class="language-js fragment current-visible code-with-highlight" data-fragment-index="0">
<code>
/*  *** MAIN *** */
    var worker = new Worker('path/to/worker.js');
    worker.addEventListener('message', event => {
        const message = event.data;
        // Handle message
    });
    worker.postMessage({action: 'do-this', data: actionData});


/*  *** WORKER *** */
    self.addEventListener('message', message => {
        const {action, data} = message;
        // Heavy computing
        self.postMessage({action: 'your-response', data: computedData});
    });
</code>
</pre>

<pre class="language-js fragment current-visible code-with-highlight" data-line="9, 14" data-fragment-index ="1">
<code>
/*  *** MAIN *** */
    var worker = new Worker('path/to/worker.js');
    worker.addEventListener('message', event => {
        const message = event.data;
        // Handle message
    });
    worker.postMessage({action: 'do-this', data: actionData});


/*  *** WORKER *** */
    self.addEventListener('message', message => {
        const {action, data} = message;
        // Heavy computing
        self.postMessage({action: 'your-response', data: computedData});
    });
</code>
</pre>


<pre class="language-js fragment current-visible code-with-highlight" data-line="6, 16" data-fragment-index ="2">
<code>
/*  *** MAIN *** */
    var worker = new Worker('path/to/worker.js');
    worker.addEventListener('message', event => {
        const message = event.data;
        // Handle message
    });
    worker.postMessage({action: 'do-this', data: actionData});


/*  *** WORKER *** */
    self.addEventListener('message', message => {
        const {action, data} = message;
        // Heavy computing
        self.postMessage({action: 'your-response', data: computedData});
    });
</code>
</pre>