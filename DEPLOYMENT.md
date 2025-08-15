# Deployment Instructions

## Frontend Deployment (Vercel)

### Step 1: Deploy to Vercel
1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click "New Project"
3. Import your GitHub repository: `Bitan02/Real_Time_Chat_Application_MERN_Stack`
4. Set the following configuration:
   - **Framework Preset**: Vite
   - **Root Directory**: `frontend`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
   - **Install Command**: `npm install`

### Step 2: Environment Variables
Add these environment variables in Vercel:
- `VITE_API_URL`: Your backend URL (e.g., `https://your-backend.onrender.com/api`)

### Step 3: Deploy
Click "Deploy" and wait for the build to complete.

## Backend Deployment (Render/Railway)

### Option 1: Render
1. Go to [render.com](https://render.com) and sign up
2. Click "New Web Service"
3. Connect your GitHub repository
4. Configure:
   - **Name**: `chat-app-backend`
   - **Root Directory**: `backend`
   - **Environment**: `Node`
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`

### Option 2: Railway
1. Go to [railway.app](https://railway.app) and sign up
2. Click "New Project" → "Deploy from GitHub repo"
3. Select your repository
4. Set the root directory to `backend`
5. Add environment variables (see below)

### Environment Variables for Backend
Add these environment variables:
- `MONGODB_URI`: Your MongoDB connection string
- `JWT_SECRET`: Your JWT secret key
- `CLOUDINARY_CLOUD_NAME`: Your Cloudinary cloud name
- `CLOUDINARY_API_KEY`: Your Cloudinary API key
- `CLOUDINARY_API_SECRET`: Your Cloudinary API secret
- `NODE_ENV`: `production`

## Update Frontend Configuration
After deploying the backend, update the frontend's axios configuration:
1. Go to your Vercel project settings
2. Update the `VITE_API_URL` environment variable with your actual backend URL
3. Redeploy the frontend

## Final Steps
1. Update the CORS configuration in your backend with your actual Vercel frontend URL
2. Test the application to ensure everything works
3. Share your deployed application URL!

## URLs to Update
- Frontend: `https://your-app.vercel.app`
- Backend: `https://your-backend.onrender.com` (or Railway URL)
