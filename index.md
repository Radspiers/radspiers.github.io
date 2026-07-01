<!-- Full Width Fixed Navigation Bar -->
<div style="position: fixed; top: 0; left: 0; width: 100vw; background-color: #24292e; color: #fff; padding: 12px 40px; display: flex; justify-content: space-between; align-items: center; z-index: 9999; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; box-shadow: 0 2px 10px rgba(0,0,0,0.35); box-sizing: border-box;">
    
    <!-- Left: Your Name -->
    <span style="font-weight: bold; font-size: 1.15rem; color: #fff; letter-spacing: 0.5px;">Richard Spiers</span>
    
    <!-- Center: Navigation Links -->
    <div style="display: flex; gap: 24px;">
        <a href="#about" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">About Me</a>
        <a href="#skills" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Skills</a>
        <a href="#work" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Professional Experience</a>
        <a href="#projects" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Personal Projects</a>
        <a href="#game-jams" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Game Jams</a>
        <a href="#education" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Education</a>
        <a href="#contact" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Contact</a>
    </div>
    
    <!-- Right: Icons -->
    <div style="display: flex; gap: 20px; align-items: center; padding-right: 20px;">
        <!-- LinkedIn Icon Link -->
        <a href="https://linkedin.com/in/richardspiers" target="_blank" style="color: #fff; text-decoration: none; display: flex; align-items: center;">
            <svg height="22" width="22" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
        </a>
        <!-- Email Icon Link -->
        <a href="mailto:zeterlore@hotmail.com" style="color: #fff; text-decoration: none; display: flex; align-items: center;">
            <svg height="22" width="22" viewBox="0 0 24 24" fill="currentColor"><path d="M0 3v18h24v-18h-24zm21.518 2l-9.518 7.713-9.518-7.713h19.036zm-19.518 14v-11.817l10 8.104 10-8.104v11.817h-20z"/></svg>
        </a>
    </div>
</div>

<style>
/* 1. Global Reset: Let sections go completely edge-to-edge natively */
  html, body {
    margin: 0 !important;
    padding: 0 !important;
    width: 100% !important;
    overflow-x: hidden;
    background-color: #fafbfc;
  }

  /* Remove the body flex rules entirely—they are causing the ghost boxes */
.container-lg, .wrapper, main {
    max-width: none !important;
    padding: 0 !important;
    margin: 0 !important;
    display: block !important; 
  }

/* Completely hide automatic markdown header link icons on hover */
h1 a, h2 a, h3 a, h4 a,
  h1 a:hover, h2 a:hover, h3 a:hover,
  [id^="anchor"], .anchor-link {
    display: none !important;
    opacity: 0 !important;
    visibility: hidden !important;
    width: 0 !important;
    height: 0 !important;
    position: absolute !important;
    pointer-events: none !important;
  }

/* Force the about section to flush with the absolute top of the window canvas */
#about {
    /* Put it back in the normal document flow */
    position: relative !important;
    
    /* PULL IT UP: This physically drags the box up to swallow that ~1/2cm gap */
    margin-top: -24px !important; 
    
    /* Safety reset to ensure it stays full width */
    width: 100% !important;
    left: 0 !important;
    top: 0 !important;
}

/* Ensure the next sections have clean breathing room and don't bunch up */
#skills, #projects, #game-jams, #education, #contact  {
    position: relative !important;
    clear: both;
}
    
  #about h1 {
    margin-top: 0 !important;
    padding-top: 0 !important;
  }

  /* Target your navigation element to make sure it doesn't push down */
  nav, .nav-bar, .navigation {
    margin-bottom: 0 !important;
    padding-bottom: 0 !important;
  }

/* Game Jam Fluid Centered Layout */
  .jam-grid {
    display: flex;
    flex-wrap: wrap;          /* Allows cards to smoothly drop to the next row */
    justify-content: center;  /* PERFECTLY CENTERS both rows, including leftover cards! */
    gap: 30px;
    max-width: 1350px;
    width: 100%;
    margin: 0 auto;
    box-sizing: border-box;
  }

  /* Game Jam Card Structure */
  .jam-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    
    /* ---> WE ASSIGN A FLEX BASIS INSTEAD OF 100% WIDTH <--- */
    width: calc(33.333% - 20px); /* Perfectly sizes them to match your 3-column look */
    min-width: 350px;            /* Prevents them from getting too thin on smaller screens */
    max-width: 430px;            /* Prevents them from bloating on massive screens */
  }

  /* Consistent Hover State */
  .jam-card:hover {
    transform: translateY(-6px);
    border-color: #ff0000;
    box-shadow: 0 12px 24px rgba(255, 0, 0, 0.08);
  }

  /* Video Frame Aspect Ratio */
  .video-frame-holder {
    position: relative;
    width: 100%;
    aspect-ratio: 16 / 9;
  }

  .video-frame-holder iframe {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    border: 0;
  }

  .tech-tag {
    display: inline-block;
    background-color: #f1f8ff;
    color: #0366d6;
    padding: 4px 10px;
    font-size: 0.75rem;
    font-weight: 600;
    border-radius: 20px;
    margin: 4px;
  }

/* Education Card Layout & Hover States */
  .edu-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    padding: 30px;
    flex: 1 1 45%; /* Dynamically balances rows if you have 1, 2, or more degrees */
    max-width: 500px;
    min-width: 290px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    text-decoration: none !important;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: center;
    align-items: center;
  }

  .edu-card:hover {
    transform: translateY(-6px);
    border-color: #28a745; /* Clean, professional green accent highlight for education achievements */
    box-shadow: 0 12px 20px rgba(40, 167, 69, 0.12);
  }

  .edu-btn {
    display: inline-block;
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #24292e;
    color: #ffffff !important;
    border-radius: 6px;
    font-size: 0.9rem;
    font-weight: 600;
    text-align: center;
    transition: background-color 0.2s;
    width: 80%;
    max-width: 200px;
  }

  .edu-card:hover .edu-btn {
    background-color: #28a745; /* Button syncs with the green hover highlight */
  }
    
/* Contact Card Styling & Animations */
  .contact-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    padding: 25px 20px;
    flex: 1 1 30%; /* Tells the browser to grow/shrink equally and aim for exactly 30% width */
    min-width: 220px; /* Lowers the minimum restriction so they don't break the row on medium screens */
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    transition: all 0.3s ease-in-out;
    text-decoration: none !important;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: center;
    align-items: center;
  }
  
  /* The Lift and Highlight Effect */
  .contact-card:hover {
    transform: translateY(-8px);
    border-color: #0366d6; /* Highlights the border with a clean blue */
    box-shadow: 0 12px 24px rgba(3, 102, 214, 0.15); /* Soft glowing shadow */
  }

  /* Interactive Button inside the Card */
  .contact-btn {
    display: inline-block;
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #24292e;
    color: #ffffff !important;
    border-radius: 6px;
    font-size: 0.9rem;
    font-weight: 600;
    text-align: center;
    transition: background-color 0.2s;
  }
  
  .contact-card:hover .contact-btn {
    background-color: #0366d6; /* Button lights up blue when card is hovered */
  }

/* Completely hide the default Cayman theme footer text */
  .site-footer {
    display: none !important;
  }

</style>

<!-- Full Screen About Me Container (Flushed to Navbar) -->
<div id="about" style="width: 100%; background-color: #7242f5; display: flex; justify-content: center; align-items: center; box-sizing: border-box; padding: 180px 0 140px 0; margin: 0;">
    
    <div style="width: 100%; max-width: 54rem; padding: 0 40px; box-sizing: border-box; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
        
        <h1 style="font-size: 2.8rem; color: #24292e; margin-top: 0; margin-bottom: 10px; border-bottom: none; font-weight: 700;">Rad Spiers</h1>
        <p style="font-size: 1.4rem; color: #586069; margin-top: 0; font-weight: 400; letter-spacing: -0.5px;">Senior Systems & Infrastructure Engineer</p>
        
        <div style="font-size: 1.15rem; line-height: 1.7; color: #2f363d; margin-top: 30px;">
            <p>AAA Software Engineer with over a decade of experience specializing in core engine systems, automated build infrastructure, and performance optimization. Proven track record of delivering stable pipelines and decoupling complex software architectures within high-stakes studio environments.</p>
            <p>Focused on engineering pragmatism, maintainable systems, and cross-department tool collaboration.</p>
        </div>

    </div>
</div>

<!-- Section: Skills -->
<div id="skills" style="width: 100%; background-color: #ffffff; padding: 60px 0; box-sizing: border-box; margin: 0;">
    
    <!-- Section Header Title -->
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 40px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-weight: 700;">Skills & Expertise</h2>

    <!-- Centered Fluid Grid Container -->
    <div class="jam-grid">
        
        <!-- ==================== CARD 1: LANGUAGES ==================== -->
        <!-- Scaled down using width calculations and reduced padding -->
        <div class="jam-card" style="aspect-ratio: 1 / 1; width: calc(18% - 15px); min-width: 200px; max-width: 240px; align-items: center; justify-content: center; text-align: center; padding: 20px; box-sizing: border-box;">
            
            <!-- Iconography: Code Brackets </> (Scaled to 36px) -->
            <div style="color: #0366d6; margin-bottom: 12px; width: 36px; height: 36px;">
                <svg viewBox="0 0 24 24" width="36" height="36" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <polyline points="16 18 22 12 16 6"></polyline>
                    <polyline points="8 6 2 12 8 18"></polyline>
                </svg>
            </div>
            
            <!-- Title: Scaled to 1.1rem -->
            <h3 style="font-size: 1.1rem; color: #24292e; margin: 0 0 8px 0; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">Languages</h3>
            
            <!-- Description Text: Scaled to 0.85rem -->
            <p style="font-size: 0.85rem; color: #586069; line-height: 1.5; margin: 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
                C++, C#, Python, SQL, x86 Assembly
            </p>
        </div>

        <!-- ==================== CARD 2: SYSTEMS ==================== -->
        <div class="jam-card" style="aspect-ratio: 1 / 1; width: calc(18% - 15px); min-width: 200px; max-width: 240px; align-items: center; justify-content: center; text-align: center; padding: 20px; box-sizing: border-box;">
            
            <!-- Iconography: Engine / Processor Gear -->
            <div style="color: #28a745; margin-bottom: 12px; width: 36px; height: 36px;">
                <svg viewBox="0 0 24 24" width="36" height="36" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <circle cx="12" cy="12" r="3"></circle>
                    <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 1 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 1 1-2.83-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 1 1 2.83-2.83l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 1 1 2.83 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z"></path>
                </svg>
            </div>
            
            <h3 style="font-size: 1.1rem; color: #24292e; margin: 0 0 8px 0; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">Core Systems</h3>
            
            <p style="font-size: 0.85rem; color: #586069; line-height: 1.5; margin: 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
                Unreal Engine runtime, Memory Arenas, Profiling, Decoupling
            </p>
        </div>

        <!-- ==================== CARD 3: INFRASTRUCTURE ==================== -->
        <div class="jam-card" style="aspect-ratio: 1 / 1; width: calc(18% - 15px); min-width: 200px; max-width: 240px; align-items: center; justify-content: center; text-align: center; padding: 20px; box-sizing: border-box;">
            
            <!-- Iconography: Server / Pipeline Stack -->
            <div style="color: #6f42c1; margin-bottom: 12px; width: 36px; height: 36px;">
                <svg viewBox="0 0 24 24" width="36" height="36" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <line x1="22" y1="12" x2="2" y2="12"></line>
                    <path d="M5.45 5.11L2 12v6a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-6l-3.45-6.89A2 2 0 0 0 16.76 4H7.24a2 2 0 0 0-1.79 1.11z"></path>
                    <line x1="6" y1="16" x2="6.01" y2="16"></line>
                    <line x1="10" y1="16" x2="10.01" y2="16"></line>
                </svg>
            </div>
            
            <h3 style="font-size: 1.1rem; color: #24292e; margin: 0 0 8px 0; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">Infrastructure</h3>
            
            <p style="font-size: 0.85rem; color: #586069; line-height: 1.5; margin: 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
                CI/CD Pipelines, Windows Tools, Automated Builds, Cook Optimization
            </p>
        </div>

        <!-- ==================== CARD 4: COLLABORATION ==================== -->
        <div class="jam-card" style="aspect-ratio: 1 / 1; width: calc(18% - 15px); min-width: 200px; max-width: 240px; align-items: center; justify-content: center; text-align: center; padding: 20px; box-sizing: border-box;">
            
            <!-- Iconography: Users / Studio Collaboration -->
            <div style="color: #e36209; margin-bottom: 12px; width: 36px; height: 36px;">
                <svg viewBox="0 0 24 24" width="36" height="36" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path>
                    <circle cx="9" cy="7" r="4"></circle>
                    <path d="M23 21v-2a4 4 0 0 0-3-3.87"></path>
                    <path d="M16 3.13a4 4 0 0 1 0 7.75"></path>
                </svg>
            </div>
            
            <h3 style="font-size: 1.1rem; color: #24292e; margin: 0 0 8px 0; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">Methodology</h3>
            
            <p style="font-size: 0.85rem; color: #586069; line-height: 1.5; margin: 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
                Developer Productivity, QA Automation, Cross-Dept Tools, AAA Delivery
            </p>
        </div>

    </div>
</div>

<!-- Section: Professional Experience -->
<div id="work" style="margin-top: 80px; padding: 60px 0; border-top: 1px solid #e1e4e8;">
    
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 50px; font-weight: 700; border-bottom: none;">Professional Experience</h2>

    <div class="jam-grid">
            
        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/3QHZxzTPsco?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Suicide Squad: Kill the Justice League</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Automation Engineer | October 2016 - December 2024</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Rocksteady Studios</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">QA</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/SwdZvJfxqtE?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Batman: Arkham VR</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Senior QA for AI | June 2015 - October 2016</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Rocksteady Studios</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/wsf78BS9VE0?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Batman: Arkham Knight</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">QA for AI | April 2014 - June 2015</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Rocksteady Studios</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/IjvKWtefU9c?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Strike Suit Zero: Director's Cut</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Senior Compliance QA | December 2013 - March 2013</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Born Ready Games</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/APMrtUd4WW8?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">FIFA 14</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Authenticity QA | October 2012 - December 2013</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Electronic Arts Canada</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/Ia43OgdBHaE?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">FIFA 13</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Authenticity QA | October 2011 - September 2012</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Electronic Arts Canada</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/An-E0GOKwvA?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">FIFA 12</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Authenticity QA | April 2011 - September 2011</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Electronic Arts Canada</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/BvuIHSEX6x8?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Fable III</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Quality Assurance | February 2010 - April 2011</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Lionhead Studios</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                </div>
            </div>
        </div>
        
    </div>
</div>

<!-- Section: Personal Projects Entries -->
<div id="projects" style="width: 100%; background-color: #fafbfc; padding: 80px 0; box-sizing: border-box; margin: 0;">
    
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 50px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-weight: 700;">Personal Projects</h2>

    <div class="jam-grid">
        
        <div class="jam-card">
            <div class="video-frame-holder" style="background-color: #e1e4e8;">
                <img src="Pictures/PythonScreenshot2.png" alt="Project Thumbnail" style="width: 100%; height: 100%; object-fit: cover; display: block;" />
            </div>
            
            <div style="padding: 24px; display: flex; flex-direction: column; flex-grow: 1; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
                
                <h3 style="font-size: 1.35rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; line-height: 1.3;">Project Title Alpha</h3>
                
                <span style="font-size: 0.9rem; color: #586069; font-weight: 700; margin-bottom: 16px; display: block; letter-spacing: 0.2px;">2026</span>
                
                <p style="font-size: 0.95rem; color: #444d56; line-height: 1.6; margin: 0 0 24px 0; flex-grow: 1;">
                    A core software architecture system designed to handle high-throughput telemetry data processing. Implemented an optimized memory arena allocator to reduce allocation overhead during intensive runtime ticks.
                </p>
                
                <div style="margin: -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Systems</span>
                    <span class="tech-tag">Optimization</span>
                </div>
                
            </div>
        </div>
        <div class="jam-card">
            <div class="video-frame-holder" style="background-color: #e1e4e8;">
                <img src="Pictures/AutomationFramework.png" alt="Project Thumbnail" style="width: 100%; height: 100%; object-fit: cover; display: block;" />
            </div>
            
            <div style="padding: 24px; display: flex; flex-direction: column; flex-grow: 1; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
                <h3 style="font-size: 1.35rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; line-height: 1.3;">Project Title Beta</h3>
                <span style="font-size: 0.9rem; color: #586069; font-weight: 700; margin-bottom: 16px; display: block; letter-spacing: 0.2px;">2025</span>
                
                <p style="font-size: 0.95rem; color: #444d56; line-height: 1.6; margin: 0 0 24px 0; flex-grow: 1;">
                    Custom built CI/CD build distribution pipeline designed for rapid multi-platform deployment targets. Decoupled asset cooking processes from standard engine execution paths to stabilize development iteration cycles.
                </p>
                
                <div style="margin: -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">Infrastructure</span>
                    <span class="tech-tag">CI/CD</span>
                </div>
            </div>
        </div>
        </div>
</div>

<!-- Section: Game Jams -->
<div id="game-jams" style="margin-top: 80px; padding: 60px 0; border-top: 1px solid #e1e4e8;">
    
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 50px; font-weight: 700; border-bottom: none;">Game Jams</h2>

    <div class="jam-grid">
            
        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/aYPwhwf2uF8?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Shift Happens</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Gameplay Programmer | October 2025</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Minigame Rumble</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/Ruh11qRzqdg?rel=0&modestbranding=1"
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Outdated</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | September 2023</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">Third Person Puzzle Game</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/ZNAHgOnTopw?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">The Banquet Below</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | September 2022</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">FPS Mystery Puzzle Game</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/MQhBs2qRt4c?rel=0&modestbranding=1"
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Malware</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | September 2021</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">2D Puzzle Platformer</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>
            </div>
        </div>

        <div class="jam-card">
            <div class="video-frame-holder">
                <iframe 
                    src="https://www.youtube.com/embed/y_-oG3KM9LY?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Time Janitors</h3>
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | September 2020</div>
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">FPS Time Travel Puzzle Adventure</div>
                
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                </div>
            </div>
        </div>
        
    </div>
</div>


<!-- Section: Education -->
<div id="education" style="margin-top: 80px; padding: 60px 0; border-top: 1px solid #e1e4e8; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
    
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 40px; font-weight: 700; border-bottom: none;">Education</h2>
    
    <!-- Education Grid Row -->
    <div style="display: flex; gap: 24px; justify-content: center; flex-wrap: wrap; max-width: 68rem; margin: 0 auto; padding: 0 20px; box-sizing: border-box;">
        
        <!-- Degree Card 1 -->
        <a href="https://www.beds.ac.uk" target="_blank" class="edu-card">
            <div style="display: flex; flex-direction: column; align-items: center;">
                
                <div style="color: #24292e; margin-bottom: 15px; display: flex; justify-content: center;">
                    <svg height="45" width="45" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c0 2 2 3 6 3s6-1 6-3v-5"/></svg>
                </div>
                
                <h3 style="font-size: 1.25rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; line-height: 1.3;">Artifical Intelligence & Robotics (BSc)</h3>
                
                <span style="font-size: 1rem; color: #586069; font-weight: 500; margin-bottom: 16px;">University of Bedfordshire</span>
                
                <span style="font-size: 1.1rem; color: #24292e; font-weight: 700; letter-spacing: 0.5px;">2003 — 2006</span>
            </div>
            <div class="edu-btn">Visit Institution</div>
        </a>

    </div>
</div>

<div id="contact" style="margin-top: 80px; padding: 60px 0; border-top: 1px solid #e1e4e8; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
    
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 40px; font-weight: 700; border-bottom: none;">Get In Touch</h2>
    
    <div style="display: flex; gap: 20px; justify-content: center; flex-wrap: nowrap; width: 100%; max-width: 68rem; margin: 0 auto; padding: 0 20px; box-sizing: border-box;">
        
        <a href="https://linkedin.com/in/richardspiers" target="_blank" class="contact-card">
            <div style="display: flex; flex-direction: column; align-items: center;">
                <div style="color: #0077b5; margin-bottom: 15px; display: flex; justify-content: center;">
                    <svg height="40" width="40" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                </div>
                <h3 style="font-size: 1.3rem; color: #24292e; margin: 0 0 10px 0; font-weight: 600;">LinkedIn</h3>
                <p style="font-size: 0.95rem; color: #586069; line-height: 1.5; margin: 0;">Let's connect professionally.</p>
            </div>
            <div class="contact-btn" style="width: 80%; max-width: 200px;">View Profile</div>
        </a>

        <a href="mailto:your.zeterlore@hotmail.com" class="contact-card">
            <div style="display: flex; flex-direction: column; align-items: center;">
                <div style="color: #ea4335; margin-bottom: 15px; display: flex; justify-content: center;">
                    <svg height="40" width="40" viewBox="0 0 24 24" fill="currentColor"><path d="M0 3v18h24v-18h-24zm21.518 2l-9.518 7.713-9.518-7.713h19.036zm-19.518 14v-11.817l10 8.104 10-8.104v11.817h-20z"/></svg>
                </div>
                <h3 style="font-size: 1.3rem; color: #24292e; margin: 0 0 10px 0; font-weight: 600;">Email</h3>
                <p style="font-size: 0.95rem; color: #586069; line-height: 1.5; margin: 0;">Send a message directly to my inbox.</p>
            </div>
            <div class="contact-btn" style="width: 80%; max-width: 200px;">Send Message</div>
        </a>

        <a href="https://radsy.itch.io" target="_blank" class="contact-card">
            <div style="display: flex; flex-direction: column; align-items: center;">
                <div style="color: #fa5c5c; margin-bottom: 15px; display: flex; justify-content: center;">
                    <svg height="40" width="40" viewBox="0 0 24 24" fill="currentColor"><path d="M3.522 4.417c-.772.046-1.464.444-1.87 1.096-.407.652-.486 1.453-.217 2.168l1.451 3.86c-1.127.42-1.884 1.507-1.886 2.715v4.51c.002 1.782 1.445 3.223 3.227 3.224h15.546c1.782-.001 3.225-1.442 3.227-3.224v-4.51c-.002-1.208-.759-2.295-1.886-2.715l1.451-3.86c.269-.715.19-1.516-.217-2.168-.406-.652-1.098-1.05-1.87-1.096zm.224 1.76h16.508c.241.014.457.139.584.343.128.204.153.454.068.68l-1.353 3.593c-.097.256-.343.424-.617.424h-13.872c-.274 0-.52-.168-.617-.424l-1.353-3.593c-.085-.226-.06-.476.068-.68.127-.204.343-.329.584-.343zm1.613 6.945c.42-.002.82.165 1.116.463l1.523 1.53 1.525-1.53c.594-.6 1.637-.6 2.23 0l1.525 1.53 1.524-1.53c.594-.6 1.637-.6 2.231 0l1.524 1.53 1.524-1.53c.63-.615 1.698-.573 2.278.09l.487.558c.267.306.413.698.412 1.103v2.856c0 .414-.336.75-.75.75s-.75-.336-.75-.75v-2.394l-.736-.843c-.144-.165-.41-.165-.554 0l-1.764 1.77c-.594.6-1.636.6-2.23 0l-1.524-1.53-1.524 1.53c-.594.6-1.637.6-2.23 0l-1.525-1.53-1.524 1.53c-.594.6-1.637.6-2.23 0l-1.765-1.77c-.143-.165-.409-.165-.553 0l-.736.843v2.394c0 .414-.336.75-.75.75s-.75-.336-.75-.75v-2.856c0-.405.146-.797.412-1.103l.488-.558c.28-.32.682-.501 1.105-.494z"/></svg>
                </div>
                <h3 style="font-size: 1.3rem; color: #24292e; margin: 0 0 10px 0; font-weight: 600;">itch.io</h3>
                <p style="font-size: 0.95rem; color: #586069; line-height: 1.5; margin: 0;">Play the games I contributed to in the Epic MegaJam.</p>
            </div>
            <div class="contact-btn" style="width: 80%; max-width: 200px;">MegaJam Entries</div>
        </a>

    </div>
</div>

<!-- Custom Professional Footer -->
<footer style="padding: 40px 0 20px 0; text-align: center; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-size: 0.9rem; color: #586069;">
    <p>© 2026 Richard Spiers. All rights reserved.</p>
</footer>
