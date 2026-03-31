# Security Deploy Checklist

## 1) Pick your server

- Apache: use `.htaccess` in this folder.
- Nginx: include `nginx-security.conf` inside your HTTPS `server` block.

## 2) HTTPS only

- Install a valid TLS certificate.
- Redirect all HTTP traffic to HTTPS.
- Keep HSTS enabled after you verify HTTPS works on every subdomain.

## 3) Keep Google-only auth flow

- Do not re-enable local passwords in frontend code.
- Keep CAPTCHA enabled before Google sign-in.
- Keep role/domain checks active (`@studenti.itisavogadro.it`, `@itisavogadro.it`).

## 4) Ops controls

- Put the site behind a WAF/CDN (Cloudflare recommended).
- Enable rate limiting for repeated requests.
- Enable access logs and alerting on anomalies.

## 5) Update policy

- Review this setup every month.
- Patch dependencies and hosting stack regularly.
