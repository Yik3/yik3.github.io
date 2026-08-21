---
layout: about
title: About
permalink: /
subtitle: Researcher, <a href='https://uril.cs.ucla.edu/'> UCLA Robot Intelligence Lab </a> </n> Robotics Intern, <a href='https://hawkrobo.com/'> HawkRobo Systems </a>

profile:
  align: right
  image: yike_photo.JPG
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>3531C Boelter Hall</p>
    <p>UCLA Robot Intelligence Lab</p>
    <p>580 Portola Plaza</p>
    <p>Los Angeles, CA 90095</p>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

# announcements:
#   enabled: true # includes a list of news items
#   scrollable: true # adds a vertical scroll bar if there are more than 3 news items
#   limit: 5 # leave blank to include all the news in the `_news` folder

# latest_posts:
#   enabled: true
#   scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
#   limit: 3 # leave blank to include all the blog posts
---
<style>
  /* 放大主页的段落和列表文字 */
  article p, article li {
    font-size: 1.3rem; /* 默认通常是 1rem，推荐在 1.1rem - 1.2rem 之间微调 */
    line-height: 1.7;   /* 配合大字体，稍微拉宽一点行距让视觉更舒适 */
  }

  /* 如果觉得 Teaching, Selected Projects 等二级标题也不够大，可以加上这段 */
  /* <!--
  article h2 {
    font-size: 2.2rem; 
  }
  --> */
  /* 如果想把右侧的个人信息（地址等）也放大
  .profile .more_info p {
    font-size: 1.1rem;
  } */
</style>
I am a senior computer engineering undergraduate student at UCLA advised by [Yuchen Cui](https://yuchencui.cc/). My primary research interests lie in robot learning and intelligent control. My previous research integrates gaze into bimanual manipulation policies to enhance long-horizon tasks, training visual-motor policies using customized and optimized data collection hardware, and designing pipelines that improves VLM Code as Policy. I interned at HawkRobo Systems where I explored a general open-door policy for in-the-wild robot dog deployment.  

I started building Robots at 6. I won a first prize in WER-J world championship. In high school, I was the president of Jinling High School's VEX Robotics Club. I led team 20089B won a First Prize in World Championship(2021), and I led team 20089X won a First Prize and ranked Semi-Finalist in Asia Championship(2023). 

I am looking for a Ph.D. position in Robotics Learning or Human Robot Interaction. I am also looking for a full-time Software Robotics Engineering position. 

If you are interested, reach out to me at yikeshi9248 [at] ucla.edu

***

<!-- Manually call Selected Publications first -->
<h2><a href="{{ '/publications/' | relative_url }}" style="color: inherit;">Notable Publications</a></h2>
<div class="publications">
  {% include selected_papers.liquid %}
</div>

<!-- Manually call Selected Projects right after -->
<h2><a href="{{ '/projects/' | relative_url }}" style="color: inherit;">Selected Projects</a></h2>

<div class="publications">
  <ol class="bibliography">
    {% assign selected_projects = site.projects | where: "selected", true | sort: "importance" %}
    {% for project in selected_projects %}
    <li>
      <div class="row">
        <!-- Left column: Thumbnail -->
        <div class="col-sm-2 abbr">
          {% if project.img %}
            <a href="{{ project.url | relative_url }}">
              <img src="{{ project.img | relative_url }}" class="teaser img-fluid z-depth-1 rounded" alt="project thumbnail">
            </a>
          {% endif %}
        </div>
        
        <!-- Right column: Text details -->
        <div class="col-sm-10">
          <div class="title"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></div>
          {% if project.authors %}
            <div class="author">{{ project.authors }}</div>
          {% endif %}
          <div class="periodical"><em>{{ project.description }}</em></div>
        </div>
      </div>
    </li>
    {% endfor %}
  </ol>
</div>

***

## Teaching
* **Learning Assistant**, *CS 188: Introduction to Robotics*, UCLA (Winter 2026)
  * Supervised by Prof. Yuchen Cui.
* **Teaching Assistant**, *CS 97: Generative AI*, UCLA (Summer 2026)
  * Supervised by Prof. Kai-Wei Chang.
* **Course Grader**, *ECE 100: Electrical and Electronics Circuits*, UCLA (Spring 2026)
  * Supervised by Prof. Yang Zhang.
* **Lab Assistant/Mentor**, *ECE 3: Introduction to Electrical Engineering*, UCLA (Fall 2024, Spring 2025, Fall 2025, Spring 2026, Fall 2026)
  * Supervised by Prof. Dennis Briggs.



***