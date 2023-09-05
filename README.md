<h2 id="arm-global-web-components-topnav-subnav">Arm Global Web Components - TopNav / SubNav</h2>
<p><br /></p>
<h3 id="how-to-use">How To Use</h3>
<pre><code><span class="hljs-section">&lt;arm-top-navigation&gt;</span> <span class="hljs-section">&lt;/arm-top-navigation&gt;</span>
</code></pre><p><br>
<br></p>
<h3 id="component-attribute">Component Attribute</h3>
<p><strong>observeId</strong> - Scroll page, observe id and show solid background</p>
<pre><code>&lt;<span class="hljs-meta">arm</span>-top-navigation observeId=<span class="hljs-string">"#id"</span>&gt; &lt;/<span class="hljs-meta">arm</span>-top-navigation&gt;
</code></pre><p><strong>subnav</strong> - load top-sub navigation css</p>
<pre><code>&lt;<span class="hljs-meta">arm</span>-top-navigation <span class="hljs-keyword">subnav&gt; </span>&lt;/<span class="hljs-meta">arm</span>-top-navigation&gt;
</code></pre><p><strong>disabled-subnav</strong> - remove top sub navigation</p>
<pre><code>&lt;<span class="hljs-meta">arm</span>-top-navigation disabled-<span class="hljs-keyword">subnav&gt; </span>&lt;/<span class="hljs-meta">arm</span>-top-navigation&gt;
</code></pre><p><strong>disabled-subnav-animation</strong> - disable sub nav animation</p>
<pre><code>&lt;<span class="hljs-meta">arm</span>-top-navigation disabled-<span class="hljs-keyword">subnav-animation&gt; </span>&lt;/<span class="hljs-meta">arm</span>-top-navigation&gt;
</code></pre><p><strong>hide-top-navigation</strong> - hide top navigation</p>
<pre><code>&lt;arm-<span class="hljs-literal">top</span>-navigation observeId=<span class="hljs-string">"#ancher"</span> subnav <span class="hljs-literal">hide</span>-<span class="hljs-literal">top</span>-navigation&gt;
</code></pre><p><strong>custom-subnav</strong> - Use custom desgin sub nav</p>
<pre><code><span class="hljs-tag">&lt;<span class="hljs-name">arm-top-navigation</span> <span class="hljs-attr">subnav</span> <span class="hljs-attr">custom-subnav</span>&gt;</span>
    <span class="hljs-tag">&lt;<span class="hljs-name">span</span> <span class="hljs-attr">slot</span>=<span class="hljs-string">"c-subnav"</span>&gt;</span>
    <span class="hljs-tag">&lt;<span class="hljs-name">style</span>&gt;</span><span class="css">
        <span class="hljs-selector-class">.custom-subnav-element</span> { <span class="hljs-attribute">color</span>: green; <span class="hljs-attribute">cursor</span>: pointer; <span class="hljs-attribute">padding</span>: <span class="hljs-number">0</span> <span class="hljs-number">12px</span>; }
    </span><span class="hljs-tag">&lt;/<span class="hljs-name">style</span>&gt;</span>
    <span class="hljs-tag">&lt;<span class="hljs-name">div</span> <span class="hljs-attr">class</span>=<span class="hljs-string">"custom-subnav-element"</span>&gt;</span> green <span class="hljs-tag">&lt;/<span class="hljs-name">div</span>&gt;</span>
    <span class="hljs-tag">&lt;<span class="hljs-name">script</span>&gt;</span><span class="javascript">
        <span class="hljs-keyword">var</span> div = <span class="hljs-built_in">document</span>.querySelector(<span class="hljs-string">'.custom-subnav-element'</span>);
        div.addEventListener(<span class="hljs-string">'click'</span>, <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params"></span>)</span>{ <span class="hljs-built_in">console</span>.log(<span class="hljs-string">'custom-subnav-element'</span>)})
    </span><span class="hljs-tag">&lt;/<span class="hljs-name">script</span>&gt;</span>
    <span class="hljs-tag">&lt;/<span class="hljs-name">div</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">arm-top-navigation</span>&gt;</span>
</code></pre><h3 id="component-arguments">Component arguments</h3>
<pre><code><span class="hljs-variable">&lt;arm-top-navigation arguments&gt;</span>


|<span class="hljs-string">arguments type                         </span>|<span class="hljs-string">Description                    </span>|
|<span class="hljs-string">---------------------------------------</span>|<span class="hljs-string">-------------------------------</span>|
|<span class="hljs-string">subnav                                 </span>|<span class="hljs-string">Show subnav                    </span>|
|<span class="hljs-string">hide-top-navigation                    </span>|<span class="hljs-string">hide top navigation            </span>|
|<span class="hljs-string">ui-route-disabled                      </span>|<span class="hljs-string">disable UI route eventlistender</span>|
</code></pre><h3 id="component-api">Component API</h3>
<pre><code>var element = document.querySelector('arm-top-navigation');


|<span class="hljs-string">API Name                               </span>|<span class="hljs-string">Description                    </span>|
|<span class="hljs-string">---------------------------------------</span>|<span class="hljs-string">-------------------------------</span>|
|<span class="hljs-string">element.showTopNavigation();           </span>|<span class="hljs-string">Show top navigation            </span>|
|<span class="hljs-string">element.showTopMainNav();              </span>|<span class="hljs-string">Show top main nav              </span>|
|<span class="hljs-string">element.showTopSubNav();               </span>|<span class="hljs-string">Show top sub nav               </span>|
|<span class="hljs-string">element.showTopSubNavWithAnimation();  </span>|<span class="hljs-string">Show top sub nav with animation</span>|
|<span class="hljs-string">element.hideTopNavigation();           </span>|<span class="hljs-string">hide top navigation            </span>|<span class="hljs-string">    
</span>|<span class="hljs-string">element.hideTopMainNav();              </span>|<span class="hljs-string">hide top main nav              </span>|
|<span class="hljs-string">element.hideTopSubNav();               </span>|<span class="hljs-string">hide top sub nav               </span>|
|<span class="hljs-string">element.enableAnimation();             </span>|<span class="hljs-string">enable animation               </span>|
|<span class="hljs-string">element.disabledAnimation();           </span>|<span class="hljs-string">disable animation              </span>|
|<span class="hljs-string">element.setSubNavActiveState(index)    </span>|<span class="hljs-string">setSubNavActiveState           </span>|
|<span class="hljs-string">element.cleanSubNavActiveState()       </span>|<span class="hljs-string">cleanSubNavActiveState         </span>|
</code></pre><h3 id="eventlistener">EventListener</h3>
<pre><code>    <span class="hljs-built_in">document</span>.addEventListener(<span class="hljs-string">"arm-top-sub-nav-search"</span>, <span class="hljs-function"><span class="hljs-keyword">function</span> (<span class="hljs-params">e</span>) </span>{
        <span class="hljs-built_in">console</span>.log(e.detail);
        <span class="hljs-built_in">var</span> <span class="hljs-built_in">url</span> = <span class="hljs-string">"https://www.arm.com/search#q="</span>;
        <span class="hljs-built_in">var</span> url2 = <span class="hljs-string">"https://developer.arm.com/search#q="</span>;
        <span class="hljs-built_in">var</span> url3 = <span class="hljs-string">"https://www.google.com/search?q="</span>;
        <span class="hljs-comment">// location.href = url3 + e.detail;</span>
    });

    <span class="hljs-built_in">document</span>.addEventListener(<span class="hljs-string">"arm-top-sub-link"</span>, <span class="hljs-function"><span class="hljs-keyword">function</span>(<span class="hljs-params">e</span>) </span>{
        <span class="hljs-built_in">console</span>.log(e);
    });

|EventListener Name                     |Description                    |
|---------------------------------------|-------------------------------|
|arm-top-sub-nav-search                 |top sub nav search callback    |
|arm-top-sub-link                       |sub nav link callback          |
</code></pre>