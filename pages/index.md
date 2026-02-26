---
layout: default
title: Home
nav: nav-split
sheet: home
permalink: /
---
<div id="first" class="section">
    <div id="intro" class="content">
        <div id="header">
            <img id="mylogo" src="assets\images\logos\Logo Yellow Primary.svg">
            <div id=greet>
                <p id=hey>Hey! I'm</p>
                <h1 id=name>Adair Torres</h1>
            </div>
        </div>
        <div id="blurb">
            <p id=selfdesc>I'm a software developer with a passion for system integration, accessibility, and game development.</p>
            <p id=position>Currently @ ThreatAngler as a Cybersecurity Consultant</p>
        </div>
    </div>
    {% include nav-split.html group=1 %}
</div>
<div id=second class="section">
    <div id=projects class="content">
        {% assign to_display = site.projects | where: "featured", true %}
        {% for project in to_display %}
        <div class="project">
            <div class="titlebar">
                <img class="logo" src="assets/images/logos/{{ project.lang_logo_file }}">
                <h4 class="title">{{ project.name }}</h4>
                <div class="slant"></div>
            </div>
            <img class="preview" src="assets/images/projects/{{ project.pathname }}/{{ project.pathname }}_preview.png">
        </div>
        {% endfor %}
    </div>
    {% include nav-split.html group=2 %}
</div>