# black-friday-bday
Birthday celebration 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Black Friday Birthday Weekend | 11/27</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-black: #070707;
      --card-bg: #111111;
      --card-border: #262626;
      --gold: #d4af37;
      --gold-light: #f3e5ab;
      --text-main: #f5f5f5;
      --text-muted: #a3a3a3;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: var(--bg-black);
      color: var(--text-main);
      font-family: 'Montserrat', sans-serif;
      line-height: 1.6;
      background-image: 
        radial-gradient(circle at 50% 0%, rgba(212, 175, 55, 0.14) 0%, transparent 55%),
        radial-gradient(circle at 85% 30%, rgba(212, 175, 55, 0.06) 0%, transparent 40%);
      min-height: 100vh;
    }

    /* Hero Section */
    header {
      text-align: center;
      padding: 4.5rem 1.5rem 3rem;
      border-bottom: 1px solid rgba(212, 175, 55, 0.25);
      max-width: 920px;
      margin: 0 auto;
    }

    .badge {
      display: inline-block;
      border: 1px solid var(--gold);
      color: var(--gold);
      padding: 0.35rem 1rem;
      font-size: 0.75rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      border-radius: 50px;
      margin-bottom: 1.25rem;
      font-weight: 600;
    }

    h1 {
      font-family: 'Cinzel', serif;
      font-size: clamp(2.2rem, 6vw, 3.8rem);
      font-weight: 800;
      letter-spacing: 0.06em;
      line-height: 1.15;
      background: linear-gradient(135deg, #ffffff 10%, var(--gold-light) 50%, var(--gold) 90%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      margin-bottom: 0.75rem;
    }

    .subtitle {
      font-size: 1.1rem;
      color: var(--text-muted);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 1.75rem;
    }

    .dress-code-banner {
      background: linear-gradient(90deg, transparent, rgba(212, 175, 55, 0.15), transparent);
      border-top: 1px solid rgba(212, 175, 55, 0.3);
      border-bottom: 1px solid rgba(212, 175, 55, 0.3);
      padding: 0.75rem 1rem;
      font-weight: 600;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      font-size: 0.9rem;
      color: var(--gold-light);
      margin-bottom: 1.75rem;
    }

    .intro-note {
      max-width: 650px;
      margin: 0 auto;
      font-size: 1rem;
      color: #e5e5e5;
      font-weight: 400;
    }

    /* Main Container */
    main {
      max-width: 920px;
      margin: 0 auto;
      padding: 3rem 1.5rem;
    }

    .section-title {
      font-family: 'Cinzel', serif;
      text-align: center;
      font-size: 1.6rem;
      color: var(--gold);
      letter-spacing: 0.1em;
      margin-bottom: 2rem;
      text-transform: uppercase;
    }

    /* Itinerary Grid */
    .events-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }

    @media (min-width: 720px) {
      .events-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    .event-card {
      background-color: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: 12px;
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: transform 0.25s ease, border-color 0.25s ease, box-shadow 0.25s ease;
      position: relative;
      overflow: hidden;
    }

    .event-card:hover {
      transform: translateY(-4px);
      border-color: rgba(212, 175, 55, 0.5);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.7);
    }

    .event-card.featured {
      border: 1px solid var(--gold);
      background: linear-gradient(160deg, #16140e 0%, #0d0d0d 100%);
    }

    .must-rsvp-tag {
      position: absolute;
      top: 1rem;
      right: 1rem;
      background-color: var(--gold);
      color: #000;
      font-size: 0.7rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      padding: 0.25rem 0.65rem;
      border-radius: 4px;
    }

    .event-date {
      color: var(--gold);
      font-weight: 700;
      font-size: 0.85rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-bottom: 0.4rem;
    }

    .event-title {
      font-family: 'Cinzel', serif;
      font-size: 1.35rem;
      font-weight: 700;
      color: #fff;
      margin-bottom: 0.85rem;
      padding-right: 4.5rem;
    }

    .event-details {
      list-style: none;
      margin-bottom: 1.5rem;
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    .event-details li {
      margin-bottom: 0.5rem;
      display: flex;
      align-items: flex-start;
      gap: 0.5rem;
    }

    .event-details strong {
      color: #e5e5e5;
      font-weight: 600;
    }

    .address-link {
      color: var(--gold-light);
      text-decoration: underline;
      text-underline-offset: 3px;
    }

    .address-link:hover {
      color: var(--gold);
    }

    /* Button Stack */
    .btn-group {
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }

    .btn-link {
      display: inline-block;
      width: 100%;
      text-align: center;
      padding: 0.8rem 1rem;
      border-radius: 6px;
      font-size: 0.82rem;
      font-weight: 600;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      text-decoration: none;
      transition: all 0.2s ease;
      cursor: pointer;
    }

    .btn-gold {
      background-color: var(--gold);
      color: #000;
      border: 1px solid var(--gold);
    }

    .btn-gold:hover {
      background-color: var(--gold-light);
    }

    .btn-outline {
      background-color: transparent;
      color: var(--gold);
      border: 1px solid rgba(212, 175, 55, 0.5);
    }

    .btn-outline:hover {
      background-color: rgba(212, 175, 55, 0.12);
      border-color: var(--gold);
    }

    /* RSVP Section */
    .rsvp-box {
      margin-top: 3.5rem;
      background-color: var(--card-bg);
      border: 1px solid rgba(212, 175, 55, 0.4);
      border-radius: 14px;
      padding: 2.5rem 1.5rem;
      text-align: center;
    }

    .rsvp-box h2 {
      font-family: 'Cinzel', serif;
      font-size: 1.7rem;
      color: var(--gold);
      margin-bottom: 0.75rem;
    }

    .rsvp-box p {
      max-width: 580px;
      margin: 0 auto 1.5rem;
      color: #d4d4d4;
      font-size: 0.96rem;
    }

    .payment-pill {
      display: inline-block;
      background: rgba(212, 175, 55, 0.12);
      border: 1px solid rgba(212, 175, 55, 0.4);
      color: var(--gold-light);
      padding: 0.55rem 1.15rem;
      border-radius: 8px;
      font-size: 0.88rem;
      font-weight: 600;
      margin-bottom: 1.5rem;
    }

    .rsvp-actions {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
      margin-bottom: 1.25rem;
    }

    .rsvp-btn {
      padding: 0.95rem 2rem;
      border-radius: 8px;
      font-weight: 700;
      font-size: 0.92rem;
      text-decoration: none;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      transition: transform 0.2s ease, opacity 0.2s ease;
    }

    .rsvp-btn:hover {
      transform: scale(1.02);
    }

    .rsvp-sms {
      background-color: var(--gold);
      color: #000;
    }

    .rsvp-call {
      background-color: #1f1f1f;
      color: #fff;
      border: 1px solid #383838;
    }

    .phone-display {
      font-size: 1.1rem;
      font-weight: 600;
      color: var(--gold-light);
      letter-spacing: 0.08em;
    }

    footer {
      text-align: center;
      padding: 2rem 1rem 3rem;
      color: var(--text-muted);
      font-size: 0.8rem;
      letter-spacing: 0.08em;
    }
  </style>
</head>
<body>

  <header>
    <div class="badge">Birthday Edition • 11/27</div>
    <h1>Black Friday<br>Birthday Weekend</h1>
    <p class="subtitle">Nov 25 – Nov 29 • Atlanta, GA 🥳</p>
    
    <div class="dress-code-banner">
      🖤 Theme &amp; Dress Code: All Black Everything 🖤
    </div>

    <p class="intro-note">
      Feel free to join me in any event that fits your schedule to celebrate me! The <strong>only</strong> one I NEED to know for sure if you’re coming is <strong>Baba’s</strong>—other than that, pull up and have some fun! 🤸🏾‍♂️
    </p>
  </header>

  <main>
    <h2 class="section-title">Weekend Lineup</h2>

    <div class="events-grid">
      
      <!-- Event 1 -->
      <article class="event-card">
        <div>
          <div class="event-date">Wednesday • 11/25</div>
          <h3 class="event-title">Belly Gang Concert &amp; El Malo</h3>
          <ul class="event-details">
            <li><span>🎤</span> <span><strong>Main Event:</strong> Belly Gang Concert</span></li>
            <li><span>🔥</span> <span><strong>Afterparty:</strong> El Malo immediately following the show</span></li>
            <li><span>📍</span> <span><strong>El Malo Address:</strong> <a href="https://maps.google.com/?q=777+Memorial+Dr+SE+Ste+A102B+Atlanta+GA+30316" target="_blank" rel="noopener" class="address-link">777 Memorial Dr SE, Ste A102B, Atlanta, GA 30316</a></span></li>
          </ul>
        </div>
        <div class="btn-group">
          <a href="https://www.ticketmaster.com/event/0E006556FAF979EA" target="_blank" rel="noopener" class="btn-link btn-gold">Belly Gang Tickets →</a>
          <a href="https://www.mashupsessions.com/" target="_blank" rel="noopener" class="btn-link btn-outline">El Malo Afterparty Info →</a>
        </div>
      </article>

      <!-- Event 2 (Featured / Must RSVP) -->
      <article class="event-card featured">
        <span class="must-rsvp-tag">Must RSVP</span>
        <div>
          <div class="event-date">Thursday • 11/26 • 10:00 PM</div>
          <h3 class="event-title">Baba’s Kitchen &amp; Grill</h3>
          <ul class="event-details">
            <li><span>💵</span> <span><strong>Cost:</strong> $55 per person (Includes Section &amp; Bottles)</span></li>
            <li><span>💳</span> <span><strong>Zelle / Apple Pay:</strong> 404-839-7539</span></li>
            <li><span>📍</span> <span><strong>Address:</strong> <a href="https://maps.google.com/?q=2184+Cheshire+Bridge+Rd+NE+Atlanta+GA+30324" target="_blank" rel="noopener" class="address-link">2184 Cheshire Bridge Rd NE, Atlanta, GA 30324</a></span></li>
            <li><span>⚠️</span> <span><strong>Note:</strong> Headcount required! Text Danielle to lock in.</span></li>
          </ul>
        </div>
        <div class="btn-group">
          <a href="sms:+14048397539?body=Hey%20Danielle!%20Count%20me%20in%20for%20Baba's%20on%2011%2F26%20($55%20pp)!" class="btn-link btn-gold">Text Danielle to RSVP →</a>
        </div>
      </article>

      <!-- Event 3 -->
      <article class="event-card">
        <div>
          <div class="event-date">Saturday • 11/28 • 9:00 AM – 2:00 PM</div>
          <h3 class="event-title">Cinnamon Toasted AM/PM Party</h3>
          <ul class="event-details">
            <li><span>💵</span> <span><strong>Cost:</strong> $35 per person</span></li>
            <li><span>📍</span> <span><strong>Location:</strong> Believe Hall</span></li>
            <li><span>🖤</span> <span><strong>Attire:</strong> All Black</span></li>
          </ul>
        </div>
        <div class="btn-group">
          <a href="https://posh.vip/e/cinnamon-toasted-thanksgiving-1?u=daniellesmith1&_t=mwhqq9fz&os=web&src=event_page" target="_blank" rel="noopener" class="btn-link btn-outline">Get Tickets on Posh →</a>
        </div>
      </article>

      <!-- Event 4 -->
      <article class="event-card">
        <div>
          <div class="event-date">Sunday • 11/29 • 7:00 PM</div>
          <h3 class="event-title">Rock Steady</h3>
          <ul class="event-details">
            <li><span>💵</span> <span><strong>Cost:</strong> FREE with RSVP before 8:00 PM</span></li>
            <li><span>📍</span> <span><strong>Address:</strong> <a href="https://maps.google.com/?q=907+Marietta+St+NW+Atlanta+GA+30318" target="_blank" rel="noopener" class="address-link">907 Marietta St NW, Atlanta, GA 30318</a></span></li>
            <li><span>🥂</span> <span><strong>Vibe:</strong> Sunday wind-down finale</span></li>
          </ul>
        </div>
        <div class="btn-group">
          <a href="https://posh.vip/e/mashup-sessions-5th-sunday" target="_blank" rel="noopener" class="btn-link btn-outline">Free RSVP on Posh →</a>
        </div>
      </article>

    </div>

    <!-- RSVP & Contact Section -->
    <section class="rsvp-box">
      <h2>RSVP &amp; Payment Info</h2>
      <p>
        Need to lock in your spot for <strong>Baba’s ($55 pp)</strong> or have questions about any of the weekend events? Reach out directly to Danielle:
      </p>
      <div class="payment-pill">
        💸 Zelle / Apple Pay for Baba’s: 404-839-7539
      </div>
      <div class="rsvp-actions">
        <a href="sms:+14048397539?body=Hey%20Danielle!%20RSVPing%20for%20the%20Black%20Friday%20Birthday%20Weekend:" class="rsvp-btn rsvp-sms">💬 Text Danielle</a>
        <a href="tel:+14048397539" class="rsvp-btn rsvp-call">📞 Call Danielle</a>
      </div>
      <div class="phone-display">404-839-7539</div>
    </section>
  </main>

  <footer>
    BLACK FRIDAY EDITION • 11/27 • WEAR ALL BLACK 🖤
  </footer>

</body>
</html>
