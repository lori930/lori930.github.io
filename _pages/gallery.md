---
permalink: /gallery/
title: "Lab Gallery"
author_profile: true
---

<style>
/* ── Timeline container ─────────────────────────────── */
.tl {
  position: relative;
  padding: 1rem 0 2rem;
  margin-top: 1.5rem;
}
.tl::before {
  content: "";
  position: absolute;
  left: 90px;
  top: 0; bottom: 0;
  width: 2px;
  background: #e0ddd6;
}

/* ── Each event row ─────────────────────────────────── */
.tl-item {
  display: flex;
  gap: 1.5rem;
  margin-bottom: 2.5rem;
  align-items: flex-start;
}

.tl-date {
  min-width: 75px;
  text-align: right;
  font-size: 12.5px;
  font-weight: 500;
  color: #888880;
  padding-top: 4px;
  line-height: 1.4;
  flex-shrink: 0;
}

/* dot on the line */
.tl-dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #2d5a3d;
  border: 2px solid #fafaf7;
  outline: 2px solid #2d5a3d;
  flex-shrink: 0;
  margin-top: 5px;
}

.tl-body {
  flex: 1;
}

.tl-title {
  font-size: 14.5px;
  font-weight: 500;
  color: #1a1a18;
  margin-bottom: 0.5rem;
  line-height: 1.4;
}

.tl-caption {
  font-size: 13px;
  color: #888880;
  margin-bottom: 0.6rem;
  font-style: italic;
}

/* ── Photo grid ─────────────────────────────────────── */
.tl-photos {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.tl-photos a {
  display: block;
  flex: 0 0 auto;
}

/* single photo — wider */
.tl-photos.single a {
  width: 320px;
}

/* multiple photos — thumbnail row */
.tl-photos.multi a {
  width: 160px;
}

.tl-photos img {
  width: 100%;
  height: 120px;
  object-fit: cover;
  border-radius: 5px;
  border: 1px solid #e0ddd6;
  transition: opacity 0.15s;
  display: block;
}

.tl-photos.single img {
  height: 200px;
}

.tl-photos img:hover { opacity: 0.85; cursor: zoom-in; }

@media (max-width: 600px) {
  .tl::before { left: 70px; }
  .tl-date    { min-width: 55px; font-size: 11px; }
  .tl-photos.single a,
  .tl-photos.multi  a { width: 130px; }
}
</style>


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
