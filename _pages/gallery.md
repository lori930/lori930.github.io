---
permalink: /gallery/
title: "Lab Gallery"
author_profile: true
---



<div class="tl">

  <!-- ═══════════════════════════════════════════════════════
       HOW TO ADD A NEW EVENT
       ───────────────────────────────────────────────────────
       1. Copy one of the <div class="tl-item"> blocks below.
       2. Update tl-date, tl-title, tl-caption.
       3. For ONE photo:   use class="tl-photos single"
          For MULTIPLE:    use class="tl-photos multi"
       4. Add one <a>/<img> pair per photo.
          href  = full-size image path (for lightbox)
          src   = same path (or a thumbnail)
          alt   = short description
       5. Upload the image(s) to images/gallery/.
       ═══════════════════════════════════════════════════════ -->


  <!-- ── 2025 · IGVC Competition ───────────────────────── -->
  <div class="tl-item">
    <div class="tl-date">Jun<br>2025</div>
    <div class="tl-dot"></div>
    <div class="tl-body">
      <div class="tl-title">IGVC 2025 — Self-Drive Challenge</div>
      <div class="tl-caption">3rd place · Yunge &amp; Shaibal</div>
      <div class="tl-photos single popup-group">
        <a href="/images/gallery/igvc-2025.jpg">
          <img src="/images/gallery/igvc-2025.jpg" alt="IGVC 2025 team photo">
        </a>
      </div>
    </div>
  </div>

  <!-- ── 2025 · Lab Gathering ──────────────────────────── -->
  <div class="tl-item">
    <div class="tl-date">2025</div>
    <div class="tl-dot"></div>
    <div class="tl-body">
      <div class="tl-title">Lab Gathering</div>
      <div class="tl-caption">EIS Lab dinner</div>
      <div class="tl-photos multi popup-group">
        <a href="/images/gallery/gathering-2025-1.jpg">
          <img src="/images/gallery/gathering-2025-1.jpg" alt="Lab gathering 2025">
        </a>
        <a href="/images/gallery/gathering-2025-2.jpg">
          <img src="/images/gallery/gathering-2025-2.jpg" alt="Lab gathering 2025">
        </a>
        <a href="/images/gallery/gathering-2025-3.jpg">
          <img src="/images/gallery/gathering-2025-3.jpg" alt="Lab gathering 2025">
        </a>
      </div>
    </div>
  </div>

  <!-- ── 2024 · Conference Presentation ───────────────── -->
  <div class="tl-item">
    <div class="tl-date">2024</div>
    <div class="tl-dot"></div>
    <div class="tl-body">
      <div class="tl-title">IEEE MOST 2024</div>
      <div class="tl-caption">Yunge presenting</div>
      <div class="tl-photos single popup-group">
        <a href="/images/gallery/most-2024.jpg">
          <img src="/images/gallery/most-2024.jpg" alt="IEEE MOST 2024 presentation">
        </a>
      </div>
    </div>
  </div>

  <!-- ── ADD MORE EVENTS ABOVE THIS LINE ───────────────── -->

</div>


<!-- Magnific Popup lightbox (already bundled in the template) -->
<script>
$(document).ready(function () {
  // Each .popup-group is an independent gallery group
  document.querySelectorAll('.popup-group').forEach(function (group) {
    $(group).find('a').magnificPopup({
      type: 'image',
      gallery: { enabled: true },
      image: { titleSrc: function (item) { return item.el.find('img').attr('alt'); } }
    });
  });
});
</script>
