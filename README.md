<h2 class="bolder">API Reference</h2>

<h3>Overview</h3>

<p>This is an open source REST API written in Python and Flask. <br />
    It can detect human faces in photos and images. <br /> 
    If it finds face(s) on image then it returns information with facial features as coordinates.
</p>

<h3>Usage</h3>

<h4>Requests</h4>

<p>All requests return a JSON object with the header:</p>

<pre>
<code>
<span>Content-Type</span>: <span>application/json</span>
</code>
</pre>

<h4>POST /detect</h4>

<div></div>

<p>To detect faces, submit a JPG or PNG photo. <br />
    You can submit the photo either as a publicly accessible URL or Base64 encoded. <br />
    Returned coordinates all begin at the top left of the photo
</p>

<h5>Required Parameters</h5>

<p><code><span>image </span></code>Publicly accessible URL or Base64 encoded photo.<br></p>

<!--h5 class="font-weight-bold pt-5 mb-0 pb-3">Optional Parameters</h5-->

<h6 class="font-weight-bold default-spacing text-uppercase">Example request</h6>

<pre class="snippet"><code class=" hljs http"><span class="hljs-request">POST <span class="hljs-string">/detect</span> HTTP/1.1</span>

<span class="hljs-attribute">Content-Type</span>: <span class="hljs-string">application/json</span>
{
    "<span>image</span>":<span><span>" </span></span><a href="https://randomuser.me/api/portraits/women/75.jpg"><span><span>https://randomuser.me/api/portraits/women/75.jpg</span></span></a><span><span>"</span></span>
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
            <span class="hljs-string">"file"</span>: <span class="hljs-string">"75.jpg"</span>,
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
</code></pre>
