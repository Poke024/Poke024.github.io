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
            <div id="namePhoto">
                <h2><a>About Me</a></h2>
                <div id="pfp">
                    <img src="/assets/images/pfp_headshot.jpg">
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
            </div>
        </div>
        <div class="tile gray" id="status">
            <h1>Currently:</h1>
            <div class="whitespace">
                <p>Surviving Finals Week</p>
            </div>
        </div>
    </div>
    <div class="col-xs-12 col-m-6 col-xl-7h tile red" id="projects">
        <h1><a>Current Projects</a></h1>
        <div id="previews">
            {% for item in site.data.projects %}
                <div class="preview white">
                    <a><img src="{{ item.preview }}"></a>
                    <div class="previewInfo">
                        <div class="previewHeader">
                            <div class="headerText">
                                <a><h3>{{ item.name }}</h3></a>
                                <p>> {{ item.status }}</p>
                            </div>
                            <p class="bubble language yellow">{{ item.language }}</p>
                        </div>
                        <p>{{ item.summary }}</p>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
</div>