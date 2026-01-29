# ATS-Optimized CV Generator 📄

Generate professional, **ATS-friendly** (Applicant Tracking System) CVs in Word format from a simple JSON file.

## ✨ Features

- **ATS-Optimized**: Clean, single-column layout that ATS systems can parse easily
- **Single Page**: Compact design that fits everything on one page
- **Multi-Language**: Generate CVs in English or Spanish
- **Profile Photo**: Optional photo support with automatic layout adjustment
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
# English (default)
python generate_cv.py

# Spanish
python generate_cv.py --lang es

# With profile photo
python generate_cv.py --photo image.jpg

# Full example: Spanish CV with photo
python generate_cv.py --input cv_data_es.json --lang es --photo image.jpg --output CV_Spanish.docx
```

## 📁 Project Structure

```
├── generate_cv.py        # Main CV generator script
├── cv_data.json          # Your CV data in English (edit this!)
├── cv_data_es.json       # Your CV data in Spanish (optional)
├── cv_data_template.json # Empty template to get started
├── requirements.txt      # Python dependencies
├── LICENSE               # MIT License
└── README.md             # This file
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
| `--lang` | `-l` | `en` | Language for section headers (`en` or `es`) |
| `--photo` | `-p` | None | Path to profile photo (jpg/png) |

## 📷 Profile Photo

You can include a profile photo in your CV:

```bash
python generate_cv.py --photo photo.jpg
```

**Layout behavior:**
- **With photo**: Name and contact info aligned left, photo on the right
- **Without photo**: Centered layout (traditional CV style)

**Supported formats:** JPG, PNG

> ⚠️ **Note for ATS**: Some ATS systems cannot process images. Consider generating two versions - one with photo for direct applications, one without for ATS portals.

## 🌍 Multi-Language Support

The generator supports **English** and **Spanish** section headers:

| English | Spanish |
|---------|--------|
| Professional Summary | Resumen Profesional |
| Technical Skills | Habilidades Técnicas |
| Professional Experience | Experiencia Profesional |
| Education | Educación |
| Certifications & Languages | Certificaciones e Idiomas |

### Full Spanish CV

To generate a CV entirely in Spanish:

1. Create a `cv_data_es.json` with all content in Spanish
2. Run: `python generate_cv.py -i cv_data_es.json -l es -o CV_Spanish.docx`

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
