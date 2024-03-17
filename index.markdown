---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: index
---

{% include head.html %}

<body>
{% include navbar.html %}

<main>
  
  <!-- Latest post is the main article -->
  {% assign post = site.posts.first %}
  {% include articol_principal.html %}

  <!-- Marketing messaging and featurettes
  ================================================== -->
  <!-- Wrap the rest of the page in another container to center all the content. -->

<div class="container marketing">

<!-- Layout: 
    1. lead article
    2. 3 articles in a line
    3. one article per line
-->
{% assign posts = site.posts %}
{% for post in posts %}
    {% if forloop.index == 1 %}
        <!-- Start a row -->
        <div class="row">
    {% endif %}
    {% if forloop.index > 1 %}
        {% include articol_text_jos.html %}
    {% else %}
        </div><!-- /.row -->    
        {% include articol_text_sus.html %}
    {% endif %}
{% endfor %}


</div><!-- /.container -->

  {% include footer.html %}

</main>

</body>