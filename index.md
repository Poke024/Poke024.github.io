---
layout: default
title: Home
---
<div class="column">
    <div class="row around">
        <div class="row" id="introProjects">
            <div class="tile fadeInLeft liftRight yellow" id="intro">
                <h1>Hi, I'm Adair Torres.</h1>
                <p>
                Thanks for visiting my website! I'm senior at the University of Kansas studying computer science, planning to graduate this month! This site acts as my own online portfolio, and a place I can reasonably infodump about my current projects and interests.
                </p>
            </div> 
            <div class="tile fadeInLeft liftRight red" id="projects">
                <h1>Current Projects</h1>
                <div class="row" id="previews">
                    {% for item in site.data.projects %}
                        <div class="preview white">
                            <img src="{{ item.preview }}">
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
        <div class="sizeWrapper column">
            <div class="tile fadeInRight liftLeft blue" id="profile">
                <div id="namePhoto">
                    <h2>About Me</h2>
                    <div id="pfp">
                        <img src="/assets/images/pfp_headshot.jpg">
                    </div>
                </div>
                <div id="profileInfo">
                    <h3><u>Contact</u></h3>
                        <a href="mailto:adair.tor24@gmail.com"><i class="gg-mail"></i><p>adair.tor24@gmail.com</p></a>
                    <h3><u>Education</u></h3>
                    <div class="wrapper" id="education">
                        <p><b>University of Kansas</b></p>
                        <p><i>B.S. in Computer Science, Expected May 2024</i></p>
                        <p>GPA: 3.83 | Organizations: ACM@KU, Upsilon Pi Epsilon</p>
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
            <div class="row around">
                <div class="tile row fadeInRight liftLeft gray" id="status">
                    <h1>Currently:</h1>
                    <p>Surviving finals week.</p>
                </div>
            </div>
        </div>
    </div>
</div>