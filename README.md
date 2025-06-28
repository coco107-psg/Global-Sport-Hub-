# Global-Sport-Hub-<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Global Sport Hub</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin:0; padding:0;
    background: #f0f2f5;
    color: #333;
  }
  header {
    background: #0077cc;
    color: white;
    padding: 20px 10px;
    text-align: center;
  }
  nav {
    background: #005fa3;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  nav button {
    background: none;
    border: none;
    color: white;
    padding: 15px 25px;
    cursor: pointer;
    font-weight: bold;
    transition: background 0.3s;
  }
  nav button:hover, nav button.active {
    background: #004b7a;
  }
  main {
    max-width: 960px;
    margin: 20px auto;
    padding: 0 10px;
  }
  section {
    display: none;
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 8px rgba(0,0,0,0.1);
    margin-bottom: 20px;
  }
  section.active {
    display: block;
  }
  h2 {
    color: #0077cc;
    margin-bottom: 15px;
  }
  .news-item, .event-item, .club-item, .community-post {
    border-bottom: 1px solid #ddd;
    padding: 10px 0;
  }
  .news-item:last-child, .event-item:last-child, .club-item:last-child, .community-post:last-child {
    border-bottom: none;
  }
  /* Responsive */
  @media (max-width: 600px) {
    nav {
      flex-direction: column;
    }
    nav button {
      padding: 10px;
      font-size: 14px;
    }
  }
</style>
</head>
<body>

<header>
  <h1>Global Sport Hub</h1>
  <p>Le site ultime pour tout savoir sur le sport dans le monde</p>
</header>

<nav>
  <button class="active" data-target="news">Actualités</button>
  <button data-target="calendar">Calendrier</button>
  <button data-target="clubs">Clubs</button>
  <button data-target="community">Communauté</button>
</nav>

<main>
  <section id="news" class="active">
    <h2>Actualités sportives</h2>
    <div class="news-item">
      <strong>Football:</strong> Le PSG remporte le championnat de Ligue 1 2025.
    </div>
    <div class="news-item">
      <strong>Tennis:</strong> Roland-Garros accueille un record de spectateurs cette année.
    </div>
    <div class="news-item">
      <strong>Basketball:</strong> Les Lakers dominent la NBA avec une nouvelle star.
    </div>
  </section>

  <section id="calendar">
    <h2>Calendrier des événements</h2>
    <div class="event-item">
      <strong>Marathon de New York</strong> - 10 Novembre 2025
    </div>
    <div class="event-item">
      <strong>Coupe du Monde de Rugby</strong> - Septembre 2025
    </div>
    <div class="event-item">
      <strong>Finale Wimbledon</strong> - Juillet 2025
    </div>
  </section>

  <section id="clubs">
    <h2>Clubs et infrastructures</h2>
    <div class="club-item">
      <strong>Real Madrid</strong> - Stade Santiago Bernabeu, Madrid
    </div>
    <div class="club-item">
      <strong>Manchester United</strong> - Old Trafford, Manchester
    </div>
    <div class="club-item">
      <strong>Paris Saint-Germain</strong> - Parc des Princes, Paris
    </div>
  </section>

  <section id="community">
    <h2>Communauté</h2>
    <div class="community-post">
      <strong>JeanD</strong>: Quel est le meilleur club de foot européen selon vous ?
    </div>
    <div class="community-post">
      <strong>SportAddict92</strong>: Je cherche un partenaire pour jouer au tennis à Paris !
    </div>
    <div class="community-post">
      <strong>MarieL</strong>: Quel équipement me conseillez-vous pour débuter le running ?
    </div>
  </section>
</main>

<script>
  const buttons = document.querySelectorAll('nav button');
  const sections = document.querySelectorAll('main section');

  buttons.forEach(btn => {
    btn.addEventListener('click', () => {
      // Reset active buttons and sections
      buttons.forEach(b => b.classList.remove('active'));
      sections.forEach(s => s.classList.remove('active'));

      // Activate clicked button and corresponding section
      btn.classList.add('active');
      const target = btn.getAttribute('data-target');
      document.getElementById(target).classList.add('active');
    });
  });
</script>

</body>
</html>
