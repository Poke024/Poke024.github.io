---
layout: default
title: Home
sheet: home
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
    <nav id="nav-one" class="links dev-layer2">
        <div class="link-nav dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">ABOUT</h2>
            <span class="navIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
        <div class="link-nav dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">WORK</h2>
            <span class="navIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
    </nav>
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
    <nav id="nav-two" class="links dev-layer2">
        <div class="link-nav dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">PROJECTS</h2>
            <span class="navIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
        <div class="link-nav dev-layer3">
            <div class="dev-layer4"></div>
            <h2 class="dev-layer4">CONTACT</h2>
            <span class="navIcon material-symbols-outlined dev-layer4">arrow_forward_ios</span>
        </div>
    </nav>
</div>