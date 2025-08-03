Wuhan-University Suspected Academic Misconduct Repository  
(WHU-Misconduct-Evidence Repo – English Specification)

0. Scope & Purpose  
This repository is dedicated exclusively to publicly available works (papers, monographs, reports, etc.) in which at least one author lists “Wuhan University / WHU” in the affiliation or correspondence address and for which academic-misconduct concerns (plagiarism, fabrication, image manipulation, duplicate publication, improper authorship, …​) have been raised.  
Goals:  
• Preserve verifiable evidence in an open format for independent examination.  
• Improve academic governance at Wuhan University through transparency.  
• Protect whistle-blowers while preventing unfounded accusations.

1. Repository Name  
Suggested GitHub name: `whu-academic-misconduct` or `whu-integrity-watch`.  
First line of the main README:  
> “This repository collects publicly verifiable evidence of alleged academic misconduct involving authors affiliated with Wuhan University (WHU).”

2. Directory Layout  
```
/root
 ├── CODE_OF_CONDUCT.md
 ├── CONTRIBUTING.md
 ├── LICENSE
 ├── README.md                # states “WHU-only scope”
 └── cases
      └── <DOI>/              # replace “/” with “_”
           ├── README.md      # ≤200-word case summary
           ├── metadata.yaml  # bibliographic & WHU fields
           ├── original/      # publisher PDFs, XML, etc.
           ├── analysis/      # similarity or forensic reports
           └── evidence/      # screenshots, e-mails, hashes
```

3. Mandatory metadata.yaml  
```yaml
doi: 10.1234/abcd.2023.001
title: "Paper Title"
authors:
  - Zhang, San
  - Li, Si
journal: Journal Name
year: 2023
url: https://doi.org/10.1234/abcd.2023.001
date_added: 2025-08-04
submitter: GitHubUserName
whu_authors:                # at least one entry
  - Zhang, San (School of Physics and Technology, Wuhan University)
affiliation_proof:          # link(s) or file(s) that show WHU affiliation
  - evidence/affil_screenshot.png
misconduct_type:            # choose: plagiarism / fabrication / image_manipulation /
                            #        duplicate_publication / authorship / other
```

4. Contribution Workflow  
1) Fork → create feature branch → add `/cases/<DOI>/…` → open Pull Request.  
2) PR template (WHU-specific checkboxes):  
   ☐ One or more authors are affiliated with Wuhan University and proof is attached.  
   ☐ All uploaded materials are legally redistributable or permission has been obtained.  
   ☐ Personal or sensitive data have been anonymized.  
3) A minimum of two maintainers (one versed in research-integrity standards) must approve before merge.

5. Evidence & Analysis Requirements  
• Submission must contain explicit proof of WHU affiliation; otherwise it is rejected.  
• All general evidence rules still apply: verifiable, complete, reproducible, neutral wording.  
• Any comparison or forensic script (e.g., diff, image-manipulation detection) must be saved inside `analysis/` with environment notes.

6. Legal & Ethical Compliance  
• Focus on documented actions, avoid personal attacks.  
• Conform to PRC Civil Code regarding reputation rights and information-network dissemination.  
• If publisher
