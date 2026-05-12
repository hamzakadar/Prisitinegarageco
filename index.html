import { useState, useEffect, useRef } from "react";

const NAV_LINKS = [
  { label: "Services", href: "#services" },
  { label: "Process", href: "#process" },
  { label: "Pricing", href: "#pricing" },
  { label: "Reviews", href: "#reviews" },
  { label: "Contact", href: "#contact" },
];

const TESTIMONIALS = [
  { name: "Sarah M.", neighborhood: "Edina", text: "I had no idea my garage could look like this. They showed up Thursday morning, and by noon everything was gone and the floor was swept clean. Zero hassle, zero hidden fees.", initials: "SM" },
  { name: "James R.", neighborhood: "Minnetonka", text: "We'd been putting this off for three years. They handled everything — old furniture, bikes, junk we forgot we had. Flat $650 made it easy to say yes. Would book again in a heartbeat.", initials: "JR" },
  { name: "Linda K.", neighborhood: "Plymouth", text: "Professional, fast, and genuinely courteous. My husband couldn't believe the before and after. Booking was simple and they showed up right on time.", initials: "LK" },
  { name: "Tom & Diane H.", neighborhood: "Wayzata", text: "We were selling our home and needed the garage cleared fast. Pristine came out within two days, hauled everything, swept it spotless. Our realtor was thrilled.", initials: "TD" },
  { name: "Marcus W.", neighborhood: "Rosemount", text: "Straight talk, fair price, excellent work. No upselling, no drama. Just showed up, cleaned it out, and left it better than I ever kept it.", initials: "MW" },
  { name: "Rachel P.", neighborhood: "Burnsville", text: "Called on Monday, they were there Wednesday. The garage looks incredible — I can actually park my car in it for the first time in years. Worth every penny.", initials: "RP" },
];

const BEFORE_AFTERS = [
  { before: "https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=700&q=80", after: "https://images.unsplash.com/photo-1558618047-f9e8de0e24c2?w=700&q=80", label: "Minnetonka" },
  { before: "https://images.unsplash.com/photo-1503951914875-452162b0f3f1?w=700&q=80", after: "https://images.unsplash.com/photo-1562426532-81e3c3e3fbcf?w=700&q=80", label: "Edina" },
  { before: "https://images.unsplash.com/photo-1565814329452-e1efa11c5b89?w=700&q=80", after: "https://images.unsplash.com/photo-1567496898669-ee935f5f647a?w=700&q=80", label: "Plymouth" },
];

const GALLERY = [
  "https://images.unsplash.com/photo-1562426532-81e3c3e3fbcf?w=800&q=80",
  "https://images.unsplash.com/photo-1558618047-f9e8de0e24c2?w=800&q=80",
  "https://images.unsplash.com/photo-1567496898669-ee935f5f647a?w=800&q=80",
  "https://images.unsplash.com/photo-1565814329452-e1efa11c5b89?w=800&q=80",
];

function useReveal() {
  const ref = useRef(null);
  const [on, setOn] = useState(false);
  useEffect(() => {
    const el = ref.current;
    if (!el) return;
    const obs = new IntersectionObserver(([e]) => { if (e.isIntersecting) { setOn(true); obs.disconnect(); } }, { threshold: 0.1 });
    obs.observe(el);
    return () => obs.disconnect();
  }, []);
  return { ref, on };
}

function Reveal({ children, delay = 0, style = {}, className = "" }) {
  const { ref, on } = useReveal();
  return (
    <div ref={ref} className={className} style={{ opacity: on ? 1 : 0, transform: on ? "translateY(0)" : "translateY(36px)", transition: `opacity 0.6s ease ${delay}ms, transform 0.6s ease ${delay}ms`, ...style }}>
      {children}
    </div>
  );
}

function Slider({ before, after, label }) {
  const [pos, setPos] = useState(50);
  const ref = useRef(null);
  const drag = useRef(false);
  const calc = (cx) => { const r = ref.current.getBoundingClientRect(); return Math.max(5, Math.min(95, ((cx - r.left) / r.width) * 100)); };
  useEffect(() => { const up = () => drag.current = false; window.addEventListener("mouseup", up); return () => window.removeEventListener("mouseup", up); }, []);
  return (
    <div ref={ref} style={{ position: "relative", overflow: "hidden", borderRadius: 3, aspectRatio: "16/11", cursor: "ew-resize", userSelect: "none" }}
      onMouseMove={e => { if (drag.current) setPos(calc(e.clientX)); }}
      onTouchMove={e => setPos(calc(e.touches[0].clientX))}>
      <img src={after} alt="After" style={{ position: "absolute", inset: 0, width: "100%", height: "100%", objectFit: "cover" }} />
      <div style={{ position: "absolute", inset: 0, overflow: "hidden", width: `${pos}%` }}>
        <img src={before} alt="Before" style={{ position: "absolute", inset: 0, width: `${10000 / pos}%`, maxWidth: "none", height: "100%", objectFit: "cover" }} />
      </div>
      <div style={{ position: "absolute", top: 0, bottom: 0, left: `${pos}%`, transform: "translateX(-50%)", width: 3, background: "white", zIndex: 3 }} />
      <div onMouseDown={() => drag.current = true} onTouchStart={() => drag.current = true}
        style={{ position: "absolute", top: "50%", left: `${pos}%`, transform: "translate(-50%,-50%)", width: 46, height: 46, borderRadius: "50%", background: "white", zIndex: 4, display: "flex", alignItems: "center", justifyContent: "center", boxShadow: "0 2px 16px rgba(0,0,0,0.35)", fontSize: 13, color: "#E84B1A", fontWeight: 900, letterSpacing: -1 }}>◁▷</div>
      <div style={{ position: "absolute", top: 12, left: 12, background: "rgba(0,0,0,0.72)", color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.14em", textTransform: "uppercase", padding: "5px 11px", borderRadius: 2, opacity: pos > 18 ? 1 : 0, transition: "opacity 0.3s" }}>Before</div>
      <div style={{ position: "absolute", top: 12, right: 12, background: "#E84B1A", color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.14em", textTransform: "uppercase", padding: "5px 11px", borderRadius: 2, opacity: pos < 82 ? 1 : 0, transition: "opacity 0.3s" }}>After</div>
      <div style={{ position: "absolute", bottom: 0, left: 0, right: 0, background: "linear-gradient(transparent, rgba(0,0,0,0.55))", padding: "20px 14px 12px", zIndex: 2 }}>
        <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.14em", textTransform: "uppercase" }}>{label} Cleanout</span>
      </div>
    </div>
  );
}

export default function App() {
  const [scrolled, setScrolled] = useState(false);
  const [menuOpen, setMenuOpen] = useState(false);
  const [form, setForm] = useState({ name: "", phone: "", address: "", size: "", message: "" });
  const [done, setDone] = useState(false);

  useEffect(() => {
    const fn = () => setScrolled(window.scrollY > 50);
    window.addEventListener("scroll", fn);
    return () => window.removeEventListener("scroll", fn);
  }, []);

  const go = (id) => { setMenuOpen(false); document.querySelector(id)?.scrollIntoView({ behavior: "smooth" }); };

  const R = "#E84B1A";
  const N = "#0D1B2A";
  const O = "#F1EEE8";

  return (
    <div style={{ fontFamily: "'DM Sans', system-ui, sans-serif", background: "#fff", color: N, overflowX: "hidden" }}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500;9..40,700;9..40,800&display=swap');
        *{box-sizing:border-box;margin:0;padding:0;}
        .bb{font-family:'Bebas Neue','Arial Black',sans-serif;letter-spacing:0.03em;}
        .btn-r{display:inline-block;background:${R};color:white;border:none;font-family:'DM Sans',sans-serif;font-weight:800;font-size:13px;letter-spacing:0.1em;text-transform:uppercase;padding:15px 34px;cursor:pointer;transition:background 0.2s,transform 0.15s;text-decoration:none;border-radius:2px;}
        .btn-r:hover{background:#C73D13;transform:translateY(-2px);}
        .btn-w{display:inline-block;border:2px solid white;color:white;font-family:'DM Sans',sans-serif;font-weight:800;font-size:13px;letter-spacing:0.1em;text-transform:uppercase;padding:13px 34px;cursor:pointer;background:transparent;transition:all 0.2s;text-decoration:none;border-radius:2px;}
        .btn-w:hover{background:white;color:${N};}
        .btn-d{display:inline-block;border:2.5px solid ${N};color:${N};font-family:'DM Sans',sans-serif;font-weight:800;font-size:13px;letter-spacing:0.1em;text-transform:uppercase;padding:13px 34px;cursor:pointer;background:transparent;transition:all 0.2s;text-decoration:none;border-radius:2px;}
        .btn-d:hover{background:${N};color:white;}
        input,textarea,select{font-family:'DM Sans',sans-serif;border:2px solid #DDD;width:100%;padding:14px 16px;font-size:15px;color:${N};outline:none;border-radius:2px;transition:border-color 0.2s;background:white;appearance:none;}
        input:focus,textarea:focus,select:focus{border-color:${R};}
        label{font-size:11px;font-weight:800;letter-spacing:0.14em;text-transform:uppercase;color:#888;display:block;margin-bottom:7px;}
        .gcard{overflow:hidden;position:relative;}
        .gcard img{transition:transform 0.4s ease;display:block;width:100%;height:100%;object-fit:cover;}
        .gcard:hover img{transform:scale(1.05);}
        .nlink{font-size:13px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;cursor:pointer;transition:color 0.2s;text-decoration:none;}
        @keyframes fup{from{opacity:0;transform:translateY(30px);}to{opacity:1;transform:translateY(0);}}
        .a1{animation:fup 0.7s ease 0.05s both;}
        .a2{animation:fup 0.7s ease 0.2s both;}
        .a3{animation:fup 0.7s ease 0.35s both;}
        .a4{animation:fup 0.7s ease 0.5s both;}
        .a5{animation:fup 0.7s ease 0.65s both;}
        .tcard{background:white;border:2px solid #E8E4DE;padding:32px 28px;transition:border-color 0.25s,transform 0.25s;}
        .tcard:hover{border-color:${R};transform:translateY(-4px);}
        @media(max-width:768px){.donly{display:none!important;}.monly{display:block!important;}}
        @media(min-width:769px){.monly{display:none!important;}}
      `}</style>

      {/* NAV */}
      <nav style={{ position: "fixed", top: 0, left: 0, right: 0, zIndex: 200, background: scrolled ? "white" : "transparent", borderBottom: scrolled ? `3px solid ${R}` : "none", transition: "background 0.3s, border 0.3s", padding: "0 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto", display: "flex", alignItems: "center", height: 68, gap: 32 }}>
          <div style={{ display: "flex", alignItems: "center", gap: 10, flexShrink: 0, cursor: "pointer" }} onClick={() => window.scrollTo({ top: 0, behavior: "smooth" })}>
            <svg width="34" height="34" viewBox="0 0 36 36" fill="none">
              <rect width="36" height="36" fill={R} />
              <path d="M7 27V17L18 11L29 17V27" stroke="white" strokeWidth="2" fill="none" strokeLinejoin="round" />
              <rect x="14" y="20" width="8" height="7" fill="white" rx="1" />
              <line x1="7" y1="27" x2="29" y2="27" stroke="white" strokeWidth="2" />
            </svg>
            <span className="bb" style={{ fontSize: 19, color: scrolled ? N : "white", letterSpacing: "0.05em" }}>Pristine Garage Co.</span>
          </div>

          <div className="donly" style={{ flex: 1, display: "flex", justifyContent: "center", gap: 36 }}>
            {NAV_LINKS.map(l => <span key={l.label} className="nlink" style={{ color: scrolled ? N : "white" }} onClick={() => go(l.href)}>{l.label}</span>)}
          </div>

          <div className="donly" style={{ flexShrink: 0, display: "flex", gap: 14, alignItems: "center" }}>
            <a href="tel:6122078736" style={{ fontSize: 14, fontWeight: 800, color: scrolled ? N : "white", textDecoration: "none", letterSpacing: "0.04em" }}>612-207-8736</a>
            <span className="btn-r" style={{ padding: "10px 22px" }} onClick={() => go("#contact")}>Book Now</span>
          </div>

          <button className="monly" style={{ marginLeft: "auto", background: "none", border: "none", cursor: "pointer", padding: 6, display: "flex", flexDirection: "column", gap: 5 }} onClick={() => setMenuOpen(!menuOpen)}>
            {[0, 1, 2].map(i => <span key={i} style={{ display: "block", width: 24, height: 2.5, background: scrolled ? N : "white", borderRadius: 1, transition: "all 0.28s", transform: menuOpen ? (i === 0 ? "rotate(45deg) translateY(7.5px)" : i === 2 ? "rotate(-45deg) translateY(-7.5px)" : "none") : "none", opacity: menuOpen && i === 1 ? 0 : 1 }} />)}
          </button>
        </div>
        {menuOpen && (
          <div style={{ background: N, padding: "24px 40px 32px" }}>
            {NAV_LINKS.map(l => <div key={l.label} className="nlink" style={{ display: "block", padding: "13px 0", fontSize: 15, color: "white", borderBottom: "1px solid rgba(255,255,255,0.07)" }} onClick={() => go(l.href)}>{l.label}</div>)}
            <div style={{ marginTop: 24, display: "flex", flexDirection: "column", gap: 12 }}>
              <a href="tel:6122078736" className="bb" style={{ color: "white", textDecoration: "none", fontSize: 26 }}>612-207-8736</a>
              <span className="btn-r" style={{ textAlign: "center" }} onClick={() => go("#contact")}>Book Now</span>
            </div>
          </div>
        )}
      </nav>

      {/* HERO */}
      <section style={{ minHeight: "100vh", background: N, display: "flex", alignItems: "center", position: "relative", overflow: "hidden" }}>
        <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=1400&q=80" alt="" style={{ position: "absolute", inset: 0, width: "100%", height: "100%", objectFit: "cover", opacity: 0.15 }} />
        <div style={{ position: "absolute", bottom: 0, left: 0, right: 0, height: 5, background: R }} />
        <div style={{ position: "absolute", top: 0, left: 0, bottom: 0, width: 5, background: R }} />

        <div style={{ maxWidth: 1280, margin: "0 auto", padding: "130px 40px 100px", position: "relative", zIndex: 1, width: "100%" }}>
          <div className="a1" style={{ display: "inline-flex", alignItems: "center", gap: 8, marginBottom: 32, background: R, padding: "6px 16px" }}>
            <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>Twin Cities · Minneapolis Metro</span>
          </div>

          <h1 className="bb a2" style={{ fontSize: "clamp(68px, 11vw, 140px)", lineHeight: 0.93, color: "white", marginBottom: 0 }}>
            We Transform<br />
            <span style={{ color: R, WebkitTextStroke: "0px" }}>Garages.</span>
          </h1>
          <h1 className="bb a3" style={{ fontSize: "clamp(68px, 11vw, 140px)", lineHeight: 0.93, color: "rgba(255,255,255,0.12)", WebkitTextStroke: "1px rgba(255,255,255,0.2)", marginBottom: 40 }}>
            Completely.
          </h1>

          <div className="a3" style={{ width: 64, height: 5, background: R, marginBottom: 32 }} />

          <p className="a4" style={{ fontSize: "clamp(16px, 2vw, 20px)", color: "rgba(255,255,255,0.65)", maxWidth: 520, lineHeight: 1.75, marginBottom: 44, fontWeight: 400 }}>
            One call. One flat price of $650. We haul everything out, sweep it clean, and hand you back a garage you'll actually want to use.
          </p>

          <div className="a5" style={{ display: "flex", gap: 16, flexWrap: "wrap", marginBottom: 56 }}>
            <span className="btn-r" style={{ fontSize: 14, padding: "17px 40px" }} onClick={() => go("#contact")}>Book Your Cleanout — $650 Flat</span>
            <a href="tel:6122078736" className="btn-w" style={{ fontSize: 14, padding: "15px 40px" }}>Call 612-207-8736</a>
          </div>

          <div className="a5" style={{ display: "flex", gap: 32, flexWrap: "wrap" }}>
            {["$650 All-In Price", "Full Haul-Away", "Same-Week Service", "Locally Owned"].map(t => (
              <div key={t} style={{ display: "flex", alignItems: "center", gap: 9, color: "rgba(255,255,255,0.5)", fontSize: 13, fontWeight: 700, letterSpacing: "0.05em", textTransform: "uppercase" }}>
                <span style={{ color: R, fontSize: 16, flexShrink: 0 }}>✓</span> {t}
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* RED STATEMENT BAND */}
      <section style={{ background: R, padding: "32px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto", display: "flex", justifyContent: "space-between", alignItems: "center", flexWrap: "wrap", gap: 20 }}>
          <div className="bb" style={{ fontSize: "clamp(22px, 3.5vw, 44px)", color: "white", lineHeight: 1 }}>
            We Show Up. We Clean It Out. You Get Your Garage Back.
          </div>
          <span className="btn-w" style={{ flexShrink: 0 }} onClick={() => go("#contact")}>Book Now</span>
        </div>
      </section>

      {/* BEFORE & AFTER */}
      <section id="services" style={{ background: O, padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto" }}>
          <Reveal>
            <div style={{ marginBottom: 60 }}>
              <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>The Transformation</span>
              </div>
              <h2 className="bb" style={{ fontSize: "clamp(40px, 6vw, 82px)", color: N, lineHeight: 0.95 }}>Real Garages.<br />Real Results.</h2>
              <p style={{ marginTop: 20, fontSize: 16, color: "#666", maxWidth: 460, lineHeight: 1.7 }}>
                Drag the slider. This is standard work — not cherry-picked. Every cleanout looks like this.
              </p>
            </div>
          </Reveal>

          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(340px, 1fr))", gap: 18 }}>
            {BEFORE_AFTERS.map((p, i) => <Reveal key={p.label} delay={i * 100}><Slider {...p} /></Reveal>)}
          </div>
        </div>
      </section>

      {/* PHOTO GALLERY */}
      <section style={{ background: N, padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto" }}>
          <Reveal>
            <div style={{ marginBottom: 56, display: "flex", justifyContent: "space-between", alignItems: "flex-end", flexWrap: "wrap", gap: 20 }}>
              <div>
                <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                  <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>Our Work</span>
                </div>
                <h2 className="bb" style={{ fontSize: "clamp(40px, 6vw, 82px)", color: "white", lineHeight: 1 }}>
                  Clean. Clear. <span style={{ color: R }}>Done.</span>
                </h2>
              </div>
              <span className="btn-r" onClick={() => go("#contact")} style={{ alignSelf: "flex-end" }}>Book a Cleanout</span>
            </div>
          </Reveal>

          {/* Desktop mosaic */}
          <div className="donly" style={{ display: "grid", gridTemplateColumns: "1.2fr 1fr 1fr", gridTemplateRows: "260px 260px", gap: 10 }}>
            {[
              { url: GALLERY[0], col: "1/2", row: "1/3" },
              { url: GALLERY[1], col: "2/3", row: "1/2" },
              { url: GALLERY[2], col: "3/4", row: "1/2" },
              { url: GALLERY[3], col: "2/4", row: "2/3" },
            ].map((img, i) => (
              <Reveal key={i} delay={i * 80} style={{ gridColumn: img.col, gridRow: img.row, height: "100%" }}>
                <div className="gcard" style={{ height: "100%" }}>
                  <img src={img.url} alt="" style={{ width: "100%", height: "100%", objectFit: "cover" }} />
                  <div style={{ position: "absolute", inset: 0, background: "rgba(13,27,42,0.25)", transition: "background 0.3s" }} />
                </div>
              </Reveal>
            ))}
          </div>

          {/* Mobile grid */}
          <div className="monly" style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 8 }}>
            {GALLERY.map((url, i) => (
              <div key={i} className="gcard" style={{ aspectRatio: "4/3" }}>
                <img src={url} alt="" style={{ width: "100%", height: "100%", objectFit: "cover" }} />
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* PRICING */}
      <section id="pricing" style={{ background: "white", padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto", display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(320px, 1fr))", gap: 72, alignItems: "center" }}>
          <Reveal>
            <div>
              <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>Pricing</span>
              </div>
              <h2 className="bb" style={{ fontSize: "clamp(40px, 6vw, 82px)", color: N, lineHeight: 0.95, marginBottom: 24 }}>
                One Price.<br />No Surprises.<br /><span style={{ color: R }}>Ever.</span>
              </h2>
              <p style={{ fontSize: 16, color: "#555", lineHeight: 1.85, marginBottom: 40 }}>
                $650 covers everything — labor, loading, haul-away, and a final sweep. No itemized fees, no fuel surcharges, no add-ons after the fact. You see the price before we start. That's the price you pay.
              </p>
              <span className="btn-r" style={{ padding: "16px 40px", fontSize: 14 }} onClick={() => go("#contact")}>Book for $650 — All-In</span>
            </div>
          </Reveal>

          <Reveal delay={150}>
            <div>
              <div style={{ background: R, padding: "32px 40px 28px" }}>
                <div className="bb" style={{ fontSize: 96, color: "white", lineHeight: 1 }}>$650</div>
                <div style={{ fontSize: 12, fontWeight: 800, letterSpacing: "0.16em", textTransform: "uppercase", color: "rgba(255,255,255,0.7)", marginTop: 4 }}>Flat Rate · All-Inclusive</div>
              </div>
              <div style={{ background: N }}>
                {[
                  "Complete haul-away — we take everything",
                  "Floor swept clean at finish",
                  "Same-week appointments available",
                  "No hidden fees, no add-ons",
                  "Locally owned Twin Cities company",
                ].map((item, i) => (
                  <div key={i} style={{ display: "flex", alignItems: "center", gap: 14, padding: "15px 36px", borderBottom: i < 4 ? "1px solid rgba(255,255,255,0.06)" : "none" }}>
                    <span style={{ color: R, fontSize: 17, flexShrink: 0 }}>✓</span>
                    <span style={{ color: "rgba(255,255,255,0.8)", fontSize: 14.5, fontWeight: 500 }}>{item}</span>
                  </div>
                ))}
              </div>
            </div>
          </Reveal>
        </div>
      </section>

      {/* PROCESS */}
      <section id="process" style={{ background: O, padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto" }}>
          <Reveal>
            <div style={{ textAlign: "center", marginBottom: 72 }}>
              <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>How It Works</span>
              </div>
              <h2 className="bb" style={{ fontSize: "clamp(40px, 6vw, 82px)", color: N, lineHeight: 1 }}>
                Three Steps. <span style={{ color: R }}>That's It.</span>
              </h2>
            </div>
          </Reveal>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(280px, 1fr))", gap: 40 }}>
            {[
              { n: "01", t: "Book in Minutes", b: "Fill out the contact form or call us. We'll confirm within 24 hours and lock in a time — often same week." },
              { n: "02", t: "We Show Up & Get Moving", b: "Our crew arrives on time, loaded and ready. We haul everything out, sort donations, and take the rest away." },
              { n: "03", t: "Your Garage Is Done", b: "We sweep, do a final walkthrough with you, and collect payment. Clean, clear, and handed back to you." },
            ].map((s, i) => (
              <Reveal key={s.n} delay={i * 130}>
                <div style={{ position: "relative", paddingTop: 56 }}>
                  <div className="bb" style={{ position: "absolute", top: -12, left: -6, fontSize: 96, color: R, opacity: 0.1, lineHeight: 1 }}>{s.n}</div>
                  <div style={{ position: "relative", zIndex: 1 }}>
                    <div style={{ width: 40, height: 4, background: R, marginBottom: 20 }} />
                    <div style={{ fontSize: 11, fontWeight: 800, letterSpacing: "0.18em", textTransform: "uppercase", color: R, marginBottom: 12 }}>Step {s.n}</div>
                    <h3 className="bb" style={{ fontSize: 30, color: N, marginBottom: 14 }}>{s.t}</h3>
                    <p style={{ fontSize: 15, lineHeight: 1.8, color: "#666" }}>{s.b}</p>
                  </div>
                </div>
              </Reveal>
            ))}
          </div>
        </div>
      </section>

      {/* WHY US */}
      <section style={{ background: "white", padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto" }}>
          <Reveal>
            <div style={{ marginBottom: 60 }}>
              <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>Why Pristine</span>
              </div>
              <h2 className="bb" style={{ fontSize: "clamp(40px, 6vw, 82px)", color: N, lineHeight: 0.95 }}>
                Garage Cleanout<br /><span style={{ color: R }}>Done Right.</span>
              </h2>
            </div>
          </Reveal>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(260px, 1fr))", gap: 4 }}>
            {[
              { t: "Flat $650 — No Exceptions", b: "No add-ons, no itemized fees, no surprises. One price. Always." },
              { t: "Same-Week Scheduling", b: "Most clients are booked within 3–5 days. We don't make you wait." },
              { t: "Everything Hauled Away", b: "Furniture, tools, boxes, bikes — we load it all and take it with us. Zero left behind." },
              { t: "Locally Owned", b: "Twin Cities company, not a franchise. We live here too." },
            ].map((item, i) => (
              <Reveal key={item.t} delay={i * 80}>
                <div style={{ borderLeft: `4px solid ${R}`, padding: "28px 30px", background: O, transition: "background 0.2s", cursor: "default" }}
                  onMouseEnter={e => e.currentTarget.style.background = "#FFE9E2"}
                  onMouseLeave={e => e.currentTarget.style.background = O}>
                  <h3 className="bb" style={{ fontSize: 22, color: N, marginBottom: 10 }}>{item.t}</h3>
                  <p style={{ fontSize: 14.5, lineHeight: 1.8, color: "#666" }}>{item.b}</p>
                </div>
              </Reveal>
            ))}
          </div>
        </div>
      </section>

      {/* REVIEWS */}
      <section id="reviews" style={{ background: N, padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto" }}>
          <Reveal>
            <div style={{ marginBottom: 60 }}>
              <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>Client Reviews</span>
              </div>
              <h2 className="bb" style={{ fontSize: "clamp(40px, 6vw, 82px)", color: "white", lineHeight: 1 }}>
                Twin Cities Homeowners<br /><span style={{ color: R }}>Love The Result.</span>
              </h2>
            </div>
          </Reveal>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill, minmax(290px, 1fr))", gap: 16 }}>
            {TESTIMONIALS.map((t, i) => (
              <Reveal key={t.name} delay={i * 65}>
                <div className="tcard" style={{ height: "100%" }}>
                  <div style={{ display: "flex", gap: 3, marginBottom: 18 }}>{[...Array(5)].map((_, j) => <span key={j} style={{ color: R, fontSize: 17 }}>★</span>)}</div>
                  <p style={{ fontSize: 14.5, lineHeight: 1.9, color: "#444", marginBottom: 24, fontStyle: "italic" }}>"{t.text}"</p>
                  <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
                    <div style={{ width: 42, height: 42, borderRadius: "50%", background: R, display: "flex", alignItems: "center", justifyContent: "center", flexShrink: 0 }}>
                      <span style={{ fontSize: 12, fontWeight: 800, color: "white" }}>{t.initials}</span>
                    </div>
                    <div>
                      <div style={{ fontSize: 14, fontWeight: 800, color: N }}>{t.name}</div>
                      <div style={{ fontSize: 12, color: "#888", marginTop: 2 }}>{t.neighborhood}, MN</div>
                    </div>
                  </div>
                </div>
              </Reveal>
            ))}
          </div>
        </div>
      </section>

      {/* CTA BAND */}
      <section style={{ background: R, padding: "72px 40px" }}>
        <Reveal>
          <div style={{ maxWidth: 1280, margin: "0 auto", display: "flex", justifyContent: "space-between", alignItems: "center", flexWrap: "wrap", gap: 28 }}>
            <div>
              <h2 className="bb" style={{ fontSize: "clamp(32px, 5vw, 68px)", color: "white", lineHeight: 1, marginBottom: 10 }}>Ready To Reclaim Your Garage?</h2>
              <p style={{ fontSize: 16, color: "rgba(255,255,255,0.75)", fontWeight: 500 }}>Call us today — most bookings land within the same week.</p>
            </div>
            <div style={{ display: "flex", gap: 16, flexWrap: "wrap" }}>
              <span className="btn-w" onClick={() => go("#contact")}>Book Online</span>
              <a href="tel:6122078736" className="btn-w">612-207-8736</a>
            </div>
          </div>
        </Reveal>
      </section>

      {/* CONTACT */}
      <section id="contact" style={{ background: "white", padding: "96px 40px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto", display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(320px, 1fr))", gap: 72, alignItems: "start" }}>
          <Reveal>
            <div>
              <div style={{ display: "inline-block", background: R, padding: "5px 14px", marginBottom: 20 }}>
                <span style={{ color: "white", fontSize: 11, fontWeight: 800, letterSpacing: "0.2em", textTransform: "uppercase" }}>Book a Cleanout</span>
              </div>
              <h2 className="bb" style={{ fontSize: "clamp(36px, 5vw, 68px)", color: N, lineHeight: 0.95, marginBottom: 24 }}>
                Let's Get Your<br /><span style={{ color: R }}>Garage Done.</span>
              </h2>
              <p style={{ fontSize: 15.5, lineHeight: 1.85, color: "#555", marginBottom: 48 }}>
                Fill out the form and we'll reach out within 24 hours. Prefer to talk? Call or text — we pick up.
              </p>
              {[
                { label: "Phone / Text", val: "612-207-8736", href: "tel:6122078736", big: true },
                { label: "Email", val: "pristinegarageco@gmail.com", href: "mailto:pristinegarageco@gmail.com" },
                { label: "Service Area", val: "Twin Cities & Minneapolis Metro" },
              ].map(item => (
                <div key={item.label} style={{ borderLeft: `4px solid ${R}`, paddingLeft: 20, marginBottom: 28 }}>
                  <div style={{ fontSize: 11, fontWeight: 800, letterSpacing: "0.16em", textTransform: "uppercase", color: "#aaa", marginBottom: 5 }}>{item.label}</div>
                  {item.href
                    ? <a href={item.href} className={item.big ? "bb" : ""} style={{ fontSize: item.big ? 30 : 15, color: N, textDecoration: "none", fontWeight: item.big ? 400 : 600, display: "block" }}>{item.val}</a>
                    : <div style={{ fontSize: 15, color: N, fontWeight: 600 }}>{item.val}</div>}
                </div>
              ))}
            </div>
          </Reveal>

          <Reveal delay={150}>
            {done ? (
              <div style={{ background: N, padding: "56px 44px", textAlign: "center" }}>
                <div style={{ width: 60, height: 60, borderRadius: "50%", background: R, display: "flex", alignItems: "center", justifyContent: "center", margin: "0 auto 24px", fontSize: 24, color: "white" }}>✓</div>
                <h3 className="bb" style={{ fontSize: 40, color: "white", marginBottom: 16 }}>Request Received</h3>
                <p style={{ fontSize: 15, lineHeight: 1.8, color: "rgba(255,255,255,0.6)" }}>We'll reach out within 24 hours. Need us sooner? Call or text <strong style={{ color: "white" }}>612-207-8736</strong>.</p>
              </div>
            ) : (
              <form onSubmit={e => { e.preventDefault(); setDone(true); }} style={{ display: "flex", flexDirection: "column", gap: 18 }}>
                <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 14 }}>
                  <div><label>Full Name</label><input required placeholder="Jane Smith" value={form.name} onChange={e => setForm({ ...form, name: e.target.value })} /></div>
                  <div><label>Phone</label><input required placeholder="612-555-0000" value={form.phone} onChange={e => setForm({ ...form, phone: e.target.value })} /></div>
                </div>
                <div><label>Home Address</label><input required placeholder="123 Main St, Minneapolis, MN" value={form.address} onChange={e => setForm({ ...form, address: e.target.value })} /></div>
                <div>
                  <label>Garage Size</label>
                  <select required value={form.size} onChange={e => setForm({ ...form, size: e.target.value })}>
                    <option value="">Select size…</option>
                    <option>1-Car Garage</option>
                    <option>2-Car Garage</option>
                    <option>3-Car Garage</option>
                    <option>Oversized / Not Sure</option>
                  </select>
                </div>
                <div><label>Tell Us About the Space (optional)</label><textarea rows={4} placeholder="Old furniture, boxes, tools — give us a heads up." value={form.message} onChange={e => setForm({ ...form, message: e.target.value })} style={{ resize: "none" }} /></div>
                <button type="submit" className="btn-r" style={{ fontSize: 14, padding: "17px", width: "100%", textAlign: "center" }}>Request My Cleanout — $650 Flat</button>
                <p style={{ fontSize: 12, color: "#aaa", textAlign: "center", fontWeight: 500 }}>We confirm within 24 hours. No commitment until we talk.</p>
              </form>
            )}
          </Reveal>
        </div>
      </section>

      {/* FOOTER */}
      <footer style={{ background: N, padding: "64px 40px 32px" }}>
        <div style={{ maxWidth: 1280, margin: "0 auto" }}>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(200px, 1fr))", gap: 48, marginBottom: 52 }}>
            <div>
              <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 18 }}>
                <svg width="30" height="30" viewBox="0 0 36 36" fill="none"><rect width="36" height="36" fill={R} /><path d="M7 27V17L18 11L29 17V27" stroke="white" strokeWidth="2" fill="none" strokeLinejoin="round" /><rect x="14" y="20" width="8" height="7" fill="white" rx="1" /><line x1="7" y1="27" x2="29" y2="27" stroke="white" strokeWidth="2" /></svg>
                <span className="bb" style={{ fontSize: 18, color: "white", letterSpacing: "0.05em" }}>Pristine Garage Co.</span>
              </div>
              <p style={{ fontSize: 13.5, lineHeight: 1.8, color: "#444" }}>Twin Cities garage cleanout specialists. Flat rate. Fast scheduling. Done right.</p>
            </div>
            <div>
              <div style={{ fontSize: 11, fontWeight: 800, letterSpacing: "0.18em", textTransform: "uppercase", color: "#333", marginBottom: 18 }}>Navigate</div>
              {NAV_LINKS.map(l => <div key={l.label} className="nlink" style={{ display: "block", marginBottom: 10, fontSize: 13, color: "#444" }} onClick={() => go(l.href)}>{l.label}</div>)}
            </div>
            <div>
              <div style={{ fontSize: 11, fontWeight: 800, letterSpacing: "0.18em", textTransform: "uppercase", color: "#333", marginBottom: 18 }}>Service Area</div>
              {["Minneapolis", "St. Paul", "Edina", "Plymouth", "Minnetonka", "Wayzata", "Rosemount", "Burnsville", "Eagan", "Eden Prairie"].map(c => <div key={c} style={{ fontSize: 13, color: "#444", marginBottom: 6 }}>{c}</div>)}
            </div>
            <div>
              <div style={{ fontSize: 11, fontWeight: 800, letterSpacing: "0.18em", textTransform: "uppercase", color: "#333", marginBottom: 18 }}>Contact</div>
              <a href="tel:6122078736" className="bb" style={{ fontSize: 32, color: "white", textDecoration: "none", display: "block", marginBottom: 4, letterSpacing: "0.04em" }}>612-207-8736</a>
              <div style={{ fontSize: 11, fontWeight: 700, color: "#333", letterSpacing: "0.1em", textTransform: "uppercase", marginBottom: 14 }}>Call or Text</div>
              <a href="mailto:pristinegarageco@gmail.com" style={{ fontSize: 13, color: "#444", textDecoration: "none", display: "block", marginBottom: 28 }}>pristinegarageco@gmail.com</a>
              <span className="btn-r" onClick={() => go("#contact")}>Book Now — $650</span>
            </div>
          </div>
          <div style={{ borderTop: "1px solid #1E2E3F", paddingTop: 22, display: "flex", justifyContent: "space-between", flexWrap: "wrap", gap: 12 }}>
            <span style={{ fontSize: 12, color: "#333" }}>© {new Date().getFullYear()} Pristine Garage Co. · Twin Cities, MN</span>
            <span style={{ fontSize: 12, color: "#333" }}>Locally owned & operated</span>
          </div>
        </div>
      </footer>
    </div>
  );
}
