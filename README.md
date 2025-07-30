# 🔍 LinkedinUserScraper

> A Python package to extract rich profile data from LinkedIn using Selenium and `undetected-chromedriver`.

---

## 🚀 Features

- 🔐 Login to LinkedIn via credentials or cookies
- 📄 Extract full **profile information**
- 🧠 Get **skills**, **certifications**, **education**, **experience**, and **projects**
- 💼 Bypass 2FA securely using `add_pin()`
- 📦 Save and reuse cookies (no login required every time)
- 🧪 Designed for scraping public user data (educational & research purposes)

---

## 📦 Installation

```bash
pip install -r requirements.txt
````

> You will need Chrome installed and matched with `undetected-chromedriver`.

---

## 🔑 Authentication

You can use either:

1. **Username & Password** (with optional 2FA)
2. **Cookies File** (recommended after first login)

---

## ✅ Example Usage

```python
from LinkedinUserScraper import LinkedInUserScraper

# Initialize
scraper = LinkedInUserScraper(username="you@example.com", password="yourpassword", save_cookies=True, cookie_file="linkedin_cookie.json")

# If 2FA is required
scraper.add_pin("123456")  # manually enter the pin received

# Scrape profile info
info = scraper.get_profile_info("manishgk9")
print(info)

# Scrape skills
skills = scraper.get_user_skills("manishgk9", number_of_skills=5)
print(skills)

# Scrape education
education = scraper.get_user_education("manishgk9")
print(education)

# Scrape certifications
certs = scraper.get_user_certifications("manishgk9")
print(certs)

# Scrape projects
projects = scraper.get_user_projects("manishgk9", num_of_projects=3)
print(projects)

# Scrape Experience
experience = scraper.get_user_experience("manishgk9", num_of_experience=3)
print(experience)

# Quit the driver
scraper.quit()
```

---

## 📊 Sample Output (Notebook-style)

### Profile Info

```python
{
  "name": "Manish Yadav",
  "headline": "Python Developer | Web Scraper",
  "location": "India",
  "about": "Experienced developer in automation and scraping",
  "profile_pic": "https://media.licdn.com/..."
}
```

---

### Skills

```python
['Python', 'Web Scraping', 'Automation', 'Django', 'Data Extraction']
```

---

### Education

```python
[
  ['IIT Delhi', 'Bachelor of Technology - BTech', 'Computer Science', '2016 – 2020'],
  ['Coursera', 'Deep Learning Specialization']
]
```

---

### Certifications

```python
[
  ['AWS Certified Developer', 'Amazon Web Services (AWS)', 'Issued Jan 2024'],
  ['Machine Learning', 'Stanford Online', 'Issued Mar 2023']
]
```

---

### Projects

```python
[
  {
    "title": "AI Resume Builder",
    "description": "Built using NLP and OpenAI to generate resumes automatically.",
    "date": "Jan 2023 – Present",
    "skills": "Python, NLP, Streamlit",
    "github": "https://github.com/username/ai-resume"
  }
]
```

### Experience

```python

[
[
   'Software IT Testing',
  'ERTL(E), STQC, MCIT, DIT, Govt of India · Internship',
  'Feb 2025 - Present · 6 mos',
  'Kolkata, West Bengal, India · On-site',
  'Web applications Security testing  using Burp suites and HCL AppScanOWSAP TOP 10',
  'Skills: Web application functional testing · Wb application security testing · Boundary Values analysis · V model SDLC'
]
]
 

```
---

## 🔧 Help Method

```python
scraper.help()
```

Will print all available methods and usage examples.

---

## 📁 .env and Cookie File

You can store credentials securely in a `.env` file or just login once and reuse cookies:

* `.env`

```
LINKEDIN_USERNAME=you@example.com
LINKEDIN_PASSWORD=yourpassword
```

* `.gitignore`

```
.env
linkedin_cookie.json
scrap_linkedin.ipynb
```

---

## 🛡️ Disclaimer

This tool is for **educational and research** purposes only. Scraping LinkedIn may violate their terms of service. Use responsibly.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork this repo
2. Create a new branch
3. Submit a pull request

---

## 👨‍💻 About the Developer

**Manish Yadav** is a passionate software developer with a strong focus on automation, web scraping, and building intelligent tools to simplify workflows. With experience in Python, Django, and browser automation frameworks like Selenium, Manish enjoys working on real-world problem-solving projects that bridge data extraction, machine learning, and automation.

* 🔗 [LinkedIn](https://www.linkedin.com/in/manishgk9)
* 💻 [GitHub](https://github.com/manishgk9/)
* 🔗 [GitHub](https://x.com/manishgk9/)
* ✉️ Reach out: `emanish365@gmail.com`

---


## 📄 License

MIT License © 2025
