![A professional photo of me](/assets/habibi.JPG)


<ul>
    {% for post in site.posts %}
    <li>
    <a href="/blog{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>