Getting Started Locally
Clone this repository to your local machine:

git clone https://github.com/dillionverma/portfolio
Move to the cloned directory

cd portfolio
Install dependencies:

pnpm install
Start the local Server:

pnpm dev
Open the Config file and make changes

Blog Admin Setup (Vercel + MongoDB + Cloudinary)
This project now stores blog posts in MongoDB (via Prisma) and uploads blog images to Cloudinary.

Copy environment variables:

cp .env.example .env.local
Fill these values in .env.local:

ADMIN_EMAIL
ADMIN_PASSWORD_HASH (sha256 hash of your admin password)
DATABASE_URL (MongoDB connection string)
CLOUDINARY_CLOUD_NAME
CLOUDINARY_API_KEY
CLOUDINARY_API_SECRET
Generate Prisma client:

npm run prisma:generate
Push schema to MongoDB:

npm run prisma:dbpush
In Vercel, add the same environment variables in Project Settings -> Environment Variables and redeploy.

License
