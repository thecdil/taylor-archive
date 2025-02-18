---
title: Oral Histories
layout: page
permalink: /oral_histories/
---

## Oral Histories

<div class="row">
<div class="col-md-8 ps-2">
This collection consists of 11 hour-long video interviews with the following people: Ed Krumpe, Gary Koehler, Teresa Cohn, Jennifer Ladino, Lauren Fins (in Moscow , Idaho), Andrew Armstrong, Colden Baxter, Janet Devlieg, Grace Peven (at the TWRC), Jim and Holly Akenson (Enterprise, Oregon) and Maurice Hornocker (Belleview, Idaho) conducted between summer of 2022 and spring of 2023.
</div>
<div class="col-md-4 p-5 text-center">

{% include feature/button.html centered="true" text="Visualize by Topic" link="visualization.html" color="primary btn-lg" %}

</div>
</div>
{% assign items = site.data.taylor %}
{% assign interviewees = site.data.interviewees %}

{% for i in interviewees %}
<div class="row my-4 py-4 bg-light border interview-card {% cycle 'end', 'start' %}">

    {% assign image_item = items | where: "interviewee",i.interviewee | first %}
    {% assign position = forloop.index | modulo: 2 %}

    {% if position == 1 %}
    {%- comment -%}Image on left{%- endcomment -%}
    <div class="col-md-4 my-3">
        <img src="{{ image_item.image_small | relative_url }}" class="img-fluid rounded my-3" alt="{{ i.interviewee }}">
    </div>
    <div class="col-md-7">
        <h2>{{ i.interviewee }}</h2>
        <p>{{ i.overview }}</p>
        <div class="btn-group">
            {% assign interviews = items | where: "interviewee",i.interviewee %}
            {% for interview in interviews %}
                {% if interview.title contains "Full Interview" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-primary m-1">Full Interview</a>
                {% elsif interview.title contains "Highlight" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-success m-1">Highlights</a>
                {% elsif interview.title contains "Part One" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-secondary m-1">Part 1</a>
                {% elsif interview.title contains "Part Two" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-secondary m-1">Part 2</a>
                {% elsif interview.title contains "Part Three" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-secondary m-1">Part 3</a>
                {% endif %}
            {% endfor %}
        </div>
    </div>
    {% else %}
    {%- comment -%}Image on right{%- endcomment -%}
    <div class="col-md-7 offset-md-1 py-2 ">
        <h2>{{ i.interviewee }}</h2>
        <p>{{ i.overview }}</p>
        <div class="btn-group">
            {% assign interviews = items | where: "interviewee",i.interviewee %}
            {% for interview in interviews %}
                {% if interview.title contains "Full Interview" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-primary m-1">Full Interview</a>
                {% elsif interview.title contains "Highlight" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-success m-1">Highlights</a>
                {% elsif interview.title contains "Part One" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-secondary m-1">Part 1</a>
                {% elsif interview.title contains "Part Two" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-secondary m-1">Part 2</a>
                {% elsif interview.title contains "Part Three" %}
                <a href="{{ interview.objectid | prepend: '/items/' | append: '.html' | relative_url }}" class="btn btn-outline-secondary m-1">Part 3</a>
                {% endif %}
            {% endfor %}
        </div>
    </div>
    <div class="col-md-4 my-3">
        <img src="{{ image_item.image_small | relative_url }}" class="img-fluid rounded my-3" alt="{{ i.interviewee }}">
    </div>
    {% endif %}
</div>
{% endfor %}

<style>
a {
    text-decoration: underline;
    color:rgb(16, 22, 31);
}

.interview-card {
    border-radius: 0 !important;
}

@media (min-width: 768px) {
    .interview-card {
        border-radius: 50rem !important;
    }
    .interview-card.start {
        border-top-right-radius: 0 !important;
        border-bottom-right-radius: 0 !important;
    }
    .interview-card.end {
        border-top-left-radius: 0 !important;
        border-bottom-left-radius: 0 !important;
    }
}
</style>