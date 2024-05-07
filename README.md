## Next.js 14 全棧身份認證實作 Full Stack Authentication With Next.js 14
使用 Next.js 14、NextAuth.js v5、MongoDB、Mongoos、TypeScript 和 Server Actions 實現全棧認證

A demo project that uses NextAuth.js v5 for authentication, connects to MongoDB with Mongoose, and supports Google OAuth and email/password login.

## Features
- OAuth: 可透過 Google 帳號進行登錄。
- OAuth: Log in with Google.

- 憑證登入: 使用電子郵件和密碼進行登入。
- Credential Login: Log in with email and password.

- 信箱驗證: 驗證用戶的電子郵件地址。
- Email Verification: Confirm user's email address.

- 重設密碼: 透過電子郵件重設用戶的密碼。
- Forgot Password: Reset user's password through an email.

- 2FA雙因素驗證: 透過電子郵件獲取六位數登錄碼。
- Two Factor Verification: Obtain a six-digit login code through an email.

- 變更設定: 更改用戶設定，包括名稱、密碼，以及切換雙因素驗證。
- Settings Edit: Change user's settings, including name, password, and toggle Two-factor verification.

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Environment Setup
Create a .env file in the root directory and add the following variables:

```env
NEXT_PUBLIC_APP_URL="http://localhost:3000"

AUTH_SECRET="YOUR_AUTH_SECRET"

MONGODB_URI="YOUR_MONGODB_URI"

GOOGLE_CLIENT_ID="YOUR_GOOGLE_CLIENT_ID"
GOOGLE_CLIENT_SECRET="YOUR_GOOGLE_CLIENT_SECRET"

RESEND_API_KEY="YOUR_RESEND_API_KEY"
RESEND_EMAIL_URL="YOUR_RESEND_EMAIL_URL"
```

GOOGLE_CLIENT_ID & GOOGLE_CLIENT_SECRET

- Navigate to [https://console.cloud.google.com](https://console.cloud.google.com/) .

- Create a new project.

- Head over to APIs & Services => Credentials.
  
- Click on CREATE CREDENTIALS => OAuth client ID.
  
- Choose the Web application.

- Add to Authorized JavaScript origins: http://localhost:3000 .

- Add to Authorized redirect URIs: http://localhost:3000/api/auth/callback/google.
  
- Finish by going to APIs & Services => OAuth consent screen and publishing the app.

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

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
