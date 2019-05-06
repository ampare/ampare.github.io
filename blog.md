---
layout: default
permalink: /blog/
active: blog
title: "Блог"
crawlertitle: "Блог"
summary: "Статьи, судебная практика, полезные материалы"
---

<!-- Masthead -->
  <header class="masthead text-white text-center">
    <div class="overlay"></div>
    <div class="container">
        <div class="col-xl-7 mx-auto">
          <h1 class="display-4">{{ page.title }}</h1>
          <p class="mb-5 lead">{{ page.summary }}</p>
        </div>
    </div>
  </header>

<section class="text-center mt-5">
    <div class="container">
        <div class="search mb-5">
          <div>
            <input type="text" id="search-input" class="input" placeholder="поиск по ключевым словам">
          </div>
          <ul id="results-container" class="dropdown"></ul>
        </div>
        <ul class="year">
          {% for post in site.posts %}
            <li class="text-left">
              <a href="{{ post.url | relative_url}}">{{ post.title }}</a>
                <small class="date text-muted font-weight-light d-none d-md-block">{{ post.date | date: "%d-%m-%Y"  }}</small>
            </li>
          {% endfor %}
        </ul>
    </div>
</section>
