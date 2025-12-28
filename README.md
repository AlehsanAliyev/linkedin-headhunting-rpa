# LinkedIn Recruiter Automation Project

This UiPath project automates the process of finding, evaluating, and reporting on IT-related candidates for open positions, based on publicly available job vacancies and LinkedIn Recruiter Lite searches.

The project was developed as part of an internship project and demonstrates end-to-end HR automation using RPA and AI-assisted analysis.

---

## Overall Logic

The automation follows these main steps:

1. **Scraping Vacancies**  
   IT-related job vacancies are scraped from the ABB careers website.

2. **Generating Boolean Expressions**  
   For each vacancy, GPT is used to generate a boolean search expression suitable for LinkedIn Recruiter Lite.

3. **Searching for Candidates**  
   The robot navigates to LinkedIn Recruiter Lite and performs candidate searches using the generated boolean expressions and predefined filters (e.g., location).

4. **Scraping Candidate Profiles**  
   Candidate profile information is extracted from the search results.

5. **Grading Candidates**  
   GPT evaluates each candidate against the vacancy requirements and assigns a score.

6. **Generating a Report**  
   The automation produces an Excel report containing candidate details and evaluation results.

---

## Workflows

### Main Workflows

- **Main.xaml**  
  Orchestrates the complete automation flow.

- **AssigningInitialInfo.xaml**  
  Initializes configuration values and variables.

- **ScrapingABBWebsite.xaml**  
  Scrapes IT-related job vacancies from the ABB careers page.

- **FlowchartVacancyCandidateAnalyser.xaml**  
  Coordinates vacancy processing and candidate analysis.

### Flowchart Workflows

- **CandidateNumberAnalyser.xaml**  
  Analyzes the number of candidates found per search.

- **ExtractAllCandidates.xaml**  
  Extracts candidate data from LinkedIn search results.

- **GPTBooleanGenerator.xaml**  
  Generates boolean search expressions using GPT.

- **GPTGradingSystem.xaml**  
  Grades candidates based on vacancy requirements.

- **GettingVacancyRequirements.xaml**  
  Extracts required skills and criteria from vacancy pages.

- **LinkedInPartDeleter.xaml**  
  Clears previous LinkedIn search results before new searches.

- **LinkedInRecruiterSearch.xaml**  
  Executes candidate searches in LinkedIn Recruiter Lite.

- **ScrapingCandidateProfile.xaml**  
  Scrapes detailed information from individual candidate profiles.

---

## Configuration

- External URLs (e.g., LinkedIn Recruiter entry point) are stored in configuration files or Orchestrator Assets.
- Session-based or authenticated deep links are **not** hardcoded in the project.
- No credentials or private tokens are stored in the repository.

---

## Authentication & Access

- A valid LinkedIn Recruiter Lite account is required to run this project.
- Authentication is performed manually by the user at runtime.
- The repository does **not** include login credentials, session URLs, or private LinkedIn links.

---

## AI Usage

GPT is used for:
- Boolean search generation
- Candidate evaluation and scoring

All prompts are generated dynamically during execution.  
No personal data is persisted outside the automation workflow.


---
## Demonstration

Screenshots and execution examples are available in the internship presentation
and are intentionally not included in this repository for data protection reasons.

---

## Notes

This repository focuses on automation logic and project structure.  
Execution requires appropriate access rights and subscriptions that are not included in the repository.

