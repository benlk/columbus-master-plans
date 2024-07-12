---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
description: "An unofficial list of all master plans for the City of Columbus"
date: 2024-07-10
---

<div
  class="usa-summary-box"
  role="region"
  aria-labelledby="summary-box-key-information"
>
  <div class="usa-summary-box__body">
    <h2 class="usa-summary-box__heading" id="summary-box-key-information">
      Master plans
    </h2>
    <p>A master plan helps a community to plan future development and growth over the long term.</p>
    <div class="usa-summary-box__text">
      <ul class="usa-list">
        <li>The City of Columbus has several topic-specific master plans</li>
        <li>Different plans are updated on different cycles</li>
        <li>Plans from regional agencies supplement and guide the City of Columbus' planning efforts</li>
      </ul>
    </div>
  </div>
</div>

## List of Columbus Master Plans

Note that some of these plans were still being actively developed when this site was last updated: on {{ site.time | date: '%A, %B %e, %Y' }}.

<ul class="usa-collection">
  {% assign columbus = site.plans | where: "scope", "columbus" | sort: "order" %}
  {% for plan in columbus %}
    {% include columbus/plan.html %}
  {% endfor %}
</ul>

## List of Regional Master Plans

<ul class="usa-collection">
  {% assign columbus = site.plans | where: "scope", "regional" | sort: "order" %}
  {% for plan in columbus %}
    {% include columbus/plan.html %}
  {% endfor %}
</ul>

## Help contribute to this site

If you're aware of a master plan that isn't listed here, and isn't listed [in the project to-do list](https://github.com/benlk/columbus-master-plans/issues), please [open an issue](https://github.com/benlk/columbus-master-plans/issues/new?assignees=benlk&labels=New+Plan&projects=&template=new-plan.md&title=New+Plan%3A+%5Bplan+name%5D) on the project's GitHub repository.
