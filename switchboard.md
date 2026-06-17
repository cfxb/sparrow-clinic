---
layout: page
title: Switchboard
description: "Switchboard is a macOS app built by a psychologist, for psychologists. Patient records, clinical notes, and referral relationships — offline, on your machine."
hero_title: Switchboard
hero_subtitle: Clinical records software
hero_image: /assets/images/hero-sky.jpg
---

<style>
  /* ── Switchboard landing — scoped to .sb-* ─────────────────
     Colour values pulled directly from _sass/_variables.scss   */

  .sb-container {
    max-width: 680px;
    margin: 0 auto;
    padding: 0 32px;
  }

  /* ── HERO COLOUR OVERRIDE — cool blue instead of warm orange ── */

  /* Replace the warm orange gradient baked into _hero.scss ::before */
  .hero::before {
    background: linear-gradient(
      to bottom,
      rgba(180, 220, 255, 0.08) 0%,
      rgba(100, 170, 240, 0.18) 60%,
      rgba(60,  130, 220, 0.28) 100%
    ) !important;
  }

  /* mix-blend-mode: color shifts image hues to blue, preserving luminance.
     z-index: 0 keeps it below .hero__content (z-index: 1). */
  .hero::after {
    content: '';
    position: absolute;
    inset: 0;
    background: hsl(210, 65%, 62%);
    mix-blend-mode: color;
    z-index: 0;
    pointer-events: none;
  }

  /* ── INTRO ── */
  .sb-intro {
    padding: 52px 0 44px;
  }

  .sb-intro-body {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 24px;
  }

  .sb-sparrow {
    width: 44px;
    height: 44px;
    flex-shrink: 0;
  }

  .sb-sparrow--lg {
    width: 56px;
    height: 56px;
  }

  .sb-intro-text {
    font-size: 1rem;
    line-height: 1.75;
    color: #2e5c58;
    max-width: 580px;
  }

  .sb-intro-text p + p { margin-top: 0.9em; }

  /* ── FEATURES ── */
  .sb-features {
    padding: 48px 0;
    border-top: 1px solid #b8e0dc;
    border-bottom: 1px solid #b8e0dc;
  }

  .sb-features-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 28px 48px;
  }

  @media (max-width: 520px) {
    .sb-features-grid { grid-template-columns: 1fr; }
  }

  .sb-feature { display: flex; flex-direction: column; gap: 4px; }

  .sb-feature-label {
    font-size: 0.72rem;
    font-weight: 500;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #6a9e9a;
  }

  .sb-feature-text {
    font-size: 0.92rem;
    color: #2e5c58;
    line-height: 1.6;
  }

  /* ── SIGNUP ── */
  .sb-signup { padding: 60px 0 80px; }

  .sb-signup-heading-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    margin-bottom: 10px;
  }

  .sb-signup-heading {
    font-family: 'Space Grotesk', system-ui, sans-serif;
    font-weight: 600;
    font-size: 1.5rem;
    letter-spacing: -0.02em;
    color: #081a18;
  }

  .sb-signup-sub {
    font-size: 0.92rem;
    color: #6a9e9a;
    margin-bottom: 28px;
    line-height: 1.65;
  }

  .sb-signup-form {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }

  .sb-signup-input {
    flex: 1;
    min-width: 220px;
    padding: 10px 14px;
    font-family: 'Inter', system-ui, sans-serif;
    font-size: 0.92rem;
    color: #081a18;
    background: #ffffff;
    border: 1px solid #b8e0dc;
    border-radius: 3px;
    outline: none;
    transition: border-color 0.15s;
  }

  .sb-signup-input:focus { border-color: #00a99d; }
  .sb-signup-input::placeholder { color: #6a9e9a; }

  .sb-signup-btn {
    padding: 10px 22px;
    font-family: 'Inter', system-ui, sans-serif;
    font-size: 0.88rem;
    font-weight: 500;
    letter-spacing: 0.02em;
    color: #ffffff;
    background: #00a99d;
    border: none;
    border-radius: 3px;
    cursor: pointer;
    transition: opacity 0.15s;
    white-space: nowrap;
  }

  .sb-signup-btn:hover { opacity: 0.85; }
  .sb-signup-btn:active { opacity: 0.7; }

  .sb-signup-confirm {
    display: none;
    align-items: center;
    gap: 10px;
    padding: 12px 16px;
    background: #f0faf9;
    border: 1px solid #b8e0dc;
    border-radius: 3px;
    font-size: 0.92rem;
    color: #00a99d;
  }

  .sb-signup-confirm.visible { display: flex; }
</style>

<section class="sb-intro">
  <div class="sb-container">
    <div class="sb-intro-body">
      <div class="sb-intro-text">
        <p>Switchboard is a macOS app built by a psychologist, for psychologists. It keeps your patient records, clinical notes, and referral relationships in one place — offline, on your machine, under your control.</p>
        <p>No subscription. No cloud sync you didn't configure. No vendor with access to your patients' data.</p>
      </div>
      <img src="/assets/images/sparrow-alt.png" alt="" class="sb-sparrow sb-sparrow--lg" aria-hidden="true">
    </div>
  </div>
</section>

<section class="sb-features">
  <div class="sb-container">
    <div class="sb-features-grid">

      <div class="sb-feature">
        <span class="sb-feature-label">Privacy by design</span>
        <p class="sb-feature-text">All data lives in a local database on your Mac. Optional continuous automatic encrypted cloud backup to your chosen secure service — you decide where your data goes.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Clinical records</span>
        <p class="sb-feature-text">Structured patient files with status tracking across your full caseload: intake, waitlist, scheduled, active, and closed cases.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Progress notes</span>
        <p class="sb-feature-text">Timestamped, signable clinical notes with a full amendment and void history. RFC 3161 cryptographic timestamps tie each note to a verifiable point in time.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Audit trail</span>
        <p class="sb-feature-text">Every note action — sign, unsign, amend, void — is logged with who did it and when. Nothing is silently overwritten.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Case checklists</span>
        <p class="sb-feature-text">Customisable per-case task lists across intake, assessment, and post-assessment stages. Defined once by you to fit your workflow, applied per patient.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Referrer network</span>
        <p class="sb-feature-text">A dedicated referrer database with referral counts, contact details, and fast lookup — so you always know where your work is coming from.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Document management</span>
        <p class="sb-feature-text">Per-patient document folders organised by type, with automatic renaming when patient status changes.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Native macOS</span>
        <p class="sb-feature-text">Built for Mac. No Electron, no web wrapper. Runs fully offline. Does not phone home.</p>
      </div>

    </div>
  </div>
</section>

<section class="sb-signup" id="notify">
  <div class="sb-container">
    <div class="sb-signup-heading-row">
      <div class="sb-signup-heading">Get notified on release</div>
      <img src="/assets/images/sparrow-alt.png" alt="" class="sb-sparrow" aria-hidden="true">
    </div>
    <p class="sb-signup-sub">Switchboard is in pre-release testing. Leave your email and we'll let you know when it's available.</p>

    <form
      class="sb-signup-form"
      id="sbNotifyForm"
      action="https://formspree.io/f/xykavbwy"
      method="POST"
    >
      <input
        class="sb-signup-input"
        type="email"
        name="email"
        placeholder="your@email.com"
        required
        autocomplete="email"
      >
      <input type="hidden" name="_subject" value="Notify on Switchboard release">
      <button class="sb-signup-btn" type="submit">Notify me</button>
    </form>

    <div class="sb-signup-confirm" id="sbConfirm" role="status" aria-live="polite">
      <span>&#10003;&nbsp; You're on the list. We'll be in touch when Switchboard is ready.</span>
    </div>
  </div>
</section>

<script>
  (function () {
    var form = document.getElementById('sbNotifyForm');
    var confirm = document.getElementById('sbConfirm');
    if (!form || !confirm) return;

    form.addEventListener('submit', async function (e) {
      e.preventDefault();
      var data = new FormData(form);
      try {
        var res = await fetch(form.action, {
          method: 'POST',
          body: data,
          headers: { 'Accept': 'application/json' }
        });
        if (res.ok) {
          form.style.display = 'none';
          confirm.classList.add('visible');
        } else {
          form.submit();
        }
      } catch (_) {
        form.submit();
      }
    });
  })();
</script>
