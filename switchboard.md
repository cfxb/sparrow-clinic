---
layout: page
title: Switchboard — Offline Practice Management for Psychologists, Therapists and Counsellors
description: "Switchboard is a macOS practice management app and local alternative to cloud EHR platforms, built for psychologists, therapists, counsellors, and allied health practitioners in private practice. Patient records, clinical notes, and referral tracking stored on your Mac — no vendor access to your data."
hero_title: Switchboard
hero_subtitle: Clinical records software
hero_image: /assets/images/hero-sky.jpg
switchboard_schema: true
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

  /* ── FAQ ── */
  .sb-faq {
    padding: 52px 0 64px;
    border-top: 1px solid #b8e0dc;
  }

  .sb-faq-heading {
    font-family: 'Space Grotesk', system-ui, sans-serif;
    font-weight: 600;
    font-size: 1.25rem;
    letter-spacing: -0.02em;
    color: #081a18;
    margin-bottom: 32px;
  }

  .sb-faq-list { display: flex; flex-direction: column; gap: 28px; }

  .sb-faq-q {
    font-size: 0.92rem;
    font-weight: 600;
    color: #081a18;
    margin-bottom: 6px;
    line-height: 1.5;
  }

  .sb-faq-a {
    font-size: 0.92rem;
    color: #2e5c58;
    line-height: 1.7;
    margin: 0;
  }
</style>

<section class="sb-intro">
  <div class="sb-container">
    <div class="sb-intro-body">
      <div class="sb-intro-text">
        <p>Switchboard is a macOS practice management app built by a psychologist for psychologists, therapists, counsellors, and allied health practitioners in private practice. It keeps your patient records, clinical notes, and referral relationships in one place — offline, on your machine, under your control. No cloud platform required. No cloud sync you didn't configure. No vendor with access to your patients' data.</p>
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
        <p class="sb-feature-text">All data lives in a local database on your Mac. Optional continuous automatic encrypted backup to your chosen secure cloud service or an external drive — you decide where your data goes.</p>
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
        <p class="sb-feature-text">Drag and drop file organization, with optional immediate backup to keep your files safe.</p>
      </div>

      <div class="sb-feature">
        <span class="sb-feature-label">Native macOS</span>
        <p class="sb-feature-text">Built for Mac. Runs fully offline on your machine. Does not phone home.</p>
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

<section class="sb-faq">
  <div class="sb-container">
    <h2 class="sb-faq-heading">Common questions</h2>
    <div class="sb-faq-list">

      <div class="sb-faq-item">
        <p class="sb-faq-q">Why choose Switchboard?</p>
        <p class="sb-faq-a">Switchboard is designed to be inexpensive and to keep your patient data exactly where it belongs — on your own machine. Unlike cloud-based practice management platforms, there is no third-party server holding your records and no vendor with access to your patients' data. No cloud platform is required to do your work. If you want backup, you choose the service and you control where your data goes. Switchboard gives you the records management tools you need without the privacy trade-offs that come with cloud-based alternatives.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">Can I try Switchboard now?</p>
        <p class="sb-faq-a">Yes. If you would like to be part of our beta testing program, leave your email in the form above and let us know you're interested in early access.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">What is Switchboard?</p>
        <p class="sb-faq-a">Switchboard is a macOS practice management app built by a psychologist for psychologists and therapists in private practice. It keeps patient records, clinical notes, referral relationships, and case checklists in one place — stored locally on your Mac, under your control. It does not share patient data with any vendor.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">Is Switchboard designed for solo or small private practices?</p>
        <p class="sb-faq-a">Yes. Switchboard is designed specifically for independent practitioners — psychologists, therapists, counsellors, psychotherapists, social workers, and other allied health professionals running their own practice. It handles the clinical records side of practice management: patient files, progress notes, case checklists, referrer tracking, and document management.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">Where is patient data stored?</p>
        <p class="sb-faq-a">All patient data is stored in a local database on your Mac. Switchboard does not send data to any cloud service unless you explicitly configure optional encrypted backup. No vendor — including Sparrow — has access to your patient records. You retain full ownership and control of your data.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">How does Switchboard handle clinical notes and audit trails?</p>
        <p class="sb-faq-a">Progress notes are timestamped and signable, with a full amendment and void history. RFC 3161 cryptographic timestamps tie each note to a verifiable point in time. Every note action — sign, unsign, amend, void — is logged with who did it and when. Nothing is silently overwritten.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">How is Switchboard different from web-based practice management software?</p>
        <p class="sb-faq-a">Most cloud-based EHR and practice management platforms run in a browser and store data on vendor-controlled servers. Switchboard runs as a native macOS app and stores all data locally — no browser, no cloud dependency, no internet connection required to access your records. Your data stays on your machine, not on a vendor's server.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">Is Switchboard suitable for US practitioners concerned about HIPAA?</p>
        <p class="sb-faq-a">Yes. Most cloud practice management and EHR platforms require you to sign a Business Associate Agreement (BAA) with the vendor because they handle your patients' Protected Health Information (PHI) on their servers. Because Switchboard stores all data locally on your Mac, there is no third-party vendor handling your PHI — the data access concern that drives the BAA requirement doesn't arise. You remain responsible for your own device security and backup practices, which is consistent with HIPAA's requirements for covered entities.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">Is Switchboard suitable for Australian allied health practitioners?</p>
        <p class="sb-faq-a">Yes. The Australian Privacy Act 1988 and the Australian Privacy Principles (APPs) require health service providers to take reasonable steps to protect personal health information from misuse and unauthorised access. With Switchboard, patient data stays on your Mac and is not transmitted to any third-party cloud vendor unless you configure optional encrypted backup. There is no offshore data storage by default, and no vendor with access to your patients' records — which addresses the core data-handling obligations under the APPs for solo and small allied health practices.</p>
      </div>

      <div class="sb-faq-item">
        <p class="sb-faq-q">When will Switchboard be available?</p>
        <p class="sb-faq-a">Late 2026. Switchboard is currently in pre-release testing. Leave your email in the form above and we'll notify you when it's ready.</p>
      </div>

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
