# SlideVault

SlideVault is a Node.js + Express + MongoDB app for uploading and browsing presentation files.

## Run locally

```bash
npm install
npm start
```

Create a `.env` file from `.env.example` and set `MONGO_URI` before starting the server.

## Deploy on Render

1. Push this repo to GitHub.
2. Create a MongoDB Atlas database and copy its connection string.
3. In Render, create a new Blueprint deployment from this repository.
4. Set the `MONGO_URI` environment variable in Render.
5. Deploy the service.

The app serves the frontend and API from the same Express server.

## Important note about uploads

This project currently stores uploaded files in the local `uploads/` folder. On platforms like Render, filesystem storage is ephemeral, so uploaded files can disappear after restarts or redeploys. For production use, move uploads to object storage such as Cloudinary, AWS S3, or Uploadcare.
