---
<!-- Full Width Fixed Navigation Bar -->
<div style="position: fixed; top: 0; left: 0; width: 100vw; background-color: #24292e; color: #fff; padding: 12px 40px; display: flex; justify-content: space-between; align-items: center; z-index: 9999; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; box-shadow: 0 2px 10px rgba(0,0,0,0.35); box-sizing: border-box;">
    
    <!-- Left: Your Name -->
    <span style="font-weight: bold; font-size: 1.15rem; color: #fff; letter-spacing: 0.5px;">Richard Spiers</span>
    
    <!-- Center: Navigation Links -->
    <div style="display: flex; gap: 24px;">
        <a href="#about" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">About Me</a>
        <a href="#skills" style="color: #fff; text-decoration: none; font-size: 0.95rem; font-weight: 500; transition: opacity 0.2s;">Skills</a>
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
  html, body {
    margin: 0 !important;
    padding: 0 !important;
  }
  .page-header {
    display: none !important;
  }
  .main-content {
    padding-top: 0 !important;
    margin-top: 0 !important;
    max-width: 64rem;
  }

  /* Game Jam Card Layout & Consistent Hover States */
  .jam-grid {
    display: grid;
    /* Dynamically handles small screens beautifully */
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px; /* Dropped from 30px to maximize internal card width space */
    max-width: 82rem; /* Opened up from 68rem to give the 3 cards complete widescreen real estate */
    margin: 0 auto;
    padding: 0 20px;
    box-sizing: border-box;
  }

  @media (min-width: 992px) {
    .jam-grid {
      /* Strictly enforce maximum of 3 columns across on desktop monitors */
      grid-template-columns: repeat(3, 1fr);
    }
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
    cursor: pointer;
    width: 100%; /* Grid now controls width perfectly */
  }

  /* The Card elevation animation on mouse hover */
  .jam-card:hover {
    transform: translateY(-6px);
    border-color: #ff0000; /* Subtle YouTube brand red border highlight on hover */
    box-shadow: 0 12px 20px rgba(255, 0, 0, 0.08);
  }

  /* Video Iframe Container to hold strict 16:9 widescreen orientation */
  .video-frame-holder {
    position: relative;
    width: 100%;
    aspect-ratio: 16 / 9;
    background: #000000;
  }

  .video-frame-holder iframe {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    border: none;
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
<div id="about" style="position: relative; left: 50%; right: 50%; margin-top: -20px; margin-left: -50vw; margin-right: -50vw; width: 100vw; min-height: 100vh; background-color: #7242f5; display: flex; align-items: center; box-sizing: border-box; padding: 80px 0 40px 0; z-index: 10;">
    
    <!-- Content Aligned wrapper -->
    <div style="max-width: 54rem; margin: 0 auto; padding: 0 40px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
        
        <h1 style="font-size: 2.8rem; color: #24292e; margin-top: 0; margin-bottom: 10px; border-bottom: none; font-weight: 700;">Rad Spiers</h1>
        <p style="font-size: 1.4rem; color: #586069; margin-top: 0; font-weight: 400; letter-spacing: -0.5px;">Senior Systems & Infrastructure Engineer</p>
        
        <div style="font-size: 1.15rem; line-height: 1.7; color: #2f363d; margin-top: 30px;">
            <p>AAA Software Engineer with over a decade of experience specializing in core engine systems, automated build infrastructure, and performance optimization. Proven track record of delivering stable pipelines and decoupling complex software architectures within high-stakes studio environments.</p>
            <p>Focused on engineering pragmatism, maintainable systems, and cross-department tool collaboration.</p>
        </div>

    </div>
</div>

## <a id="skills"></a>Technical Core

... [your skills text] ...

## <a id="projects"></a>Featured Engineering Sandbox

... [your projects text] ...

## <a id="history"></a>AAA Production History

... [your history text] ...

<!-- Section: Game Jam Entries -->
<div id="game-jams" style="margin-top: 80px; padding: 60px 0; border-top: 1px solid #e1e4e8;">
    
    <h2 style="font-size: 2rem; color: #24292e; text-align: center; margin-bottom: 50px; font-weight: 700; border-bottom: none;">Game Jams</h2>
    
    <div class="jam-grid">
        
        <!-- Game Entry 1 (Hover Box) -->
        <div class="jam-card">
            
            <!-- In-Place YouTube Player Wrapper -->
            <div class="video-frame-holder">
                <!-- YouTube natively handles the Red Play, Share, and Watch Later Clock overlay widgets here -->
                <iframe 
                    src="https://www.youtube.com/embed/y_-oG3KM9LY?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <!-- Metadata & Content Wrapper -->
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                
                <!-- Game Title Bold -->
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Time Janitors</h3>
                
                <!-- Job Title | Release Year -->
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | December 2020</div>
                
                <!-- Game Genre -->
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">FPS Time Travel Puzzle Adventure</div>
                
                <!-- Achievements -->
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <!-- Divider Line -->
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <!-- Technology Tags Footer -->
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>

            </div>
        </div>

        <!-- Game Entry 2 (Hover Box) -->
        <div class="jam-card">
            
            <!-- In-Place YouTube Player Wrapper -->
            <div class="video-frame-holder">
                <!-- YouTube natively handles the Red Play, Share, and Watch Later Clock overlay widgets here -->
                <iframe 
                    src="https://www.youtube.com/embed/dQw4w9WgXcQ?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <!-- Metadata & Content Wrapper -->
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                
                <!-- Game Title Bold -->
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">Malware</h3>
                
                <!-- Job Title | Release Year -->
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | September 2021 </div>
                
                <!-- Game Genre -->
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">2D Puzzle Platformer</div>
                
                <!-- Achievements -->
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <!-- Divider Line -->
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <!-- Technology Tags Footer -->
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
                </div>

            </div>
        </div>

        <!-- Game Entry 3 (Hover Box) -->
        <div class="jam-card">
            
            <!-- In-Place YouTube Player Wrapper -->
            <div class="video-frame-holder">
                <!-- YouTube natively handles the Red Play, Share, and Watch Later Clock overlay widgets here -->
                <iframe 
                    src="https://www.youtube.com/embed/ZNAHgOnTopw?rel=0&modestbranding=1" 
                    title="Gameplay Showcase"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    allowfullscreen>
                </iframe>
            </div>
            
            <!-- Metadata & Content Wrapper -->
            <div style="padding: 25px; display: flex; flex-direction: column; flex-grow: 1;">
                
                <!-- Game Title Bold -->
                <h3 style="font-size: 1.4rem; color: #24292e; margin: 0 0 4px 0; font-weight: 700; border-bottom: none;">The Banquet Below</h3>
                
                <!-- Job Title | Release Year -->
                <div style="font-size: 0.9rem; color: #586069; font-weight: 500; margin-bottom: 4px;">Generalist Programmer | September 2022 </div>
                
                <!-- Game Genre -->
                <div style="font-size: 0.9rem; color: #586069; font-style: italic; margin-bottom: 20px;">FPS Mystery Puzzle Game</div>
                
                <!-- Achievements -->
                <ul style="padding-left: 20px; color: #24292e; font-size: 0.9rem; line-height: 1.6; margin: 0 0 25px 0; flex-grow: 1;">
                    <li>Designed and shipped a complete custom arcade movement system within 48 hours.</li>
                    <li>Optimized particle simulation arrays to maintain 60 FPS overhead boundaries on basic mobile targets.</li>
                    <li>Integrated real-time system tracking data directly using itch.io API frameworks.</li>
                </ul>
                
                <!-- Divider Line -->
                <hr style="border: 0; border-top: 1px solid #e1e4e8; margin: 0 0 15px 0;">
                
                <!-- Technology Tags Footer -->
                <div style="margin: 0 -4px; display: flex; flex-wrap: wrap;">
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Perforce</span>
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
