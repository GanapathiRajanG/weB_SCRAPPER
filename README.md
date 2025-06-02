# NeoScraper - Django Web Scraper

This project has been successfully converted from Flask to Django. NeoScraper is an advanced web content extractor that analyzes websites and extracts key information including headings, metadata, important content, images, and links.

> **Note:** NeoScraper is designed as a **local web scraping and data analysis platform** that runs on your own system. No data is sent to external servers.

## 🚀 Features

- **Web Scraping**: Extract content from any website
- **Modern UI**: Beautiful, animated interface with glassmorphism design
- **Content Analysis**: Extracts headings, bold text, paragraphs, images, and links
- **History Tracking**: Stores and displays previous scraping sessions
- **Django Admin**: Full admin interface for managing scraped data
- **REST API**: JSON endpoints for programmatic access
- **Local Processing**: All data processing happens on your machine

## 📁 Project Structure

```
web_scraper_django/
├── manage.py
├── requirements.txt
├── README.md
├── web_scraper_django/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
└── scraper/
    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── models.py
    ├── views.py
    ├── urls.py
    ├── migrations/
    └── templates/
        └── scraper/
            └── index.html
```
## 🛠️ Local Setup & Installation

Follow these steps to set up NeoScraper on your local machine:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/neoscraper.git
   cd neoscraper
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Migrations**:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create Superuser** (optional, for admin access):
   ```bash
   python manage.py createsuperuser
   ```

6. **Start Development Server**:
   ```bash
   python manage.py runserver
   ```

7. **Access the Application**:
   - Main App: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
   - Admin Panel: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

## 📡 API Endpoints

- `GET /` - Main application interface
- `POST /scrape/` - Scrape a website (JSON: `{"url": "https://example.com"}`)
- `GET /history/` - Get scraping history

## 🎯 Usage

1. Open the web interface at [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
2. Enter a website URL in the input field
3. Click "Analyze" to scrape the website
4. View extracted content organized by type
5. Check the history section for previous scrapes

## 🔧 Technical Details

- **Framework**: Django 4.2.7
- **Database**: SQLite (easily configurable for PostgreSQL/MySQL)
- **Frontend**: Vanilla JavaScript with modern CSS animations
- **Scraping**: BeautifulSoup4 + Requests
- **Storage**: Django ORM with JSONField for complex data structures

- ## 🔒 Privacy & Security

- All data is stored locally in your SQLite database
- No data is sent to external servers
- Scraping is performed directly from your machine
- Consider legal and ethical implications when scraping websites

## 🚀 Next Steps

The Django conversion is complete and fully functional. You can now:
- Add user authentication
- Implement more advanced scraping features
- Add data export functionality
- Scale with Django's ecosystem
- Deploy using Django deployment best practices
