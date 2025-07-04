
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Megha Jain - Technical Documentation Expert</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #2d3748;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .resume-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            animation: fadeInUp 0.8s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header {
            background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);
            color: white;
            padding: 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 20px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            font-weight: bold;
            position: relative;
            z-index: 1;
        }

        .name {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .title {
            font-size: 1.3rem;
            opacity: 0.9;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            position: relative;
            z-index: 1;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .nav-tabs {
            display: flex;
            background: #f7fafc;
            border-bottom: 1px solid #e2e8f0;
            overflow-x: auto;
        }

        .nav-tab {
            padding: 15px 25px;
            background: none;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            white-space: nowrap;
            position: relative;
        }

        .nav-tab:hover {
            background: rgba(102, 126, 234, 0.1);
        }

        .nav-tab.active {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
        }

        .nav-tab.active::after {
            content: '';
            position: absolute;
            bottom: -1px;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(135deg, #667eea, #764ba2);
        }

        .content {
            padding: 40px;
            min-height: 500px;
        }

        .section {
            display: none;
            animation: fadeIn 0.5s ease-in;
        }

        .section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 30px;
            color: #1a202c;
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .summary {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #4a5568;
            margin-bottom: 30px;
        }

        .strengths-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .strength-item {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1));
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #667eea;
            transition: transform 0.3s ease;
        }

        .strength-item:hover {
            transform: translateY(-2px);
        }

        .skills-category {
            margin-bottom: 30px;
        }

        .skills-category h3 {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: #2d3748;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: transform 0.3s ease;
        }

        .skill-tag:hover {
            transform: scale(1.05);
        }

        .experience-item {
            background: #f7fafc;
            padding: 25px;
            border-radius: 10px;
            margin-bottom: 25px;
            border-left: 4px solid #667eea;
            transition: all 0.3s ease;
        }

        .experience-item:hover {
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transform: translateY(-2px);
        }

        .job-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }

        .job-title {
            font-size: 1.3rem;
            font-weight: 600;
            color: #1a202c;
        }

        .company {
            font-size: 1.1rem;
            color: #667eea;
            font-weight: 500;
        }

        .duration {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 5px 15px;
            border-radius: 15px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        .job-description ul {
            margin-left: 20px;
            margin-top: 10px;
        }

        .job-description li {
            margin-bottom: 8px;
            color: #4a5568;
        }

        .highlight {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1));
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            border-left: 4px solid #667eea;
        }

        .highlight h3 {
            color: #1a202c;
            margin-bottom: 10px;
        }

        .certification-item {
            background: #f7fafc;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 3px solid #667eea;
        }

        .certification-item h4 {
            color: #1a202c;
            margin-bottom: 5px;
        }

        .certification-item p {
            color: #4a5568;
            font-size: 0.9rem;
        }

        .education-item {
            background: #f7fafc;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 15px;
            border-left: 4px solid #667eea;
        }

        .education-item h3 {
            color: #1a202c;
            margin-bottom: 5px;
        }

        .education-item p {
            color: #4a5568;
        }

        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }

            .header {
                padding: 30px 20px;
            }

            .name {
                font-size: 2rem;
            }

            .contact-info {
                flex-direction: column;
                gap: 15px;
            }

            .content {
                padding: 20px;
            }

            .job-header {
                flex-direction: column;
                gap: 10px;
            }

            .nav-tabs {
                flex-wrap: wrap;
            }

            .nav-tab {
                flex: 1;
                min-width: 120px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="resume-card">
            <div class="header">
                <div class="profile-img">TD</div>
                <h1 class="name">Technical Documentation Professional</h1>
                <p class="title">Senior Technical Writer & Documentation Manager</p>
                <div class="contact-info">
                    <div class="contact-item">
                        <span>📧</span>
                        <span>your.email@example.com</span>
                    </div>
                    <div class="contact-item">
                        <span>📱</span>
                        <span>+91 XXX XXX XXXX</span>
                    </div>
                    <div class="contact-item">
                        <span>💼</span>
                        <span>LinkedIn Profile</span>
                    </div>
                    <div class="contact-item">
                        <span>📍</span>
                        <span>Delhi, India</span>
                    </div>
                </div>
            </div>

            <div class="nav-tabs">
                <button class="nav-tab active" onclick="showSection('summary')">Summary</button>
                <button class="nav-tab" onclick="showSection('experience')">Experience</button>
                <button class="nav-tab" onclick="showSection('skills')">Skills</button>
                <button class="nav-tab" onclick="showSection('highlights')">Highlights</button>
                <button class="nav-tab" onclick="showSection('education')">Education</button>
            </div>

            <div class="content">
                <div id="summary" class="section active">
                    <h2 class="section-title">Professional Summary</h2>
                    <div class="summary">
                        Senior technical documentation professional with 10 years of experience in technical content projects, nearly 7 years as a writer, and over 3.5 years as a manager. Extensive track record of success, drawing on a wealth of technical insights and deep technology skillset to improve project document workflow, developer journey, delivery, content strategies, and quality, maximizing user understanding for products such as Data Privacy, Logistics, Telecom, SaaS, Cloud Security, and other dynamic technologies delivered by top companies.
                    </div>

                    <h3 style="margin-bottom: 20px; color: #1a202c;">Core Strengths</h3>
                    <div class="strengths-grid">
                        <div class="strength-item">Team Building & Leadership</div>
                        <div class="strength-item">Technical Documentation</div>
                        <div class="strength-item">Document & Training Management</div>
                        <div class="strength-item">User Stories & Personas</div>
                        <div class="strength-item">Content & Knowledge Management</div>
                        <div class="strength-item">Strategic Planning & Gap Analysis</div>
                        <div class="strength-item">Product Analysis & Evaluation</div>
                        <div class="strength-item">Program & Project Management</div>
                        <div class="strength-item">Workflow Optimization</div>
                        <div class="strength-item">Data Privacy & Security</div>
                        <div class="strength-item">Cross-Functional Collaboration</div>
                        <div class="strength-item">Staff Training & Development</div>
                        <div class="strength-item">Complex Problem-Solving</div>
                        <div class="strength-item">Research & Analysis</div>
                        <div class="strength-item">Customer Success</div>
                    </div>
                </div>

                <div id="experience" class="section">
                    <h2 class="section-title">Professional Experience</h2>
                    
                    <div class="experience-item">
                        <div class="job-header">
                            <div>
                                <div class="job-title">Lead Technical Writer</div>
                                <div class="company">DELHIVERY LTD</div>
                            </div>
                            <div class="duration">Aug 2024 - Present</div>
                        </div>
                        <div class="job-description">
                            <ul>
                                <li>Collaborating with cross-functional teams and leadership to develop and manage documentation for Delhivery's core products and developer platforms, driving the process from initial design to implementation.</li>
                                <li>Responsible for planning, coordinating, and owning the documentation roadmap, focusing on timely delivery of milestones and achieving a 20% improvement in documentation quality and usability metrics.</li>
                            </ul>
                        </div>
                    </div>

                    <div class="experience-item">
                        <div class="job-header">
                            <div>
                                <div class="job-title">Senior Technical Writer</div>
                                <div class="company">RELYANCE AI (GOODWORDS LLC)</div>
                            </div>
                            <div class="duration">Dec 2023 - June 2024</div>
                        </div>
                        <div class="job-description">
                            <ul>
                                <li>Teamed up with the Relyance AI team to strategize, develop, and release documentation for data privacy solutions that empower organizations to protect their confidential data and comply with regulatory standards.</li>
                                <li>Developed and executed documentation processes, suggesting and combining cutting-edge tools and knowledge base portals to improve productivity and information accessibility.</li>
                                <li>Transformed platform APIs and developer documentation, enhancing accessibility, training, and user experience.</li>
                            </ul>
                        </div>
                    </div>

                    <div class="experience-item">
                        <div class="job-header">
                            <div>
                                <div class="job-title">Senior/Lead Technical Writer & Consultant</div>
                                <div class="company">LOGINEXT SOLUTIONS</div>
                            </div>
                            <div class="duration">Aug 2023 - Dec 2023</div>
                        </div>
                        <div class="job-description">
                            <ul>
                                <li>Enhanced Content Optimization strategies to improve online content performance.</li>
                                <li>Successfully facilitated webinars and onboarding email campaigns to optimize content, resulting in a remarkable increase in open rates from 0.47% to 35% and click-through rates from 0% to 3.5%.</li>
                                <li>Managed team's performance, goals, KRAs, and training development program.</li>
                                <li>Reviewed and analyzed the team's Help articles, API documentation, developer portal documents, and the UX/UI writing content to ensure high-quality content.</li>
                            </ul>
                        </div>
                    </div>

                    <div class="experience-item">
                        <div class="job-header">
                            <div>
                                <div class="job-title">Lead – Technical Content & Learning</div>
                                <div class="company">SUMO LOGIC</div>
                            </div>
                            <div class="duration">Oct 2022 - July 2023</div>
                        </div>
                        <div class="job-description">
                            <ul>
                                <li>Hired, coached, and groomed writers in India.</li>
                                <li>Maintained strong collaborative relationships with global leads to facilitate seamless project assignments and integration of Chatbot to the production environment using Generative AI tools like ChatGPT.</li>
                                <li>Involved in the initiative to perform site analytics on the documentation platform, delivering key insights for ongoing product feature development and enhancements.</li>
                                <li>Directed team's initiatives to implement the docs-as-code approach, enhancing the documentation site and increasing the contributions of developers and end users.</li>
                            </ul>
                        </div>
                    </div>

                    <div class="experience-item">
                        <div class="job-header">
                            <div>
                                <div class="job-title">Senior Technical Writer</div>
                                <div class="company">INNOVACCER</div>
                            </div>
                            <div class="duration">Jan 2022 - Oct 2022</div>
                        </div>
                        <div class="job-description">
                            <ul>
                                <li>Managed documentation efforts for the platform products while initially overseeing a single writer and actively working to expand the team.</li>
                                <li>Ideated, designed, and worked hand-in-hand with the Helpjuice team to build and deliver a developer documentation portal that became a vital resource supporting developers building apps on the platform.</li>
                                <li>Delivered documentation set for Innovaccer's Developer Portal, providing sandbox testing and deployment guidance on integrating AI, ML, and NLP capabilities into third-party applications.</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div id="skills" class="section">
                    <h2 class="section-title">Technical Skills</h2>
                    
                    <div class="skills-category">
                        <h3>Authoring & Interactive Adoption Tools</h3>
                        <div class="skills-list">
                            <span class="skill-tag">Adobe RoboHelp</span>
                            <span class="skill-tag">Madcap Flare</span>
                            <span class="skill-tag">DITA</span>
                            <span class="skill-tag">XML Authoring (Oxygen)</span>
                            <span class="skill-tag">Microsoft Office</span>
                            <span class="skill-tag">G Suite</span>
                            <span class="skill-tag">WalkMe</span>
                            <span class="skill-tag">Whatfix</span>
                        </div>
                    </div>

                    <div class="skills-category">
                        <h3>Markup Language & Version Control</h3>
                        <div class="skills-list">
                            <span class="skill-tag">Markdown</span>
                            <span class="skill-tag">VS Code</span>
                            <span class="skill-tag">GitHub</span>
                            <span class="skill-tag">Perforce</span>
                            <span class="skill-tag">SVN</span>
                            <span class="skill-tag">JIRA</span>
                            <span class="skill-tag">Asana</span>
                        </div>
                    </div>

                    <div class="skills-category">
                        <h3>Content Management & Knowledge Base</h3>
                        <div class="skills-list">
                            <span class="skill-tag">WordPress</span>
                            <span class="skill-tag">Notion</span>
                            <span class="skill-tag">Drupal</span>
                            <span class="skill-tag">Zendesk</span>
                            <span class="skill-tag">Confluence</span>
                            <span class="skill-tag">Document 360</span>
                            <span class="skill-tag">Helpjuice</span>
                        </div>
                    </div>

                    <div class="skills-category">
                        <h3>Cloud Platforms & AI</h3>
                        <div class="skills-list">
                            <span class="skill-tag">AWS Cloud</span>
                            <span class="skill-tag">Google Cloud</span>
                            <span class="skill-tag">ChatGPT</span>
                            <span class="skill-tag">Kindo.ai</span>
                        </div>
                    </div>

                    <div class="skills-category">
                        <h3>Video & Design Tools</h3>
                        <div class="skills-list">
                            <span class="skill-tag">Adobe Captivate</span>
                            <span class="skill-tag">Camtasia</span>
                            <span class="skill-tag">Powtoon</span>
                            <span class="skill-tag">Draw.io</span>
                            <span class="skill-tag">Lucid Charts</span>
                        </div>
                    </div>

                    <div class="skills-category">
                        <h3>Methodologies & Analytics</h3>
                        <div class="skills-list">
                            <span class="skill-tag">Agile</span>
                            <span class="skill-tag">Docs-as-Code</span>
                            <span class="skill-tag">DevOps</span>
                            <span class="skill-tag">Waterfall</span>
                            <span class="skill-tag">DDLC</span>
                            <span class="skill-tag">Google Analytics</span>
                        </div>
                    </div>
                </div>

                <div id="highlights" class="section">
                    <h2 class="section-title">Career Highlights</h2>
                    
                    <div class="highlight">
                        <h3>🎯 Thought Leadership</h3>
                        <p>Authored and presented thought leadership pieces at the RSA conference, outlining the pivotal role of code analysis in data privacy compliance such as GDPR.</p>
                    </div>

                    <div class="highlight">
                        <h3>🔄 Digital Transformation</h3>
                        <p>Successfully led the transition from traditional documentation methods to DITA XML authoring using Oxygen XML Editor, ensuring a smooth and efficient migration process for the entire documentation team.</p>
                    </div>

                    <div class="highlight">
                        <h3>🚀 Developer Engagement</h3>
                        <p>Championed docs-as-code approach to boost developer engagement on the open-source platform, adding over 300 contributors in six months, reducing the review process duration, and increasing stakeholder engagement by 50% within the first year of implementation.</p>
                    </div>

                    <div class="highlight">
                        <h3>📈 Campaign Success</h3>
                        <p>Led Customer Onboarding campaigns to optimize and measure content efficacy, resulting in a significant increase in open rates (from 0.47% to 35%) and click-through rates (from 0% to 3.5%).</p>
                    </div>

                    <div class="certification-item">
                        <h4>Certified Product Owner by Scrum Alliance</h4>
                        <p>Professional certification in Agile methodologies and product management</p>
                    </div>

                    <div class="certification-item">
                        <h4>Data Privacy Fundamentals - Northeastern University</h4>
                        <p>Specialized certification in data privacy and compliance</p>
                    </div>

                    <div class="certification-item">
                        <h4>Data Privacy Laws - Pennsylvania University</h4>
                        <p>Advanced certification in data privacy legal frameworks</p>
                    </div>

                    <div class="certification-item">
                        <h4>Assertive Communication & Business Communication</h4>
                        <p>Del Carnegie Gurgaon - Professional communication skills certification</p>
                    </div>
                </div>

                <div id="education" class="section">
                    <h2 class="section-title">Education & Certifications</h2>
                    
                    <div class="education-item">
                        <h3>Master of Science in Information Technology</h3>
                        <p>Jain University</p>
                    </div>

                    <div class="education-item">
                        <h3>Bachelor of Computer Application</h3>
                        <p>SS Jain Subodh PG College</p>
                    </div>

                    <h3 style="margin: 30px 0 20px 0; color: #1a202c;">Professional Certifications</h3>
                    
                    <div class="certification-item">
                        <h4>Certified Product Owner</h4>
                        <p>Scrum Alliance</p>
                    </div>

                    <div class="certification-item">
                        <h4>Data Privacy Fundamentals</h4>
                        <p>Northeastern University</p>
                    </div>

                    <div class="certification-item">
                        <h4>Data Privacy Laws</h4>
                        <p>Pennsylvania University</p>
                    </div>

                    <div class="certification-item">
                        <h4>Assertive Communication & Business Communication</h4>
                        <p>Del Carnegie Gurgaon</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });

            // Remove active class from all tabs
            const tabs = document.querySelectorAll('.nav-tab');
            tabs.forEach(tab => {
                tab.classList.remove('active');
            });

            // Show selected section
            document.getElementById(sectionId).classList.add('active');

            // Add active class to clicked tab
            event.target.classList.add('active');
        }

        // Add smooth scrolling and interaction effects
        document.addEventListener('DOMContentLoaded', function() {
            // Add hover effects to experience items
            const experienceItems = document.querySelectorAll('.experience-item');
            experienceItems.forEach(item => {
                item.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-5px)';
                });
                item.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });

            // Add click effects to skill tags
            const skillTags = document.querySelectorAll('.skill-tag');
            skillTags.forEach(tag => {
                tag.addEventListener('click', function() {
                    this.style.transform = 'scale(1.1)';
                    setTimeout(() => {
                        this.style.transform = 'scale(1)';
                    }, 200);
                });
            });
        });
    </script>
</body>
</html>
