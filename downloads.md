---
layout: page
title: Downloads
permalink: /downloads/
---

You can download the 1.9 pre-release installer for Fuse
[here](https://github.com/fuse-open/fuse-studio/releases).

<div id="current-version">
  <div id="current-version-mac" style="display: none;">
    <a></a>
  </div>
  <div id="current-version-win" style="display: none;">
    <a></a>
  </div>

  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script>
    var url = "https://api.github.com/repos/fuse-open/fuse-studio/releases";
    function updateRelease(latest) {
      $('#current-version-mac > a').attr('href', latest.assets[0].browser_download_url);
      $('#current-version-mac > a').text("Fuse Studio v" + latest.name + ", macOS");
      $('#current-version-win > a').attr('href', latest.assets[1].browser_download_url);
      $('#current-version-win > a').text("Fuse Studio v" + latest.name + ", Windows");
    }
    $.getJSON(url + "/latest").done(updateRelease).fail(function() {
      $.getJSON(url).done(function (releases) {
        if (releases.length > 0)
          updateRelease(releases[0]);
      });
    });

    if (navigator.platform === "MacIntel")
      document.getElementById("current-version-mac").style.display = "block";
    else if (navigator.platform === "Win32")
      document.getElementById("current-version-win").style.display = "block";
  </script>
</div>

Fuse 1.8 (and older) can be downloaded
[here](https://github.com/fusetools/fuse-releases/releases).
