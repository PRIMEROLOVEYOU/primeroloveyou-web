<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PRIMERO LOVE YOU | Trilogía oficial</title>
  <meta name="description" content="Web oficial de PRIMERO LOVE YOU de Christian C. D'Rosoy. Capítulos gratuitos, galería, personajes, vídeo, reseñas y compra en Amazon y Málaga." />
  <meta name="author" content="Christian C. D'Rosoy" />
  <meta name="theme-color" content="#0b0b12" />
  <meta property="og:title" content="PRIMERO LOVE YOU | El hijo del mañana" />
  <meta property="og:description" content="Romance, ciencia ficción y suspenso emocional. Lee los primeros capítulos gratis." />
  <meta property="og:type" content="website" />
  <meta name="twitter:card" content="summary_large_image" />
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4.1.7"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
  <style>
    html { scroll-behavior: smooth; }
    body { font-family: Inter, system-ui, sans-serif; background: #07070b; color: #f4f4f5; }
    .glass { backdrop-filter: blur(16px); background: rgba(255,255,255,.06); }
    .hero-mask { background: linear-gradient(180deg, rgba(7,7,11,.10) 0%, rgba(7,7,11,.68) 50%, rgba(7,7,11,1) 100%); }
    .gold-text { background: linear-gradient(90deg,#f7e6a1,#d9b96e,#f9efd1); -webkit-background-clip:text; background-clip:text; color: transparent; }
    .chapter { font-family: Georgia, 'Times New Roman', serif; font-size: 1.04rem; line-height: 1.96; color: #d4d4d8; text-align: justify; hyphens: auto; }
    .chapter p + p { margin-top: 1rem; }
    .loc { font-size:.78rem; letter-spacing:.14em; text-transform:uppercase; color:#a1a1aa; border-left:2px solid #d9b96e; padding-left:.75rem; margin-bottom:1.2rem; }
    .ring { box-shadow: 0 0 0 1px rgba(255,255,255,.08), 0 16px 60px rgba(0,0,0,.35); }
    #malaga-map { min-height: 420px; }
    .map-card { transition: transform .18s ease, border-color .18s ease, background .18s ease; }
    .map-card:hover { transform: translateY(-2px); }
    .map-card.active { border-color: rgba(251,191,36,.7); background: rgba(251,191,36,.08); }
    #mobile-menu { display:none; }
    #mobile-menu.open { display:flex; }
  </style>
</head>
<body class="selection:bg-amber-300 selection:text-black">

  <header class="fixed top-0 left-0 right-0 z-50 border-b border-white/10 bg-[#09090f]/82 backdrop-blur-xl">
    <div class="max-w-7xl mx-auto px-4 md:px-6 h-16 flex items-center justify-between gap-4">
      <a href="#inicio" class="flex items-center gap-3 shrink-0">
        <div class="w-9 h-9 rounded-full border border-amber-300/35 bg-white/5 flex items-center justify-center text-amber-300 text-lg">✦</div>
        <div class="hidden sm:block">
          <p class="text-sm font-semibold tracking-wide">PRIMERO LOVE YOU</p>
          <p class="text-[10px] uppercase tracking-[0.3em] text-zinc-400">Trilogía oficial</p>
        </div>
      </a>
      <nav class="hidden lg:flex items-center gap-4 text-sm text-zinc-300">
        <a href="#autor" class="hover:text-white transition-colors">Autor</a>
        <a href="#sinopsis" class="hover:text-white transition-colors">Sinopsis</a>
        <a href="#novela" class="hover:text-white transition-colors">La novela</a>
        <a href="#malaga-en-la-novela" class="hover:text-white transition-colors">Málaga en la novela</a>
        <a href="#leer" class="hover:text-white transition-colors">Leer gratis</a>
        <a href="#galeria" class="hover:text-white transition-colors">Galería</a>
        <a href="#personajes" class="hover:text-white transition-colors">Personajes</a>
        <a href="#video" class="hover:text-white transition-colors">Vídeo</a>
        <a href="#resenas" class="inline-flex items-center gap-1.5 rounded-full border border-white/15 bg-white/5 px-3 py-1.5 text-zinc-100 hover:bg-white/10 transition-colors">✦ Reseñas</a>
        <a href="#contacto" class="hover:text-white transition-colors">Contacto</a>
      </nav>
      <div class="flex items-center gap-3">
        <a href="https://www.amazon.es/dp/B0H12QX4HW" target="_blank" rel="noreferrer" class="hidden md:inline-flex items-center gap-2 rounded-full bg-gradient-to-r from-amber-300 to-amber-200 px-4 py-2 text-sm font-semibold text-black hover:from-amber-200 hover:to-amber-100 transition-colors">Comprar</a>
        <button id="menu-btn" class="lg:hidden w-10 h-10 rounded-full border border-white/15 bg-white/5 flex items-center justify-center text-white" onclick="document.getElementById('mobile-menu').classList.toggle('open')">☰</button>
      </div>
    </div>
    <div id="mobile-menu" class="lg:hidden flex-col border-t border-white/10 bg-[#09090f]/96 px-4 py-4 gap-3 text-sm text-zinc-300">
      <a href="#autor" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Autor</a>
      <a href="#sinopsis" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Sinopsis</a>
      <a href="#novela" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">La novela</a>
      <a href="#malaga-en-la-novela" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Málaga en la novela</a>
      <a href="#leer" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Leer gratis</a>
      <a href="#galeria" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Galería</a>
      <a href="#personajes" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Personajes</a>
      <a href="#video" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Vídeo</a>
      <a href="#resenas" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">✦ Reseñas</a>
      <a href="#contacto" onclick="document.getElementById('mobile-menu').classList.remove('open')" class="hover:text-white">Contacto</a>
    </div>
  </header>

  <main class="pt-16">
    <section id="inicio" class="relative min-h-[100svh] flex items-end">
      <img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_portada.png?token=NmuhNXnye1ivFgOzAk6VXJEj36koM2RTZ8vUcM2Ny9Y&exp=1783982841" alt="Portada PRIMERO LOVE YOU" class="absolute inset-0 h-full w-full object-cover" />
      <div class="absolute inset-0 hero-mask"></div>
      <div class="relative max-w-7xl mx-auto w-full px-4 md:px-6 py-20 md:py-24">
        <div class="max-w-4xl">
          <p class="text-[11px] md:text-xs uppercase tracking-[0.4em] text-amber-200/85 mb-5">Web oficial · Libro I · Experiencia cinematográfica</p>
          <h1 class="text-4xl sm:text-5xl md:text-7xl font-semibold leading-[0.95] tracking-tight text-white">PRIMERO LOVE YOU<span class="block gold-text mt-2">El hijo del mañana</span></h1>
          <div class="mt-7 max-w-3xl glass rounded-3xl border border-white/10 p-6 md:p-8 ring">
            <p class="text-xl md:text-3xl leading-tight text-white font-medium">«Echar de menos a alguien que no conoces es una forma de locura que no tiene diagnóstico.»</p>
          </div>
          <div class="mt-8 flex flex-col sm:flex-row gap-3">
            <a href="#leer" class="inline-flex items-center justify-center gap-2 rounded-full bg-white px-6 py-3 font-semibold text-black hover:bg-zinc-100 transition-colors">Leer capítulos gratis</a>
            <a href="https://www.amazon.es/dp/B0H12QX4HW" target="_blank" rel="noreferrer" class="inline-flex items-center justify-center gap-2 rounded-full border border-white/20 bg-white/8 px-6 py-3 font-semibold text-white hover:bg-white/14 transition-colors">Comprar en Amazon</a>
          </div>
        </div>
      </div>
    </section>

    <section id="autor" class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28">
      <div class="grid lg:grid-cols-[0.9fr,1.1fr] gap-10 md:gap-14 items-center">
        <div><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_autor.jpg?token=1TECubNcVMkTOnEzZ0sJpwRheAcSHHcj_U3k6mfR6J8&exp=1783982841" alt="Christian C. D'Rosoy" class="w-full max-w-md mx-auto rounded-[2rem] object-cover border border-white/10 shadow-2xl shadow-black/30" loading="lazy" /></div>
        <div>
          <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Sobre el autor</p>
          <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Christian C. D'Rosoy</h2>
          <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed">Una voz narrativa con identidad propia, sensibilidad contemporánea y una forma de contar que mezcla emoción, tensión, misterio y mirada cinematográfica.</p>
        </div>
      </div>
    </section>

    <section id="sinopsis" class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28 scroll-mt-24 relative">
      <div class="max-w-4xl mx-auto text-center">
        <p class="text-[11px] tracking-[0.42em] uppercase text-amber-300/80 mb-3">Sinopsis</p>
      </div>

      <div class="mt-8 grid md:grid-cols-2 gap-5 items-start">
        <figure class="overflow-hidden rounded-[1.9rem] border border-white/10 bg-black/20 shadow-2xl shadow-black/25 ring">
          <img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_sipnosis_(1?token=vrTW6-h6Vrds1i_NpNRfCEIZRaZhX5FMUcn1KXGeyjw&exp=1783982841).png" alt="Málaga también es ficción" class="block w-full h-[22rem] md:h-[26rem] object-cover" loading="eager" decoding="async" />
          <figcaption class="px-5 py-4 text-sm tracking-wide uppercase text-amber-200/90 border-t border-white/10 bg-black/35">Málaga también es ficción</figcaption>
        </figure>
        <figure class="overflow-hidden rounded-[1.9rem] border border-white/10 bg-black/20 shadow-2xl shadow-black/25 ring">
          <img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_sipnosis_(2?token=CMYOThymB4EhRTxZDrhvkf2jlSjr0Lsa4JCKd6GwJ-Q&exp=1783982841).png" alt="¿Quién es CC2?" class="block w-full h-[22rem] md:h-[26rem] object-cover" loading="eager" decoding="async" />
          <figcaption class="px-5 py-4 text-sm tracking-wide uppercase text-amber-200/90 border-t border-white/10 bg-black/35">¿Quién es CC2?</figcaption>
        </figure>
      </div>

      <div class="mt-8 rounded-[2.15rem] border border-amber-300/18 bg-[linear-gradient(180deg,rgba(255,255,255,.055),rgba(255,255,255,.03))] p-6 md:p-10 ring shadow-2xl shadow-black/20">
        <div class="mx-auto max-w-3xl chapter text-left text-zinc-300">
          <p class="text-xl md:text-2xl font-semibold leading-tight text-white mb-6">¿Qué harías si un niño desconocido te abrazara llorando... y te llamara papá?</p>
          <p class="text-xl md:text-2xl font-semibold leading-tight text-white mb-6">¿Y si supiera cosas sobre tu vida que todavía no han ocurrido?</p>
          <p class="text-xl md:text-2xl font-semibold leading-tight text-white mb-6">¿Y si el amor de tu vida ya hubiera vivido esta historia antes que tú?</p>
        </div>
      </div>
    </section>

    <section id="novela" class="border-y border-white/10 bg-white/[0.03]">
      <div class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28 grid lg:grid-cols-[0.9fr,1.1fr] gap-12 items-center">
        <div><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_inicio_con_una_imagen_de_portada_a_pantalla_completa..jpg.jpg?token=Wy8q3vbSQ0ExpRomySg4R0S7Tj43kuapTkZOLXHDy2k&exp=1783982841" alt="Libro I" class="w-full rounded-[2rem] object-cover border border-white/10 shadow-2xl shadow-black/30" loading="lazy" /></div>
        <div>
          <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">La novela</p>
          <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Libro I — El hijo del mañana</h2>
          <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed">¿Qué harías si un niño apareciera en tu vida asegurando ser tu hijo… y lo más aterrador fuera descubrir que dice la verdad?</p>
        </div>
      </div>
    </section>

    <section id="malaga-en-la-novela" class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28 scroll-mt-24">
      <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Mapa interactivo</p>
      <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Málaga en la novela</h2>
      <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed max-w-3xl">Lugares confirmados por el manuscrito y puntos aproximados para recorrer el universo de <strong>PRIMERO LOVE YOU</strong>. Pulsa cualquier tarjeta para centrar el mapa y abrir su marcador.</p>

      <div class="mt-10 grid xl:grid-cols-[1.3fr,0.7fr] gap-6 items-start">
        <div class="rounded-[2rem] overflow-hidden border border-white/10 bg-black/30 ring shadow-2xl shadow-black/30">
          <div id="malaga-map" class="h-[420px] md:h-[560px]"></div>
        </div>
        <aside class="rounded-[2rem] border border-white/10 bg-white/[0.04] p-5 md:p-6 ring">
          <div class="flex items-center justify-between gap-3 mb-4">
            <div>
              <p class="text-[11px] tracking-[0.35em] uppercase text-amber-200/80">Lugares destacados</p>
              <h3 class="mt-2 text-2xl font-semibold text-white">Pincha y explora</h3>
            </div>
          </div>
          <div id="malaga-places" class="grid gap-3"></div>
        </aside>
      </div>
    </section>

    <section id="leer" class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28">
      <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Leer gratis</p>
      <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Dedicatoria, prólogo y capítulos 1 al 6</h2>
      <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed max-w-3xl">Formato editorial completo. Lee los primeros capítulos de la novela directamente aquí.</p>

      <div class="space-y-10 mt-10">
        <article id="prologo" class="scroll-mt-24 rounded-[2rem] overflow-hidden border border-white/10 ring">
          <div class="px-6 md:px-10 py-6 bg-gradient-to-r from-black/70 to-zinc-900/70 border-b border-white/10">
            <span class="inline-flex rounded-full border border-amber-300/30 bg-amber-300/10 px-3 py-1 text-xs uppercase tracking-[0.25em] text-amber-200">Prólogo</span>
            <h3 class="mt-3 text-2xl md:text-3xl font-semibold text-white">Prólogo</h3>
          </div>
          <div class="bg-[#0d0d15] px-6 md:px-14 py-12 md:py-16">
            <div class="max-w-2xl mx-auto chapter">
              <p>«Echar de menos a alguien que no conoces es una forma de locura que no tiene diagnóstico». —CC</p>
              <p>Hay ausencias que no dejan fotografías. No tienen fecha ni entierro. Y, sin embargo, pesan más que los muertos con nombre.</p>
            </div>
          </div>
        </article>

        <article id="cap1" class="scroll-mt-24 rounded-[2rem] overflow-hidden border border-white/10 ring">
          <div class="px-6 md:px-10 py-6 bg-gradient-to-r from-black/70 to-zinc-900/70 border-b border-white/10">
            <span class="inline-flex rounded-full border border-amber-300/30 bg-amber-300/10 px-3 py-1 text-xs uppercase tracking-[0.25em] text-amber-200">Capítulo 1</span>
            <h3 class="mt-3 text-2xl md:text-3xl font-semibold text-white">Todavía no ha pasado</h3>
            <p class="mt-2 loc">Lunes · 08:15 h · Calle La Unión · Málaga · 2026</p>
          </div>
          <div class="bg-[#0d0d15] px-6 md:px-14 py-12 md:py-16">
            <div class="max-w-2xl mx-auto chapter">
              <p>Hay exactamente dos momentos en la vida de todo hombre en los que el tiempo se detiene de verdad: cuando alguien te dice que vas a ser padre y cuando te lo reclama un niño al que nunca has visto.</p>
            </div>
          </div>
        </article>
      </div>
    </section>

    <section id="galeria" class="border-y border-white/10 bg-white/[0.03]">
      <div class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28">
        <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Galería</p>
        <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Presentación del libro</h2>
        <div class="grid grid-cols-2 lg:grid-cols-4 gap-4 md:gap-5 mt-12">
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-1.jpg.jpeg?token=rPqCkHOx04ekIXlZcr4r_XPHva41-8BitZfXds3YKXI&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-1.jpg.jpeg?token=rPqCkHOx04ekIXlZcr4r_XPHva41-8BitZfXds3YKXI&exp=1783982841" alt="Presentación 1" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-2.jpg.jpg?token=jDzOf7zPQcP2edeAdE5aKleNpHzoiw8jYDCjK6HPMMw&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-2.jpg.jpg?token=jDzOf7zPQcP2edeAdE5aKleNpHzoiw8jYDCjK6HPMMw&exp=1783982841" alt="Presentación 2" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-3.jpg.jpg?token=7Iq46Zojk5183uxugRYXBg1k9kpMJGbTnKxKdKTTqwI&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-3.jpg.jpg?token=7Iq46Zojk5183uxugRYXBg1k9kpMJGbTnKxKdKTTqwI&exp=1783982841" alt="Presentación 3" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria4_.jpg.jpeg?token=OwsDNZIBKXeNMizopFEi7d6K4mNyPBghodOBTRJhN5I&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria4_.jpg.jpeg?token=OwsDNZIBKXeNMizopFEi7d6K4mNyPBghodOBTRJhN5I&exp=1783982841" alt="Presentación 4" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-5.jpg.jpeg?token=suQesx09vE5Di6BlRr8HuIzLn_IG2DNFy9njnRxO1dg&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-5.jpg.jpeg?token=suQesx09vE5Di6BlRr8HuIzLn_IG2DNFy9njnRxO1dg&exp=1783982841" alt="Presentación 5" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-6.jpg.jpg?token=oYd7mHQYOsaSrec9l9SNHYs3JGuTqxNnVzF86sis3VM&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-6.jpg.jpg?token=oYd7mHQYOsaSrec9l9SNHYs3JGuTqxNnVzF86sis3VM&exp=1783982841" alt="Presentación 6" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
          <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-7.jpg.jpeg?token=lD2tmKbgs2R-z8HHB8kQbhc94B4NKLLWXVtEdw1zi0g&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_galeria-7.jpg.jpeg?token=lD2tmKbgs2R-z8HHB8kQbhc94B4NKLLWXVtEdw1zi0g&exp=1783982841" alt="Presentación 7" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        </div>
      </div>
    </section>

    <section id="personajes" class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28">
      <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Personajes</p>
      <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Así podría verse el universo humano de la novela</h2>
      <div class="grid grid-cols-2 lg:grid-cols-4 gap-4 md:gap-5 mt-12">
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-01.jpg?token=hFf8W-M-d1S1n7MVcNEnxtdEh4nLSQDJZ8P2hLmFCNY&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-01.jpg?token=hFf8W-M-d1S1n7MVcNEnxtdEh4nLSQDJZ8P2hLmFCNY&exp=1783982841" alt="Personaje 1" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-1.jpg.jpg?token=UdwMeVygKnYKwGgkPnHLII9AgYUs9RiBOT6if4sH0Xo&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-1.jpg.jpg?token=UdwMeVygKnYKwGgkPnHLII9AgYUs9RiBOT6if4sH0Xo&exp=1783982841" alt="Personaje 2" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-2.jpg.jpg?token=N8fixiPA-MbXJeVjpZkfb59FPOIbHi22Pau6s4NFW1w&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-2.jpg.jpg?token=N8fixiPA-MbXJeVjpZkfb59FPOIbHi22Pau6s4NFW1w&exp=1783982841" alt="Personaje 3" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-3.jpg.jpg?token=9T6NE8ccmnrtHQVeqHmRxaAA_6JP5zIjRLL7r4_bQIs&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-3.jpg.jpg?token=9T6NE8ccmnrtHQVeqHmRxaAA_6JP5zIjRLL7r4_bQIs&exp=1783982841" alt="Personaje 4" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-4.jpg.jpg?token=hEFJICpHlYOIRZcT3oVOISqa5lr4koNDdJ8oHU_avfc&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-4.jpg.jpg?token=hEFJICpHlYOIRZcT3oVOISqa5lr4koNDdJ8oHU_avfc&exp=1783982841" alt="Personaje 5" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-5.jpg.jpg?token=d8BxxAhMvs_yezWVDy8syIDaquanMNbREVLhA5dkjrs&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-5.jpg.jpg?token=d8BxxAhMvs_yezWVDy8syIDaquanMNbREVLhA5dkjrs&exp=1783982841" alt="Personaje 6" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-6.jpg.png?token=2MzdvZ8VZIbNS42EiU3zXWE3sT0Yir6mALVMj7D6DvU&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-6.jpg.png?token=2MzdvZ8VZIbNS42EiU3zXWE3sT0Yir6mALVMj7D6DvU&exp=1783982841" alt="Personaje 7" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-8.jpg.jpg?token=mP2pg5dqSlZmdnidT5hrXf9dFEDJ0k7hLPb5B3BxA70&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-8.jpg.jpg?token=mP2pg5dqSlZmdnidT5hrXf9dFEDJ0k7hLPb5B3BxA70&exp=1783982841" alt="Personaje 8" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-9.jpg.jpg?token=8GiAIjyIi2_QxicbkppguPa9M_3ZbTfgHZqOc3Qw_h8&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-9.jpg.jpg?token=8GiAIjyIi2_QxicbkppguPa9M_3ZbTfgHZqOc3Qw_h8&exp=1783982841" alt="Personaje 9" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-10.png?token=JBBEL6qCam1AZVzUMh3o261Yu513jFfW0ZbSHw5vngI&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-10.png?token=JBBEL6qCam1AZVzUMh3o261Yu513jFfW0ZbSHw5vngI&exp=1783982841" alt="Personaje 10" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-11.jpg?token=u5ALTk-3pskmKbIJQOeNdg376X93jiunSQ7qr2VXlsI&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-11.jpg?token=u5ALTk-3pskmKbIJQOeNdg376X93jiunSQ7qr2VXlsI&exp=1783982841" alt="Personaje 11" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-12.png?token=S8NemjMZ1WoEZVmqamn3rYMmDkm0rpNVtSihMBvevSs&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-12.png?token=S8NemjMZ1WoEZVmqamn3rYMmDkm0rpNVtSihMBvevSs&exp=1783982841" alt="Personaje 12" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
        <a href="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-13.png?token=GAM3XuiTJAFGHuHlagWhnsUiM2yP7kO01Fkm5y55yY8&exp=1783982841" target="_blank" rel="noreferrer" class="group relative overflow-hidden rounded-[1.75rem] border border-white/10 bg-white/5"><img src="https://cms.aikit.es/api/tools/threads/6a551cc0cf0f50d33f8c7814/file/6a551cc0cf0f50d33f8c7814_personaje-13.png?token=GAM3XuiTJAFGHuHlagWhnsUiM2yP7kO01Fkm5y55yY8&exp=1783982841" alt="Personaje 13" class="h-56 md:h-72 w-full object-cover transition-transform duration-500 group-hover:scale-105" loading="lazy" /></a>
      </div>
    </section>

    <section id="video" class="border-y border-white/10 bg-white/[0.03]">
      <div class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28">
        <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Vídeo</p>
        <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Booktrailer / presentación</h2>
        <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed max-w-3xl">Descubre el universo visual de PRIMERO LOVE YOU.</p>
        <div class="mt-12 rounded-[2rem] overflow-hidden border border-white/10 bg-black/30 shadow-2xl shadow-black/30">
          <div class="aspect-video w-full">
            <iframe class="w-full h-full" src="https://www.youtube.com/embed/ADlNpdwBY0o" title="Vídeo PRIMERO LOVE YOU" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
          </div>
        </div>
      </div>
    </section>

    <section id="comprar" class="max-w-7xl mx-auto px-4 md:px-6 py-20 md:py-28">
      <div class="grid xl:grid-cols-[1.3fr,0.7fr] gap-10">
        <div id="resenas">
          <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Opiniones de lectores</p>
          <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Lo que dicen quienes lo han leído</h2>
          <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed max-w-3xl">Reseñas verificadas de Amazon.</p>
        </div>
        <aside class="rounded-[2rem] border border-white/10 bg-gradient-to-b from-white/6 to-white/[0.03] p-6 md:p-8 h-fit ring">
          <div class="inline-flex items-center gap-2 rounded-full border border-amber-300/30 bg-amber-300/10 px-4 py-1.5 text-[11px] uppercase tracking-[0.35em] text-amber-100">Compra física en Málaga</div>
          <h3 class="mt-4 flex items-center gap-2 text-2xl font-semibold text-white">Librerías Proteo Prometeo</h3>
          <p class="mt-2 text-sm text-zinc-300">Tu ejemplar también puede comprarse físicamente en uno de los puntos libreros más reconocidos de Málaga.</p>
        </aside>
      </div>
    </section>

    <section id="contacto" class="border-t border-white/10 bg-black/20">
      <div class="max-w-7xl mx-auto px-4 md:px-6 py-14">
        <p class="text-[11px] tracking-[0.35em] uppercase text-amber-300/80 mb-3">Contacto y redes</p>
        <h2 class="text-3xl md:text-5xl font-semibold text-white leading-tight">Christian C. D'Rosoy</h2>
        <p class="mt-4 text-zinc-300 text-base md:text-lg leading-relaxed max-w-3xl">Correo y redes sociales oficiales del proyecto.</p>
        <div class="mt-6 flex flex-wrap gap-3">
          <a href="mailto:christiancdrosoy@hotmail.com" class="inline-flex items-center gap-2 rounded-full border border-white/15 px-4 py-2 text-sm text-white hover:bg-white/8 transition-colors">✉ Correo</a>
          <a href="https://www.instagram.com/primeroloveyou_libro?igsh=YTJhOWJ6M2Fkc2Ru&utm_source=qr" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 rounded-full border border-white/15 px-4 py-2 text-sm text-white hover:bg-white/8 transition-colors">Instagram</a>
          <a href="https://www.facebook.com/share/g/163orYLTEDm/?mibextid=wwXIfr" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 rounded-full border border-white/15 px-4 py-2 text-sm text-white hover:bg-white/8 transition-colors">Facebook</a>
          <a href="https://www.tiktok.com/@primeroloveyou_libro?_r=1&_t=ZN-97yLDwzYbXn" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 rounded-full border border-white/15 px-4 py-2 text-sm text-white hover:bg-white/8 transition-colors">TikTok</a>
          <a href="https://youtube.com/shorts/ADlNpdwBY0o" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 rounded-full border border-white/15 px-4 py-2 text-sm text-white hover:bg-white/8 transition-colors">YouTube</a>
        </div>
        <div class="mt-10 flex flex-col md:flex-row gap-4 items-start md:items-center justify-between">
          <div>
            <p class="font-semibold text-white">© 2026 Christian C. D'Rosoy</p>
            <p class="text-sm text-zinc-400 mt-1">PRIMERO LOVE YOU · Libro I · Trilogía oficial · Ediciones 52.1 · Málaga, España</p>
          </div>
          <a href="#inicio" class="inline-flex items-center gap-2 rounded-full border border-white/15 px-4 py-2 text-sm text-white hover:bg-white/8 transition-colors">↑ Volver arriba</a>
        </div>
      </div>
    </section>

  </main>
  <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const places = [
        { name: 'Cafetería Los Valle', zone: 'Perchel Sur', address: 'C. Cuarteles, 54', lat: 36.7130199, lon: -4.4290695, note: 'Desayunos, café y arranque de la historia.', approx: false },
        { name: "Tano's", zone: 'Huelin', address: 'C. Río Rocío, 18', lat: 36.7037455, lon: -4.43365, note: 'Bar de barrio ligado al paisaje de Huelin.', approx: false },
        { name: 'Le Grand Café Centro', zone: 'Perchel Norte', address: 'Pasillo Guimbarda', lat: 36.7205867, lon: -4.4257911, note: 'Refugio de la Guardia Pretoriana.', approx: false },
        { name: 'Bar Indiana', zone: 'Centro Histórico', address: 'C. Nosquera, 12', lat: 36.7231608, lon: -4.4222651, note: 'Punto nocturno del centro.', approx: false },
        { name: 'Colegio García Lorca', zone: 'Soho / Centro', address: 'C. Alemania, 14', lat: 36.7129362, lon: -4.4249044, note: 'El primer gran giro de la novela.', approx: false },
        { name: 'Calle Peregrino', zone: 'El Perchel', address: 'Calle Peregrino', lat: 36.7145073, lon: -4.428058, note: 'Casa de infancia y nodo familiar.', approx: false },
        { name: 'Calle La Unión', zone: 'Cruz de Humilladero', address: 'Calle La Unión', lat: 36.70979, lon: -4.4418457, note: 'La casa de Christian en 2026.', approx: false },
        { name: 'Sacaba Beach', zone: 'Carretera de Cádiz', address: 'Sacaba Beach', lat: 36.6795841, lon: -4.4482431, note: 'Verano, costa y memoria.', approx: false },
        { name: 'Playa de Huelin', zone: 'Huelin', address: 'Paseo Marítimo de Huelin', lat: 36.7010, lon: -4.4390, note: 'Paseo y reflexión frente al mar.', approx: true },
        { name: 'GOfit Huelin', zone: 'Huelin', address: 'GOfit Huelin', lat: 36.7029, lon: -4.4368, note: 'Piscina y reset mental.', approx: true },
        { name: 'Avenida Juan XXIII', zone: 'Perchel Norte', address: 'Avenida Juan XXIII', lat: 36.7180, lon: -4.4270, note: 'Café con Silvia.', approx: true },
        { name: 'Ciudad Jardín', zone: 'Ciudad Jardín', address: 'Ciudad Jardín', lat: 36.7310, lon: -4.4270, note: 'Territorio de Curro y el taller.', approx: true },
        { name: 'Bar Santa', zone: 'Beatas', address: 'Calle Beatas', lat: 36.7238, lon: -4.4200, note: 'Flashback ochentero.', approx: true },
        { name: 'Ikigaink Experience', zone: 'La Malagueta / Centro', address: 'Estudio de tatuaje', lat: 36.7210, lon: -4.4125, note: 'Estudio de Annette. Ubicación aproximada.', approx: true }
      ];
      const pinIcon = L.divIcon({ className: '', iconSize: [30, 42], iconAnchor: [15, 41], popupAnchor: [0, -38], html: '<div style="position:relative;width:30px;height:42px;filter:drop-shadow(0 10px 18px rgba(0,0,0,.45));"><svg viewBox="0 0 30 42" width="30" height="42" aria-hidden="true" style="display:block;"><path d="M15 1C8.37 1 3 6.37 3 13c0 8.1 9.1 19.55 11.9 22.83.6.7 1.7.7 2.3 0C20.9 32.55 30 21.1 30 13 30 6.37 24.63 1 15 1Z" fill="#0f172a" stroke="rgba(251,191,36,.85)" stroke-width="1.3"/><circle cx="15" cy="13" r="4.6" fill="#fbbf24"/><circle cx="15" cy="13" r="2.15" fill="#111827"/></svg></div>' });
      const map = L.map('malaga-map', { scrollWheelZoom: false, zoomControl: true, zoomSnap: 0.25 }).setView([36.7163, -4.4268], 13.2);
      L.tileLayer('https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png', { subdomains: 'abcd', maxZoom: 19, attribution: '&copy; OpenStreetMap contributors &copy; CARTO' }).addTo(map);
      const markers = []; const bounds = [];
      places.forEach((place) => { const marker = L.marker([place.lat, place.lon], { icon: pinIcon }).addTo(map); markers.push(marker); bounds.push([place.lat, place.lon]); const approxBadge = place.approx ? '<span style="display:inline-block;padding:2px 8px;border-radius:999px;background:rgba(251,191,36,.15);color:#fcd34d;font-size:11px;letter-spacing:.12em;text-transform:uppercase;">Aprox.</span>' : ''; marker.bindPopup(`<div style="min-width:220px;max-width:280px;font-family:Inter,system-ui,sans-serif;color:#111827;"><div style="display:flex;justify-content:space-between;gap:12px;align-items:flex-start;margin-bottom:8px;"><strong style="font-size:14px;line-height:1.2;">${place.name}</strong>${approxBadge}</div><div style="font-size:12px;color:#374151;margin-bottom:4px;">${place.address} · ${place.zone}</div><div style="font-size:12px;color:#6b7280;line-height:1.4;">${place.note}</div></div>`); });
      if (bounds.length) map.fitBounds(bounds, { padding: [40, 40] });
      const list = document.getElementById('malaga-places');
      const escapeHtml = (s) => String(s).replaceAll('&', '&amp;').replaceAll('<', '&lt;').replaceAll('>', '&gt;').replaceAll('"', '&quot;');
      list.innerHTML = places.map((place, i) => `<button type="button" data-place-index="${i}" class="map-card text-left w-full rounded-2xl border border-white/10 bg-black/20 p-4 hover:border-amber-300/40 hover:bg-amber-300/8 transition-all"><div class="flex items-start justify-between gap-3"><div><p class="text-sm font-semibold text-white">${escapeHtml(place.name)}</p><p class="mt-1 text-xs uppercase tracking-[0.24em] text-amber-200/70">${escapeHtml(place.zone)}</p></div>${place.approx ? '<span class="inline-flex items-center rounded-full border border-amber-300/25 bg-amber-300/10 px-2.5 py-1 text-[10px] uppercase tracking-[0.18em] text-amber-100">Aprox.</span>' : ''}</div><p class="mt-3 text-sm text-zinc-300 leading-relaxed">${escapeHtml(place.address)}</p><p class="mt-2 text-sm text-zinc-400 leading-relaxed">${escapeHtml(place.note)}</p></button>`).join('');
      const cards = [...list.querySelectorAll('[data-place-index]')];
      const activate = (idx) => { const place = places[idx]; map.setView([place.lat, place.lon], Math.max(map.getZoom(), 15), { animate: true }); markers[idx].openPopup(); cards.forEach((el) => el.classList.remove('active')); cards[idx]?.classList.add('active'); };
      cards.forEach((card) => card.addEventListener('click', () => activate(Number(card.dataset.placeIndex))));
      if (cards[0]) cards[0].classList.add('active');
    });
  </script>
</body>
</html>
