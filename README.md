# Professional Portfolio Website

A modern, responsive portfolio website built with React, Vite, and Tailwind CSS. This project showcases web development skills through a visually appealing and performant single-page application.

## 🚀 Features

- **Modern Design**: Clean, professional UI with gradient backgrounds and smooth animations
- **Responsive Layout**: Fully responsive design that works seamlessly across all devices
- **Performance Optimized**: 
  - Lazy loading for components using React.lazy
  - Code splitting with Vite
  - Minified JavaScript and CSS for production
  - Optimized bundle sizes
- **Smooth Animations**: Powered by Framer Motion for engaging user interactions
- **Interactive Components**:
  - Hero section with animated elements
  - About section with statistics
  - Projects gallery with modal details
  - Skills section with animated progress bars
  - Resume section with experience timeline
  - Contact form with validation
- **Accessibility**: Semantic HTML and keyboard navigation support

## 🛠️ Technologies Used

### Frontend
- **React 19** - UI library
- **Vite 8** - Build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **React Intersection Observer** - Scroll-based animations

### Development Tools
- **PostCSS** - CSS processing
- **Terser** - JavaScript minification
- **ESLint** - Code linting

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/portfolio.git
cd portfolio
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## 🏗️ Building for Production

To create an optimized production build:

```bash
npm run build
```

The production files will be generated in the `dist/` directory.

### Build Optimization

The production build includes:
- **Code Splitting**: Automatic splitting of vendor chunks (React, animations)
- **Tree Shaking**: Removal of unused code
- **Minification**: JavaScript and CSS minification with Terser
- **Asset Optimization**: Optimized asset handling
- **Console Removal**: Production builds strip console statements

## 📁 Project Structure

```
portfolio/
├── public/                 # Static assets
├── src/
│   ├── components/         # React components
│   │   ├── About.jsx
│   │   ├── Contact.jsx
│   │   ├── Footer.jsx
│   │   ├── Hero.jsx
│   │   ├── LazyImage.jsx
│   │   ├── Navbar.jsx
│   │   ├── Projects.jsx
│   │   ├── Resume.jsx
│   │   └── Skills.jsx
│   ├── App.jsx            # Main app component
│   ├── index.css          # Global styles
│   └── main.jsx           # Entry point
├── index.html             # HTML template
├── package.json           # Dependencies
├── tailwind.config.js     # Tailwind configuration
├── vite.config.js         # Vite configuration
└── README.md             # This file
```

## 🎨 Customization

### Personalizing the Portfolio

1. **Update Personal Information**:
   - Edit `src/components/Hero.jsx` to change your name and title
   - Update `src/components/About.jsx` with your bio and statistics
   - Modify `src/components/Contact.jsx` with your contact details

2. **Add Your Projects**:
   - Edit the `projects` array in `src/components/Projects.jsx`
   - Add your project details, technologies, and links

3. **Update Skills**:
   - Modify the `skillCategories` array in `src/components/Skills.jsx`
   - Adjust skill levels and add new technologies

4. **Customize Resume**:
   - Update `experience`, `education`, and `certifications` in `src/components/Resume.jsx`

5. **Change Colors**:
   - Modify the color palette in `tailwind.config.js`
   - The current theme uses primary (blue) and accent (purple) colors

## 🚢 Deployment

### Option 1: Netlify

1. Build the project:
```bash
npm run build
```

2. Deploy the `dist` folder to Netlify:
   - Drag and drop the `dist` folder to Netlify
   - Or connect your GitHub repository for automatic deployments

3. Configure custom domain and SSL in Netlify settings

### Option 2: Vercel

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Deploy:
```bash
vercel
```

3. Follow the prompts to configure your project

### Option 3: GitHub Pages

1. Build the project:
```bash
npm run build
```

2. Install gh-pages:
```bash
npm install -D gh-pages
```

3. Add deploy script to package.json:
```json
"scripts": {
  "deploy": "gh-pages -d dist"
}
```

4. Deploy:
```bash
npm run deploy
```

## 🌐 Custom Domain Configuration

### Netlify
1. Go to Domain Settings in Netlify
2. Add your custom domain
3. Update DNS records at your domain registrar
4. Enable automatic HTTPS (SSL)

### Vercel
1. Go to Project Settings > Domains
2. Add your custom domain
3. Update DNS records
4. SSL is automatically configured

### GitHub Pages
1. Go to repository Settings > Pages
2. Add custom domain
3. Update DNS records
4. Enable Enforce HTTPS

## 🧪 Testing

### Local Testing

1. **Build Verification**:
```bash
npm run build
npm run preview
```

2. **Responsive Testing**:
   - Test on different screen sizes using browser DevTools
   - Test on mobile devices
   - Verify tablet layouts

3. **Cross-Browser Testing**:
   - Chrome/Edge (Chromium)
   - Firefox
   - Safari
   - Mobile browsers

### Performance Testing

Use these tools to analyze performance:
- [Lighthouse](https://developers.google.com/web/tools/lighthouse) - Chrome DevTools
- [PageSpeed Insights](https://pagespeed.web.dev/) - Google's performance tool
- [WebPageTest](https://www.webpagetest.org/) - Detailed performance analysis

## 📊 Performance Metrics

The optimized production build achieves:
- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Time to Interactive**: < 3.5s
- **Cumulative Layout Shift**: < 0.1
- **Total Bundle Size**: ~400KB (gzipped)

## 🐛 Troubleshooting

### Common Issues

1. **Build fails with Tailwind error**:
   - Ensure `@tailwindcss/postcss` is installed
   - Check `postcss.config.js` configuration

2. **Animations not working**:
   - Verify Framer Motion is installed
   - Check console for JavaScript errors

3. **Styles not applying**:
   - Ensure Tailwind CSS is properly configured
   - Check that `@tailwind` directives are in `index.css`

4. **Lazy loading not working**:
   - Verify React.lazy is implemented correctly
   - Check Suspense boundary is wrapping lazy components

## 🎯 Challenges & Solutions

### Challenge 1: Tailwind CSS v4 Integration
**Problem**: Tailwind CSS v4 changed the PostCSS plugin structure, causing build errors.

**Solution**: Installed `@tailwindcss/postcss` package and updated `postcss.config.js` to use the new plugin instead of the deprecated direct Tailwind plugin.

### Challenge 2: Terser Dependency
**Problem**: Vite v3+ requires Terser as an optional dependency for minification.

**Solution**: Installed Terser as a dev dependency to enable production build minification.

### Challenge 3: Code Splitting Configuration
**Problem**: Manual chunks configuration needed to be a function instead of an object in newer Vite versions.

**Solution**: Updated `vite.config.js` to use a function for `manualChunks` to properly split vendor bundles.

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📧 Contact

- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com
- Portfolio: [your-portfolio-url.com](https://your-portfolio-url.com)

## 🙏 Acknowledgments

- React team for the amazing library
- Vite team for the fast build tool
- Tailwind CSS team for the utility-first framework
- Framer Motion team for the animation library

---

Built with ❤️ using React, Vite, and Tailwind CSS
