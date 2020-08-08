# qauland.github.io

Based on [Mundana Jekyll Theme by WowThemes.net](https://bootstrapstarter.com/bootstrap-templates/mundana-theme-jekyll/).

Archived for reference purposes.

### Deleted codes

```html
<!-- Begin post excerpts, let's highlight the first 4 posts on top -->
<div class="row remove-site-content-margin">
    
    <!-- latest post -->
    {% assign latest_post = site.posts[0] %}
    <div class="col-md-6">
    <div class="card border-0 mb-4 box-shadow">   
    <a href="{{site.baseurl}}{{latest_post.url}}">
    <div class="topfirstimage" style="background-image: url({% if latest_post.image contains "://" %}{{ latest_post.image }}{% else %} {{site.baseurl}}/{{ latest_post.image}}{% endif %}); height: 200px;    background-size: cover;    background-repeat: no-repeat;"></div>     
    </a>
    <div class="card-body px-0 pb-0 d-flex flex-column align-items-start">
    <h2 class="h4 font-weight-bold">
    <a class="text-dark" href="{{site.baseurl}}{{latest_post.url}}">{{ latest_post.title }}</a>
    </h2>
    <p class="excerpt">
        {{ latest_post.excerpt | strip_html | strip_newlines | truncate: 136 }}
    </p>
    <div>
        <small class="d-block text-muted">
            In <span class="catlist">
                {% for category in latest_post.categories %}
                <a class="text-capitalize text-muted smoothscroll" href="{{site.baseurl}}/categories.html#{{ category | downcase }}">{{ category }}</a><span class="sep">, </span>
                {% endfor %}
                </span>                   
        </small>
        <small class="text-muted">
            {{ latest_post.date | date: '%b %d, %Y' }}
        </small>
    </div>
    </div>
    </div>
    </div>
    
    <div class="col-md-6">
        
        <!-- second latest post -->
        {%- assign second_post = site.posts[1] -%}        
        <div class="mb-3 d-flex align-items-center">                
                {% if second_post.image %}
                <div class="col-md-4">
                <a href="{{site.baseurl}}{{second_post.url}}">
                 <img class="w-100" src="{% if second_post.image contains "://" %}{{ second_post.image }}{% else %}{{ second_post.image | absolute_url }}{% endif %}" alt="{{ second_post.title }}">
                </a>
                </div>
                {% endif %}                
                <div>
                    <h2 class="mb-2 h6 font-weight-bold">
                    <a class="text-dark" href="{{site.baseurl}}{{second_post.url}}">{{ second_post.title }}</a>
                    </h2>
                    <small class="d-block text-muted">
                        In <span class="catlist">
                        {% for category in second_post.categories %}
                        <a class="text-capitalize text-muted smoothscroll" href="{{site.baseurl}}/categories.html#{{ category | downcase }}">{{ category }}</a><span class="sep">, </span>
                        {% endfor %}
                        </span>                   
                    </small>
                    <small class="text-muted">
                        {{ second_post.date | date: '%b %d, %Y' }}
                    </small>
                </div>
            </div>
        
        <!-- third latest post -->
        {%- assign third_post = site.posts[2] -%}        
        <div class="mb-3 d-flex align-items-center">                
                {% if third_post.image %}
                <div class="col-md-4">
                <a href="{{site.baseurl}}{{third_post.url}}">
                 <img class="w-100" src="{% if third_post.image contains "://" %}{{ third_post.image }}{% else %}{{site.baseurl}}/{{ third_post.image }}{% endif %}" alt="{{ third_post.title }}">
                </a>
                </div>
                {% endif %}                
                <div>
                    <h2 class="mb-2 h6 font-weight-bold">
                    <a class="text-dark" href="{{site.baseurl}}{{third_post.url}}">{{ third_post.title }}</a>
                    </h2>
                    <small class="d-block text-muted">
                        In <span class="catlist">
                        {% for category in third_post.categories %}
                        <a class="text-capitalize text-muted smoothscroll" href="{{site.baseurl}}/categories.html#{{ category | downcase }}">{{ category }}</a><span class="sep">, </span>
                        {% endfor %}
                        </span>                   
                    </small>
                    <small class="text-muted">
                        {{ third_post.date | date: '%b %d, %Y' }}
                    </small>
                </div>
            </div>
        
        <!-- fourth latest post -->
        {%- assign fourth_post = site.posts[3] -%}        
        <div class="mb-3 d-flex align-items-center">                
                {% if fourth_post.image %}
                <div class="col-md-4">
                <a href="{{site.baseurl}}{{fourth_post.url}}">
                <img class="w-100" src="{% if fourth_post.image contains "://" %}{{ fourth_post.image }}{% else %}{{site.baseurl}}/{{ fourth_post.image }}{% endif %}" alt="{{ fourth_post.title }}">
                </a>
                </div>
                {% endif %}                
                <div>
                    <h2 class="mb-2 h6 font-weight-bold">
                    <a class="text-dark" href="{{site.baseurl}}{{fourth_post.url}}">{{ fourth_post.title }}</a>
                    </h2>
                    <small class="d-block text-muted">
                        In <span class="catlist">
                        {% for category in fourth_post.categories %}
                        <a class="text-capitalize text-muted smoothscroll" href="{{site.baseurl}}/categories.html#{{ category | downcase }}">{{ category }}</a><span class="sep">, </span>
                        {% endfor %}
                        </span>                   
                    </small>
                    <small class="text-muted">
                        {{ fourth_post.date | date: '%b %d, %Y' }}
                    </small>
                </div>
            </div>
        
    </div>
    
</div>
```
