<h2 class="bolder">API Reference</h2>

<h3>Overview</h3>

<p>This open source python API detects human faces in photos and images and returns information on facial features as coordinates on the image it finds.</p>

<h3>Requests</h3>

<p>Requests return a JSON object with the header:</p>

<pre>
<code class=" hljs http">
<span class="hljs-attribute">Content-Type</span>: <span class="hljs-string">application/json</span>
</code>
</pre>

<h3>Usage</h3>

<h3 id="post-detect" class="font-weight-bold">POST /detect</h3>

<div class="p-3"></div>

<p>To detect faces, submit a JPG or PNG photo.  You can submit the photo either as a publicly accessible URL or Base64 encoded..</p>

<p>One additional thing to note is that the returned coordinates all begin at the top left of the photo.</p>

<h5>Required Parameters</h5>

<p><code><span>image </span></code>Publicly accessible URL or Base64 encoded photo.<br></p>

<!--h5 class="font-weight-bold pt-5 mb-0 pb-3">Optional Parameters</h5-->

<h6 class="font-weight-bold default-spacing text-uppercase">Example request</h6>

<pre class="snippet"><code class=" hljs http"><span class="hljs-request">POST <span class="hljs-string">/detect</span> HTTP/1.1</span>

<span class="hljs-attribute">Content-Type</span>: <span class="hljs-string">application/json</span>
{
    "<span>image</span>":<span><span>" </span></span><a href="https://www.randomlists.com/img/people/rachel_zoe.webp"><span><span>https://www.randomlists.com/img/people/rachel_zoe.webp</span></span></a><span><span>"</span></span>
}</code></pre>

<div class="p-3"></div>

<h6 class="font-weight-bold default-spacing text-uppercase">Examle response</h6>

<pre class="snippet"><code class=" hljs scss">200
<span class="hljs-attribute">Content</span>-Type<span class="hljs-value">: application/json</span></code><code style="border-top:1px solid #3a3e4d;" class=" hljs vbscript">{
    <span class="hljs-string">"images"</span>: [
        {
            <span class="hljs-string">"status"</span>: <span class="hljs-string">"Complete"</span>,
            <span class="hljs-string">"width"</span>: <span class="hljs-number">1536</span>,
            <span class="hljs-string">"height"</span>: <span class="hljs-number">2048</span>,
            <span class="hljs-string">"file"</span>: <span class="hljs-string">"rachel_zoe.webp"</span>,
            <span class="hljs-string">"faces"</span>: [
                {
                    <span class="hljs-string">"topLeftX"</span>: <span class="hljs-number">390</span>,
                    <span class="hljs-string">"topLeftY"</span>: <span class="hljs-number">706</span>,
                    <span class="hljs-string">"chinTipX"</span>: <span class="hljs-number">780</span>,
                    <span class="hljs-string">"rightEyeCenterX"</span>: <span class="hljs-number">587</span>,
                    <span class="hljs-string">"yaw"</span>: -<span class="hljs-number">3</span>,
                    <span class="hljs-string">"chinTipY"</span>: <span class="hljs-number">1548</span>,
                    <span class="hljs-string">"confidence"</span>: <span class="hljs-number">0.99997</span>,
                    <span class="hljs-string">"height"</span>: <span class="hljs-number">780</span>,
                    <span class="hljs-string">"rightEyeCenterY"</span>: <span class="hljs-number">904</span>,
                    <span class="hljs-string">"width"</span>: <span class="hljs-number">781</span>,
                    <span class="hljs-string">"leftEyeCenterY"</span>: <span class="hljs-number">907</span>,
                    <span class="hljs-string">"leftEyeCenterX"</span>: <span class="hljs-number">955</span>,
                    <span class="hljs-string">"pitch"</span>: -<span class="hljs-number">17</span>,
                    <span class="hljs-string">"attributes"</span>: {
                        <span class="hljs-string">"lips"</span>: <span class="hljs-string">"Together"</span>,
                        <span class="hljs-string">"asian"</span>: <span class="hljs-number">0.25658</span>,
                        <span class="hljs-string">"gender"</span>: {
                            <span class="hljs-string">"type"</span>: <span class="hljs-string">"F"</span>
                        },
                        <span class="hljs-string">"age"</span>: <span class="hljs-number">26</span>,
                        <span class="hljs-string">"hispanic"</span>: <span class="hljs-number">0.41825</span>,
                        <span class="hljs-string">"other"</span>: <span class="hljs-number">0.11144</span>,
                        <span class="hljs-string">"black"</span>: <span class="hljs-number">0.16007</span>,
                        <span class="hljs-string">"white"</span>: <span class="hljs-number">0.05365</span>,
                        <span class="hljs-string">"glasses"</span>: <span class="hljs-string">"None"</span>
                    },
                    <span class="hljs-string">"face_id"</span>: <span class="hljs-number">1</span>,
                    <span class="hljs-string">"quality"</span>: <span class="hljs-number">0.79333</span>,
                    <span class="hljs-string">"roll"</span>: -<span class="hljs-number">1</span>
                }
            ]
        }
    ]
}
+ <span class="hljs-built_in">Response</span> <span class="hljs-number">200</span> (application/json)
    + Body
{
    <span class="hljs-string">"Errors"</span>: [
    {
        <span class="hljs-string">"Message"</span>: <span class="hljs-string">"no faces found in the image"</span>,
        <span class="hljs-string">"ErrCode"</span>: <span class="hljs-number">5002</span>
    }]
}</code></pre>
