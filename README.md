# Vercel deployment of Laravel app
A proof of concept to deploy a Laravel app as a lambda function on Vercel.

Approach copied from [Caleb Porzio's blog post](https://calebporzio.com/easy-free-serverless-laravel-with-vercel)

The deployed app is just a fresh Laravel app.

### Significant files:

- `api/index.php` --> makes `public/index.php` the api entry-point
- `.vercelignore` --> avoid uploading `vendor` to Vercel on deployment
- `vercel.json` --> set some vercel env properties. Among other things, changes the runtime to `vercel-php`, which takes care of setting up the laravel app (composer install etc).
