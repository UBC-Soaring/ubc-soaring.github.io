---
title: "Executive Positions"

feature_row:
  - title: Nathan Pennie
    alt: Nathan Pennie
    image_path: /assets/site-images/exec-nathan-pennie.png
    excerpt: |
      **President**
      
      Nathan began soaring a the [Greater Boston Soaring Club](https://www.soargbsc.com/) in Sterling, MA, USA and the
      [Franconia Soaring Association](http://franconiasoaring.org/) in Franconia, NH, USA. He holds a Private Pilot
      Glider license in the United States, and has around 180 flights and 75 hours in the air.
      
      [<i class="fas fa-link" aria-hidden="true"></i>](https://www.kb1rd.net/){: .btn .btn--primary}
      [\[m\]](https://matrix.to/#/@kb1rd:kb1rd.net){: .btn .btn--primary}
      [<i class="fab fa-instagram" aria-hidden="true"></i>](https://instagram.com/kb1rd_){: .btn .btn--primary}
      [<i class="fab fa-linkedin" aria-hidden="true"></i>](https://www.linkedin.com/in/kb1rd){: .btn .btn--primary}
---

# Current Execs

{% include feature_row %}

## Unfilled Positions

**Treasurer, VP Marketing, VP External, VP Internal, and Secretary.**

If you would like to run for one of these positions, please see [the announcement](/announcements/2024/04-11-exec.html).

# Definition of Roles
For reference, the formal definition of the roles as stated in the bylaws is below:

{% for role in site.data.execs.roles %}
## {{ role.name }}

{{ role.responsibilities | markdownify }}
{% endfor %}
