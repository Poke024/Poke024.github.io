---
layout: default
title: Home
---
<div class="row">
    <div class="col-xs-12 col-m-5h col-xl-7 tile yellow" id="intro">
        <h1>Hi, I'm Adair Torres.</h1>
        <div class="whitespace">
            <p>
            Thanks for visiting my website! This site acts as my own online portfolio, and a place I can reasonably infodump about my current projects and interests.
            </p>
        </div>
    </div>
    <div class="col-xs-12 col-m-5h col-xl-4" id="profileContainer">
        <div class="tile blue" id="profile">
            <div id="header">
                <h2><a class="link-white">About Me</a></h2>
                <div id="pfp">
                    <img src="/assets/images/index/portrait_headshot.jpg">
                </div>
            </div>
            <div class="whitespace" id="profileInfo">
                <h3><u>Contact</u></h3>
                    <a id="eLink" href="#" onclick="setEmail()"><i class="fa-regular fa-envelope fa-lg"></i><p>Email Me</p></a>
                <h3><u>Education</u></h3>
                <div class="wrapper" id="education">
                    <p><b>University of Kansas</b></p>
                    <p><i>B.S. in Computer Science, May 2024</i></p>
                    <p>GPA: 3.82 | Organizations: ACM@KU, Upsilon Pi Epsilon</p>
                </div>
                {% for category in site.data.bubbles %}
                    <div class="bubbleset">
                        <h3><u>{{ category.header }}</u></h3>
                        <div class="wrapper">
                            {% for item in category.items %}
                                <p class="bubble info {{ category.color }}">{{ item.text }}</p>
                            {% endfor %}
                        </div>
                    </div>
                {% endfor %}
            </div>
        </div>
        <div class="tile gray" id="status">
            <h1>Currently:</h1>
            <div class="whitespace">
                <a><p>Job Hunting</p></a>
            </div>
        </div>
    </div>
    <div class="col-xs-12 col-m-6 col-xl-7h tile red" id="projects">
        <h1><a>Current Projects</a></h1>
        {% assign to_display = site.projects | where: "featured", true %}
        {% include previews.html %}
    </div>
</div>