---
layout: default
title: Home
---
<div class="tileContainer">
    <div class="tile liftRight red" id="projects">
        <h1>Current Projects</h1>
        <div class="wrapper">
            {% for item in site.data.projects %}
                <div class="preview white">
                    <img src="{{ item.preview }}">
                    <div class="previewInfo">
                        <div class="previewHeader">
                            <div class="headerText">
                                <h3>{{ item.name }}</h3>
                                <p>> {{ item.status }}</p>
                            </div>
                            <p class="bubble language yellow">{{ item.language }}</p>
                        </div>
                        <div class="previewSummary">
                            <p>{{ item.summary }}</p>
                        </div>
                    </div>
                </div>
                <div class="boxSpacer"></div>
            {% endfor %}
        </div>
    </div>
    <div class="horizontalSpacer"></div>
    <div class="tile liftLeft blue" id="profile">
        <div id="namePhoto">
            <h2>Adair Torres</h2>
            <div id="pfp">
                <img src="/assets/images/pfp_headshot.jpg">
            </div>
        </div>
        <div id="profileInfo">
            <h3><u>Contact</u></h3>
                <a><i class="gg-mail"></i><p>adair.tor24@gmail.com</p></a>
            <h3><u>Interests</u></h3>
            <div class="wrapper">
                {% for item in site.data.interests %}
                    <p class="bubble info gray">{{item.text}}</p>
                {% endfor %}
            </div>
            <h3><u>Technical Skills</u></h3>
            <div class="wrapper">
                {% for item in site.data.technical %}
                    <p class="bubble info yellow">{{item.text}}</p>
                {% endfor %}
            </div>
            <h3><u>Soft Skills</u></h3>
            <div class="wrapper">
                {% for item in site.data.soft %}
                    <p class="bubble info gray">{{item.text}}</p>
                {% endfor %}
            </div>
            <h3><u>Hobbies</u></h3>
            <div class="wrapper">
                {% for item in site.data.hobbies %}
                    <p class="bubble info yellow">{{item.text}}</p>
                {% endfor %}
            </div>
        <div>
    </div>
</div>