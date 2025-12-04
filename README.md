# Azure AZ-900 Fundamentals Training Website

A simple, beginner-friendly static website explaining Microsoft Azure AZ-900 fundamentals using easy-to-understand analogies and examples.

## 📋 Overview

This website provides a simplified introduction to Azure cloud computing concepts, perfect for beginners preparing for the AZ-900 certification exam. All content is explained using simple analogies (like the "toy library" for cloud computing) to make complex concepts easy to understand.

## 🎯 Topics Covered

- **Cloud Computing Basics** - What is the cloud and why use it?
- **Microsoft Azure Introduction** - Overview of Azure platform
- **Cloud Service Types** - IaaS, PaaS, and SaaS explained simply
- **Core Azure Services** - Virtual Machines, Storage, Databases, and more
- **Azure Pricing** - Pay-as-you-go model explained
- **Azure Regions** - Understanding data centers and locations
- **Support Options** - Different support tiers available

## 🚀 Deploying to Azure Static Web Apps

### Prerequisites
- An Azure account ([create one for free](https://azure.microsoft.com/free/))
- Git installed on your computer

### Deployment Steps

1. **Initialize Git Repository** (if not already done)
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Azure AZ-900 training site"
   ```

2. **Push to GitHub**
   - Create a new repository on GitHub
   - Follow GitHub's instructions to push your local repository

3. **Create Azure Static Web App**
   - Go to [Azure Portal](https://portal.azure.com)
   - Click "Create a resource"
   - Search for "Static Web App" and select it
   - Click "Create"
   - Fill in the details:
     - **Subscription**: Select your subscription
     - **Resource Group**: Create new or use existing
     - **Name**: Choose a unique name
     - **Region**: Select closest to your users
     - **Source**: Choose "GitHub"
     - **Organization**: Your GitHub username
     - **Repository**: Select your repository
     - **Branch**: main (or master)
     - **Build Presets**: Custom
     - **App location**: / (root)
     - **Output location**: Leave empty
   - Click "Review + Create" then "Create"

4. **Automatic Deployment**
   - Azure will automatically deploy your site
   - A GitHub Action workflow will be created automatically
   - Your site will be live at: `https://your-app-name.azurestaticapps.net`

### Alternative: Deploy via Azure CLI

```bash
# Login to Azure
az login

# Create a static web app
az staticwebapp create \
  --name your-app-name \
  --resource-group your-resource-group \
  --source https://github.com/your-username/your-repo \
  --location "West Europe" \
  --branch main \
  --app-location "/" \
  --login-with-github
```

## 📁 Project Structure

```
homepage/
├── index.html          # Main HTML file with all content
├── styles.css          # Styling and layout
├── .gitignore         # Git ignore file
└── README.md          # This file
```

## 🎨 Features

- **Responsive Design** - Works on desktop, tablet, and mobile
- **Modern UI** - Beautiful gradient backgrounds and card-based layout
- **Beginner-Friendly** - All concepts explained with simple analogies
- **No Dependencies** - Pure HTML and CSS, no frameworks needed
- **Fast Loading** - Optimized for quick page loads
- **SEO Optimized** - Proper meta tags and semantic HTML

## 🔧 Local Development

To view the site locally:

1. Simply open `index.html` in your web browser
2. Or use a local server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve
   ```
3. Navigate to `http://localhost:8000`

## 📝 Customization

Feel free to customize the content:
- Edit `index.html` to modify content
- Update `styles.css` to change colors and styling
- Add more sections as needed

## 🌟 Tips for AZ-900 Exam

- Read through all sections carefully
- Understand the analogies and relate them to real Azure concepts
- Practice with the [Azure Portal](https://portal.azure.com)
- Take advantage of [Microsoft Learn](https://learn.microsoft.com/training/azure/) free training
- Try the [Azure free tier](https://azure.microsoft.com/free/) to get hands-on experience

## 📚 Additional Resources

- [Microsoft Learn - AZ-900](https://learn.microsoft.com/certifications/exams/az-900)
- [Azure Documentation](https://docs.microsoft.com/azure/)
- [Azure Pricing Calculator](https://azure.microsoft.com/pricing/calculator/)

## 📄 License

This project is free to use for educational purposes.

---

**Good luck with your AZ-900 certification!** 🚀
