---
layout: default
title: Contact
nav: nav-split
sheet: contact
permalink: /contact
---
<div id="content">
    <div id="links" class="section">
        <h1>Get in Touch</h1>
        <div id="socials">
            <ul> 
                {% for item in site.data.socials.links %}
                    <li>
                        <a class="socialLink" href="{{ item.url }}"><i class="{{ item.icon }} fa-xl"></i>{{ item.name }}</a>
                    </li>
                {% endfor %}
            </ul>
        </div>
    </div>
    <div class="section">
        <div class="titlebar">
            <div class="slant"></div>
            <h4 class="title">Contact</h4>
            <div class="slant"></div>
        </div>
        <form>
            <div>
                <h6>Name</h6>
                <input/>
            </div>
            <div>
                <h6>Email</h6>
                <input/>
            </div>
            <div>
                <h6>Message</h6>
                <input/>
            </div>
            <button>Submit</button>
        </form>
    </div>
</div>