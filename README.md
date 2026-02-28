# Litter Lift

A web application for reporting and tracking litter and waste in neighborhoods. Built to help communities keep their surroundings clean by enabling residents to report litter locations, track cleanup progress, and participate in community-driven waste management.

## Features

- **Report Litter Locations** - Submit reports with photos and automatic geolocation to pinpoint litter spots in your neighborhood
- **Track Cleanup Status** - Monitor the progress of reported litter from submission to cleanup completion
- **Community Leaderboard** - Recognize and rank top contributors who actively participate in cleanup efforts
- **Interactive Map View** - Visualize all reported litter locations on an interactive map powered by Leaflet/Mapbox
- **Photo Upload** - Attach images to litter reports for better identification and verification
- **Email Notifications** - Get notified when nearby litter is reported or when your reports are addressed
- **Admin Dashboard** - Manage all reports, update statuses, and oversee community activity
- **Recycling Requests** - Request pickup for recyclable items with location-based service center matching
- **Payment/Donation System** - Support the initiative through Stripe-powered donations

## Tech Stack

- **Backend**: Node.js, Express.js
- **Templating**: EJS (Embedded JavaScript)
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT (JSON Web Tokens) with bcrypt password hashing
- **Maps**: Leaflet.js with OpenCage Geocoding API
- **File Uploads**: Multer
- **Email**: Nodemailer
- **Payments**: Stripe
- **AI Chatbot**: Python Flask with NLP (optional)
- **Deployment**: Vercel

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local instance or MongoDB Atlas connection string)
- Python 3.x (optional, for the chatbot feature)

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/aakashdvd/Litter_Lift-.git
   cd Litter_Lift-
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```
   MONGODB_URI=mongodb://localhost:27017/litterLift
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASS=your-app-password
   ADMIN_PASSKEY=your-admin-secret
   OPENCAGE_API_KEY=your-opencage-key
   STRIPE_SECRET_KEY=your-stripe-key
   BASE_URL=http://localhost:3000
   ```

4. **Start the application**
   ```bash
   node app.js
   ```

5. **Open in browser**
   Navigate to `http://localhost:3000`

## How It Works

1. **Users register** and log in to access the platform
2. **Report litter** by uploading a photo - the app automatically detects your location using browser geolocation and converts coordinates to a readable address via OpenCage API
3. **Nearest service centers** are identified based on the report location
4. **Email notifications** are sent to the appropriate service center and the user receives a confirmation
5. **Admins review** incoming reports on the dashboard and update cleanup status
6. **Community leaderboard** tracks active participants and completed cleanups
7. **Map view** displays all active litter reports so anyone can see problem areas in their neighborhood

## Project Structure

```
Litter_Lift-/
├── app.js                 # Main Express application
├── config/
│   ├── multerconfig.js    # File upload configuration
│   ├── garbageConfig.js   # Garbage geocoding and service center logic
│   ├── recyclingConfig.js # Recycling geocoding and center logic
│   ├── chatbot.py         # Flask chatbot server
│   └── train_data.csv     # Chatbot training data
├── models/
│   ├── user.js            # User schema
│   ├── admin.js           # Admin schema
│   ├── garbage.js         # Garbage report schema
│   └── recycleItem.js     # Recycling request schema
├── public/
│   ├── images/            # Static images and icons
│   ├── javascripts/       # Client-side JavaScript
│   ├── stylesheets/       # CSS files
│   └── video/             # Video assets
├── views/                 # EJS templates
│   ├── homepage.ejs       # Landing page
│   ├── index.ejs          # Main index
│   ├── map.ejs            # Map view
│   ├── userCreate.ejs     # User registration
│   ├── userLogin.ejs      # User login
│   ├── userProfile.ejs    # User dashboard
│   ├── adminProfile.ejs   # Admin dashboard
│   ├── UploadG.ejs        # Garbage upload form
│   ├── UploadR.ejs        # Recycling upload form
│   └── chatbot.ejs        # Chatbot interface
├── uploads/               # User uploaded files
├── package.json
├── vercel.json            # Vercel deployment config
└── .gitignore
```

## License

ISC
