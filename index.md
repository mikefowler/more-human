---
title: Home
layout: default
---
<div class="wordplay">
  <header>
    <div class="wordplay__title">
      <h1 class="wordplay__word">More <span class="wordplay__title__muted">Human</span></h1>
    </div>
    <div class="wordplay__content text-right-md space-top-2" aria-hidden="true">
      <h2 class="wordplay__description size-4 font-sans-serif">
        {% assign bold_title = site.title | prepend: "<strong>" | append: "</strong>" %}
        {{ site.description | replace: site.title, bold_title }}
      </h2>
      <nav>
        <ul class="nav space-top-4 size-5">
          {% for link in site.data.navigation %}
            <li><a class="nav__link" href="{{ link.href }}">{{ link.text }}</a></li>
          {% endfor %}
        </ul>
      </nav>
    </div>
  </header>

  <div class="wordplay__words">
    {% for word in site.data.wordplay %}
      <div class="wordplay__section">
        <span class="wordplay__word font-serif heading-1">
          <span class="text-hidden">More</span>
          <span class="text-{{ word.color }}">{{ word.name }}</span>
        </span>
      </div>
    {% endfor %}
  </div>
</div>
