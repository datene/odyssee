---
layout: default
title: Team
description: Meet the team
permalink: /team/
picture: /images/animation.gif
---

<div class="container">
  <div class="row">
    {% for team_member in site.team_members %}
    <div class="col-xs-12 col-lg-6">
      <div class="team-member">
        <div class="avatar" style="background-image:url('{{ site.url  }}{{ site.baseurl  }}{{ team_member.avatar }}" alt="{{ team_member.name }}');"></div>
        <div class="member-info">
          <h3>
            {{ team_member.name }}
          </h3>
          <h4>
            {{ team_member.title }}
          </h4>
          <p>
            <strong>
              Past:
            </strong>
            {{ team_member.past }}
          </p>
          <p>
            <strong>
              Future:
            </strong>
            {{ team_member.future }}
          </p>
          {% if team_member.linkedin %}
          <a href="{{ team_member.linkedin }}" class="linkedin">
            <i class="fa fa-linkedin fa-2x"></i>
          </a>
          {% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
  <div class="row">
  <h3 class="text-center">
    Contributors
  </h3>
    {% for member in site.members %}
    <div class="col-xs-6 col-lg-3">
      <div class="team-member">
        <div class="avatar" style="background-image:url('{{ site.url  }}{{ site.baseurl  }}{{ member.avatar }}" alt="{{ member.name }}');"></div>
        <div class="member-info">
          <h3>
            {{ member.name }}
          </h3>
          <h4>
            {{ member.title }}
          </h4>
          <p>
            <strong>
              Contribution:
            </strong>
            {{ member.contribution }}
          </p>
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</div>


