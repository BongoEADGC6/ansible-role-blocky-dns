# Blocky DNS AD blocker Ansible Role

This role sets up https://github.com/0xERR0R/blocky 

Supported on x86_64 and arm64 Linux only.

Provides very simple configuration for quick start with advertisement blocking.

Following variables can be set:

- **blocky_dns_version** - string, version of binary, default `0.18`
- **blocky_dns_resolvers** - list, default [upstream DNS resolvers](https://0xerr0r.github.io/blocky/configuration/#upstream-configuration), default `tcp-tls:1.1.1.1:853`, `tcp-tls:8.8.8.8:853`
- **blocky_dns_blacklists** - list, list of AD blocking URLS, default check in code
- **blocky_dns_port** - int, port that will be used by blocky, default `53`
- **blocky_http_port** - int, port to serve http for metrics, default `4000`
- **blocky_tls_port** - int, Port(s) and optional bind ip address(es) to serve DoT DNS endpoint (DNS-over-TLS), default not set
- **blocky_log_level** - enum (debug, info, warn, error), blocky log level, default not set
- **blocky_log_privacy** - bool, Obfuscate log output (replace all alphanumeric characters with `*`) for user sensitive data like request domains or responses to increase privacy, default not set

For more information about blocky config please refer to it's [documentation](https://0xerr0r.github.io/blocky/configuration).
