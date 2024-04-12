---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: splash
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/bkg.jpg
  actions:
    - label: "Join!"
      url: "/join/"
  caption: "Photo by **[Ekansh Saxena](https://unsplash.com/@ekansh005)** on **[Unsplash](https://unsplash.com/photos/white-airplane-on-sky-51djUJsmpPc)**"

excerpt: >-
  **If you've ever wondered what it's like to be a hawk, eagle, or falcon, soaring is the sport for you!** Just because you
  don't have power doesn't mean you just glide to the ground; Soaring flights have gone as high as 76,124 ft (23,203 m,
  Perlan Project). With the mountains nearby in Vancouver, we have access to some of the most unique soaring terrain in
  the world.
---

# Posts

<ul class="taxonomy__index">
  {% assign postsInYear = site.posts | where_exp: "item", "item.hidden != true" | group_by_exp: 'post', 'post.date | date: "%Y"' %}
  {% for year in postsInYear %}
    <li>
      <a href="#{{ year.name }}">
        <strong>{{ year.name }}</strong> <span class="taxonomy__count">{{ year.items | size }}</span>
      </a>
    </li>
  {% endfor %}
</ul>

{% assign entries_layout = page.entries_layout | default: 'list' %}
{% assign postsByYear = site.posts | where_exp: "item", "item.hidden != true" | group_by_exp: 'post', 'post.date | date: "%Y"' %}
{% for year in postsByYear %}
  <section id="{{ year.name }}" class="taxonomy__section">
    <h2 class="archive__subtitle">{{ year.name }}</h2>
    <div class="entries-{{ entries_layout }}">
      {% for post in year.items %}
        {% include archive-single.html type=entries_layout %}
      {% endfor %}
    </div>
    <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }} &uarr;</a>
  </section>
{% endfor %}
