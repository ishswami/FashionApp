This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## PDF Generation Setup

For PDF generation to work in local development, you need to set up Chrome/Chromium:

### Windows Local Development
1. Install Google Chrome if you haven't already
2. Find your Chrome executable path (usually `C:\Program Files\Google\Chrome\Application\chrome.exe`)
3. Set the environment variable:
   ```bash
   set PUPPETEER_EXECUTABLE_PATH="C:\Program Files\Google\Chrome\Application\chrome.exe"
   ```
   Or add it to your `.env.local` file:
   ```
   PUPPETEER_EXECUTABLE_PATH="C:\Program Files\Google\Chrome\Application\chrome.exe"
   ```

### macOS/Linux Local Development
1. Install Google Chrome or Chromium
2. Set the environment variable to your Chrome/Chromium path:
   ```bash
   export PUPPETEER_EXECUTABLE_PATH="/usr/bin/google-chrome"
   ```

### Production (Vercel)
PDF generation works automatically in production using the `@sparticuz/chromium` package.

### Testing PDF Generation
After setting up the environment variables, you can test PDF generation by visiting:
- Test PDF: `http://localhost:3000/api/test-pdf`
- This will generate a simple test PDF to verify the setup is working correctly.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.


Where the new order ID will appear:
Invoice PDF Cloudinary folder:
invoices/<dateFolder>/<orderId>/...
→ Now: invoices/16-07-2025/20250716001/customer.pdf (for example)
WhatsApp invoice link:
https://fashion-app-kappa.vercel.app/api/proxy-pdf?type=customer&oid=20250716001