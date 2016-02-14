---
layout: page
title: About
class: 'post'
navigation: True
logo: 'https://lh3.googleusercontent.com/-BM_iWOmV5V4/AAAAAAAAAAI/AAAAAAAAAVI/w5rfSEMC-D4/s149-p-rw-no/photo.jpg'
current: about
---

This is a demo blog for Ghost, it contains dummy content which allows you to click around and see what a Ghost blog running the default theme looks like.

We use this for testing and for reference!

If you'd like to set up your own blog, head on over to [https://ghost.org](https://ghost.org) and sign up.

<ul>
  {% for member in site.data.author %}
  <li>
    {% if member.image contains 'http' %}
    <img src="{{member.image}}" alt="{{member.author}}" />
    {% else %}
    <img src="{{member.image | prepend: site.baseurl}}" alt="{{member.author}}" />
    {% endif %}
    <h2>{{member.author}}</h2>
    <p>
      {{member.bio}}
    </p>
  </li>
  {% endfor %}
</ul>
