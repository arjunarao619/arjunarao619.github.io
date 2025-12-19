# Google Analytics Setup & Viewing Stats Guide

## Step 1: Set Up Google Analytics 4

1. Go to [Google Analytics](https://analytics.google.com/)
2. Sign in with your Google account
3. Click **Admin** (gear icon) in the bottom left
4. In the **Account** column, click **Create Account**
5. Fill in:
   - Account name: "Personal Website" (or your choice)
   - Click **Next**
6. Set up property:
   - Property name: "arjunashokrao.me" (or your domain)
   - Time zone: Your timezone
   - Currency: Your currency
   - Click **Next**
7. Business information (optional):
   - Select your industry
   - Business size
   - Click **Create**
8. Accept the Terms of Service

## Step 2: Get Your Measurement ID

1. In Google Analytics, go to **Admin** → **Data Streams**
2. Click **Add stream** → **Web**
3. Enter:
   - Website URL: `https://arjunashokrao.me`
   - Stream name: "Website"
4. Click **Create stream**
5. **Copy your Measurement ID** (format: `G-XXXXXXXXXX`)

## Step 3: Add to Your Website

1. Open `index.html`
2. Find this line:
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   ```
3. Replace `G-XXXXXXXXXX` with your actual Measurement ID (appears twice)
4. Save and push to GitHub

## Step 4: Verify It's Working

1. Visit your website
2. In Google Analytics, go to **Reports** → **Realtime**
3. You should see your visit appear within 30 seconds
4. If you don't see data, wait a few minutes (GA4 can take 24-48 hours for full data)

## How to View Your Stats

### Real-Time Data
- **Reports** → **Realtime**: See visitors right now
- Shows: Active users, top pages, traffic sources, locations

### Location Data
- **Reports** → **User attributes** → **Demographic details**
- **Reports** → **Tech** → **Tech details** → **Location**
- Shows: Country, city, region of your visitors

### Page Views & Popular Pages
- **Reports** → **Engagement** → **Pages and screens**
- Shows: Which pages get the most views, average time on page

### Traffic Sources
- **Reports** → **Acquisition** → **Traffic acquisition**
- Shows: Where visitors come from (direct, search, social, etc.)

### Device & Browser Info
- **Reports** → **Tech** → **Tech details**
- Shows: Browsers, operating systems, device categories

### User Behavior
- **Reports** → **Engagement** → **Events**
- Shows: Scroll depth, link clicks, time on page (if you add custom events)

### Time-Based Analysis
- **Reports** → **Life cycle** → **Acquisition**
- Use date range picker (top right) to see:
  - Last 7 days
  - Last 30 days
  - Custom date ranges
  - Compare periods

### Export Data
- Click the **Share** icon (top right of any report)
- Export to PDF, Google Sheets, or CSV

## Pro Tips

1. **Create Custom Reports**: 
   - Click **Explore** (left sidebar) → **Blank**
   - Drag dimensions and metrics to create custom views

2. **Set Up Goals/Conversions**:
   - Admin → **Events** → Mark important events as conversions

3. **View Location Map**:
   - Reports → **User attributes** → **Demographic details**
   - Click on a country to see city-level breakdown

4. **Mobile vs Desktop**:
   - Reports → **Tech** → **Tech details** → **Device category**

5. **Peak Hours**:
   - Reports → **User attributes** → **Demographic details**
   - Look at "Hour" dimension to see when most visitors come

## Important Notes

- **Data Delay**: Real-time data appears immediately, but full reports can take 24-48 hours
- **Privacy**: IP addresses are anonymized automatically
- **Free Tier**: Google Analytics is free and handles up to 10 million hits/month
- **Data Retention**: Default is 14 months, can be extended to 50 months in settings

## Troubleshooting

- **No data showing**: 
  - Check that your Measurement ID is correct
  - Verify the script is in your HTML
  - Wait 24-48 hours for initial data
  - Use browser extension "Google Analytics Debugger" to test

- **Location not showing**:
  - Location data is approximate (city-level, not exact addresses)
  - Some visitors may show as "not set" if location can't be determined

