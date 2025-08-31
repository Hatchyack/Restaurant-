/* styles.css - Pancho Villa Design */

:root{
  --container-max:1100px;
  --accent: #c1121f;       /* kräftiges Rot */
  --accent2: #007f5f;      /* sattes Grün */
  --bg:#fffdf8;            /* leicht warmes Weiß */
  --text:#111;
  --muted:#555;
  --radius:10px;
  --gap:16px;
  --shadow: 0 6px 18px rgba(0,0,0,0.08);
}

*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  background:var(--bg);
  color:var(--text);
  line-height:1.4;
}

/* Container */
.container{
  width:calc(100% - 32px);
  max-width:var(--container-max);
  margin:0 auto;
  padding:24px 16px;
}

/* Header */
.site-header{
  background:#fff;
  position:sticky;
  top:0;
  z-index:40;
  border-bottom:4px solid var(--accent2);
}
.logo img{display:block;}

/* Navigation */
.nav{margin-left:auto;}
.nav ul{list-style:none;margin:0;padding:0;display:flex;gap:16px;align-items:center}
.nav a{
  text-decoration:none;
  color:var(--text);
  padding:8px 12px;
  border-radius:8px;
  transition:background 0.2s;
}
.nav a:hover{background:var(--accent2);color:#fff;}
.nav-toggle{display:none;background:none;border:1px solid #ddd;padding:8px 10px;border-radius:8px;cursor:pointer}

/* Hero */
.hero{
  background:linear-gradient(135deg,var(--accent) 0%,var(--accent2) 100%);
  color:#fff;
  padding:40px 0;
}
.hero-text h1{font-size:2.5rem;margin:0 0 12px 0}
.hero-text p{margin:0 0 16px 0;color:#fdfdfd}
.cta{
  display:inline-block;
  text-decoration:none;
  padding:12px 18px;
  border-radius:8px;
  background:#fff;
  color:var(--accent);
  font-weight:600;
}

/* Menu */
.menu-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:12px}
.menu-card{background:#fff;padding:16px;border-radius:12px;box-shadow:var(--shadow);border-top:4px solid var(--accent)}
.menu-card h3{margin-top:0;color:var(--accent2)}
.menu-note{color:var(--muted);margin-top:12px}

/* Gallery */
.gallery-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px}
.gallery img{width:100%;height:180px;object-fit:cover;border-radius:8px}

/* Form */
.form{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;background:#fff;padding:16px;border-radius:12px;box-shadow:var(--shadow)}
.form label{display:flex;flex-direction:column;font-size:0.9rem;color:var(--muted)}
.form input,.form textarea{padding:10px;border-radius:8px;border:1px solid #e6e6e6}
.form-actions{grid-column:1 / -1;display:flex;gap:12px;align-items:center}
.btn{padding:10px 14px;border-radius:8px;border:0;background:var(--accent);color:#fff;cursor:pointer}
.btn.secondary{background:var(--accent2);color:#fff}

/* Contact */
.map iframe{width:100%;height:260px;border:0;border-radius:8px}

/* Footer */
.site-footer{padding:18px 0;background:#fff;border-top:4px solid var(--accent);margin-top:24px;text-align:center}
.site-footer p{margin:4px 0;color:var(--muted)}

/* Responsive */
@media(max-width:900px){
  .menu-grid{grid-template-columns:repeat(2,1fr)}
  .gallery-grid{grid-template-columns:repeat(2,1fr)}
  .form{grid-template-columns:1fr}
}
@media(max-width:700px){
  .nav{display:none}
  .nav-toggle{display:inline-block;margin-left:auto}
  .nav.open{display:block;position:absolute;right:16px;top:64px;background:#fff;padding:12px;border-radius:8px;box-shadow:var(--shadow)}
  .menu-grid{grid-template-columns:1fr}
  .gallery-grid{grid-template-columns:1fr}
}