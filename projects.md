---
layout: gallery
color: red
title: All Projects
---
{% for item in site.data.projects %}
<div class="preview white">
    <a><img src="{{ item.preview }}"></a>
    <div class="previewInfo">
        <div class="previewHeader">
            <div class="headerText">
                <a><h3>{{ item.name }}</h3></a>
                <p>{{ item.status }}</p>
            </div>
            <p class="bubble language yellow">{{ item.language }}</p>
        </div>
        <p>{{ item.summary }}</p>
    </div>
</div>
{% endfor %}