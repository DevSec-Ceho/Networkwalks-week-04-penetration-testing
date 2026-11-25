

<div align="center">

<h1>WEEK 04 – WEB APPLICATION PENETRATION TESTING</h1>

<h3>Cybersecurity & Ethical Hacking Practical Training</h3>

<p><strong>NetworkWalks | Batch B084 | Week 04</strong></p>

<img src="https://img.shields.io/badge/Training-NetworkWalks-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Batch-B084-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Focus-Penetration%20Testing-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />

</div>

---

<h2>📌 Project Overview</h2>

<p>This project documents Week 04 of my Cybersecurity and Ethical Hacking practical training with NetworkWalks.</p>

<p>The project focuses on a black-box web application penetration-testing assessment. It covers reconnaissance, network scanning, directory enumeration, web application vulnerability assessment, PDF password security testing, and metadata analysis.</p>

<p>The primary objective was to understand how security weaknesses can affect web applications and how penetration-testing techniques can help identify potential vulnerabilities before they are exploited by malicious actors.</p>

<h2>🎯 Project Objectives</h2>

<ul>
  <li>Perform reconnaissance and information gathering.</li>
  <li>Identify exposed services and potential attack surfaces.</li>
  <li>Conduct directory and file enumeration.</li>
  <li>Understand SQL injection and authentication security risks.</li>
  <li>Assess potential information disclosure vulnerabilities.</li>
  <li>Extract and analyze PDF password hashes in an authorized testing environment.</li>
  <li>Perform password security testing using John the Ripper and NetworkWalks tools.</li>
  <li>Examine PDF document metadata using ExifTool.</li>
  <li>Document findings and recommend appropriate security improvements.</li>
</ul>

<h2>🛠️ Tools and Technologies Used</h2>

<ul>
  <li><strong>Nmap:</strong> Used for network scanning, host discovery, and service identification.</li>
  <li><strong>Gobuster:</strong> Used for directory and file enumeration.</li>
  <li><strong>John the Ripper:</strong> Used for authorized password hash auditing.</li>
  <li><strong>pdf2john:</strong> Used to extract password hashes from PDF documents for security testing.</li>
  <li><strong>ExifTool:</strong> Used to inspect document metadata.</li>
  <li><strong>NetworkWalks Hash Extractor:</strong> Used for extracting password hashes during practical exercises.</li>
  <li><strong>NetworkWalks Password Cracker:</strong> Used for password security testing.</li>
</ul>

<h2>🔍 Assessment Methodology</h2>

<h3>1. Reconnaissance and Information Gathering</h3>

<p>The first stage involved gathering information about the target web application and identifying potential entry points that could be examined during the assessment.</p>

<p>Activities included:</p>

<ul>
  <li>Gathering publicly accessible information about the target.</li>
  <li>Performing network scanning and service discovery using Nmap.</li>
  <li>Enumerating directories and files using Gobuster.</li>
  <li>Reviewing publicly accessible resources.</li>
  <li>Identifying potential areas of information disclosure.</li>
</ul>

<h3>2. Web Application Vulnerability Assessment</h3>

<p>The second stage focused on examining the application's security controls and identifying possible weaknesses in input handling, authentication, and information management.</p>

<p>The assessment covered:</p>

<ul>
  <li>SQL injection vulnerability assessment.</li>
  <li>Authentication and access-control testing.</li>
  <li>Username enumeration risks.</li>
  <li>Reviewing application error messages.</li>
  <li>Checking for exposed files and directories.</li>
  <li>Assessing the security implications of publicly accessible resources.</li>
</ul>

<h3>3. PDF Password Security Assessment</h3>

<p>This stage focused on understanding PDF document password protection and evaluating password strength through authorized password auditing techniques.</p>

<p>Activities included:</p>

<ul>
  <li>Extracting PDF password hashes using pdf2john and NetworkWalks Hash Extractor.</li>
  <li>Analyzing extracted password hashes.</li>
  <li>Using John the Ripper to perform password security testing.</li>
  <li>Using NetworkWalks Password Cracker for practical password auditing.</li>
  <li>Understanding the risks associated with weak document passwords.</li>
</ul>

<h3>4. Metadata Analysis and Information Disclosure</h3>

<p>The final stage involved examining document metadata and reviewing potentially exposed information to understand how improperly protected resources can create security risks.</p>

<p>Activities included:</p>

<ul>
  <li>Inspecting PDF document metadata using ExifTool.</li>
  <li>Reviewing publicly accessible files and resources.</li>
  <li>Identifying potential sensitive information disclosure.</li>
  <li>Understanding the risks associated with exposed organizational information.</li>
  <li>Documenting observations and possible remediation measures.</li>
</ul>

<h2>⚠️ Identified Security Findings</h2>

<p>The assessment write-up covered the following vulnerability categories and potential security weaknesses:</p>

<table>
  <thead>
    <tr>
      <th>Security Finding</th>
      <th>Severity</th>
      <th>Potential Impact</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>SQL Injection and Authentication Weaknesses</td>
      <td><strong>Critical</strong></td>
      <td>Could compromise authentication and expose application data.</td>
    </tr>
    <tr>
      <td>Exposed Database Backup Files</td>
      <td><strong>Critical</strong></td>
      <td>Could expose confidential organizational information.</td>
    </tr>
    <tr>
      <td>Weak PDF Encryption Passwords</td>
      <td><strong>High</strong></td>
      <td>Could allow unauthorized access to protected documents.</td>
    </tr>
    <tr>
      <td>Sensitive Path Disclosure</td>
      <td><strong>Medium</strong></td>
      <td>Could reveal internal application paths and resources.</td>
    </tr>
    <tr>
      <td>Directory Listing Enabled</td>
      <td><strong>Medium</strong></td>
      <td>Could expose files and directory structures.</td>
    </tr>
    <tr>
      <td>Username Enumeration</td>
      <td><strong>Medium</strong></td>
      <td>Could help attackers identify valid user accounts.</td>
    </tr>
    <tr>
      <td>Verbose SQL Error Messages</td>
      <td><strong>Low</strong></td>
      <td>Could reveal technical details about the application's backend.</td>
    </tr>
  </tbody>
</table>

<p><em>Note: These are the findings described in the supplied assessment material. Severity ratings and individual findings should be independently verified before being presented as confirmed results.</em></p>

<h2>🛡️ Security Recommendations</h2>

<p>Based on the vulnerability categories covered in the assessment, the following security measures are recommended:</p>

<ul>
  <li>Use prepared statements and parameterized queries to prevent SQL injection.</li>
  <li>Implement strong authentication and access-control mechanisms.</li>
  <li>Store database backups outside publicly accessible web directories.</li>
  <li>Use strong encryption and unique passwords for protected PDF documents.</li>
  <li>Disable directory listing on production web servers.</li>
  <li>Restrict access to sensitive application paths and files.</li>
  <li>Use generic error messages instead of exposing database and application details.</li>
  <li>Implement appropriate monitoring, logging, and regular security updates.</li>
  <li>Review publicly accessible resources to prevent accidental information disclosure.</li>
</ul>

<h2>📚 Key Learning Outcomes</h2>

<p>This practical exercise helped strengthen my understanding of several important cybersecurity concepts, including:</p>

<ul>
  <li>Web application reconnaissance and information gathering.</li>
  <li>Network scanning and service discovery using Nmap.</li>
  <li>Directory and file enumeration using Gobuster.</li>
  <li>Common web application vulnerabilities and their potential impact.</li>
  <li>SQL injection and authentication security risks.</li>
  <li>PDF password hash extraction and password auditing.</li>
  <li>Password security testing using John the Ripper.</li>
  <li>Document metadata analysis using ExifTool.</li>
  <li>Information disclosure risks and security remediation.</li>
  <li>Technical documentation and vulnerability reporting.</li>
</ul>

<h2>📸 Screenshots and Practical Evidence</h2>

<p>The screenshots below provide visual evidence of the practical activities covered throughout this assessment. Collectively, they document the reconnaissance and information-gathering process, network scanning, directory enumeration, web application vulnerability assessment, PDF password hash extraction, password security testing using John the Ripper and NetworkWalks tools, and document metadata analysis using ExifTool. Each screenshot captures part of the practical workflow and demonstrates the tools, techniques, and observations involved in identifying potential security weaknesses and understanding their impact. Together, they provide a visual record of the technical exercises and skills covered during this project.</p>

<h3>Milestone 1: Reconnaissance and Web Application Testing</h3>
<img width="1912" height="899" alt="pentest1" src="https://github.com/user-attachments/assets/a2c4430f-9b1a-486b-a450-2dc0cd4c7c12" />
<img width="1097" height="529" alt="pentest2" src="https://github.com/user-attachments/assets/2833e557-4960-457c-95b8-81bd9f38043b" />
<img width="824" height="579" alt="pentest3" src="https://github.com/user-attachments/assets/c8c93108-e542-4528-909a-f715f206dc5f" />


<h3>Milestone 2: PDF Password Security Assessment</h3>
<img width="1845" height="735" alt="pentest101" src="https://github.com/user-attachments/assets/11f4d54a-bf9d-4926-8077-13a1c0de07bc" />
<img width="1919" height="712" alt="pentest102" src="https://github.com/user-attachments/assets/77d3bd59-9385-480e-84e3-cd534ddb3c3c" />
<img width="1901" height="800" alt="pentest111" src="https://github.com/user-attachments/assets/5b5860a5-df01-4735-9c1b-0eae22efbdde" />
<img width="1919" height="877" alt="pentest112" src="https://github.com/user-attachments/assets/83decfd1-0b40-4831-9ae5-8e544bcc41ab" />
<img width="1919" height="811" alt="pentest121" src="https://github.com/user-attachments/assets/17d31928-aef2-446f-9d1e-9122e38d164c" />
<img width="1919" height="922" alt="pentest122" src="https://github.com/user-attachments/assets/0623ff00-3882-47e8-8b50-4f893be4e09c" />



<h3>Milestone 3: Metadata Analysis and Information Disclosure</h3>
<img width="1744" height="904" alt="metadata" src="https://github.com/user-attachments/assets/e985d698-12d5-4c2f-b41a-3eb2e5b0771a" />
<img width="1919" height="926" alt="pentest10" src="https://github.com/user-attachments/assets/587a2f0e-141d-43b7-8760-ed2f1bd0a240" />
<img width="1918" height="928" alt="pentest11" src="https://github.com/user-attachments/assets/aca6ed3d-065b-42ce-a7dc-4a53231ed66b" />
<img width="1907" height="962" alt="pentest12" src="https://github.com/user-attachments/assets/865a7cc8-bb7c-43b0-b9e7-98046aba9049" />
<img width="1094" height="138" alt="pentest13" src="https://github.com/user-attachments/assets/7d64a676-0a23-4689-8c31-c258f3524163" />
<img width="1466" height="758" alt="pentest8" src="https://github.com/user-attachments/assets/4c7944b3-c5ae-4c80-b213-773eab77788f" />



<h2>🙏 Acknowledgement</h2>

<p>I sincerely appreciate <strong>NetworkWalks</strong> for providing practical cybersecurity training and hands-on learning opportunities.</p>

<p>Special appreciation to <strong>Waqas Karim (CCIE)</strong> for the knowledge, guidance, and practical exposure provided throughout the training.</p>

<h2>⚖️ Disclaimer</h2>

<p>This documentation is intended for educational and authorized cybersecurity training purposes only. Security testing should only be conducted on systems for which appropriate permission has been granted.</p>

<p>All screenshots and supporting evidence must be reviewed and redacted before publication. Patient records, employee information, credentials, financial information, and other confidential organizational data must never be exposed in this repository.</p>

<p>Target-specific findings should only be presented as personally verified results when the assessment was actually performed and authorized.</p>

---

<div align="center">

<h3>NetworkWalks Cybersecurity Internship</h3>

<p><strong>Batch B084 | Week 04</strong></p>

<p>Learning • Practicing • Securing</p>

</div>

