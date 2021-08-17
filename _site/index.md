## Welcome to The Unvarnished Geek!


![Sometimes simpler is better](/assets/terminal.png)

This will be a blog for those of us who want to use digital tools to create and communicate meaningful things *without* the noise and clutter of most modern computing, and to keep the process elegant and streamlined from our initial thoughts to worldwide deployment.

## Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

