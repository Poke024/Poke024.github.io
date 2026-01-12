---
layout: default
title: Home
sheet: home
---
<div id=first class="section dev-layer1">
    <div id=intro class="content dev-layer2">
        <div id=logo class="dev-layer3">
            <div class="dev-layer4">
                <img src="assets\images\logos\Logo Yellow Primary.svg">
            </div>
        </div>
        <div id=greet class="dev-layer3">
            <p id=hey class="dev-layer4">Hey! I'm</p>
            <h1 id=name class="dev-layer4">Adair Torres</h1>
        </div>
        <div id=bio class="dev-layer3">
            <p id=selfdesc class="dev-layer4">I'm a software developer with a passion for system integration,<br>accessibility, and game development.</p>
            <p id=position class="dev-layer4">Currently @ ThreatAngler as a Cybersecurity Consultant</p>
        </div>
    </div>
    <nav id=pages class="links dev-layer2">
        <div class="link-nav dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">About</h2>
            <span class="pageIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
        <div class="link-nav dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">Work</h2>
            <span class="pageIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
    </nav>
</div>
<div id=second class="section dev-layer1">
    <div id=projects class="content dev-layer2">
        {% assign to_display = site.projects | where: "featured", true %}
        {% for project in to_display %}
        <div class="project dev-layer3">
            <div class="title dev-layer4">
                <img class="dev-layer5" src="assets/images/logos/{{ project.lang_logo_file }}">
                <h4 class="dev-layer5">{{ project.name }}</h4>
                <div class="title-corner"></div>
            </div>
            <div class="preview dev-layer4">
                <img src="assets/images/projects/{{ project.pathname }}/{{ project.pathname }}_preview.png">
            </div>
        </div>
        {% endfor %}
    </div>
    <nav id=socials class="links dev-layer2">
        <div class="link-external dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">Projects</h2>
            <span class="pageIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
        <div class="link-external dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">Contact</h2>
            <span class="pageIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
    </nav>
</div>