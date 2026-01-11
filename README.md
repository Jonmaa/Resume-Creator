# ATS-Optimized CV Generator 📄

Generate professional, **ATS-friendly** (Applicant Tracking System) CVs in Word format from a simple JSON file.

## ✨ Features

- **ATS-Optimized**: Clean, single-column layout that ATS systems can parse easily
- **Single Page**: Compact design that fits everything on one page
- **Customizable**: Edit `cv_data.json` with your information
- **Professional Design**: Clean typography with proper hierarchy
- **Easy to Use**: Just edit JSON and run the script

## 🚀 Quick Start

### 1. Install Dependencies

```bash
pip install python-docx
```

### 2. Edit Your CV Data

Edit the `cv_data.json` file with your information:

```json
{
  "personal": {
    "name": "Your Name",
    "title": "Your Professional Title",
    "email": "your.email@example.com",
    "phone": "+1 234 567 890",
    "location": "City, Country",
    "github": "github.com/yourusername",
    "linkedin": "linkedin.com/in/yourusername"
  },
  "summary": "Your professional summary...",
  "skills": {
    "Category 1": "Skill1, Skill2, Skill3",
    "Category 2": "Skill4, Skill5, Skill6"
  },
  ...
}
```

### 3. Generate Your CV

```bash
python generate_cv.py
```

Or specify custom input/output:

```bash
python generate_cv.py --input my_data.json --output my_cv.docx
```

## 📁 Project Structure

```
├── generate_cv.py      # Main CV generator script
├── cv_data.json        # Your CV data (edit this!)
├── requirements.txt    # Python dependencies
└── README.md          # This file
```

## 📋 JSON Schema

### Personal Information
```json
{
  "personal": {
    "name": "Required - Your full name",
    "title": "Required - Professional title",
    "email": "Optional - Email address",
    "phone": "Optional - Phone number",
    "location": "Optional - City, Country",
    "github": "Optional - GitHub profile",
    "linkedin": "Optional - LinkedIn profile",
    "portfolio": "Optional - Personal website"
  }
}
```

### Skills
```json
{
  "skills": {
    "Category Name": "Comma-separated skills"
  }
}
```

### Experience
```json
{
  "experience": [
    {
      "title": "Job Title",
      "company": "Company Name",
      "location": "City, Country",
      "dates": "Start Date – End Date",
      "achievements": [
        "Achievement 1 with metrics",
        "Achievement 2 with impact"
      ]
    }
  ]
}
```

### Education
```json
{
  "education": [
    {
      "degree": "Degree Name",
      "institution": "University Name",
      "dates": "Start – End",
      "details": "Optional - GPA, thesis, honors"
    }
  ]
}
```

### Certifications & Languages
```json
{
  "certifications": ["Cert 1", "Cert 2"],
  "languages": [
    {"language": "English", "level": "Native"},
    {"language": "Spanish", "level": "Advanced (C1)"}
  ]
}
```

## 🎯 ATS Optimization Tips

1. **Use keywords** from the job description in your summary and skills
2. **Quantify achievements** with numbers and percentages
3. **Use standard section headers** (Experience, Education, Skills)
4. **Avoid tables and columns** - use simple formatting
5. **No images or graphics** - ATS can't read them
6. **Use standard fonts** - the generator uses safe fonts

## 📝 Command Line Options

| Option | Short | Default | Description |
|--------|-------|---------|-------------|
| `--input` | `-i` | `cv_data.json` | Input JSON file path |
| `--output` | `-o` | `CV_Optimized_ATS.docx` | Output Word file path |

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with ❤️ for job seekers everywhere
