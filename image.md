---
layout: page
title: Image
subtitle: Image recognition
published: true
css: image.css
---


<html>
<body>


<input type="url" id="myURL" value="http://cdn2-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-8.jpg">


<button onclick="myFunction()">Classify</button>
<pre id="json"></pre>

<script src="//algorithmia.com/v1/clients/js/algorithmia-0.2.0.js" type="text/javascript"></script>
<script>
function myFunction() {
    var x = document.getElementById("myURL").value;
    Algorithmia.client("simBrvTtxJZg/c/TZCBlTVKAm4p1")
           .algo("algo://deeplearning/InceptionNet/1.0.2")
           .pipe(x)
           .then(function(output) {
             console.log(output.result.tags);
             var str = JSON.stringify(output.result.tags, null, 2); // spacing level = 2
             document.getElementById("json").innerHTML =str;
             
             <div class="skills">
              <ul class="lines">
                <li class="line l--0">
                  <span class="line__label title">
                    Confidence:
                  </span>
                </li>
                <li class="line l--25">
                  <span class="line__label">
                    Not sure
                  </span>
                </li>
                <li class="line l--50">
                  <span class="line__label">
                    Sure Sure
                  </span>
                </li>
                <li class="line l--75">
                  <span class="line__label">
                    Pretty Sure
                  </span>
                </li>
                <li class="line l--100">
                  <span class="line__label">
                    Damn Sure
                  </span>
                </li>
              </ul>

              <div class="charts">
                <div class="chart chart--dev">
                  <span class="chart__title">Image Recognition</span>
                  <ul class="chart--horiz">
                    <li class="chart__bar" data-skill="95">
                      <span class="chart__label">
                        HTML(5)
                      </span>
                    </li>
                    <li class="chart__bar" data-skill="95">
                      <span class="chart__label">
                        CSS(3) & SCSS
                      </span>
                    </li>
                    <li class="chart__bar" data-skill="70">
                      <span class="chart__label">
                        JavaScript
                      </span>
                    </li>
                    <li class="chart__bar" data-skill="65">
                      <span class="chart__label">
                        AngularJS
                      </span>
                    </li>
                    <li class="chart__bar" data-skill="60">
                      <span class="chart__label">
                        jQuery
                      </span>
                    </li>

                    <li class="chart__bar" data-skill="60">
                      <span class="chart__label">
                        Umbraco
                      </span>
                    </li>
                  </ul>
                </div>

           	});
          
}

</script>

</body>
</html>