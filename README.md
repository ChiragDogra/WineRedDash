# WineRed Product Dashboard

A modern, performant, and aesthetic product dashboard built with vanilla JavaScript, featuring global semantic search, responsive design, and PWA capabilities.

## ✨ Features

### 🎯 **Global Semantic Search**
- Search across all product categories from anywhere in the app
- Real-time search with debounced input (300ms delay)
- Searches through Style ID, Style Name, Category, Color, and Components
- Highlighted search results for better visibility
- Works both on home screen and within categories

### 🏷️ **Category Management**
- Beautiful category cards with product counts
- Smooth transitions between category and product views
- Responsive grid layout that adapts to all screen sizes
- Hover effects and visual feedback

### 📱 **Responsive Design**
- Mobile-first approach with progressive enhancement
- Optimized for all devices (mobile, tablet, desktop)
- Touch-friendly interface with proper spacing
- Adaptive grid layouts that work on any screen size

### 🚀 **Performance Optimizations**
- **Lazy Loading**: Images load only when needed
- **Debounced Search**: Prevents excessive API calls
- **Efficient Caching**: Service Worker for offline support
- **Optimized Fonts**: Preloaded Google Fonts with proper fallbacks
- **Minimal DOM Manipulation**: Efficient rendering with modern JavaScript
- **Image Optimization**: Proper sizing and loading strategies

### 🎨 **Brand Identity**
- **Primary Color**: #921944 (WineRed brand color)
- **Heading Font**: Fahkwang (elegant serif for titles)
- **Body Font**: DM Sans (clean, readable sans-serif)
- **Modern UI**: Smooth animations, shadows, and hover effects

### 📱 **PWA Features**
- Installable as a native app
- Offline support with Service Worker
- App-like experience with proper manifest
- Background sync capabilities
- Push notification support

## 🛠️ Technical Implementation

### **Architecture**
- **Vanilla JavaScript**: No framework dependencies for maximum performance
- **ES6+ Classes**: Modern JavaScript with proper encapsulation
- **CSS Custom Properties**: Consistent theming with CSS variables
- **Grid & Flexbox**: Modern CSS layouts for responsive design

### **Performance Features**
- **Service Worker**: Intelligent caching strategies
  - Static files: Cache first
  - API calls: Network first
  - Images: Cache first with fallback
- **Lazy Loading**: Images and content load progressively
- **Debounced Search**: Prevents excessive API calls during typing
- **Efficient DOM Updates**: Minimal re-rendering and smart updates

### **Search Implementation**
- **Semantic Search**: Searches across multiple product attributes
- **Real-time Results**: Instant feedback as user types
- **Smart Highlighting**: Search terms are highlighted in results
- **Global Scope**: Search works from any page or view

## 📁 File Structure

```
WineRedDashboard/
├── index.html          # Main dashboard with categories and search
├── details.html        # Product details page
├── sw.js              # Service Worker for PWA features
├── manifest.json      # PWA manifest file
└── README.md          # This documentation
```

## 🚀 Getting Started

### **Prerequisites**
- Modern web browser with ES6+ support
- Web server (local or hosted)
- HTTPS connection (required for Service Worker)

### **Installation**

1. **Clone or Download** the project files
2. **Host on Web Server**: Place files on a web server (local or remote)
3. **Access**: Open `index.html` in your browser

### **Local Development**

```bash
# Using Python (Python 3)
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## 🔧 Configuration

### **API Endpoints**
The dashboard uses two main APIs:
- **Categories & Products**: `https://api.sheetbest.com/sheets/2e8a9012-e63e-44d0-9062-9d4a72289553`
- **Product Details**: `https://sheetdb.io/api/v1/s19ir31sq3v11/search?ItemID={id}`

### **Customization**
- **Colors**: Modify CSS custom properties in `:root`
- **Fonts**: Update Google Fonts links in `<head>`
- **Layout**: Adjust grid breakpoints in CSS media queries

## 📱 Browser Support

- **Chrome**: 60+ (Full PWA support)
- **Firefox**: 55+ (Full PWA support)
- **Safari**: 11.1+ (Limited PWA support)
- **Edge**: 79+ (Full PWA support)

## 🚀 Performance Metrics

### **Optimizations Implemented**
- ✅ **Lazy Loading**: Images load progressively
- ✅ **Debounced Search**: Prevents excessive API calls
- ✅ **Service Worker**: Intelligent caching strategies
- ✅ **Font Preloading**: Critical fonts load early
- ✅ **Image Preloading**: Logo loads immediately
- ✅ **Efficient DOM**: Minimal re-rendering
- ✅ **CSS Variables**: Consistent theming
- ✅ **Modern Layouts**: Grid and Flexbox

### **Expected Performance**
- **First Load**: ~2-3 seconds (depends on network)
- **Subsequent Loads**: ~0.5-1 second (cached)
- **Search Response**: <100ms (debounced)
- **Image Loading**: Progressive with lazy loading
- **Offline Support**: Full functionality with cached data

## 🎨 Design System

### **Color Palette**
```css
--brand-primary: #921944      /* Main brand color */
--brand-primary-light: #b02a56
--brand-primary-dark: #7a1538
--text-primary: #2d3748       /* Main text */
--text-secondary: #4a5568     /* Secondary text */
--background: #ffffff          /* Main background */
--background-secondary: #f7fafc /* Secondary background */
--border: #e2e8f0            /* Borders and dividers */
```

### **Typography**
- **Headings**: Fahkwang (elegant serif)
- **Body Text**: DM Sans (clean sans-serif)
- **Font Weights**: 300, 400, 500, 600, 700

### **Spacing & Layout**
- **Container Max Width**: 1400px
- **Grid Gaps**: 2rem (32px)
- **Border Radius**: 12px
- **Shadows**: Subtle depth with CSS variables

## 🔍 Search Functionality

### **How It Works**
1. **Global Search Bar**: Always visible in header
2. **Semantic Indexing**: Builds search index on data load
3. **Real-time Results**: Updates as user types
4. **Smart Highlighting**: Search terms highlighted in results
5. **Cross-category**: Searches all products regardless of current view

### **Search Fields**
- Style ID
- Style Name
- Category
- Color
- Components

### **Search Features**
- **Debounced Input**: 300ms delay to prevent excessive API calls
- **Case Insensitive**: Searches work regardless of case
- **Partial Matching**: Finds partial text matches
- **Instant Results**: No page refresh required

## 📱 Responsive Design

### **Breakpoints**
- **Mobile**: <480px (single column)
- **Tablet**: 480px - 768px (adaptive columns)
- **Desktop**: >768px (full grid layout)

### **Mobile Optimizations**
- Touch-friendly button sizes
- Proper spacing for mobile devices
- Optimized navigation for small screens
- Responsive images and layouts

## 🚀 PWA Features

### **Service Worker**
- **Static Caching**: HTML, CSS, fonts
- **Dynamic Caching**: API responses, images
- **Offline Support**: Full functionality when offline
- **Background Sync**: Syncs data when connection restored

### **Installation**
- **Add to Home Screen**: Install as native app
- **Offline Access**: Works without internet
- **App-like Experience**: Full-screen, no browser UI

## 🐛 Troubleshooting

### **Common Issues**

1. **Service Worker Not Working**
   - Ensure HTTPS connection
   - Clear browser cache
   - Check browser console for errors

2. **Images Not Loading**
   - Check network connection
   - Verify image URLs in API response
   - Clear browser cache

3. **Search Not Working**
   - Check API endpoint accessibility
   - Verify data structure in API response
   - Check browser console for errors

### **Debug Mode**
Enable debug logging by opening browser console and looking for:
- Service Worker registration messages
- API call logs
- Performance metrics

## 🔮 Future Enhancements

### **Planned Features**
- [ ] Advanced filtering options
- [ ] Product comparison tools
- [ ] User preferences and favorites
- [ ] Analytics dashboard
- [ ] Multi-language support
- [ ] Dark mode theme

### **Performance Improvements**
- [ ] Virtual scrolling for large datasets
- [ ] Advanced image optimization
- [ ] WebAssembly for complex operations
- [ ] Background data sync

## 📄 License

This project is proprietary software for WineRed. All rights reserved.

## 🤝 Support

For technical support or feature requests, please contact the development team.

---

**Built with ❤️ for WineRed**
*Modern, Fast, and Beautiful Product Dashboard*
