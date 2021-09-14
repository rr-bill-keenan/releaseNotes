---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Release Notes Home
---
<h1>Quick Links</h1>

<p>This will send an update message to the release notice slack channel<p>
<a href="https://forms.office.com/Pages/ResponsePage.aspx?id=2bCoUwDZzEidflk13I1bFzsOSeWBs-lHk1DsA7zYn_VUNVY3Vlg5STFSUzJZSTJRWTRSSjY5R0RETS4u" target="_new">Heads Up Form</a>


<p>Have a Production Release?<p>
<a href="https://forms.office.com/Pages/ResponsePage.aspx?id=2bCoUwDZzEidflk13I1bFzsOSeWBs-lHk1DsA7zYn_VUOUVQOUk2V1FYTTlBUjcyMkJPTTJFVUpCVi4u" target="_new">Production Release</a>



<p>Launching an Experiment?<p>
<a href="https://forms.office.com/Pages/ResponsePage.aspx?id=2bCoUwDZzEidflk13I1bFzsOSeWBs-lHk1DsA7zYn_VUN0w2MFhCOERDQVhHOEtNQ1pQREdGOTRaSS4u" target="_new">New Experiment</a>


<p>Updating an Experiment?<p>
<a href="https://forms.office.com/Pages/ResponsePage.aspx?id=2bCoUwDZzEidflk13I1bFzsOSeWBs-lHk1DsA7zYn_VUQ0hYMEVBNU1GVDY4UExZM0lKSFBFVFY1VS4u" target="_new">Experiment Update</a>

  {% if site.paginate %}
    {% assign posts = paginator.posts %}
  {% else %}
    {% assign posts = site.posts %}
  {% endif %}


<h2>Release Dates</h2>


  {%- if posts.size > 0 -%}
    {%- if page.list_title -%}
      <h2 class="post-list-heading">{{ page.list_title }} </h2>
    {%- endif -%}
    <ul class="post-list">
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      {%- for post in posts -%}
      <li>
        <span class="post-meta"><a class="alt" href="{{ post.url | relative_url }}">{{ post.title  | escape }}</a></span>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

    {% if site.paginate %}
      <div class="pager">
        <ul class="pagination">
        {%- if paginator.previous_page %}
          <li><a href="{{ paginator.previous_page_path | relative_url }}" class="previous-page">{{ paginator.previous_page }}</a></li>
        {%- else %}
          <li><div class="pager-edge">•</div></li>
        {%- endif %}
          <li><div class="current-page">{{ paginator.page }}</div></li>
        {%- if paginator.next_page %}
          <li><a href="{{ paginator.next_page_path | relative_url }}" class="next-page">{{ paginator.next_page }}</a></li>
        {%- else %}
          <li><div class="pager-edge">•</div></li>
        {%- endif %}
        </ul>
      </div>
    {%- endif %}

  {%- endif -%}