# https_ssl

| File | Description |
| --- | --- |
| `0-world_wide_web` | Bash script that audits a domain's `www`, `lb-01`, `web-01`, `web-02` subdomains with `dig` and `awk` |
| `1-haproxy_ssl_termination` | HAProxy config terminating SSL on port 443 (certificate from certbot) |
| `2-redirect_http_to_https` | HAProxy config that 301-redirects HTTP to HTTPS |

Usage: `./0-world_wide_web example.tech [subdomain]`

The HAProxy configs expect the certificate and key combined in
`/etc/haproxy/certs/www.pem` (`cat fullchain.pem privkey.pem > www.pem`).
