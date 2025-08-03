Proposed English Specification  
Evidence & Documentation Repository for Suspected Academic Misconduct In WHU
=====================================================================

1. Purpose  
   • Provide an open, well-organized place to archive publicly verifiable materials related to alleged academic integrity problems.  
   • Enable independent review and transparency while respecting legal, ethical and privacy constraints.  
   • The project is strictly evidence-driven; no unsubstantiated claims or personal attacks are permitted.

2. Repository Structure  
```
/root
 ├── CODE_OF_CONDUCT.md
 ├── CONTRIBUTING.md
 ├── LICENSE
 ├── README.md
 └── cases
      └── <DOI>/
           ├── README.md          <-- concise case summary
           ├── metadata.yaml      <-- mandatory bibliographic info
           ├── original/          <-- publisher-supplied files (PDF, XML, etc.)
           ├── analysis/          <-- plagiarism or image-manipulation reports
           └── evidence/          <-- screenshots, correspondence, archival links
```
• Folder name is the exact DOI with slashes replaced by underscores, e.g.  
  `10.1234/abcd.2023.001` → `10.1234_abcd.2023.001`  
• If a work lacks a DOI, use an official repository identifier (e.g. arXiv ID) or create a UUID and document the choice in `metadata.yaml`.

3. Minimum File Requirements per Case  
metadata.yaml   – YAML key/value pairs  
```
doi: 10.1234/abcd.2023.001
title: "Paper Title"
authors:
  - FamilyName, GivenName
journal: Journal Name
year: 2023
url: https://doi.org/10.1234/abcd.2023.001
date_added: 2025-08-04
submitter: GitHubUsername
```
case README.md – Max 200 words: what the evidence purports to show and which policy it allegedly violates.  
analysis/      – At least one machine-generated or human-written analysis file (e.g. a plagiarism similarity report).  
evidence/      – Raw, unaltered files supporting the analysis: publisher PDFs, archived web pages (via Internet Archive), email headers, conference slides, etc.

4. Contribution Workflow  
1. Fork ➜ create feature branch ➜ add `/cases/<DOI>/…` ➜ pull request.  
2. PR template forces checkboxes:  
   ☐ All files are publicly redistributable; no copyright infringement.  
   ☐ Personal data redacted unless already public.  
   ☐ Evidence is complete, timestamped, and replicable.  
3. Two maintainers must approve before merge.

5. Evidence Standards  
• Verifiability: Provide the original source URL or archive hash (e.g. SHA-256).  
• Completeness: Upload the whole document, not cropped screenshots, when licenses allow.  
• Traceability: Keep all image or text comparisons reproducible (e.g. diff scripts, plagiarism report settings).  
• Neutral Tone: Use factual language; avoid accusatory or defamatory wording.

6. Legal & Ethical Compliance  
• Content must comply with the laws of the repository host and applicable jurisdictions.  
• No leaks of non-public personal data, medical records, or student records.  
• Respect publisher licenses; link when redistribution is not permitted.  
• Submitters retain copyright to their own analyses but license them under CC-BY-4.0 unless specified otherwise.

7. Code of Conduct (see CODE_OF_CONDUCT.md)  
• Be respectful, evidence-based, and free of harassment.  
• Discussions focus on methodological rigor, not individuals’ character.

8. Disclaimer  
The repository maintainers do not state that wrongdoing has occurred; materials are provided solely to facilitate independent evaluation. Allegations remain allegations until validated by competent authorities.

9. Recommended Tools (optional)  
• Text overlap: iThenticate, Turnitin, VronPlag.  
• Image forensics: ImageTwin, Forensically, doctored-image-detectors.  
• Archiving: Internet Archive “Save Page Now,” perma.cc, SHA-256 hashing.  

10. Licensing  
• Repository documentation: CC-BY-4.0.  
• Code snippets: MIT.  
• Third-party PDFs: linked or included only if license permits redistribution; otherwise store hash + link.

(End of specification)
