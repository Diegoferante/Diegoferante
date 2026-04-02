<!D<!--título--> 
<div id="user-content-toc">
  <ul align="center">
   <img src="https://www.alura.com.br/artigos/assets/hello-world-em-varias-linguagens/imagem1.gif" jsaction="" class="sFlh5c FyHeAf iPVvYb" style="max-width: 1500px; height:351px; margin: 800px; width: 1800px;" alt="Hello World em várias linguagens de programação | Alura" jsname="kn3ccd"> <summary><h1 style="display: inline-block">Hello World</h1></summary>
</div> 
  Hi 👋, I'm Diego!    
  - 🌱<img width="1052" height="297" src="https://bkpsitecpsnew.blob.core.windows.net/uploadsitecps/sites/126/2024/06/logo_etec_matao.png" class="custom-logo" alt="Etec Sylvio de Mattos Carvalho" decoding="async" fetchpriority="high">

  - 🔭I'm looking to learn how to develop a system to enter the job market in the future
</p>

<!-- Dropdown -->
<details>
  <summary>👨‍💻 More about me</summary>


  - ⚡ https://steamcommunity.com/profiles/76561198006194141/
</details>

<!-- Links --> 
[![Youtube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@diegoferrante5179?si=GQSgGUkXz4myGcoU/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/diego-ferrante-927926b3/)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/diegocristianoferrante/?hl=pt-br/)
<!-- GithubStats -->


<!-- GIF -->
<p align="left">
  <img align="center"
<img height="500" src="https://user-images.githubusercontent.com/74038190/225813708-98b745f2-7d22-48cf-9150-083f1b00d6c9.gif"  />
</div>
</p>

## 🔥 Skills
<!-- Skills: Programming Languages -->
  <div style="flex-basis: 48%;">
    <h3>Programming Languages</h3>
    <img align="center" alt="Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
    <img align="center" alt="HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
    <img align="center" alt="CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
    <img align="center" alt="Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
    <img align="center" alt="C" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg">
  </div>
  
  <!-- Skills: Tools & Frameworks -->
  <div style="flex-basis: 48%;">
    <h3>Tools & Frameworks</h3>
    <img align="center" alt="VScode" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg">
    <img align="center" alt="Jupyter" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg">
    <img align="center" alt="Chris-AWS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg">
    <img align="center" alt="Bash" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg">
  </div>
  
  <!-- Skills: Libraries -->
  <div style="flex-basis: 48%;">
    <h3>Libraries</h3>
    <img align="center" alt="Numpy" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg">
    <img align="center" alt="Pandas" src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/>
    <img align="center" alt="Seaborn" src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/>
    <img align="center" alt="Scikit-learn" src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/>
  </div>
 <!DOCTYPE html>
<html lang="pt-br">
  <head>
  
/* ============================================================
   HOME PAGE — METAL EXPRESS
   Design: Industrial Noir — Black/Yellow, Bebas Neue headings,
   diagonal cuts, animated truck, metal textures.
   ============================================================ */

import { useEffect, useRef, useState } from "react";

const HERO_BG = "https://d2xsxph8kpxj0f.cloudfront.net/310519663508172715/ah389yNsZw2szkxHeNWXwL/hero-bg-4UNmrZSsFhaSFRT82eejH3.webp";
const TRUCK_SIDE = "https://d2xsxph8kpxj0f.cloudfront.net/310519663508172715/ah389yNsZw2szkxHeNWXwL/truck-side-J2ktQoLsJ36GpYWrhrttT4.webp";
const ROAD_TEXTURE = "https://d2xsxph8kpxj0f.cloudfront.net/310519663508172715/ah389yNsZw2szkxHeNWXwL/road-texture-NBG6EbSbj3A5vy3pYDAfR5.webp";
const METAL_TEXTURE = "https://d2xsxph8kpxj0f.cloudfront.net/310519663508172715/ah389yNsZw2szkxHeNWXwL/metal-texture-a4WDR3S6VoWARynYRNW997.webp";

// Animated truck component with smooth motion and wheel rotation
function AnimatedTruck() {
  const truckRef = useRef<HTMLDivElement>(null);
  const wheelRef = useRef<HTMLDivElement>(null);
  const posRef = useRef(-320);
  const animRef = useRef<number>(0);
  const rotationRef = useRef(0);

  useEffect(() => {
    const animate = () => {
      // Smooth linear motion from left to right
      posRef.current += 3;
      
      // Reset position when truck exits screen on the right
      if (posRef.current > window.innerWidth + 100) {
        posRef.current = -320;
      }

      // Rotate wheels based on distance traveled
      rotationRef.current += 12;
      if (rotationRef.current >= 360) {
        rotationRef.current = 0;
      }

      if (truckRef.current) {
        truckRef.current.style.transform = `translateX(${posRef.current}px)`;
      }
      
      if (wheelRef.current) {
        wheelRef.current.style.transform = `rotate(${rotationRef.current}deg)`;
      }

      animRef.current = requestAnimationFrame(animate);
    };
    
    animRef.current = requestAnimationFrame(animate);
    return () => cancelAnimationFrame(animRef.current);
  }, []);

  return (
    <div
      ref={truckRef}
      style={{
        position: "absolute",
        bottom: "8px",
        left: "0",
        transform: "translateX(-320px)",
        willChange: "transform",
        zIndex: 10,
        display: "flex",
        alignItems: "center",
        gap: "0.5rem",
      }}
    >
      {/* Truck emoji - flipped to face forward */}
      <span style={{
        fontSize: "72px",
        lineHeight: 1,
        display: "block",
        filter: "drop-shadow(0 0 16px rgba(245,197,24,0.6)) drop-shadow(0 4px 8px rgba(0,0,0,0.5))",
        textShadow: "0 2px 4px rgba(0,0,0,0.3)",
        transform: "scaleX(-1)",
      }}>
        🚚
      </span>
      
      {/* Spinning wheel effect (decorative) */}
      <div
        ref={wheelRef}
        style={{
          width: "16px",
          height: "16px",
          borderRadius: "50%",
          background: "radial-gradient(circle at 30% 30%, #F5C518, #4A4A4A)",
          boxShadow: "0 0 8px rgba(245,197,24,0.4), inset -2px -2px 4px rgba(0,0,0,0.5)",
          position: "absolute",
          bottom: "-8px",
          left: "12px",
          willChange: "transform",
        }}
      />
    </div>
  );
}

// Animated counter
function Counter({ target, suffix = "" }: { target: number; suffix?: string }) {
  const [count, setCount] = useState(0);
  const ref = useRef<HTMLSpanElement>(null);
  const started = useRef(false);

  useEffect(() => {
    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting && !started.current) {
          started.current = true;
          const duration = 1800;
          const steps = 60;
          const increment = target / steps;
          let current = 0;
          const timer = setInterval(() => {
            current += increment;
            if (current >= target) {
              setCount(target);
              clearInterval(timer);
            } else {
              setCount(Math.floor(current));
            }
          }, duration / steps);
        }
      },
      { threshold: 0.3 }
    );
    if (ref.current) observer.observe(ref.current);
    return () => observer.disconnect();
  }, [target]);

  return (
    <span ref={ref}>
      {count.toLocaleString("pt-BR")}
      {suffix}
    </span>
  );
}

// Service card
function ServiceCard({ icon, title, desc }: { icon: string; title: string; desc: string }) {
  return (
    <div
      style={{
        background: "linear-gradient(135deg, #111 0%, #1a1a1a 100%)",
        border: "1px solid #2a2a2a",
        borderTop: "3px solid #F5C518",
        padding: "2rem 1.5rem",
        transition: "transform 0.2s ease, box-shadow 0.2s ease",
      }}
      onMouseEnter={(e) => {
        (e.currentTarget as HTMLDivElement).style.transform = "translateY(-4px)";
        (e.currentTarget as HTMLDivElement).style.boxShadow = "0 12px 40px rgba(245,197,24,0.15)";
      }}
      onMouseLeave={(e) => {
        (e.currentTarget as HTMLDivElement).style.transform = "translateY(0)";
        (e.currentTarget as HTMLDivElement).style.boxShadow = "none";
      }}
    >
      <div style={{ fontSize: "2.5rem", marginBottom: "1rem" }}>{icon}</div>
      <h3 style={{ fontFamily: "'Bebas Neue', sans-serif", fontSize: "1.5rem", color: "#F5C518", marginBottom: "0.75rem", letterSpacing: "0.05em" }}>
        {title}
      </h3>
      <p style={{ color: "#aaa", lineHeight: 1.6, fontSize: "0.95rem" }}>{desc}</p>
    </div>
  );
}

export default function Home() {
  const [scrolled, setScrolled] = useState(false);

  useEffect(() => {
    const handleScroll = () => setScrolled(window.scrollY > 60);
    window.addEventListener("scroll", handleScroll);
    return () => window.removeEventListener("scroll", handleScroll);
  }, []);

  const handleWhatsApp = () => {
    window.open("https://wa.me/5516996253699", "_blank");
  };

  return (
    <div style={{ background: "#0A0A0A", minHeight: "100vh", overflowX: "hidden" }}>

      {/* ── NAVBAR ── */}
      <nav
        style={{
          position: "fixed",
          top: 0,
          left: 0,
          right: 0,
          zIndex: 100,
          padding: "1rem 2rem",
          display: "flex",
          alignItems: "center",
          justifyContent: "space-between",
          background: scrolled ? "rgba(10,10,10,0.97)" : "transparent",
          backdropFilter: scrolled ? "blur(12px)" : "none",
          borderBottom: scrolled ? "1px solid #222" : "none",
          transition: "all 0.3s ease",
        }}
      >
        <div style={{ display: "flex", alignItems: "center", gap: "0.75rem" }}>
          <span style={{ fontSize: "1.8rem" }}>🚚</span>
          <span style={{ fontFamily: "'Bebas Neue', sans-serif", fontSize: "1.8rem", color: "#F5C518", letterSpacing: "0.08em" }}>
            Metal Express
          </span>
        </div>
        <button
          onClick={handleWhatsApp}
          className="pulse-glow"
          style={{
            background: "#25D366",
            color: "#fff",
            border: "none",
            padding: "0.6rem 1.4rem",
            fontFamily: "'Roboto Condensed', sans-serif",
            fontWeight: 700,
            fontSize: "0.9rem",
            letterSpacing: "0.05em",
            cursor: "pointer",
            display: "flex",
            alignItems: "center",
            gap: "0.5rem",
            transition: "background 0.2s ease",
          }}
          onMouseEnter={(e) => ((e.currentTarget as HTMLButtonElement).style.background = "#1da851")}
          onMouseLeave={(e) => ((e.currentTarget as HTMLButtonElement).style.background = "#25D366")}
        >
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z" />
          </svg>
          FALE CONOSCO
        </button>
      </nav>

      {/* ── HERO SECTION ── */}
      <section
        style={{
          position: "relative",
          height: "100vh",
          minHeight: "600px",
          display: "flex",
          alignItems: "center",
          overflow: "hidden",
        }}
      >
        {/* Background image */}
        <div
          style={{
            position: "absolute",
            inset: 0,
            backgroundImage: `url(${HERO_BG})`,
            backgroundSize: "cover",
            backgroundPosition: "center",
            filter: "brightness(0.35)",
          }}
        />
        {/* Overlay gradient */}
        <div
          style={{
            position: "absolute",
            inset: 0,
            background: "linear-gradient(90deg, rgba(10,10,10,0.95) 0%, rgba(10,10,10,0.6) 50%, rgba(10,10,10,0.3) 100%)",
          }}
        />
        {/* Yellow bottom accent line */}
        <div style={{ position: "absolute", bottom: 0, left: 0, right: 0, height: "4px", background: "#F5C518" }} />

        {/* Content */}
        <div
          style={{
            position: "relative",
            zIndex: 5,
            padding: "0 2rem",
            maxWidth: "700px",
            marginLeft: "max(2rem, calc(50vw - 640px))",
          }}
        >
          <div className="fade-in-up fade-in-up-delay-1">
            <span
              style={{
                display: "inline-block",
                background: "#F5C518",
                color: "#0A0A0A",
                fontFamily: "'Roboto Condensed', sans-serif",
                fontWeight: 700,
                fontSize: "0.8rem",
                letterSpacing: "0.15em",
                padding: "0.3rem 0.8rem",
                marginBottom: "1.5rem",
                textTransform: "uppercase",
              }}
            >
              Transporte de Cargas
            </span>
          </div>

          <h1
            className="fade-in-up fade-in-up-delay-2"
            style={{
              fontFamily: "'Bebas Neue', sans-serif",
              fontSize: "clamp(4rem, 10vw, 8rem)",
              lineHeight: 0.9,
              color: "#fff",
              margin: "0 0 0.5rem",
              letterSpacing: "0.03em",
            }}
          >
            METAL
            <br />
            <span style={{ color: "#F5C518" }}>EXPRESS</span>
          </h1>

          <p
            className="fade-in-up fade-in-up-delay-3"
            style={{
              fontFamily: "'Roboto Condensed', sans-serif",
              fontSize: "1.3rem",
              color: "#ccc",
              marginBottom: "2.5rem",
              lineHeight: 1.5,
              letterSpacing: "0.02em",
            }}
          >
            Velocidade e confiança em cada entrega.
            <br />
            Sua carga, nossa responsabilidade.
          </p>

          <div className="fade-in-up fade-in-up-delay-4" style={{ display: "flex", gap: "1rem", flexWrap: "wrap" }}>
            <button
              onClick={handleWhatsApp}
              className="pulse-glow"
              style={{
                background: "#F5C518",
                color: "#0A0A0A",
                border: "none",
                padding: "1rem 2.5rem",
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "1.3rem",
                letterSpacing: "0.1em",
                cursor: "pointer",
                display: "flex",
                alignItems: "center",
                gap: "0.6rem",
                transition: "background 0.2s ease, transform 0.1s ease",
              }}
              onMouseEnter={(e) => {
                (e.currentTarget as HTMLButtonElement).style.background = "#C9A010";
                (e.currentTarget as HTMLButtonElement).style.transform = "scale(1.03)";
              }}
              onMouseLeave={(e) => {
                (e.currentTarget as HTMLButtonElement).style.background = "#F5C518";
                (e.currentTarget as HTMLButtonElement).style.transform = "scale(1)";
              }}
            >
              📱 (16) 99625-3699
            </button>
            <a
              href="#servicos"
              style={{
                background: "transparent",
                color: "#fff",
                border: "2px solid #4A4A4A",
                padding: "1rem 2rem",
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "1.3rem",
                letterSpacing: "0.1em",
                cursor: "pointer",
                textDecoration: "none",
                display: "flex",
                alignItems: "center",
                transition: "border-color 0.2s ease, color 0.2s ease",
              }}
              onMouseEnter={(e) => {
                (e.currentTarget as HTMLAnchorElement).style.borderColor = "#F5C518";
                (e.currentTarget as HTMLAnchorElement).style.color = "#F5C518";
              }}
              onMouseLeave={(e) => {
                (e.currentTarget as HTMLAnchorElement).style.borderColor = "#4A4A4A";
                (e.currentTarget as HTMLAnchorElement).style.color = "#fff";
              }}
            >
              NOSSOS SERVIÇOS
            </a>
          </div>
        </div>
      </section>

      {/* ── TRUCK ANIMATION STRIP ── */}
      <div
        style={{
          position: "relative",
          background: "#0D0D0D",
          borderTop: "3px solid #F5C518",
          borderBottom: "3px solid #F5C518",
          height: "120px",
          overflow: "hidden",
        }}
      >
        {/* Road markings */}
        <div
          style={{
            position: "absolute",
            top: "50%",
            left: 0,
            right: 0,
            height: "4px",
            background: "repeating-linear-gradient(90deg, #333 0px, #333 40px, transparent 40px, transparent 80px)",
            transform: "translateY(-50%)",
            animation: "roadMove 1s linear infinite",
          }}
        />
        <AnimatedTruck />
        {/* Speed lines */}
        <div style={{ position: "absolute", inset: 0, background: "linear-gradient(90deg, #0D0D0D 0%, transparent 15%, transparent 85%, #0D0D0D 100%)" }} />
      </div>

      {/* ── STATS SECTION ── */}
      <section
        style={{
          background: `url(${METAL_TEXTURE}) center/cover`,
          position: "relative",
          padding: "5rem 2rem",
        }}
      >
        <div style={{ position: "absolute", inset: 0, background: "rgba(10,10,10,0.88)" }} />
        <div
          style={{
            position: "relative",
            maxWidth: "1100px",
            margin: "0 auto",
            display: "grid",
            gridTemplateColumns: "repeat(auto-fit, minmax(200px, 1fr))",
            gap: "2rem",
            textAlign: "center",
          }}
        >
          {[
            { value: 500, suffix: "+", label: "Entregas Realizadas" },
            { value: 100, suffix: "%", label: "Comprometimento" },
            { value: 24, suffix: "h", label: "Atendimento" },
            { value: 6, suffix: " meses", label: "De Experiência" },
          ].map((stat) => (
            <div key={stat.label}>
              <div
                style={{
                  fontFamily: "'Bebas Neue', sans-serif",
                  fontSize: "clamp(3rem, 6vw, 5rem)",
                  color: "#F5C518",
                  lineHeight: 1,
                  letterSpacing: "0.02em",
                }}
              >
                <Counter target={stat.value} suffix={stat.suffix} />
              </div>
              <div
                style={{
                  fontFamily: "'Roboto Condensed', sans-serif",
                  fontSize: "0.9rem",
                  color: "#888",
                  letterSpacing: "0.12em",
                  textTransform: "uppercase",
                  marginTop: "0.5rem",
                }}
              >
                {stat.label}
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* ── SERVICES SECTION ── */}
      <section
        id="servicos"
        style={{
          background: "#0A0A0A",
          padding: "6rem 2rem",
          position: "relative",
        }}
      >
        {/* Diagonal top border */}
        <div
          style={{
            position: "absolute",
            top: 0,
            left: 0,
            right: 0,
            height: "5px",
            background: "linear-gradient(90deg, #F5C518 0%, #C9A010 50%, transparent 100%)",
          }}
        />

        <div style={{ maxWidth: "1100px", margin: "0 auto" }}>
          <div style={{ marginBottom: "3.5rem" }}>
            <span
              style={{
                fontFamily: "'Roboto Condensed', sans-serif",
                fontSize: "0.8rem",
                letterSpacing: "0.2em",
                color: "#F5C518",
                textTransform: "uppercase",
              }}
            >
              O que oferecemos
            </span>
            <h2
              style={{
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "clamp(2.5rem, 5vw, 4rem)",
                color: "#fff",
                margin: "0.5rem 0 1rem",
                letterSpacing: "0.05em",
              }}
            >
              NOSSOS SERVIÇOS
            </h2>
            <div style={{ width: "60px", height: "4px", background: "#F5C518" }} />
          </div>

          <div
            style={{
              display: "grid",
              gridTemplateColumns: "repeat(auto-fit, minmax(260px, 1fr))",
              gap: "1.5rem",
            }}
          >
            <ServiceCard
              icon="📦"
              title="Transporte de Cargas"
              desc="Entregamos sua carga com segurança e pontualidade em todo o território nacional, com rastreamento em tempo real."
            />
            <ServiceCard
              icon="⚡"
              title="Entrega Expressa"
              desc="Quando o tempo é crítico, nossa frota está pronta para entregas urgentes com máxima agilidade e eficiência."
            />
            <ServiceCard
              icon="🏗️"
              title="Cargas Especiais"
              desc="Equipamentos pesados, materiais frágeis ou cargas de grande porte — temos a solução certa para cada necessidade."
            />
            <ServiceCard
              icon="🗺️"
              title="Logística Completa"
              desc="Planejamento de rotas, armazenagem temporária e gestão logística integrada para otimizar sua cadeia de suprimentos."
            />
          </div>
        </div>
      </section>

      {/* ── TRUCK SHOWCASE SECTION ── */}
      <section
        style={{
          position: "relative",
          overflow: "hidden",
          background: "#080808",
        }}
      >
        <div
          style={{
            display: "grid",
            gridTemplateColumns: "1fr 1fr",
            minHeight: "500px",
          }}
          className="truck-showcase"
        >
          {/* Image side */}
          <div
            style={{
              backgroundImage: `url(${TRUCK_SIDE})`,
              backgroundSize: "cover",
              backgroundPosition: "center",
              minHeight: "400px",
            }}
          />
          {/* Text side */}
          <div
            style={{
              background: "#0F0F0F",
              padding: "4rem 3rem",
              display: "flex",
              flexDirection: "column",
              justifyContent: "center",
              borderLeft: "4px solid #F5C518",
            }}
          >
            <span
              style={{
                fontFamily: "'Roboto Condensed', sans-serif",
                fontSize: "0.8rem",
                letterSpacing: "0.2em",
                color: "#F5C518",
                textTransform: "uppercase",
                marginBottom: "1rem",
              }}
            >
              Nossa Frota
            </span>
            <h2
              style={{
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "clamp(2rem, 4vw, 3.5rem)",
                color: "#fff",
                margin: "0 0 1.5rem",
                lineHeight: 1,
                letterSpacing: "0.05em",
              }}
            >
              FROTA MODERNA
              <br />
              <span style={{ color: "#F5C518" }}>SEMPRE PRONTA</span>
            </h2>
            <p
              style={{
                color: "#999",
                lineHeight: 1.7,
                fontSize: "1rem",
                marginBottom: "2rem",
                fontFamily: "'Roboto Condensed', sans-serif",
              }}
            >
              Mantemos nossa frota em perfeito estado de conservação, com manutenção preventiva rigorosa e tecnologia de rastreamento de última geração. Cada veículo é preparado para garantir a integridade da sua carga do ponto de origem ao destino final.
            </p>
            <ul
              style={{
                listStyle: "none",
                padding: 0,
                margin: "0 0 2rem",
                display: "flex",
                flexDirection: "column",
                gap: "0.75rem",
              }}
            >
              {[
                "Rastreamento GPS em tempo real",
                "Manutenção preventiva certificada",
                "Motoristas habilitados e treinados",
                "Seguro de carga incluso",
              ].map((item) => (
                <li
                  key={item}
                  style={{
                    display: "flex",
                    alignItems: "center",
                    gap: "0.75rem",
                    color: "#ccc",
                    fontFamily: "'Roboto Condensed', sans-serif",
                    fontSize: "0.95rem",
                  }}
                >
                  <span style={{ color: "#F5C518", fontWeight: 700, fontSize: "1.1rem" }}>▶</span>
                  {item}
                </li>
              ))}
            </ul>
            <button
              onClick={handleWhatsApp}
              style={{
                background: "#F5C518",
                color: "#0A0A0A",
                border: "none",
                padding: "0.9rem 2rem",
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "1.2rem",
                letterSpacing: "0.1em",
                cursor: "pointer",
                alignSelf: "flex-start",
                transition: "background 0.2s ease",
              }}
              onMouseEnter={(e) => ((e.currentTarget as HTMLButtonElement).style.background = "#C9A010")}
              onMouseLeave={(e) => ((e.currentTarget as HTMLButtonElement).style.background = "#F5C518")}
            >
              SOLICITAR ORÇAMENTO
            </button>
          </div>
        </div>
      </section>

      {/* ── ROAD DIVIDER ── */}
      <div
        style={{
          height: "200px",
          backgroundImage: `url(${ROAD_TEXTURE})`,
          backgroundSize: "cover",
          backgroundPosition: "center",
          position: "relative",
          overflow: "hidden",
        }}
      >
        <div style={{ position: "absolute", inset: 0, background: "rgba(10,10,10,0.7)" }} />
        <div
          style={{
            position: "absolute",
            inset: 0,
            display: "flex",
            alignItems: "center",
            justifyContent: "center",
          }}
        >
          <p
            style={{
              fontFamily: "'Bebas Neue', sans-serif",
              fontSize: "clamp(1.5rem, 4vw, 3rem)",
              color: "#F5C518",
              letterSpacing: "0.15em",
              textAlign: "center",
              textShadow: "0 2px 20px rgba(0,0,0,0.8)",
            }}
          >
            CADA KM RODADO É UMA PROMESSA CUMPRIDA
          </p>
        </div>
      </div>

      {/* ── CONTACT / CTA SECTION ── */}
      <section
        style={{
          background: "#0A0A0A",
          padding: "6rem 2rem",
          position: "relative",
        }}
        id="contato"
      >
        <div
          style={{
            maxWidth: "800px",
            margin: "0 auto",
            textAlign: "center",
          }}
        >
          <span
            style={{
              fontFamily: "'Roboto Condensed', sans-serif",
              fontSize: "0.8rem",
              letterSpacing: "0.2em",
              color: "#F5C518",
              textTransform: "uppercase",
            }}
          >
            Entre em Contato
          </span>
          <h2
            style={{
              fontFamily: "'Bebas Neue', sans-serif",
              fontSize: "clamp(2.5rem, 6vw, 5rem)",
              color: "#fff",
              margin: "0.5rem 0 1.5rem",
              letterSpacing: "0.05em",
              lineHeight: 1,
            }}
          >
            PRONTO PARA
            <br />
            <span style={{ color: "#F5C518" }}>FAZER SUA ENTREGA?</span>
          </h2>
          <p
            style={{
              color: "#888",
              fontSize: "1.1rem",
              lineHeight: 1.7,
              marginBottom: "3rem",
              fontFamily: "'Roboto Condensed', sans-serif",
            }}
          >
            Entre em contato agora pelo WhatsApp e receba um orçamento rápido e sem compromisso. Nossa equipe está disponível para atender você.
          </p>

          {/* Contact card */}
          <div
            style={{
              background: "#111",
              border: "1px solid #222",
              borderTop: "4px solid #F5C518",
              padding: "3rem 2rem",
              display: "inline-flex",
              flexDirection: "column",
              alignItems: "center",
              gap: "1.5rem",
              minWidth: "320px",
            }}
          >
            <div style={{ fontSize: "3rem" }}>📱</div>
            <div>
              <div
                style={{
                  fontFamily: "'Bebas Neue', sans-serif",
                  fontSize: "2.5rem",
                  color: "#F5C518",
                  letterSpacing: "0.05em",
                }}
              >
                (16) 99625-3699
              </div>
              <div
                style={{
                  color: "#666",
                  fontSize: "0.85rem",
                  letterSpacing: "0.1em",
                  textTransform: "uppercase",
                  fontFamily: "'Roboto Condensed', sans-serif",
                }}
              >
                WhatsApp disponível 24h
              </div>
            </div>
            <button
              onClick={handleWhatsApp}
              className="pulse-glow"
              style={{
                background: "#25D366",
                color: "#fff",
                border: "none",
                padding: "1rem 3rem",
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "1.4rem",
                letterSpacing: "0.1em",
                cursor: "pointer",
                display: "flex",
                alignItems: "center",
                gap: "0.75rem",
                width: "100%",
                justifyContent: "center",
                transition: "background 0.2s ease",
              }}
              onMouseEnter={(e) => ((e.currentTarget as HTMLButtonElement).style.background = "#1da851")}
              onMouseLeave={(e) => ((e.currentTarget as HTMLButtonElement).style.background = "#25D366")}
            >
              <svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor">
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z" />
              </svg>
              CHAMAR NO WHATSAPP
            </button>
          </div>
        </div>
      </section>

      {/* ── FOOTER ── */}
      <footer
        style={{
          background: "#050505",
          borderTop: "3px solid #F5C518",
          padding: "2.5rem 2rem",
        }}
      >
        <div
          style={{
            maxWidth: "1100px",
            margin: "0 auto",
            display: "flex",
            alignItems: "center",
            justifyContent: "space-between",
            flexWrap: "wrap",
            gap: "1rem",
          }}
        >
          <div style={{ display: "flex", alignItems: "center", gap: "0.75rem" }}>
            <span style={{ fontSize: "1.5rem" }}>🚚</span>
            <span
              style={{
                fontFamily: "'Bebas Neue', sans-serif",
                fontSize: "1.5rem",
                color: "#F5C518",
                letterSpacing: "0.08em",
              }}
            >
              Metal Express
            </span>
          </div>
          <p
            style={{
              color: "#555",
              fontSize: "0.85rem",
              fontFamily: "'Roboto Condensed', sans-serif",
              margin: 0,
            }}
          >
            Velocidade e confiança em cada entrega
          </p>
          <p
            style={{
              color: "#444",
              fontSize: "0.8rem",
              fontFamily: "'Roboto Condensed', sans-serif",
              margin: 0,
            }}
          >
            © {new Date().getFullYear()} Metal Express. Todos os direitos reservados.
          </p>
        </div>
      </footer>

      {/* ── RESPONSIVE STYLES ── */}
      <style>{`
        @media (max-width: 768px) {
          .truck-showcase {
            grid-template-columns: 1fr !important;
          }
        }
      `}</style>
    </div>
  );
}
