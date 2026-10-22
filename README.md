# Nginx + PHP-FPM

This image is built for `linux/amd64` and provides:

- PHP-FPM 8.5 based on Alpine Linux 3.24
- Nginx 1.12.1
- OpenSSL 1.0.2l with ChaCha20-Poly1305
- Certificate Transparency 1.3.2
- Brotli 1.0.2
- TLS dynamic record sizing
- Memcached extension 3.4.0
- PHP extensions commonly required by WordPress

PHP-FPM listens on `/tmp/php-cgi.sock`, matching the bundled Nginx FastCGI
configuration.

## Compatibility notes

The image is intended for an existing WordPress environment. Review the
included virtual-host, certificate, document-root, and timezone configuration
before deployment. Mounting `/usr/local/nginx` replaces the Nginx configuration
bundled in the image.

Some CentOS 7 hosts may deny Nginx `pwrite` calls through their default seccomp
policy, even after upgrading Docker. The container runtime security policy must
allow these calls for Nginx to start.
