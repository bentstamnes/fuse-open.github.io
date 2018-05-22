---
layout: page
title: Logo Contest
permalink: /logo-contest/
---

After Fuse 1.9, the Fuse Open project will need a new logo and/or logomark that
new icon-sets can be based on, to avoid confusion with Fusetools and future
Fusetools projects.

We've decided to ask the community for help! The Fuse community has a lot of
creative people who are great at exactly this kind of work! So, if you're
interested please submit a logo here!

## Guidelines:
- Entries should to be visually distinct fron the current "fat-comma" logo.
- It should be possible to create a visually clear icon from the logo, even in
  small resolutions (even 16x16 pixels).
- The logo must be available under the
  [CC BY 4.0 license](https://creativecommons.org/licenses/by/4.0/).
- The logo cannot contain fonts that require a license. This means that either
  only license-free fonts may be used, or the font needs to be properly licensed,
  and converted to outlines (or rasterized) before distribution.
- Entries that are obviously jokes, or of offending nature, will not be
  accepted.
- Optional: The logo should spell "Fuse Open".
- Optional: It's very nice if the logo is easy to adopt to spell "Fuse Studio"
  as well.
- Optional: [SVG](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics) fonts
  are preferred, as they are easier to rescale.

## How to enter

### By E-Mail

You can submit your logo simply by e-mailing it to
[our mailing list](mailto:fuse-open@googlegroups.com). Please prefix the
subject of the e-mail with "[logo-contest]" to make submissions easy to
filter.

### Via Pull-Request

Alternatively, if you want to ease our burden a bit, you can also submit by
sending a pull-request to the
[GitHub repository](https://github.com/fuse-open/fuse-open.github.io) for our
website.

If so, add your logo to the [`assets/images/logo-contest/`-subdirectory](https://github.com/fuse-open/fuse-open.github.io/tree/master/assets/images/logo-contest/),
and add your entry to [`_data/logo-contest.yml`](https://github.com/fuse-open/fuse-open.github.io/blob/master/_data/logo-contest.yml),
in the following format:

```
- file: filename.png
  author: John Doe
  email: john.doe@example.com
```

You can see an example-submission [here](https://github.com/kusma/fuse-open.github.io/compare/logo-contest...example-submission).

## Deadline

The deadline is Friday 1st of June 2018. Please submit your entries before
then.

## Submissions

{% if site.data.logo-contest %}
<table>
  <thead>
    <tr>
      <th>Logo</th>
      <th>Author</th>
    </tr>
  </thead>
  <tbody>
{% for logo in site.data.logo-contest %}
    <tr>
      <td><a href="{{ site.baseurl }}/assets/images/logo-contest/{{ logo.file }}"><img src="{{ site.baseurl }}/assets/images/logo-contest/{{ logo.file }}" alt="Logo by {{ logo.author }}" /></a></td>
      <td><span style="white-space:nowrap"><a href="mailto:{{ logo.email }}">{{ logo.author }}</a></span></td>
    </tr>
{% endfor %}
  </tbody>
</table>
{% else %}

There's no sumbissions yet :(

Want to be the first?

{% endif %}
