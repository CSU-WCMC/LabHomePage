---
layout: none
permalink: /
---
{% assign en_path = '/en/' | relative_url %}
{% assign zh_path = '/zh/' | relative_url %}
<script>
  (function () {
    var lang = (navigator.language || navigator.userLanguage || "en").toLowerCase();
    var target = lang.indexOf("zh") === 0 ? "{{ zh_path }}" : "{{ en_path }}";
    window.location.replace(target);
  })();
</script>
<noscript>
  <meta http-equiv="refresh" content="0; url={{ zh_path }}" />
</noscript>
