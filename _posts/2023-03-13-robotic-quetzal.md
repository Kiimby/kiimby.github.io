---
layout: posts
title:  "Quetzal"
categories:
    - Portfolio
header:
  teaser: /assets/images/Teaser/QuetzalTeaser.png
  og_image: /assets/images/page-header-og-image.png
tags: 
    - Sculpture 
    - 3D Printing

---

Quetzal sculpt stand made for 3D printing as a commission for Pilas Tecnología Guatemaya.

[//]: <> (First close up render)

{% capture fig_img %}
![Foo]({{ "/assets/images/Portfolio/QuetzalSculpture/quetzalcloseup2.jpg" | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Body close up.</figcaption>
</figure>

[//]: <> (Second close up render)

{% capture fig_img %}
![Foo]({{ "/assets/images/Portfolio/QuetzalSculpture/quetzalcloseup3.jpg" | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Tail close up.</figcaption>
</figure>

[//]: <> (Turn around renders)
{% capture fig_img %}
![Foo]({{ "/assets/images/Portfolio/QuetzalSculpture/quetzalturnaround.jpg" | relative_url }})
{% endcapture %}

<figure>
  {{ fig_img | markdownify | remove: "<p>" | remove: "</p>" }}
  <figcaption>Different views.</figcaption>
</figure>


```yaml
header:
  teaser: /assets/images/Teaser/QuetzalTeaser.png
  og_image: /assets/images/page-header-og-image.png
  ```