<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hazem | Mathematics & Data Science Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,600;0,9..144,700;1,9..144,500&family=Work+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --cream:#F6EFE4;
    --white:#FFFDFA;
    --coklat:#5B3A29;
    --coklat-tua:#2B1B14;
    --tan:#C9A27E;
    --hitam:#161110;
    --garis:#E1D3BE;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--cream);
    color:var(--coklat-tua);
    font-family:'Work Sans',sans-serif;
    font-weight:400;
    line-height:1.6;
  }
  h1,h2,h3,h4{
    font-family:'Fraunces',serif;
    font-weight:600;
    color:var(--coklat-tua);
  }
  a{color:inherit;text-decoration:none;}
  .wrap{max-width:1080px;margin:0 auto;padding:0 32px;}

  /* NAV */
  nav{
    position:sticky;top:0;z-index:50;
    background:rgba(246,239,228,0.9);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--garis);
  }
  nav .wrap{display:flex;justify-content:space-between;align-items:center;height:72px;}
  .brand{font-family:'Fraunces',serif;font-weight:700;font-size:20px;letter-spacing:0.5px;}
  .navlinks{display:flex;gap:32px;font-size:14px;letter-spacing:0.3px;}
  .navlinks a{opacity:0.75;transition:opacity .2s;}
  .navlinks a:hover{opacity:1;}

  /* HERO */
  .hero{
    position:relative;
    min-height:88vh;
    display:flex;
    align-items:center;
    overflow:hidden;
    background:linear-gradient(180deg,var(--cream) 0%, var(--white) 100%);
  }
  .horse-bg{
    position:absolute;
    right:-8%;
    bottom:-4%;
    width:70%;
    max-width:820px;
    opacity:0.94;
    pointer-events:none;
  }
  .horse-bg svg{width:100%;height:auto;display:block;}
  .hero-overlay{
    position:absolute;inset:0;
    background:linear-gradient(90deg, var(--cream) 30%, rgba(246,239,228,0.15) 62%, rgba(246,239,228,0) 100%);
    pointer-events:none;
  }
  .hero-content{position:relative;z-index:2;max-width:560px;}
  .eyebrow{
    font-size:13px;letter-spacing:2px;text-transform:uppercase;
    color:var(--coklat);font-weight:500;margin-bottom:18px;
    display:flex;align-items:center;gap:10px;
  }
  .eyebrow::before{content:"";width:28px;height:1px;background:var(--coklat);display:inline-block;}
  .hero h1{
    font-size:clamp(38px,6vw,58px);
    line-height:1.08;
    margin-bottom:20px;
  }
  .hero h1 em{font-style:italic;color:var(--coklat);}
  .hero p.lede{
    font-size:17px;color:#4a372c;max-width:460px;margin-bottom:32px;
  }
  .cta-row{display:flex;gap:16px;flex-wrap:wrap;}
  .btn{
    display:inline-block;padding:14px 28px;font-size:14px;letter-spacing:0.3px;
    border-radius:2px;transition:all .2s ease;font-weight:500;
  }
  .btn-solid{background:var(--coklat-tua);color:var(--white);}
  .btn-solid:hover{background:var(--hitam);}
  .btn-outline{border:1px solid var(--coklat-tua);color:var(--coklat-tua);}
  .btn-outline:hover{background:var(--coklat-tua);color:var(--white);}

  /* SECTION GENERIC */
  section{padding:96px 0;}
  .section-head{margin-bottom:48px;max-width:600px;}
  .section-head .eyebrow{margin-bottom:10px;}
  .section-head h2{font-size:clamp(28px,4vw,38px);}

  /* ABOUT */
  .about-grid{display:grid;grid-template-columns:1.1fr 0.9fr;gap:64px;align-items:start;}
  .about-grid p{color:#4a372c;margin-bottom:16px;font-size:15.5px;}
  .facts{display:flex;flex-direction:column;gap:24px;border-left:2px solid var(--tan);padding-left:24px;}
  .fact-label{font-size:12px;text-transform:uppercase;letter-spacing:1.5px;color:var(--coklat);margin-bottom:4px;}
  .fact-value{font-family:'Fraunces',serif;font-size:19px;color:var(--coklat-tua);}

  /* SKILLS */
  .skills-band{background:var(--coklat-tua);color:var(--cream);}
  .skills-band h2{color:var(--cream);}
  .skills-band .eyebrow{color:var(--tan);}
  .skills-band .eyebrow::before{background:var(--tan);}
  .skill-cols{display:grid;grid-template-columns:1fr 1fr;gap:48px;}
  .skill-list{list-style:none;}
  .skill-list li{
    padding:14px 0;border-bottom:1px solid rgba(246,239,228,0.15);
    display:flex;justify-content:space-between;font-size:15px;
  }
  .skill-list li span.tag{color:var(--tan);font-size:12px;letter-spacing:1px;text-transform:uppercase;}

  /* PROJECTS */
  .proj-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:28px;}
  .proj-card{
    background:var(--white);border:1px solid var(--garis);padding:32px;
    transition:transform .25s ease, box-shadow .25s ease;
  }
  .proj-card:hover{transform:translateY(-4px);box-shadow:0 16px 32px rgba(43,27,20,0.08);}
  .proj-num{font-family:'Fraunces',serif;font-size:13px;color:var(--tan);margin-bottom:12px;letter-spacing:1px;}
  .proj-card h3{font-size:21px;margin-bottom:10px;}
  .proj-card p{font-size:14.5px;color:#4a372c;margin-bottom:16px;}
  .proj-link{font-size:13px;font-weight:500;color:var(--coklat);border-bottom:1px solid var(--coklat);padding-bottom:2px;}

  /* CONTACT */
  .contact-band{
    background:var(--coklat-tua);
    color:var(--cream);
    text-align:center;
  }
  .contact-band h2{color:var(--cream);font-size:clamp(30px,5vw,44px);margin-bottom:20px;}
  .contact-band p{color:var(--tan);max-width:480px;margin:0 auto 36px;}
  .contact-links{display:flex;justify-content:center;gap:28px;flex-wrap:wrap;font-size:14px;}
  .contact-links a{border-bottom:1px solid rgba(246,239,228,0.4);padding-bottom:3px;}
  .contact-links a:hover{border-color:var(--tan);color:var(--tan);}

  footer{padding:28px 0;text-align:center;font-size:12.5px;color:#8a7360;}

  @media(max-width:820px){
    .navlinks{display:none;}
    .about-grid,.skill-cols,.proj-grid{grid-template-columns:1fr;}
    .horse-bg{width:100%;right:-10%;opacity:0.5;}
    .hero-overlay{background:linear-gradient(180deg, var(--cream) 55%, rgba(246,239,228,0.2) 100%);}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="brand">HAZEM</div>
    <div class="navlinks">
      <a href="#about">Tentang</a>
      <a href="#skills">Keahlian</a>
      <a href="#projects">Proyek</a>
      <a href="#contact">Kontak</a>
    </div>
  </div>
</nav>

<section class="hero">
  <div class="horse-bg" aria-hidden="true">
    <svg viewBox="0 0 800 600" xmlns="http://www.w3.org/2000/svg">
      <path fill="#161110" d="M120 560c-6-18 4-36 22-44 30-13 46-38 50-70 3-24-2-49-14-73-16-32-18-66-4-96 20-42 62-66 92-100 18-21 26-47 24-76-2-27-16-52-12-80 4-30 26-54 54-66 24-10 50-9 74 2 30 14 48 42 66 68 16 24 32 49 58 63 22 12 48 14 70 26 26 14 42 40 46 69 3 20-2 41-14 58-16 22-42 33-68 36-22 3-46-1-64-14-14-10-24-25-38-35-10-7-22-11-34-12-2 22 4 45 18 62 16 20 40 31 52 54 10 20 8 44-4 62-14 22-38 34-63 38-8 26 2 53 22 70 16 14 38 20 46 40 6 16 0 35-14 45-16 12-38 12-56 4-20-9-34-27-52-39-14-10-31-15-48-16-4 20 2 41 16 56 12 13 30 19 38 35 7 14 3 32-9 42-14 12-33 13-49 5-22-11-34-33-56-45-16-9-35-11-53-8-2 20 6 40 22 53 14 12 33 15 44 30 9 12 8 29-2 40-11 13-30 15-46 8-20-9-32-29-52-38-14-6-30-6-44-1-1 16 5 32 17 43 10 9 24 13 31 25 6 11 3 26-7 34-11 9-27 9-40 2-8-4-14-11-22-14z"/>
      <path fill="#161110" d="M300 250c-8 20-6 44 6 62 4-24 0-49-6-62z" opacity="0.9"/>
      <ellipse cx="120" cy="540" rx="60" ry="8" fill="#2B1B14" opacity="0.25"/>
    </svg>
  </div>
  <div class="hero-overlay"></div>
  <div class="wrap">
    <div class="hero-content">
      <div class="eyebrow">Mathematics & Data Science</div>
      <h1>Menemukan <em>pola</em>,<br>menyusun <em>keputusan</em>.</h1>
      <p class="lede">
        Saya Hazem — lulusan Matematika dan Sains Data dari Universitas Andalas,
        fokus pada analisis, geometri, dan data yang berbicara. Setiap angka
        punya arah, tugas saya menemukannya.
      </p>
      <div class="cta-row">
        <a href="#projects" class="btn btn-solid">Lihat Proyek</a>
        <a href="#contact" class="btn btn-outline">Hubungi Saya</a>
      </div>
    </div>
  </div>
</section>

<section id="about">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">Tentang Saya</div>
      <h2>Dari ruang kuliah ke lembar data</h2>
    </div>
    <div class="about-grid">
      <div>
        <p>
          Saya lulusan program studi Matematika dan Sains Data, Universitas Andalas,
          dengan konsentrasi Analisis dan Geometri. Skripsi saya membahas kinematika
          gerak sliding-rolling antar permukaan reguler menggunakan pendekatan Darboux
          frame dan adjoint, dilengkapi simulasi numerik dengan MATLAB.
        </p>
        <p>
          Latar belakang akademik saya mencakup analisis real, statistika matematika,
          metode numerik, dan geometri diferensial — fondasi yang saya bawa ke dunia
          data: berpikir terstruktur, teliti terhadap detail, dan terbiasa memvalidasi
          setiap kesimpulan.
        </p>
        <p>
          Saat ini saya membuka diri untuk peran di bidang data analytics, perbankan,
          business development, finance, maupun pengajaran.
        </p>
      </div>
      <div class="facts">
        <div>
          <div class="fact-label">Lokasi</div>
          <div class="fact-value">Padang, Sumatera Barat</div>
        </div>
        <div>
          <div class="fact-label">Pendidikan</div>
          <div class="fact-value">S1 Matematika & Sains Data — Universitas Andalas</div>
        </div>
        <div>
          <div class="fact-label">IPK</div>
          <div class="fact-value">3.48 / 4.00</div>
        </div>
        <div>
          <div class="fact-label">Status</div>
          <div class="fact-value">Fresh Graduate</div>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="skills-band" id="skills">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">Keahlian</div>
      <h2>Alat & pendekatan yang saya pakai</h2>
    </div>
    <div class="skill-cols">
      <ul class="skill-list">
        <li>Python <span class="tag">Analisis Data</span></li>
        <li>MATLAB <span class="tag">Simulasi Numerik</span></li>
        <li>SQL (MySQL Workbench) <span class="tag">Query & Database</span></li>
        <li>R <span class="tag">Statistika</span></li>
      </ul>
      <ul class="skill-list">
        <li>Minitab <span class="tag">Statistical Analysis</span></li>
        <li>Google Sheets <span class="tag">Data Wrangling</span></li>
        <li>Microsoft Excel <span class="tag">Pivot & Reporting</span></li>
        <li>LaTeX <span class="tag">Scientific Writing</span></li>
      </ul>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-head">
      <div class="eyebrow">Proyek</div>
      <h2>Beberapa hal yang sudah saya kerjakan</h2>
    </div>
    <div class="proj-grid">
      <div class="proj-card">
        <div class="proj-num">01</div>
        <h3>Kinematika Sliding-Rolling — Darboux Frame</h3>
        <p>Penelitian skripsi tentang gerak sliding-rolling antar permukaan reguler
        menggunakan pendekatan Darboux frame dan adjoint, divalidasi dengan simulasi MATLAB.</p>
        <a href="#" class="proj-link">Lihat detail →</a>
      </div>
      <div class="proj-card">
        <div class="proj-num">02</div>
        <h3>Dashboard Admisi Unand 2025</h3>
        <p>Dashboard interaktif Tableau Public dari data admisi 59 program studi:
        proporsi peminat per fakultas dan tingkat keketatan tiap prodi.</p>
        <a href="#" class="proj-link">Lihat detail →</a>
      </div>
      <div class="proj-card">
        <div class="proj-num">03</div>
        <h3>Analisis Indeks Saham</h3>
        <p>Proyek analisis data di Google Sheets untuk membangun dan mengkaji
        pergerakan indeks pasar saham.</p>
        <a href="#" class="proj-link">Lihat detail →</a>
      </div>
      <div class="proj-card">
        <div class="proj-num">04</div>
        <h3>Latihan SQL — MySQL Workbench</h3>
        <p>Rangkaian studi kasus query dan manajemen database menggunakan
        MySQL Workbench untuk memperkuat kemampuan data wrangling.</p>
        <a href="#" class="proj-link">Lihat detail →</a>
      </div>
    </div>
  </div>
</section>

<section class="contact-band" id="contact">
  <div class="wrap">
    <h2>Mari terhubung</h2>
    <p>Terbuka untuk peluang di bidang data analytics, perbankan, business development,
    finance, maupun pengajaran.</p>
    <div class="contact-links">
      <a href="mailto:nama@email.com">Email</a>
      <a href="https://linkedin.com/in/username" target="_blank">LinkedIn</a>
      <a href="https://github.com/hazemhawari22" target="_blank">GitHub</a>
      <a href="https://wa.me/62xxxxxxxxxx" target="_blank">WhatsApp</a>
    </div>
  </div>
</section>

<footer>
  © 2026 Hazem. Dibangun dengan HTML, CSS, dan sedikit geometri.
</footer>

</body>
</html>
