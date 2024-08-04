# LinkedIn_AIHawk

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Configuration](#configuration)
5. [Usage](#usage)
6. [Optional Resume Feature](#optional-resume-feature)
7. [Documentation](#documentation)
8. [Troubleshooting](#troubleshooting)
9. [Contributors](#contributors)
10. [License](#license)
11. [Conclusion](#conclusion)

## Introduction

LinkedIn_AIHawk is a cutting-edge, automated tool designed to revolutionize the job search and application process on LinkedIn. In today's fiercely competitive job market, where opportunities can vanish in the blink of an eye, this program offers job seekers a significant advantage. By leveraging the power of automation and artificial intelligence, LinkedIn_AIHawk enables users to apply to a vast number of relevant positions efficiently and in a personalized manner, maximizing their chances of landing their dream job.

### The Challenge of Modern Job Hunting

In the digital age, the job search landscape has undergone a dramatic transformation. While online platforms like LinkedIn have opened up a world of opportunities, they have also intensified competition. Job seekers often find themselves spending countless hours scrolling through listings, tailoring applications, and repetitively filling out forms. This process can be not only time-consuming but also emotionally draining, leading to job search fatigue and missed opportunities.

### Enter LinkedIn_AIHawk: Your Personal Job Search Assistant

LinkedIn_AIHawk steps in as a game-changing solution to these challenges. It's not just a tool; it's your tireless, 24/7 job search partner. By automating the most time-consuming aspects of the job search process, it allows you to focus on what truly matters - preparing for interviews and developing your professional skills.

## Features

1. **Intelligent Job Search Automation**
   - Customizable search criteria
   - Continuous scanning for new openings
   - Smart filtering to exclude irrelevant listings

2. **Rapid and Efficient Application Submission**
   - One-click applications using LinkedIn's "Easy Apply" feature
   - Form auto-fill using your profile information
   - Automatic document attachment (resume, cover letter)

3. **AI-Powered Personalization**
   - Dynamic response generation for employer-specific questions
   - Tone and style matching to fit company culture
   - Keyword optimization for improved application relevance

4. **Volume Management with Quality**
   - Bulk application capability
   - Quality control measures
   - Detailed application tracking

5. **Intelligent Filtering and Blacklisting**
   - Company blacklist to avoid unwanted employers
   - Title filtering to focus on relevant positions

6. **Dynamic Resume Generation**
   - Automatically creates tailored resumes for each application
   - Customizes resume content based on job requirements

7. **Secure Data Handling**
   - Manages sensitive information securely using YAML files

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-repo/LinkedInJobBot.git
   cd LinkedInJobBot
   ```

2. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```



## Configuration

LinkedIn_AIHawk relies on three main configuration files:

### 1. secrets.yaml

Contains sensitive information. Never share or commit this file to version control.

- `email`: Your LinkedIn account email
- `password`: Your LinkedIn account password
- `openai_api_key`: Your OpenAI API key for GPT integration

### 2. config.yaml

Defines your job search parameters and bot behavior.

- `remote`: Set to `true` to include remote jobs, `false` to exclude them
- `experienceLevel`: Set desired experience levels to `true`
- `jobTypes`: Set desired job types to `true`
- `date`: Choose one time range for job postings
- `positions`: List job titles you're interested in
- `locations`: List locations you want to search in
- `distance`: Set the radius for your job search (in miles)
- `companyBlacklist`: List companies you want to exclude from your search
- `titleBlacklist`: List keywords in job titles you want to avoid

### 3. plain_text_resume_template.yaml

Contains your resume information in a structured format. Fill it out with your personal details, education, work experience, and skills. This information is used to auto-fill application forms and generate customized resumes.

## Usage

1. **Prepare the Data Folder:**
   Ensure that your data_folder contains the following files:
   - `secrets.yaml`
   - `config.yaml`
   - `plain_text_resume.yaml`
   - `resume.pdf` (optional)

2. **Run the Bot:**
   ```bash
   python main.py [--resume PATH_TO_RESUME_PDF]
   ```

## Optional Resume Feature

LinkedIn_AIHawk offers flexibility in how it handles your resume:

- **Using a Specific Resume:**
  If you want to use a specific PDF resume for all applications, run the bot with the `--resume` option:
  ```bash
  python main.py --resume /path/to/your/resume.pdf
  ```

- **Dynamic Resume Generation:**
  If you don't use the `--resume` option, the bot will automatically generate a unique resume for each application. This feature uses the information from your `plain_text_resume.yaml` file and tailors it to each specific job application, potentially increasing your chances of success by customizing your resume for each position.

## Documentation

For detailed information on each component and their respective roles, please refer to the [Documentation](docs/documentation.md) file.

## Troubleshooting

- **ChromeDriver Issues:** Ensure ChromeDriver is compatible with your installed Chrome version.
- **Missing Files:** Verify that all necessary files are present in the data folder.
- **Invalid YAML:** Check your YAML files for syntax errors.

## Contributors

- [feder-cr](https://github.com/your-github-profile) - Creator and Maintainer

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Conclusion

LinkedIn_AIHawk provides a significant advantage in the modern job market by automating and enhancing the job application process. With features like dynamic resume generation and AI-powered personalization, it offers unparalleled flexibility and efficiency. Whether you're a job seeker aiming to maximize your chances of landing a job, a recruiter looking to streamline application submissions, or a career advisor seeking to offer better services, LinkedIn_AIHawk is an invaluable resource. By leveraging cutting-edge automation and artificial intelligence, this tool not only saves time but also significantly increases the effectiveness and quality of job applications in today's competitive landscape.
