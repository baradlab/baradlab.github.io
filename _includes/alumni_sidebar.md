## Barad Lab Alumni
{% assign sorted_alumni = site.members | sort: "enddate" | reverse %}
{% for member in sorted_alumni %}

{% comment %} Only show members with valid end dates {% endcomment %}
{% unless member.enddate and member.enddate != empty and member.enddate != blank and member.enddate.size > 0 and member.enddate[0] != '' %}
{% continue %}
{% endunless %}

{% assign position = member.position | downcase %}
{% if position contains "intern" or position contains "visiting" 
  or position contains "high school" %}
{% continue %}
{% endif %}

<hr>
<div id = "{{member.name}}" style="padding-top: 60px; margin-top: -60px;">
<p><strong>{{member.name}}</strong><br>
<em>{{member.position | markdownify | remove: '<p>' | remove: '</p>' }}</em><br>

{% if member.pronouns %}
<em>{{member.pronouns}}</em> <br>
{% endif %}

{% assign start = member.startdate | first | date:"%Y" %}
{% assign end = member.enddate | last | date:"%Y" %}

{% if start == end %}
{{ start }}<br>
{% else %}
{{ start }} - {{ end }}<br>
{% endif %}

{% if member.subsequent %}
Subsequently: {{member.subsequent}} <br>
{% endif %}

{% if member.email %}
{% unless member.email contains "ohsu.edu" or member.email contains "baradlab" %}
<em>{{member.email}}</em> <br>
{% endunless %}
{% endif %}

{% if member.website %}
<a style="overflow-wrap: break-word;" href= "{{member.website}}">{{member.website}}</a> <br>
{% endif %}

{% if member.orcid %}
<a href="http://orcid.org"><img class="inline-block mem-icon" src="{{site.cdn}}img/site/logos/orcid_logo.svg"></a>
<a href="http://orcid.org/{{member.orcid}}"> {{member.orcid}}</a> <br>
{% endif %}

{% if member.linkedin %}
<a href="http://www.linkedin.com"><img class="inline-block mem-icon" src="{{site.cdn}}img/site/logos/linkedin_logo.svg"></a>
<a href= "http://www.linkedin.com/in/{{member.linkedin}}"> {{member.linkedin}} </a> <br>
{% endif %}

{% if member.scholar %}
<a href="http://scholar.google.com"><img class="inline-block mem-icon" src="{{site.cdn}}img/site/logos/gscholar_logo.svg"></a>
<a href= "http://scholar.google.com/citations?user={{member.scholar}}"> {% if member.timeline_name %}{{ member.timeline_name }}{% else %}{{ member.name | split: " " | first }}{% endif %}'s Citations </a> <br>
{% endif %}

{% if member.twitter %}
<a href="http://twitter.com"><img class="inline-block mem-icon" src="{{site.cdn}}img/site/logos/twitter_logo.svg"></a>
<a href= "http://twitter.com/{{member.twitter}}"> @{{member.twitter}} </a> <br>
{% endif %}

{% if member.bluesky %}
<a href="http://bsky.app"><img class="inline-block mem-icon" src="{{site.cdn}}img/site/logos/bluesky_logo.svg"></a>
<a href= "http://bsky.app/profile/{{member.bluesky}}"> @{{member.bluesky}} </a> <br>
{% endif %}

{% if member.github %}
<a href="http://github.com"><img class="inline-bloc mem-icon" src="{{site.cdn}}img/site/logos/github_logo.svg"></a>
<a href= "http://github.com/{{member.github}}"> {{member.github}} </a> <br>
{% endif %}
</p>
</div>
{% endfor %}

{% comment %} Check if there are any undergraduate interns before showing the section {% endcomment %}
{% assign has_undergraduate_interns = false %}
{% for undergraduate in sorted_alumni %}
  {% assign position = undergraduate.position | downcase %}
  {% if position contains "intern" %}
    {% assign has_undergraduate_interns = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_undergraduate_interns %}
<br>
## Undergraduate Interns
{% for undergraduate in sorted_alumni %}

{% assign position = undergraduate.position | downcase %}

{% unless position contains "intern" %}
    {% continue %}
{% endunless %}

<hr>
<div id = "{{undergraduate.name}}" style="padding-top: 60px; margin-top: -60px;">
<p><strong>{{undergraduate.name}}</strong> - <em>{{undergraduate.position | markdownify | remove: '<p>' | remove: '</p>' }}</em><br>

{% if undergraduate.pronouns %}
<em>{{undergraduate.pronouns}}</em><br>
{% endif %}

{% assign start = undergraduate.startdate | first | date:"%Y" %}
{% assign end = undergraduate.enddate | last | date:"%Y" %}

{% if start == end %}
{{ start }}<br>
{% else %}
{{ start }} - {{ end }}<br>
{% endif %}

{% if undergraduate.subsequent %}
Subsequently: {{undergraduate.subsequent}}<br>
{% endif %}
</p>
</div> {% endfor %}
{% endif %}


{% comment %} Check if there are any high school interns before showing the section {% endcomment %}
{% assign has_high_school_interns = false %}
{% for student in sorted_alumni %}
  {% assign position = student.position | downcase %}
  {% if position contains "high school" %}
    {% assign has_high_school_interns = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_high_school_interns %}
<br>
## High School Interns
{% for student in sorted_alumni %}

{% assign position = student.position | downcase %}
{% unless position contains "high school"%}
{% continue %}
{% endunless %}

<hr>
<div id = "{{student.name}}" style="padding-top: 60px; margin-top: -60px;">
<p><strong>{{student.name}}</strong><br>

{% assign start = student.startdate | first | date:"%Y" %}
{% assign end = student.enddate | last | date:"%Y" %}

{% if start == end %}
{{ start }}<br>
{% else %}
{{ start }} - {{ end }}<br>
{% endif %}

{% if student.pronouns %}
<em>{{student.pronouns}}</em> <br>
{% endif %}
{% if student.subsequent %}
Subsequently: {{student.subsequent}}<br>
{% endif %}
</p>
</div> {% endfor %}
{% endif %}


{% comment %} Check if there are any visitors before showing the section {% endcomment %}
{% assign has_visitors = false %}
{% for visitor in sorted_alumni %}
  {% assign position = visitor.position | downcase %}
  {% if position contains "visiting" %}
    {% assign has_visitors = true %}
    {% break %}
  {% endif %}
{% endfor %}

{% if has_visitors %}
<br>
## Barad Lab Visitors
{% for visitor in sorted_alumni %}

{% assign position = visitor.position | downcase %}
{% unless position contains "visiting" %}
{% continue %}
{% endunless %}

<hr>
<div id = "{{visitor.name}}" style="padding-top: 60px; margin-top: -60px;">
{% if visitor.current %}
<p><strong>{{visitor.name}}</strong> - <em>{{visitor.position | markdownify | remove: '<p>' | remove: '</p>' }} from {{visitor.current}}</em><br>
{% else  %}
<p><strong>{{visitor.name}}</strong> - <em>{{visitor.position | markdownify | remove: '<p>' | remove: '</p>' }}</em><br>
{% endif %}

{% assign start = visitor.startdate | first | date:"%Y" %}
{% assign end = visitor.enddate | last | date:"%Y" %}

{% if end %}
{% if start == end %}
{{ start }}<br>
{% else %}
{{ start }} - {{ end }}<br>
{% endif %}
{% else %}
{{ start }} - Present<br>
{% endif %}

{% if visitor.pronouns %}
<em>{{visitor.pronouns}}</em> <br>
{% endif %}
</p>
</div> {% endfor %}
{% endif %}