---
layout: default
title: Home
nav: nav-split
sheet: home
permalink: /
---
<div id="first" class="section dev-layer1">
    <div id="intro" class="content dev-layer2">
        <div id="header" class="dev-layer3">
            <img id="mylogo" class="dev-layer4" src="assets\images\logos\Logo Yellow Primary.svg">
            <div id=greet class="dev-layer4">
                <p id=hey class="dev-layer5">Hey! I'm</p>
                <h1 id=name class="dev-layer5">Adair Torres</h1>
            </div>
        </div>
        <div id="blurb" class="dev-layer3">
            <p id=selfdesc class="dev-layer4">I'm a software developer with a passion for system integration, accessibility, and game development.</p>
            <p id=position class="dev-layer4">Currently @ ThreatAngler as a Cybersecurity Consultant</p>
        </div>
    </div>
    {% include nav-split.html group=1 %}
</div>
<div id=second class="section dev-layer1">
    <div id=projects class="content dev-layer2">
        {% assign to_display = site.projects | where: "featured", true %}
        {% for project in to_display %}
        <div class="project dev-layer3">
            <div class="titlebar dev-layer4">
                <img class="logo dev-layer5" src="assets/images/logos/{{ project.lang_logo_file }}">
                <h4 class="title dev-layer5">{{ project.name }}</h4>
                <div class="slant dev-layer5"></div>
            </div>
            <img class="preview dev-layer4" src="assets/images/projects/{{ project.pathname }}/{{ project.pathname }}_preview.png">
        </div>
        {% endfor %}
    </div>
    {% include nav-split.html group=2 %}
</div>