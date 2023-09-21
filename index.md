---
layout: default
title: Home
---
<div class="row">
    <div class="left">
        <div class="sectionBox" id="projects">
            <div class="wrapper">
                <h1>Current Projects</h1>
                <div id="projectsContainer">
                    {% for item in site.data.projects %}
                        <div class="projectBox">
                            <img class="projectPreview" src="{{ item.preview }}">
                            <div class="projectInfo">
                                <div class="projectHeader">
                                    <div class="headerInfo">
                                        <h3>{{ item.name }}</h3>
                                        <p>> {{ item.status }}</p>
                                    </div>
                                    <p class="projectLanguage">{{ item.language }}</p>
                                </div>
                                <div class="projectSummary">
                                    <p>{{ item.summary }}</p>
                                </div>
                            </div>
                        </div>
                        <div class="boxSpacer"></div>
                    {% endfor %}
                </div>
            </div>
        </div>
    </div>
    <div class="right">
        <div class="sectionBox" id="profile">
            <div class="wrapper" id="profileInfo">
                <h2>Adair Torres</h2>
                <center><img id="profilePic" src="/assets/images/profile.JPG"></center>
                <h3>Contact</h3>
                <p>adair.tor24@gmail.com</p>
            </div>
        </div>
    </div>
</div>