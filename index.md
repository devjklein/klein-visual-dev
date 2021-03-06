---
title: Homepage
layout: default
current: index
---

<main class="content  white" id="main">
  <!-- Home background & introduction -->
  <section aria-label="Homepage introduction" class="row  splash  overflow  green">
    <div class="row">
      <div class="splash__intro">
      
          <div class="splash__type">
            <h1 class="splash__type--header  light">Hello!</h1>
            <p class="splash__type--content">My name is David Klein, and I am a multidisciplinary designer who specializes in branding and web development. My goal is to provide my clients with exceptional designs that excite the creative senses and instill total brand confidence.</p>
            <p class="splash__type--content"><strong>We can create something exceptional together.</strong></p>
            <a aria-label="Email Klein Visual" class="btn button" href="mailto:kleinvisual@outlook.com">Let's Talk</a>
          </div>
          
          <div class="splash__avatar">
            {% include image.html url="img/portraits/me" alt="Portrait of David Klein wearing a blue plaid button down shirt." %}
          </div>
      </div>
      
      
      <!-- Parallax Background -->
      <div class="mtn-scene  js-mtn-scene" data-hover-only="false" relative-input="true" data-scalar-x="10" data-scalar-y="25">
      
        <div data-depth="0.05" class="mtn-scene__layer" id="js-mtn-clouds-sm"></div>
        
        <div data-depth="0.1" class="mtn-scene__layer mtn-center">
          <img src="{{ "/img/mtn-scene/mountains.svg" | relative_url }}" alt="An ilustrated mountain, tinted green, rises in the distance as clouds float by.">
        </div>
        
        <div data-depth="0.15" class="mtn-scene__layer" id="js-mtn-clouds-md"></div>
        
        <div data-depth="0.2" class="mtn-scene__layer" id="js-mtn-clouds-lg"></div>
        
      </div>
      
      <div class="mtn-scene--fallback">
      </div>
    </div>
  </section>
  
  <section aria-label="" class="row">
    <div class="mtn-scene__controls">
      <!--<button aria-label="Reverse background animation and run parallax" class="js-mtn-scene__button  mtn-scene__button  mtn-scene__reverse  js-mtn-scene__reverse">Reverse</button>-->
      <span class="mtn-scene__label">Background<br>animation:&nbsp;&nbsp;</span>
      <button aria-label="Run background animation and parallax" class="js-mtn-scene__button  btn-small  mtn-scene__play  js-mtn-scene__play  active">Play</button>
      <button aria-label="Stop background animation and parallax" class="js-mtn-scene__button  btn-small  mtn-scene__stop  js-mtn-scene__stop">Stop</button>
    </div>
  </section>
  
  
  
  
  <section class="row  white  full" aria-label="Design Samples">
    
      <h2>Featured Projects</h2>
      {% for num in (1..3) %}
        {% for project in site.design %}
          {% if project.featured == num %}
            <div class="col-4">
              <a aria-label="Link to {{project.title | strip_html }} project" href="{{ site.baseurl }}{{ project.url }}" class="hover-panel">
                {% capture image %}{{ project.image }}{% endcapture %}
                {% capture alt %}{{ project.alt }}{% endcapture %}
                {% include image.html url=image alt=alt %}
                <div class="hover-panel__overlay  green"><h3 class="light">{{ project.title }}</h3></div>
              </a>
            </div>
          {% endif %}
        {% endfor %}
      {% endfor %}
      
      <div class="col-12">
        <a aria-label="Explore more projects" class="btn  btn--center  btn--large" href="{{ "/portfolio/design" | relative_url }}">See More</a>
      </div>
      
  </section>
  
  
  
  
  <section class="row  white" aria-label="Capabilities">
    <h2>My Capabilities</h2>
    <div class="skill-panel">
      <div class="col-4  skill-panel__image">
        <a aria-label="Visit design portfolio" href="{{ "/portfolio/design" | relative_url }}" class="hover-panel  white">
          {% include image.html url="/img/llamas/llama-branding" alt="An illustrated cartoon llama stands in front of an easel displaying a color wheel." type="png" %}
        </a>
      </div>
      <div class="col-8  skill-panel__body">
        <h3 class="skill-panel__header">Branding</h3>
        <p class="skill-panel__copy">My passion is breathing life into an idea. In the case of branding, that idea is everything you need to take your business to the next level. I take pride in designing exceptional brands that give you and your customers total confidence in your company.</p>
      </div>
    </div>
    
    
    
    
    <div class="skill-panel">
      <div class="col-8  skill-panel__body">
        <h3 class="skill-panel__header">Web Design</h3>
        <p class="skill-panel__copy">Fast. Responsive. Accessible. Search engine optimized. As a web designer, I obsess over these details because I understand the tight correlation between site performance and conversion rates, where even fractions of a millisecond make all the difference.</p>
      </div>
      <div class="col-4  skill-panel__image">
        <a aria-label="Visit design portfolio" href="{{ "/portfolio/design" | relative_url }}" class="hover-panel  white">
          {% include image.html url="/img/llamas/llama-web" alt="An illustrated cartoon llama stands in front of a computer screen with a generic website shown." type="png" %}
        </a> 
      </div>
    </div>
    
    
    <div class="skill-panel">
      <div class="col-4  skill-panel__image">
        <a aria-label="Visit photography portfolio" href="{{ "/portfolio/photography" | relative_url }}" class="hover-panel  white">
        {% include image.html url="/img/llamas/llama-photo" alt="An illustrated cartoon llama with a camera on a tripod." type="png" %}
      </a>
      </div>
      <div class="col-8  skill-panel__body">
        <h3 class="skill-panel__header">Photography</h3>
        <p class="skill-panel__copy">Need that perfect corporate headshot? Or maybe you're interested in a family photo shoot? How about real estate photos that make your home shine? I love spending time behind the lens, and I specialize in leveraging technical skill alongside artistic creativity to capture winning images that you will love.</p>
      </div>
    </div>
    
    <div class="skill-panel">
      <div class="col-8  skill-panel__body">
        <h3 class="skill-panel__header">Motion Graphics</h3>
        <p class="skill-panel__copy">Ready to take your multimedia to the next level? There's nothing like seeing your ideas or products in motion, and I can help with that! My motion graphics capabilities include filming, editing, CGI, and every step in between.</p>
      </div>
      <div class="col-4  skill-panel__image">
        <a aria-label="Visit design portfolio" href="{{ "/portfolio/design" | relative_url }}" class="hover-panel  white">
          {% include image.html url="/img/llamas/llama-fancy" alt="An illustrated cartoon llama with an old film camera on a tripod." type="png" %}
      </a>
      </div>
    </div>
  </section>
  
  
  
  
  
</main>
