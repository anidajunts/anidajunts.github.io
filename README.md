
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Ani Dajunts — Shopify portfolio featuring storefront customization, custom Liquid sections and responsive landing pages.">
<title>Ani Dajunts | Shopify Portfolio</title>

<style>
:root {
  --cream:#F5F0E8;
  --white:#FFFCF8;
  --brown:#2B211C;
  --taupe:#897668;
  --soft:#D6CCC2;
  --wine:#641C35;
}

* { box-sizing:border-box; }

html { scroll-behavior:smooth; }

body {
  margin:0;
  font-family:Arial,Helvetica,sans-serif;
  background:var(--cream);
  color:var(--brown);
  line-height:1.7;
}

a { color:inherit; }

.container {
  width:calc(100% - 40px);
  max-width:1120px;
  margin:auto;
}

header {
  background:var(--white);
  border-bottom:1px solid var(--soft);
}

.nav {
  min-height:85px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}

.brand {
  font-family:Georgia,serif;
  font-size:22px;
  letter-spacing:2px;
  text-decoration:none;
}

nav {
  display:flex;
  gap:25px;
  flex-wrap:wrap;
}

nav a {
  font-size:12px;
  text-transform:uppercase;
  letter-spacing:1px;
  text-decoration:none;
}

nav a:hover { color:var(--wine); }

.hero {
  text-align:center;
  padding:115px 20px 105px;
  background:linear-gradient(135deg,#F5F0E8,#E8DDD4);
}

.eyebrow {
  color:var(--taupe);
  text-transform:uppercase;
  letter-spacing:3px;
  font-size:12px;
  font-weight:bold;
}

h1,h2,h3 {
  font-family:Georgia,serif;
  font-weight:400;
  line-height:1.2;
}

h1 {
  font-size:clamp(44px,6vw,76px);
  max-width:850px;
  margin:20px auto;
}

h2 {
  font-size:clamp(32px,4vw,48px);
  margin:10px 0 25px;
}

h3 {
  font-size:27px;
  margin:10px 0;
}

.hero p {
  max-width:670px;
  margin:0 auto 30px;
  color:#6F5D52;
  font-size:17px;
}

.button {
  display:inline-block;
  background:var(--brown);
  color:white;
  padding:15px 30px;
  font-size:12px;
  font-weight:bold;
  text-transform:uppercase;
  letter-spacing:1.5px;
  text-decoration:none;
  transition:background .25s;
}

.button:hover {
  background:var(--wine);
}

section { padding:85px 0; }

.section-heading {
  text-align:center;
  max-width:720px;
  margin:0 auto 45px;
}

.section-heading p {
  color:#6F5D52;
}

.projects {
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:30px;
}

.project {
  background:var(--white);
  border:1px solid var(--soft);
  overflow:hidden;
  transition:transform .3s,box-shadow .3s;
}

.project:hover {
  transform:translateY(-5px);
  box-shadow:0 15px 35px #2B211C14;
}

.project-image {
  height:310px;
  overflow:hidden;
  background:#E8DDD4;
}

.project-image img {
  width:100%;
  height:100%;
  object-fit:cover;
  display:block;
}

.project-content {
  padding:30px;
}

.project-tag {
  font-size:11px;
  color:var(--taupe);
  text-transform:uppercase;
  letter-spacing:2px;
}

.project-content p {
  color:#6F5D52;
  font-size:14px;
}

.tags {
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  margin:22px 0;
}

.tags span {
  border:1px solid var(--soft);
  padding:6px 10px;
  font-size:11px;
}

.project-link {
  display:inline-block;
  font-size:12px;
  font-weight:bold;
  text-decoration:none;
  text-transform:uppercase;
  letter-spacing:1px;
  border-bottom:1px solid var(--wine);
  padding-bottom:5px;
}

.project-link:hover {
  color:var(--wine);
}

.about {
  background:var(--white);
}

.about-grid {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:70px;
  align-items:center;
}

.about-panel {
  background:var(--cream);
  padding:60px 45px;
  border:1px solid var(--soft);
  text-align:center;
}

.about-panel .initials {
  font-family:Georgia,serif;
  font-size:85px;
  color:var(--wine);
  line-height:1.2;
}

.about-panel p {
  font-size:12px;
  letter-spacing:2px;
  text-transform:uppercase;
  color:var(--taupe);
}

.about-text p {
  color:#6F5D52;
}

.skills {
  display:grid;
  grid-template-columns:repeat(3,minmax(0,1fr));
  gap:20px;
}

.skill {
  background:var(--white);
  border:1px solid var(--soft);
  padding:30px 25px;
}

.skill-number {
  color:var(--taupe);
  font-family:Georgia,serif;
  font-size:30px;
}

.skill h3 {
  font-size:22px;
  margin:15px 0;
}

.skill p {
  color:#6F5D52;
  font-size:14px;
}

.contact {
  text-align:center;
  background:var(--wine);
  color:white;
}

.contact h2 {
  color:white;
}

.contact p {
  max-width:620px;
  margin:0 auto 28px;
  color:#F3E3E2;
}

.contact .button {
  background:var(--white);
  color:var(--wine);
}

footer {
  background:var(--brown);
  color:#E9DFD7;
  text-align:center;
  padding:25px;
  font-size:12px;
  letter-spacing:1px;
}

@media(max-width:800px) {
  .projects,
  .about-grid {
    grid-template-columns:1fr;
  }

  .skills {
    grid-template-columns:repeat(2,minmax(0,1fr));
  }

  .about-grid { gap:30px; }

  section { padding:60px 0; }
}

@media(max-width:550px) {
  .nav {
    flex-direction:column;
    justify-content:center;
    padding:18px 0;
    gap:12px;
  }

  nav {
    justify-content:center;
    gap:17px;
  }

  .hero { padding:75px 20px; }

  .projects,
  .skills {
    grid-template-columns:1fr;
  }

  .project-image { height:240px; }

  .project-content { padding:23px; }

  .about-panel { padding:40px 20px; }

  .brand { font-size:19px; }
}
</style>
</head>

<body>

<header>
  <div class="container nav">
    <a class="brand" href="#">ANI DAJUNTS</a>
    <nav aria-label="Main navigation">
      <a href="#projects">Projects</a>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<main>

<section class="hero">
  <div class="eyebrow">
    Shopify Design & Development Portfolio
  </div>

  <h1>
    Thoughtful Digital
    Experiences.
  </h1>

  <p>
    Creating elegant Shopify storefronts,
    custom sections and conversion-focused
    landing pages with attention to detail,
    functionality and responsive design.
  </p>

  <a class="button" href="#projects">
    Explore My Work
  </a>
</section>

<section id="projects">
  <div class="container">

    <div class="section-heading">
      <div class="eyebrow">Selected Work</div>
      <h2>Featured Projects</h2>
      <p>
        A selection of Shopify projects
        created as part of my practical training.
      </p>
    </div>

    <div class="projects">

      <article class="project">
        <div class="project-image">
          <img
            src="https://images.unsplash.com/photo-1548036328-c9fa89d128fa?auto=format&amp;fit=crop&amp;w=1100&amp;q=85"
            alt="Illustrative leather handbag photograph for MONPIEL project"
            loading="lazy">
        </div>

        <div class="project-content">
          <div class="project-tag">
            Shopify Store Customization
          </div>

          <h3>MONPIEL</h3>

          <p>
            A leather accessories Shopify store
            featuring a refined visual identity,
            custom Liquid sections, multilingual
            content, product page enhancements
            and responsive layouts.
          </p>

          <div class="tags">
            <span>Shopify</span>
            <span>Custom Liquid</span>
            <span>EN / RU</span>
            <span>Responsive Design</span>
          </div>

          <a
            class="project-link"
            href="https://ani-dajunts-eh01900t.myshopify.com/"
            target="_blank"
            rel="noopener noreferrer">
            View Shopify Store →
          </a>
        </div>
      </article>

      <article class="project">
        <div class="project-image">
          <img
            src="https://cdn.shopify.com/s/files/1/0747/1693/8409/files/SPORTE.png?v=1793185488"
            alt="SPORTÉ Christmas corporate gift concept"
            loading="lazy">
        </div>

        <div class="project-content">
          <div class="project-tag">
            Shopify Landing Page
          </div>

          <h3>SPORTÉ Christmas Gifts</h3>

          <p>
            A festive corporate gifting landing
            page featuring a premium holiday
            aesthetic, promotional countdown,
            product benefits, comparison cards,
            FAQ and contact inquiry form.
          </p>

          <div class="tags">
            <span>Landing Page</span>
            <span>HTML & CSS</span>
            <span>Custom Liquid</span>
            <span>Mobile Responsive</span>
          </div>

          <a
            class="project-link"
            href="https://lw8k56k9iwc4hr9q-74716938409.shopifypreview.com"
            target="_blank"
            rel="noopener noreferrer">
            View Project Preview →
          </a>
        </div>
      </article>

    </div>
  </div>
</section>

<section id="about" class="about">
  <div class="container about-grid">

    <div class="about-panel">
      <div class="initials">AD</div>
      <h3>Ani Dajunts</h3>
      <p>Shopify & Digital Marketing</p>
    </div>

    <div class="about-text">
      <div class="eyebrow">About Me</div>

      <h2>
        Combining Creativity
        With Functionality.
      </h2>

      <p>
        I am a digital marketing professional
        expanding my expertise in Shopify
        store development and customization.
      </p>

      <p>
        My work focuses on clean design,
        intuitive user experiences and
        practical e-commerce solutions.
        I enjoy creating custom sections
        and responsive pages that balance
        visual appeal with functionality.
      </p>

      <p>
        This portfolio showcases my hands-on
        Shopify training projects and
        ongoing development journey.
      </p>
    </div>

  </div>
</section>

<section id="skills">
  <div class="container">

    <div class="section-heading">
      <div class="eyebrow">My Expertise</div>
      <h2>Skills & Tools</h2>
    </div>

    <div class="skills">

      <div class="skill">
        <div class="skill-number">01</div>
        <h3>Shopify Customization</h3>
        <p>
          Theme editing, templates,
          product pages and store layouts.
        </p>
      </div>

      <div class="skill">
        <div class="skill-number">02</div>
        <h3>Custom Liquid</h3>
        <p>
          Custom content sections,
          HTML and CSS styling.
        </p>
      </div>

      <div class="skill">
        <div class="skill-number">03</div>
        <h3>Responsive Design</h3>
        <p>
          Mobile-friendly layouts,
          navigation and readable content.
        </p>
      </div>

      <div class="skill">
        <div class="skill-number">04</div>
        <h3>Shopify Apps</h3>
        <p>
          Reviews, forms, translations
          and storefront enhancements.
        </p>
      </div>

      <div class="skill">
        <div class="skill-number">05</div>
        <h3>Landing Pages</h3>
        <p>
          Promotional pages with
          clear calls to action.
        </p>
      </div>

      <div class="skill">
        <div class="skill-number">06</div>
        <h3>Digital Marketing</h3>
        <p>
          Customer communication,
          messaging and campaign strategy.
        </p>
      </div>

    </div>
  </div>
</section>

<section id="contact" class="contact">
  <div class="container">
    <div class="eyebrow" style="color:#E7C8B3">
      Let's Connect
    </div>

    <h2>Let's Create Something Meaningful.</h2>

    <p>
      Interested in Shopify customization,
      landing pages or digital marketing?
      Explore my projects and connect
      with me through GitHub.
    </p>

    <a
      class="button"
      href="https://github.com/anidajunts"
      target="_blank"
      rel="noopener noreferrer">
      Visit My GitHub
    </a>
  </div>
</section>

</main>

<footer>
  © 2026 Ani Dajunts · Shopify Portfolio
</footer>

</body>
</html>
